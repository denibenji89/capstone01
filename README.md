# capstone01

<b>Project 1: Infra Optimization </b>

Question 1b.	Automate the provisioning of an EC2 instance using Ansible or Chef Puppet
See ec2.yaml for provisioning of EC2 instance in VPC using Ansible

Question 1d.	Implement the network policies at the database pod to allow ingress traffic from the front-end application pod
See mysql-network-policy.yaml with pod selector for mysql tier on port 3306.

Question 1e.	Create a new user with permissions to create, list, get, update, and delete pods
See /create-user folder for outputs, 
For Roles and role-binding wiht user: create-user/podadmin-role.yaml and create-user/ben-podadmin-binding.yaml

Question 1f.	Configure application on the pod
Step 1: Create secret for mysql password
kubectl create secret generic mysql-pass --from-literal password=Password123
Step 2: Create MySQL database application by kubectl apply the following files mysql-app.yaml,  mysql-pv.yaml,  mysql-pvc.yaml,  mysql-service.yaml
Step 3: Create Wordpress application by kubectl apply the following files wp-app.yaml,  wp-lbservice.yaml,  wp-pv.yaml,  wp-pvc.yaml
