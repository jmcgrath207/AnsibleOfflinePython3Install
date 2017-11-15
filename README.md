
### Works with:
- Ubuntu 16.04 LTS
- Linux Mint 18.2


### To get Setup, Install git, clone the repo, and the ansible to perform the provision
```bash

sudo add-apt-repository ppa:ansible/ansible
sudo apt-get update

sudo apt-get install -y ansible git
cd /tmp
git clone https://github.com/jmcgrath207/AnsibleUbuntuBasedtDesktop.git
cd AnsibleUbuntuBasedtDesktop/
sudo ansible-playbook playbook.yml --tags "WorkInstall"
```

#### Run Multiple Tags

```bash
sudo ansible-playbook playbook.yml --tags "WorkInstall, Spotify, SublimeText3"
```

#### After Install if complete, Restart or log out for change to take effect

#### Tags

- [All Tags](TAGS.md)
- [Base Install Tags](roles/BaseInstall/TAGS.md)
- [Home Install Tags](roles/HomeInstall/TAGS.md)
- [Work Install Tags](roles/WorkInstall/TAGS.md)
- [Extra Install Tags](roles/ExtraInstall/TAGS.md)



### Other Helpful Stuff

##### Wireshark run as local user
```bash
sudo dpkg-reconfigure wireshark-common
sudo adduser $USER wireshark
```



#### Google Chrome Addons
- lastpass
- Cookie AutoDelete
- ublock
- Https Everywhere
- Grammarly
- Tamper Monkey
- Rain Drop
- Cookie Auto Delete
#### Google Chrome Dev Tools
- Augury
- Redux DevTools


#### System Level
Disable Bluetooth



#### Make output more readable
```bash
sudo ansible-playbook playbook.yml | sed 's/\\n/\n/g'
```


#### Grab Key ID
```bash
wget https://deb.nodesource.com/gpgkey/nodesource.gpg.key
pgpdump nodesource.gpg.key


sudo apt-key list
```

#### See All Tags bash command:

```bash
grep -r "tags:" ~/PycharmProjects/AnsibleUbuntuBasedtDesktop/roles/. |   sed -r  's/.*tags:|\[|\]|.*lways.*//g' | uniq | grep '[^[:blank:]]'

```

