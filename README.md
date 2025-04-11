
# 🗳️ Votação Microsserviços

Este projeto é uma aplicação web baseada em microsserviços, desenvolvida com foco em escalabilidade, modularidade e facilidade de manutenção. A arquitetura é composta por múltiplos serviços independentes que se comunicam entre si para fornecer uma plataforma de votação.

## 📦 Estrutura do Projeto

O repositório está organizado da seguinte forma:

- `deployments/`: Contém os manifests do Kubernetes para implantar os serviços.
- `namespaces/`: Define os namespaces utilizados para segmentar os ambientes no cluster Kubernetes.
- `services/`: Inclui os arquivos de configuração dos serviços que compõem a aplicação.

## 🚀 Tecnologias Utilizadas

- **Kubernetes**: Orquestração de containers para implantar e gerenciar os microsserviços.
- **Docker**: Containerização dos serviços para garantir portabilidade e consistência.
- **Spring Boot**: Framework utilizado para desenvolver os microsserviços em Java.
- **Redis**: Banco de dados NoSQL utilizado para armazenar os dados da aplicação.
- **Postgre**: Banco de dados SQL utilizado também para armazenar os dados da aplicação.

## ⚙️ Pré-requisitos

Antes de iniciar, certifique-se de ter instalado:

- [Docker](https://www.docker.com/)
- [Kubernetes](https://kubernetes.io/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

## 🛠️ Como Executar

1. **Clone o repositório:**

   ```bash
   git clone https://github.com/PedroAngeloVargas/Votacao_Microsservicos.git
   cd Votacao_Microsservicos
   ```

2. **Configure os namespaces:**

   ```bash
   kubectl apply -f namespaces/
   ```

3. **Implante os serviços:**

   ```bash
   kubectl apply -f deployments/
   kubectl apply -f services/
   ```

4. **Verifique os pods em execução:**

   ```bash
   kubectl get pods --all-namespaces
   ```

5. **Verifique o endereço IP do serviço:**

   Dependendo da configuração do seu cluster, você pode acessar a aplicação via NodePort (localmente) ou LoadBalancer (nuvem), nesse caso está configurado para LoadBalancer. Verifique o serviço exposto:

   ```bash
   kubectl get svc -n vote
   ```

6. **Acesse a aplicação:**

   Insira o endereço ipv4 do LoadBalancer ou NodePort na url do navegador
---

*Créditos ao usuário Mumshad Mannambeth pelo uso das docker images*
link do Docker Hub: https://hub.docker.com/u/kodekloud
