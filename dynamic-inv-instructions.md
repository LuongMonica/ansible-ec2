https://aws.amazon.com/blogs/apn/getting-started-with-ansible-and-dynamic-amazon-ec2-inventory-management/

use the files ec2.py and ec2.ini
- ec2.py: your inventory file
  - make sure to chmod it so that it's executable: chmod a+x
- ec2.ini: your config file
  - i edited this file to limit the regions the instances will be deployed

test it works with your account:
`ansible all -m ping -i ec2.py`
`./ec2.py --list`

set env vars:
- for aws:
  - AWS_REGION
  - AWS_ACCESS_KEY_ID
  - AWS_SECRET_ACCESS_KEY
- for ansible:
  - ANSIBLE_HOSTS
  - EC2_INI_PATH

examples:
(put in ~/.bashrc or ~/.profile)
- `export ANSIBLE_HOSTS=/etc/ansible/ec2.py`
- `export EC2_INI_PATH=/etc/ansible/ec2.ini`
- `export AWS_REGION=us-east-1`
