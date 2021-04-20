# ansible-ec2
project 5 for cit496

prereqs:
- amazon.aws (https://github.com/ansible-collections/amazon.aws)
  - install with: `ansible-galaxy collection install amazon.aws`
  - the collection also needs boto/boto3/botocore
    - install with: `apt install python-boto python-boto3 python-botocore`

3 playbooks:
- provisions aws ec2 instance
- configures the instance to run a LAMP stack
  - result: in browser will show id # which auto increments when you refresh the page 
- terminates the instance

to run playbook:
`ansible-playbook -i ec2.py -u ubuntu <playbook>`
