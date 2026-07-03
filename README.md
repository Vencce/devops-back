# Backend - Projeto DevOps

## Descrição
Este repositório contém a API Backend do projeto acadêmico desenvolvido no IFC - Campus Araquari. A API processa a lógica de negócios, conecta-se a um banco de dados PostgreSQL e opera dentro de um ambiente em cluster gerenciado por Kubernetes.

## Tecnologias Utilizadas
* Python
* PostgreSQL
* Docker
* GitHub Actions

## Integração Contínua e Entrega Contínua (CI/CD)
O repositório conta com um pipeline automatizado executado pelo GitHub Actions. A cada nova alteração na branch `main`:
1. Uma nova imagem da API é gerada.
2. A imagem é enviada e armazenada no Docker Hub.
3. O workflow altera o arquivo de manifesto no repositório de infraestrutura (GitOps).
4. O ArgoCD aplica a nova versão no cluster sem causar inatividade no serviço (Zero Downtime).
