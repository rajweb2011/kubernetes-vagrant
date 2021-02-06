
The vagrant file will do the following:
1.  Provision all local VMs using VirtualBox
2.  Install k8s control plane
3.  Initialize cluster with Flannel CIDR block & install Flannel
4.  Join the nodes to the master
5.  Create and copy the SSH key to all machines so you can SSH to any node from the Master.  
8.  Make required Ubuntu OS mods for the cluster to function properly

prerequests 
$ vagrant plugin install vagrant-disksize


## Starting the cluster
vagrant up
## Clean up
$ vagrant destroy -f
## SSH and other Commands
$ vagrant ssh master
$ vagrant ssh node1
$ vagrant ssh node2
$ vagrant ssh node3


Get the status of the Nodes:

$ k get nodes -o wide

$ ssh node1
$ ssh node2
$ ssh node3
