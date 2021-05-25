
# FlashStack Converged Infrastructure deployment using Ansible for OpenShift Container Platform 4 bare-metal IPI installation

 This repository is for FlashStack automated deployment covering the following to support OpenShift COntainer platform 4 bare-metal:
 1. Cisco UCS
 2. Cisco Nexus
 3. Pure FlashArray//X R3

This repository contains Ansible playbooks to configure Cisco Nexus, Cisco UCS, Pure FlashArray to prepare the bare-metal infrastructure for OCP4 installation. This repository can be used for setting up Cisco devices as well as Pure FlashArray as covered in following Cisco Validated Design (CVD):
https://www.cisco.com/c/en/us/td/docs/unified_computing/ucs/UCS_CVDs/flashstack_redhat-OCP.html

![image](https://user-images.githubusercontent.com/3585414/116255002-d566e280-a73f-11eb-86f5-d61c4ea4edf5.png)

 
The first three steps illustrated above to deploy FlashStack infrastructure is covered in this repository.

OpenShift IPI automated installation is not part of this repo and the IPI installation repo is available at https://github.com/openshift-kni/baremetal-deploy/tree/master/ansible-ipi-install.

## Usage:
All the details of deploying the FlashStack along with OpenShift Container Platform 4 IPI automated installation is covered in the above mentioned CVD. Refer the document for detailed instructions on how to execute the Ansible Playbooks to bring up the OpenShift Container Platform environment delivered as Infrastructure as Code (IaC).


### Playbook Execution Commands – Summary:
Setup all the variables before executing the playbooks as detailed in the CVD “https://www.cisco.com/c/en/us/td/docs/unified_computing/ucs/UCS_CVDs/flashstack_redhat-OCP.html”

1.	Setup LAN on Nexus and UCS: "ansible-playbook ./Setup_LAN_Connectivity.yml -i inventory"
2.	Setup Cisco UCS: "ansible-playbook ./Setup_UCS.yml -i inventory"
3.	Setup Pure FlashArray: "ansible-playbook ./Setup_MDS.yml -i inventory"
4.	Setup OCP 4 Cluster using IPI install: "ansible-playbook -i inventory/hosts playbook.yml 






