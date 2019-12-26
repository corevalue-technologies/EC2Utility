EC2Utility

Usages: you can turn ON or OFF you aws ec2 instances directly by a get request.<br/>
Need: many time when we are away from laptop and we have to immediatly turn the EC2 off or on, we can use it by our mobile phone. :-)

use below instructions after setting up go and aws cli

CREATE ONE lambda and set its hook as EC2Utility

run below command

``env GOOS=linux GOARCH=amd64 go build -o /tmp/EC2Utility . && zip -j /tmp/EC2Utility.zip /tmp/EC2Utility && aws lambda update-function-code --function-name Ec2Utility --zip-file fileb:///tmp/EC2Utility.zip``
