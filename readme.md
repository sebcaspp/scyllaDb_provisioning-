

TODO:
=====
- agregar los ssh keys de las maquinas ->  FAILED! => {"msg": "Using a SSH password instead of a key is not possible because Host Key checking is enabled and sshpass does not support this.  Please add this host's fingerprint to your known_hosts file to manage this host."}

- remover del apt-list el repo de cd-rom

Run ansible
===========

ansible-playbook --ask-pass --ask-become-pass setup.yml --verbose --skip-tags "prereq"



