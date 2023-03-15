# Ansible | Installing Kuberentes Clusted (1 Master Node and 1 Worker Node) using Kubeadm

## Project Stack.

![alt text](https://github.com/mo7medsalah7/Install-Kubernetes-Cluster-Using-Ansible-and-Kubeadm/blob/main/diagrams/project_stack.png)

### Operatin System
- **CentOS Stram 9** (Ansible Controller).
- **Centos Stram 8** (Kubernetes Master Node).
- **Centos Stream 8** (Kubernetes Worker Node).

### Container Runtime
- **CRI-O** (https://cri-o.io/)

> **_NOTE:_**
Docker Engine does not implement the CRI which is a requirement for a container runtime to work with Kubernetes. For that reason, an additional service cri-dockerd has to be installed. cri-dockerd is a project based on the legacy built-in Docker Engine support that was removed from the kubelet in version 1.24.

> **_NOTE:_**
Docker as container runtime has become deprecated to work with Kubernetes starting from v1.24. 


### Kubernetes Cluster
- **Kubeadm**:- performs the actions necessary to get a minimum viable cluster up and running.

### Configuration Management
- **Ansible**.


# Roles
- This architecture utilizes the roles that i created in Github repositories and they are public for the community.

### The roles are listed below:-
- **All Nodes( Master and Workers)**
  – Install Kubectl, Kubelet and Kubeadm:-
**https://github.com/mo7medsalah7/Ansible_Install_Kubeadm_Kubectl_Kubelet_Linux_Role**

  – Install Container Runtime Role
 **https://github.com/mo7medsalah7/Ansible_install_CRIO_Role**

- **Master Node Only**
  – Install Master Node Role
**https://github.com/mo7medsalah7/Ansible_Kubeadm_K8S_Master_Role**

  – Install CNI Plugin (Flannel)
**https://github.com/mo7medsalah7/Ansible_install_CNI_Kubeadm_Role**

- **Worker Node only**
  – Install Worker Node Role
**https://github.com/mo7medsalah7/Ansible_Worker_Nodes_Role**

# Verification
- Go to the Master Node and run the following command.
 - `kubectl get nodes`

![alt text](https://github.com/mo7medsalah7/Install-Kubernetes-Cluster-Using-Ansible-and-Kubeadm/blob/main/diagrams/verification.png)
