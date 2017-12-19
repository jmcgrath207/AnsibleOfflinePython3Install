

### Run Play Book with Commands
```bash
ansible-playbook  playbook.yml --tags "BaseInstall" -u username -i hostname, -k
```


### Change the python interputer path of remove host
```bash
ansible-playbook playbook.yml --extra-vars ansible_python_interpreter=/usr/bin/python3 --tags "BaseInstall" -u username -i hostname, -k
```


### ensure packages are installed on Host systems ###
#### Note: Python will not compile and pip will not install without these packages

##### Yum Based
```bash
sudo yum install openssl-devel gcc rsync -y
```

##### Apt-get Based
```bash
Apt-get based: apt-get install libssl-dev openssl gcc rsync -y
```

https://stackoverflow.com/questions/22592686/compiling-python-3-4-is-not-copying-pip



### Once complete you can use your installation

ex.
```bash
Python:
/home/user/python3/bin/python3  /home/user/python3/bin/ansible-playbook
/home/user/python3/bin/python3  /home/user/python3/bin/sshuttle

Pip:
/home/user/python3/bin/python3 /home/user/python3/bin/pip3 show  ansible
```