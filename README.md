# Setting up with Ansible

Start by getting ansible on your host:

http://docs.ansible.com/ansible/intro_installation.html#installing-the-control-machine

Add some ansible galaxy packages (may require sudo to install on your machine)

    ansible-galaxy install antoiner77.caddy

Setup the ENV if you want to operate outside of the repo:

    export ANSIBLE_REPO="$(git rev-parse --show-toplevel)"
    export ANSIBLE_CONFIG="${ANSIBLE_REPO}/ansible/ansible.cfg"
    export ANSIBLE_INVENTORY="${ANSIBLE_REPO}/ansible/hosts"
    ls -l "${ANSIBLE_CONFIG}" "${ANSIBLE_INVENTORY}"

Check the connectivity

    ansible all -m ping

Deploy

    ansible-playbook site.yml
