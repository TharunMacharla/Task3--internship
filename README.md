![WhatsApp Image 2025-04-10 at 21 19 07_a45f4524](https://github.com/user-attachments/assets/98f82389-a006-45a5-8335-737565cf66ef)# Terraform Docker Container Provisioning

This project demonstrates how to provision a local Docker container using *Terraform*.

# Objective

Provision and manage a Docker container using Terraform.


# Project Structure

. ├── main.tf # Terraform configuration file ├── README.md # Project documentation

# Steps to follow:

**1. Launch and Connect to Your Instance**
Create a new EC2 instance (Amazon Linux/Ubuntu recommended).
Connect to the instance via SSH:
ssh -i your-key.pem ec2-user@your-public-ip

**2. Install AWS CLI, Terraform, and Configure AWS**
   
**3. Set Up Terraform Project**
Create a new directory and navigate into it:
mkdir terraform-docker && cd terraform-docker
Create two files:
main.tf – To define provider and required versions
resource.tf – To define the Docker container resource

**4. Initialize and Apply Terraform**
Run the following commands:
terraform init
terraform validate
terraform plan
terraform apply
Confirm when prompted. This will provision a Docker container.

**5. Verify Docker Container**
Check if the container is running:
docker container list
docker ps -a

**6 Access Your Application**
Copy the public IP address of your EC2 instance.
Append the port number exposed by the container (e.g., :8080).
Paste it into your browser:
<your-ec2-public-ip>:<port>

**7. Destroy the Infrastructure (Clean Up)**
When you're done, destroy the Docker container with:
terraform destroy
Confirm the destroy operation when prompted.
   
# Results:

![Screenshot (124)](https://github.com/user-attachments/assets/c42e0f1d-256b-4610-827f-e9cd67a35a57)

![Screenshot (126)](https://github.com/user-attachments/assets/87ea756d-c68e-4b4b-9482-99e8eb337a2f)

