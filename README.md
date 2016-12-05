# Setting up with Ansible

Start by getting ansible on your host:

http://docs.ansible.com/ansible/intro_installation.html#installing-the-control-machine

Add some ansible galaxy packages (may require sudo to install on your machine)

    ansible-galaxy install antoiner77.caddy

Check the connectivity

    ansible all -m ping

Deploy

    ansible-playbook site.yml
