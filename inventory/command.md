ansible-playbook -i inventory /etc/ansible/playbook/ntp.yml -l etcd --extra-vars hostname=master
ansible-playbook -i inventory /etc/ansible/playbook/ntp.yml -l 10.10.11.106 --extra-vars hostname=node-1
ansible-playbook -i inventory /etc/ansible/playbook/ntp.yml -l 10.10.11.119 --extra-vars hostname=node-2
ansible-playbook -i inventory -l all /etc/ansible/playbook/ansible-docker.yml --extra-vars "changedns=true, proxy_env=[]" --tags change-dns
