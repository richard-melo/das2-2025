# Design e Arquitetura de Software 2 Rihard Luiz Melo Neto

## Aula 24/02
- Well-Architect Framework
  - Excelencia operacional
  - Segurança
  - Confiabilidade (Reliabillity)
  - Eficiência em performance
  - Otimização de custos
  - Sustentabilidade

## Aula 27/02/2025
### Design trade-offs
- Consistencia (Informação foi mandada para o banco e existe a garantia que ela fique lá)
- Durabilidade 
- Space (Terceira forma normal - BD)
- Melhorar a disponibilidade de uma aplicação = custo maior
- Tratar recursos como descartáveis [// adicionado para complementar o conceito de infraestrutura imutável]
- Escalabilidade/Elasticidade [// importante para arquiteturas cloud]

## Aula 06/03
- Trade-Offs
  - Evitar ponto único de falha
  - Otimização de custo
  - Use de cache
  - Proteger sua infraestrutura
- Infraestrutura global da AWS
  - Regiões
  - Zonas de Disponibilidade
  - Local Zones
  - Data Centers

## Aula 10/03
- Infraestrutura global da AWS
  - POPs - Edge Location
- Segurança
  - Modelo de responsabilidade compartilhada
  - Autenticação
  - Autorização
  - Princípio do privilégio mínimo
  - Criptografia

## Aula 13/03
- Modelo de responsabilidade compartilhada
- Princípio do privilégio mínimo
- Autenticação
- Autorização
- Identity and Access Management
- Usuários
- Acesso pela console / acesso programático

## Aula 17/03
- Policy de Identidade
- Policy de Recurso
- S3

## Aula 20/03
- Amazon S3
    - Static site (site em html, css)
    - Financial analysis
    - Disaster recovery
    - Todos os arquivos são criptografados
    - Uploads:
        - web
        - cli
        - api rest
    - Multipart upload 
        (para OBJETOS que tem o tamanho maior que 5 tb)
    - AWS Transfer family
    - Object storage classes (Preço e disponibilidade)
        - Classes quentes (acesso imediato) | Preço de armazenamento maior e altamente disponível
            - S3 Standard (padrão, melhor disp, menor preço)
        - Classes frias (sem acesso imediato) [// S3 Glacier para arquivamento de longo prazo]

## Aula 24/03
- S3 - Gerenciamento de ciclo de vida
- S3 - Versionamento
- S3 - CORS

```bash
[
    {
        "AllowedHeaders": [
            "*"
        ],
        "AllowedMethods": [
            "GET",
            "PUT",
            "POST",
            "DELETE"
        ],
        "AllowedOrigins": [
            "http://127.0.0.1:5500"
        ],
        "ExposeHeaders": [
            "x-amz-server-side-encryption",
            "x-amz-request-id",
            "x-amz-id-2"
        ],
        "MaxAgeSeconds": 3000
    }
]
## Aula 27/03
- Amazon S3 (códigos práticos)
    - Criação e configuração de buckets via CLI ou SDK
    - Aplicação de políticas de acesso [// prática de controle de acesso]
    - Upload e download de arquivos
    - Versionamento de objetos em código
    - Testes com diferentes tipos de permissões

## Aula 31/03
- Amazon S3 (continuação dos códigos)
    - Configuração de CORS via linha de comando
    - Multipart upload para arquivos grandes
    - Simulação de cenários com recuperação de desastres
    - Uso de storage classes [// balancear custo e disponibilidade]

## Aula 03/04
- Amazon EC2 [// serviço de máquinas virtuais escaláveis]
- EBS (Elastic Block Store) [// armazenamento persistente conectado às instâncias EC2]
- AMI (Amazon Machine Image) [// imagens com SO + apps pré-configurados]

## Aula 07/04
- Placement strategies:
    - Cluster [// baixa latência, alta performance]
    - Spread [// maior disponibilidade e tolerância a falhas]
    - Partition [// isolamento de falhas em grandes cargas]
- EC2 Purchase Models:
    - On-demand [// pago por hora ou segundo, flexível]
    - Reserved [// reserva com desconto, ideal para cargas previsíveis]
    - Savings Plans [// compromisso de uso em troca de desconto]
    - Spot [// uso de instâncias ociosas com grande desconto]

## Aula 10/04
- RDS (Relational Database Service) [// serviço gerenciado de banco de dados relacional]
- Bancos de dados relacionais
    - MySQL, PostgreSQL, Oracle [// modelo baseado em tabelas]
- Bancos de dados não relacionais
    - DynamoDB, MongoDB [// modelo flexível, sem esquema fixo]

# Segundo Bimestre

## Aula 05/05
- VPC (Virtual Private Cloud) [// rede virtual privada na AWS]
- CIDR (Classless Inter-Domain Routing) [// define o intervalo de IPs da VPC]
- Subnet pública [// sub-rede com acesso à internet via IGW]

## Aula 12/05
- Guided Lab: Creating a Virtual Private Cloud
    - Configuração de VPC, subnets, tabelas de rotas, gateways
- Challenge Lab: VPC Networking do Café [// simulação de ambiente completo]
- Laboratórios disponíveis no [Canvas](https://awsacademy.instructure.com/courses/113113)

## Aula 15/05
- Continuação dos laboratórios de VPC [Canvas]
    - Reforço na criação e segmentação de rede
    - Configuração de segurança e conectividade
    - Desafios com NAT Gateway, ACLs, roteamento

## Aula 19/05
- VPC Peering [// permite comunicação entre duas VPCs]
- AWS VPN Site-to-Site [// conexão segura entre rede local e AWS]
- AWS Direct Connect [// link físico dedicado para alta performance]

## Aula 26/05
- IAM Groups [// gerenciamento coletivo de permissões]
- Roles e AWS STS (Security Token Service) [// autenticação temporária baseada em políticas]
- AWS Cognito [// autenticação e gerenciamento de usuários para apps web/mobile]

## Aula 29/05
- Criptografia Simétrica [// mesma chave para criptografar e descriptografar]
- Criptografia Assimétrica [// par de chaves pública/privada para segurança e troca segura de dados]

## Aula 09/06
# Aula do dia 09/06

Fazer os laboratórios Canvas
# Realizar os laboratórios disponíveis na plataforma Canvas

Guided lab: Creating a Highly Available Environment
# Laboratório guiado para criar um ambiente altamente disponível (ex: múltiplas zonas de disponibilidade)

Challenge (Café) lab: Creating a Scalable and Highly Available Environment for the Café
# Laboratório desafio do projeto Café, criando um ambiente escalável e altamente disponível

## Aula 12/06
# Aula do dia 12/06

Fazer os laboratórios Canvas
# Realizar os laboratórios disponíveis na plataforma Canvas

Guided lab: Creating a Highly Available Environment
# Laboratório guiado para criar um ambiente altamente disponível (provavelmente revisão ou aprofundamento do anterior)

Challenge (Café) lab: Creating a Scalable and Highly Available Environment for the Café
# Laboratório desafio do projeto Café, criando um ambiente escalável e altamente disponível (continuação ou nova versão)

## Aula 16/06
# Aula do dia 16/06

Load Balancer
# Estudo sobre balanceadores de carga (distribuição de tráfego entre instâncias/servidores)

DNS
# Estudo sobre DNS (Domain Name System) e seu funcionamento na web

## Aula 23/06
# Aula do dia 23/06

Infraestrutura como código
# Conceito de Infrastructure as Code (IaC), usando ferramentas como CloudFormation, Terraform, etc.

## Aula 26/06
# Aula do dia 26/06

Como reduzir acoplamento das aplicações
# Estudo sobre boas práticas para reduzir acoplamento entre aplicações (ex: APIs, microserviços, filas)
