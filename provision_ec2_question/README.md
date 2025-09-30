# EC2 Provisioning – Ansible Challenge

## Scenario
Your team needs to automate the creation of an **EC2 instance** in AWS using **Ansible**. The playbook should create a running instance in a specific VPC and subnet, apply tags, and make it accessible for login.

---

## Requirements
Your playbook should:

1. **Create an EC2 instance**  
   - Launch the instance in a specified VPC and subnet.  
   - Use variables for region, instance type, AMI ID, and key pair.    

2. **Access configuration**  
   - Use `key_name` to allow access to the instance:  
     - **Linux**: SSH with the key pair.  
     - **Windows**: Use the key pair to decrypt the Administrator password for RDP.  

3. **Tagging**  
   - Add tags (Example: `Name` and `Project`, etc.) 

4. **Validation**  
   - Wait until the instance is in the `running` state.  
   - Output the instance’s private IP address.  

---

## Guidelines
- Make the playbook **idempotent** (running it multiple times should not create duplicate instances).  
- Make it **reusable** (parameterize variables instead of hardcoding values).  
- Keep it **readable** (use clear task names and comments).  

---

## Stretch Goals (Optional)
- Attach security groups for network access (e.g., SSH for Linux or RDP for Windows).
- Launch multiple instances using loops.  
- Add **termination protection** to prevent accidental deletion.  

---

## What We’re Looking For
- Understanding of the `amazon.aws.ec2_instance` module.  
- Proper handling of **variables** and **tags**.  
- Awareness of **Linux vs. Windows access differences**.  
- Clean, maintainable Ansible code.  
