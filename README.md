# DevOps-TerraformP4

Automating Infrastructure using Terraform.
Project 4 

DESCRIPTION

Use Terraform to provision infrastructure

 

Description:

Nowadays, infrastructure automation is critical. We tend to put the most emphasis on software development processes, but infrastructure deployment strategy is just as important. Infrastructure automation not only aids disaster recovery, but it also facilitates testing and development.

Your organization is adopting the DevOps methodology and in order to automate provisioning of infrastructure there's a need to setup a centralised server for Jenkins.

Terraform is a tool that allows you to provision various infrastructure components. Ansible is a platform for managing configurations and deploying applications. It means you'll use Terraform to build a virtual machine, for example, and then use Ansible to instal the necessary applications on that machine.

Considering the Organizational requirement you are asked to automate the infrastructure using Terraform first and install other required automation tools in it.

Tools required: Terraform, AWS account with security credentials, Keypair

 

Expected Deliverables:

Launch an EC2 instance using Terraform

Connect to the instance

Install Jenkins, Java and Python in the instance

-----------------------------------------------------------------------

Chmod 400 keypair.pem
Ssh-add keypair.pem
Ssh ec2-user@ipadd
Sudo bash     -> navigate to ROOT user

Install Teraform in in the current EC2-instance
yum install teraform 

Create IAM Admin-user via AWS EC2 instance

Configure AWS in EC2 instance with the new EC2 instance

> aws configyre
> AWS Access ID   > AWS Secret access key > region(us-east-1)  > default output (json)
> aws sts get-caller-identity

Ssh ec2-user@ip
Sudo bash
Yum install git
git clone https://github.com/iJacob10/DevOps-TerraformP4

    // creating key-gen
Ssh-keygen
    //copy the public key 
Cat ~/.ssh/id_ras.pub
    // and paste it to main.tf public_key 
Vim main.tf

> Terraform init             -> to initialize the folder to terraform
> terraform plan   	         -> to view the proposed terraform plan (Stage)
> terraform apply	           -> to apply the proposed plan to the new IAM user
> Terraform state refresh    -> to refresh the ip with local ip. Since, local state is not getting refreshed – the ip is not getting updated to public_ip

Validating Installations of Jenkins, Java and Python in the new instance created via terraform

Ssh-add
Ssh ec2-user@browserip
Docker ps    -> Jenkins
             -> Java -version
             -> Python .






