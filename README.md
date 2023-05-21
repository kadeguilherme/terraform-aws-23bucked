# Módulo de Back-end S3 para Terraform

Este módulo fornece uma solução para configurar um back-end remoto S3 para o Terraform. 
## Recursos
Este modulo cria os seguintes recursos:
-  Bucket S3
-  Dynamodb
-  KMS
-  IAM AWS

# Uso
Para usar este modulo, inclua o seguinte trecho de codigo em seu arquivo de configuraćao Terraform:

```hcl
provider "aws" {
  region = "us-east-1"
}
 
module "s3backend" {
  source    = "github.com/kadeguilherme/terraform-aws-s3bucked"     
  namespace = "<name>"
}
 
output "s3backend_config" {
  value = module.s3backend.config                    
}
```
