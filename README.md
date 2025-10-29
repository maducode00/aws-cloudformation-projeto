# 🚀 Projeto de Infraestrutura Automatizada na AWS com CloudFormation

Este projeto tem como objetivo demonstrar a criação de uma infraestrutura básica na AWS utilizando o serviço **CloudFormation**, que permite definir e provisionar recursos de forma automatizada através de templates em YAML.

---

## 📦 Recursos Criados

O template `infraestrutura.yaml` provisiona os seguintes componentes:

- **VPC (Virtual Private Cloud)**: Rede isolada para os recursos
- **Sub-rede pública**: Permite que a instância EC2 tenha acesso à internet
- **Internet Gateway**: Conecta a VPC à internet
- **Tabela de rotas**: Define o caminho de saída para a internet
- **Grupo de segurança (Security Group)**: Libera acesso via SSH (porta 22)
- **Instância EC2**: Servidor virtual com Amazon Linux
- **Bucket S3**: Armazenamento de objetos com nome dinâmico

---

## 📁 Estrutura do Repositório

aws-cloudformation-projeto/
 ├── infraestrutura.yaml # Template CloudFormation com os recursos 
 └── README.md # Documentação do projeto

 
---

## 🛠️ Pré-requisitos

Antes de iniciar, você precisa:

- Uma conta na [AWS](https://aws.amazon.com/)
- Permissões para criar recursos via CloudFormation
- Familiaridade com o console da AWS ou AWS CLI

---

## 📋 Como Usar o Template

### 1. Acesse o Console do CloudFormation

- [AWS CloudFormation Console](https://console.aws.amazon.com/cloudformation)

### 2. Crie uma Nova Stack

1. Clique em **Create Stack** → **With new resources (standard)**
2. Escolha **Upload a template file**
3. Envie o arquivo `infraestrutura.yaml`
4. Clique em **Next**
5. Dê um nome para a stack (ex: `InfraMaria`)
6. Clique em **Next** até a tela de revisão
7. Marque a opção de permissão (se necessário)
8. Clique em **Create Stack**

### 3. Acompanhe a Criação

- Acesse a aba **Events** para ver o progresso
- Aguarde o status **CREATE_COMPLETE**

---

## 🔍 Verificando os Recursos Criados

- **EC2**: [Console EC2](https://console.aws.amazon.com/ec2)
- **S3**: [Console S3](https://console.aws.amazon.com/s3)
- **VPC/Sub-rede**: [Console VPC](https://console.aws.amazon.com/vpc)

---

## 📌 Observações

- O template usa uma **Amazon Machine Image (AMI)** específica. Verifique se o ID `ami-0c55b159cbfafe1f0` está disponível na sua região. Você pode substituir por outro AMI compatível.
- O bucket S3 é nomeado dinamicamente com base na região e conta AWS.
- O acesso SSH está liberado para qualquer IP (`0.0.0.0/0`). Para produção, recomenda-se restringir esse acesso.

---

## 📈 Possíveis Expansões

Você pode evoluir este projeto adicionando:

- Banco de dados RDS
- Auto Scaling Group
- Load Balancer (ELB)
- Versionamento no S3
- Lambda Functions
- Monitoramento com CloudWatch

Se quiser ajuda para expandir, é só pedir!

---

## 👩‍💻 Autor

Projeto criado por **Maria**, como parte de um desafio de automação de infraestrutura na nuvem com AWS e CloudFormation.

---

## 📄 Licença

Este projeto está sob a licença MIT. Sinta-se livre para usar, modificar e compartilhar.


