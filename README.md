# ICT-Campus-ITS

Comando per avere una lista delle instance esistenti
```
aws ec2 describe-instances --query 'Reservations[*].Instances[*].{ID:InstanceId,State:State.Name,Type:InstanceType,PublicIP:PublicIpAddress}' --output table
```
