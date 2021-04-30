# CloudArchitecture
This repo contains environmrnts I setup in the cloud (aws/azure) using automation tools like  terraform and cloudformation.
The yaml files can be found in the respective folders. Some require more context like the ones below;

## Kubernetes The Not SO Hard Way
So I created a cloudformation template to manually set up a simple kubernetes cluster on 3 ubuntu vm's( one master and two worker nodes) in a custom vpc with subnet &n internet gateway. The config was done using userdata ofcourse you will need to add the worker nodes manually.


![Photo](/aws/thenotsohardway.png)

# Steps to set a kubernetes cluster
These are just series of commands that can be found on the [kubernetes documentation page](https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/){:target="_blank"}
* Letting iptable see bridged traffic
* Installing container runtime(docker)
* Configure the Docker daemon to use systemd for the management
* installing kubeadm, kubelet and kubectl
* Setting up cluster with kubeadm
* Setting up network Addon "weave"

The first 4 steps should be carried out on all nodes while the final two steps should be carried out on just the master node.
Ps I'm  still ahving a tough time troubleshooting some networking issues. You could also use a vagrant template to set this up on virtualbox tho you would have to run the commands manually checkout this repo [link to repo](https://github.com/goekezie/certified-kubernetes-administrator-course) 
