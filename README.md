# deploying-highly-available-openstack
deploying highly available openstack


### install ansible
```
yum install ansible
```

### config ansible env
```
# vim /etc/ansible/ansible.cfg
[ssh_connection]
ssh_args = -C -o ControlMaster=auto -o ControlPersist=60s -o StrictHostKeyChecking=no
#- or -#
[defaults]
host_key_checking = True

# vim /etc/ansible/hosts
[cluster1]
node-1 ansible_ssh_host=172.30.121.194 ansible_ssh_pass=123456
node-2 ansible_ssh_host=172.30.121.195 ansible_ssh_pass=123456
node-3 ansible_ssh_host=172.30.121.196 ansible_ssh_pass=123456
```

