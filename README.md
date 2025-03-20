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
- Tratar recursos com

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
  - Modelo de responsabilidade compartilhado
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
        - Classes frias (sem acesso imediato)
            


