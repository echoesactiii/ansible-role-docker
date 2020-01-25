# ansible-role-docker

This is a simple ansible role for setting up docker on a CentOS7 host. It supports [the firewalld hack](https://unix.stackexchange.com/questions/199966/how-to-configure-centos-7-firewalld-to-allow-docker-containers-free-access-to-th) for docker as well.

## Vars & defaults

	docker_admin_users:
	# These users will be added to the 'docker' group.
	  - username: root
	docker_yum_dependencies:
	# These will be installed via yum
	  - python-setuptools
	  - python-pip
	  - docker-compose
	docker_pip_dependencies:
	# These will be installed via pip
	  - docker
	docker_firewalld: true # This enables the firewalld hack - set to false if not using firewalld.
