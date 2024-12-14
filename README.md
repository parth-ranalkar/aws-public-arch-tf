# AWS Architecture with Terraform  

This repository contains a Terraform configuration to deploy a highly available AWS infrastructure, including:  
- **2 EC2 instances** in different Availability Zones  
- **VPC** with public subnets, Internet Gateway, and routing tables  
- **Application Load Balancer (ALB)** for traffic distribution  
- **Security Groups** for controlled access  
- **S3 bucket** for storage  

## 📜 Architecture Overview  
![tf(1)](https://github.com/user-attachments/assets/43deb334-c0e3-44ab-86d0-d72f6abb9c10)

### Features  
- High availability by deploying resources across multiple AZs  
- Load balancing using ALB with health checks  
- Secure access through properly configured security groups  
- Automated deployment using Terraform  

## 🚀 Getting Started  

### Prerequisites  
- AWS account with appropriate permissions  
- Terraform installed ([Download here](https://www.terraform.io/downloads))  
- An SSH key pair for EC2 access  

### Setup Instructions  

1. **Clone the Repository**  
   ```bash
   git clone https://github.com/your-username/aws-public-arch-tf.git
   cd aws-public-arch-tf
Set Up Variables
Create a terraform.tfvars file to provide input values. Example:

cidr_block = "10.0.0.0/16"

Review and Edit Configuration
Update the configurations in main.tf if needed. For example:

    AMI IDs
    Instance types

Initialize Terraform
Initialize Terraform to download required provider plugins:

terraform init

Plan and Apply
Review the execution plan and deploy resources:

terraform plan
terraform apply

Access Resources

    ALB DNS Name: Output after running terraform apply.
    Connect to EC2 instances using SSH:

        ssh -i your-key.pem ec2-user@<instance-public-ip>

📂 Project Structure

├── main.tf              # Core Terraform configuration  
├── provider.tf          # AWS provider configuration  
├── variables.tf         # Input variables    
├── userdata.sh          # Script for EC2 initialization  
└── README.md            # Project documentation  

🛠️ Customization

    AMI IDs: Update the ami field to use your region's latest AMI.
    Instance Types: Change instance_type based on your workload requirements.
    Subnets: Modify cidr_block to fit your IP addressing scheme.

📝 Notes

    Ensure your AWS credentials are configured locally using aws configure or via environment variables.
    The userdata.sh file is used for instance initialization. Customize it to suit your application setup.


🏆 Acknowledgements

Inspired by the need to automate infrastructure deployments and learn Terraform in depth!

Feel free to fork, star ⭐, and contribute to this project! 🚀


Make sure to replace placeholders like `parth-ranalkar` with actual values. Let me know if you want further tweaks!


