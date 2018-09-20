Create and launch an EC2 Ubuntu instance with Nginx

**Prerequisites:**
- AWS account
- Python
- Ansible
- boto3

Create your own `aws_pass.yml` file with `ansible-vault create aws_keys.yml` and include the below lines replacing XXXXXXXXXXXX with your credentials:
```
aws_access_key: XXXXXXXXXXXX
aws_secret_key: XXXXXXXXXXXX
```

Install and run:
```
git clone https://github.com/imukadam/ec2-nginx
cd ec2-nginx
rm aws_keys.yml
ansible-vault create aws_keys.yml
ansible-playbook aws_provisioning.yml --ask-vault-pass
```