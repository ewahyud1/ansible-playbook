## Environment Configuration

***Pre-requisites***: 

The server(s) requires [WinRM Listener](https://docs.ansible.com/ansible/2.9/user_guide/windows_setup.html#winrm-setup) enabled. 
Server(s) will need to be accessible within the LAN or domain (data center); and playbooks require at least local Admin privileges to execute.

## Executing the playbook against the hosts

- `servers` is the file containing the list of servers/hosts
- `logfiles-cleanup.yaml` is the playbook that drives the action against the servers

The command to execute is as follows:

`
ansible-playbook -i ./ansible-playbook/windows/servers ./ansible-playbook/windows/logfiles-cleanup.yaml -e ansible_user=<username> -e ansible_password=<password>
`

If executing the command from a local computer, you can omit the `ansible_user` & `ansible_password`.  You can enter them directly into the servers 
file and be mindful when sharing/exposing it
