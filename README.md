

### Run Play Book with Commands

ansible-playbook  playbook.yml --tags "BaseInstall" -u username -i hostname, -k


### Change the python interputer path of remove host

ansible-playbook playbook.yml --extra-vars ansible_python_interpreter=/usr/bin/python3 --tags "BaseInstall" -u username -i hostname, -k


### ensure packages are installed on Host systems ###
#### Note: Python will not compile and pip will not install without these packages
Yum Based: sudo yum install openssl-devel gcc -y
Apt-get based: apt-get install libssl-dev openssl gcc -y



https://stackoverflow.com/questions/22592686/compiling-python-3-4-is-not-copying-pip