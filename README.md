# GO Application in docker and Kubernetes

This project aims at creating and deploying a simole Go applicationm which connects to redis and increments counter by one on each hit. 
The idea is to deploy the app using docker on Vagrant VM which is configured using Ansible. Once deployed the application can be accessed on `curl http://localhost:8000`.
The same app is also deployable in Kubernetes in order to provide HA and Self tolerance. The application can be accessed here through LoadBalancer IP.

### Requirements:
1. Vagrant.
2. Ansible.
3. kubectl 1.15+(Optional).

### Steps:
1. Build and push the Docker image in goapp by following the instructions in [README.md](goapp/README.md).
2. Once done using [Vagrantfile](Vagrantfile) boot the Virtual Machine and configure it using Ansibe.
3. Once the VM configured the application can be accessed on `curl http://localhost:8000`.

### Vagrant VM configuration.
1. Use `vagrant up` to provision the VM which will be configured by ansible.
2. The values of the variables can be configured in [ansible/roles/vagrant/vars/main.yaml](ansible/roles/vagrant/vars/main.yaml).
<!--[a relative link](other_file.md)-->
3. The vm can be reconfigured again post setup and the same can be applied by using `vagrant provision`.