 Provision-a-local-Docker-container-using-Terraform

 📌 Project Objective
 To implement Infrastructure as Code (IaC) using **Terraform** to automate the provisioning of a **Docker container** (NGINX) on a cloud-hosted **EC2 instance**.

 🧰 Tools & Technologies Used

- **Terraform** (v1.0+)
- **Docker** (v20+)
- **AWS EC2** (Ubuntu)

# Install Docker
sudo apt update
sudo apt install -y docker.io
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker $USER

![Screenshot 2025-05-17 102507](https://github.com/user-attachments/assets/60dbbeaa-9ce1-4918-a768-e90dd4c07a18)

# Install Terraform
sudo apt install -y curl unzip gnupg software-properties-common
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | \
  sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update
sudo apt install terraform


🚀 Terraform Commands
terraform init

![Screenshot 2025-05-17 103433](https://github.com/user-attachments/assets/66853849-4192-4c18-9c04-db3498e81260)

terraform plan

![Screenshot 2025-05-17 104057](https://github.com/user-attachments/assets/a1cd0da3-be9b-499b-b4e3-a07dca7eee1d)

terraform apply

🔍 Check Container
docker ps
![Screenshot 2025-05-17 104145](https://github.com/user-attachments/assets/5e84a051-b877-4ac0-a9e9-b6facfe19c8e)


🧹 Destroy Infrastructure
