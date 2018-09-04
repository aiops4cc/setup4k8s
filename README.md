# buildk8s
The Automation Scripts is only used for initial a fresh kubernetes cluster envrionment
Support OS: Centos and Ubuntu
Prequisite:
1. The ansbile server can ssh to kubernetes master/worker node without password and be able to sudo to root
2. The target master/worker node be able to access internet
3. Centos Version is 7 or higher

Be Caution:
Don't run the script in production environment, the script include kubeadm reset, it will reset all your current configuration
This script is just used for study kubneretes and setup a testing environment for you

Usuage:
1. Upload the correct ip in hosts inventory
2. Remove all docker and kubernetes on target master/worker
   ansible-playbook -i hosts cleanhouse4k8s.yml
3. Setup Kubentes Cluster
   ansible-playbook -i hosts setupk8scluster.yml
