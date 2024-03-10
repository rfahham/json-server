# ERROR

TASK [Gathering Facts] ***************************************************************************************************************************************************************************************
fatal: [44.204.208.40]: UNREACHABLE! => {ansible  -m ping44.204.208.40 port 22: Connection timed out", "unreachable": true}

ssh ec2-user@ec2-44-204-208-40.compute-1.amazonaws.com 
ssh -i "aws-instance-key.pem" ec2-user@ec2-3-219-242-186.compute-1.amazonaws.com

Solução: Configurar o Security Group

***************************************************************************************************************************************************************************************

terraform init        

Initializing the backend...

Initializing provider plugins...
- Finding hashicorp/aws versions matching "5.37.0"...
- Finding latest version of hashicorp/http...
- Installing hashicorp/aws v5.37.0...
- Installing hashicorp/http v3.4.2...
╷
│ Error: Failed to install provider
│ 
│ Error while installing hashicorp/aws v5.37.0: chmod .terraform/providers/registry.terraform.io/hashicorp/aws/5.37.0/linux_amd64/terraform-provider-aws_v5.37.0_x5:
│ operation not permitted
╵

╷
│ Error: Failed to install provider
│ 
│ Error while installing hashicorp/http v3.4.2: chmod .terraform/providers/registry.terraform.io/hashicorp/http/3.4.2/linux_amd64/terraform-provider-http_v3.4.2_x5:
│ operation not permitted


Solução: sudo terraform providers lock && terraform init

***************************************************************************************************************************************************************************************
