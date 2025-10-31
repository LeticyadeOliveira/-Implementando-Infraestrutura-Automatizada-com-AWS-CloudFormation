# Projeto: Implementando Infraestrutura Automatizada com AWS CloudFormation
O objetivo deste repositório é demonstrar o meu aprendizado na **prática** sobre AWS SDKs e AWS CLI, que são ferramentas de desenvolvimento e linha de comando. E implementar uma **infraestrutura automatizada com AWS CloudFormation de forma simulada e segura.**

# CloudFormation e automatização 
-  O AWS CloudFormation é um serviço da AWS que auxilia na automação de criação de recursos na AWS por meio de templates escritos em JSON ou YAML.

- [Arquivo YAML](cloudformations.infra.yaml


Nesse caso eu escolhi YAML, caso o arquivo fosse executado na AWS, o comando seria:
``` bash
aws cloudformation create-stack \
  --stack-name simulacao-luana \
  --template-body file://infra.yaml
```
 - O CloadFormation através desse arquivo yaml, vai:
   1. Criar o bucket S3;
   2. Criar o grupo de segurança com portas 22 e 80 abertas;
   3. Criar a instância EC2 vinculada a esse grupo.


## Apresentando um exemplo prático de como um arquivo YAML define recursos na AWS, como:
- Um **bucket S3** (armazenamento de arquivos)
- Uma **instância EC2** (máquina virtual)
- Um **grupo de segurança** (controle de acessos)
