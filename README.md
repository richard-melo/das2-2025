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
- Códigos S3  
  // Prática com comandos para manipulação de buckets e objetos no Amazon S3  
  - Criar buckets  
  - Fazer upload e download de arquivos  
  - Aplicar políticas de acesso  
  - Testar permissões com diferentes usuários e roles  
  - Utilização de versionamento e lifecycle rules via código

## Aula 31/03
- Códigos S3  
  // Continuação da prática com Amazon S3 utilizando AWS CLI ou SDK  
  - Configuração de CORS via linha de comando  
  - Upload de arquivos grandes com multipart upload  
  - Simulação de cenários de backup, restore e recuperação de desastres  
  - Uso de diferentes classes de armazenamento (Standard, Glacier, etc.)

## Aula 03/04
- Computing (EC2)  // serviço de máquinas virtuais escaláveis da AWS  
- EBS (Elastic Block Store)  // volumes de armazenamento persistente para EC2  
- AMI (Amazon Machine Image)  // imagens usadas para inicializar instâncias EC2

## Aula 07/04
- Placement  
  - Cluster  // instâncias próximas fisicamente para baixa latência e alta performance  
  - Spread  // instâncias distribuídas para alta disponibilidade  
  - Partition  // separação lógica em grupos para isolamento de falhas  
- EC2 Purchase model  
  - On-demand  // paga conforme o uso, ideal para cargas variáveis  
  - Reserved  // instâncias reservadas com desconto, para uso constante  
  - Savings plans  // plano de compromisso com uso, com desconto flexível  
  - Spot  // uso de capacidade ociosa com grande desconto, porém sem garantia de execução contínua

## Aula 10/04
- RDS (Relational Database Service)  // banco de dados gerenciado pela AWS  
- Bancos de dados relacionais  
  // organizados por tabelas, colunas e relações (ex: MySQL, PostgreSQL, Oracle)  
- Bancos de dados não relacionais  
  // estrutura flexível e escalável, ideal para dados sem esquema fixo (ex: DynamoDB, MongoDB)

# Segundo Bimestre

## Aula 05/05
- VPC (Virtual Private Cloud)  // rede virtual isolada na AWS  
- CIDR (Classless Inter-Domain Routing)  
  // definição de intervalo de IPs usados pela VPC  
- Subnet Pública  
  // permite acesso direto à internet, ideal para servidores web

## Aula 12/05
- Fazer os laboratórios [Canvas](https://awsacademy.instructure.com/courses/113113)  
- Guided lab: Creating a Virtual Private Cloud  
  // prática guiada na criação de VPCs com subnets, rotas e gateways  
- Challenge (Café) lab: Creating a VPC Networking Environment for the Café  
  // simulação de ambiente de rede real usando recursos como NAT, IGW e ACLs

## Aula 15/05
- Continuação dos laboratórios [Canvas](https://awsacademy.instructure.com/courses/113113)  
  // reforço prático de conceitos aprendidos sobre VPC  
- Guided lab: Creating a Virtual Private Cloud  
- Challenge (Café) lab: Creating a VPC Networking Environment for the Café

## Aula 19/05
- VPC Peering  
  // conectar duas VPCs diferentes para comunicação privada entre elas  
- AWS VPN Site-to-Site  
  // conexão segura entre redes locais e a nuvem AWS via VPN  
- AWS Direct Connect  
  // conexão física dedicada entre o data center e a AWS, com alta velocidade e baixa latência

## Aula 26/05
- IAM Groups  // grupos para facilitar a aplicação de políticas a múltiplos usuários  
- Roles (funções) e AWS STS (Security Token Service)  
  // funções temporárias com permissões específicas para acessar recursos  
- AWS Cognito  
  // serviço para autenticação e gerenciamento de usuários em aplicações web e mobile

## Aula 29/05
- Criptografia simétrica  
  // mesma chave é usada para criptografar e descriptografar os dados  
- Criptografia assimétrica  
  // usa um par de chaves (pública e privada), mais segura para comunicação entre partes diferentes