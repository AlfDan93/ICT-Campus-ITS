# ICT-Campus-ITS

Installazione di Ansible
```
sudo apt install python3-pip
pip3 install boto3 botocore
sudo apt install ansible
```

Installazione collezioni Ansible
```
ansible-galaxy collection install amazon.aws
ansible-galaxy collection install ansible.posix
```


Comando per avere una lista delle instance esistenti
```
aws ec2 describe-instances --query 'Reservations[*].Instances[*].{ID:InstanceId,State:State.Name,Type:InstanceType,PublicIP:PublicIpAddress}' --output table
```

Comando per avviare una instanza con aws-cli
```
aws ec2 start-instances --instance-ids $instance_id
```

Comando per stoppare una instanza con aws-cli
```
aws ec2 stop-instances --instance-ids $instance_id
```

Comando per cancellare una instaza con aws-cli
```
aws ec2 terminate-instances --instance-ids $instance_id
```
