

### Run Play Book with Commands
```bash
ansible-playbook  playbook.yml --tags "BaseInstall" --extra-vars "python_folder_name=Userpython3" -u username -i hostname, -k  
```


### Change the python interputer path of remove host
```bash
ansible-playbook playbook.yml --extra-vars "ansible_python_interpreter=/usr/bin/python3   python_folder_name=Userpython3" --tags "BaseInstall" -u username -i hostname, -k
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
/home/user/python_folder_name/bin/python3  /home/user/python3/python_folder_name/ansible-playbook
/home/user/python_folder_name/bin/python3  /home/user/python3/python_folder_name/sshuttle

Pip:
/home/user/python_folder_name/bin/python3 /home/user/python_folder_name/bin/pip3 show  ansible
```