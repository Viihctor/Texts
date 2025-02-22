# Capítulo 7 – Arquitetura  

## 1. Introdução à Arquitetura de Software  
A arquitetura de software é definida como o projeto em mais alto nível de um sistema. Em vez de focar em classes individuais, ela se concentra em módulos, componentes, subsistemas e serviços. Além disso, envolve decisões críticas, como a escolha da linguagem de programação e banco de dados, que dificilmente podem ser revertidas no futuro.  

## 2. Padrões Arquiteturais  

### 2.1 Arquitetura em Camadas  
Organiza o sistema em camadas hierárquicas, onde cada camada só pode se comunicar com a imediatamente inferior. A Arquitetura em Três Camadas é um exemplo clássico:  
1. **Interface com o Usuário** – responsável pela apresentação e interação com o usuário.  
2. **Lógica de Negócio** – define as regras e operações do sistema.  
3. **Banco de Dados** – gerencia a persistência dos dados.  
Esse modelo facilita a manutenção, escalabilidade e reutilização de código.  

### 2.2 Arquitetura MVC (Model-View-Controller)  
MVC divide a aplicação em três partes:  
- **Modelo**: gerencia os dados e regras de negócio.  
- **Visão**: representa a interface do usuário.  
- **Controlador**: gerencia as interações entre Modelo e Visão.  
Esse padrão facilita a separação de responsabilidades, permitindo múltiplas interfaces para os mesmos dados e facilitando a testabilidade.  

### 2.3 Arquitetura baseada em Microsserviços  
Divide o sistema em módulos independentes (serviços autônomos), que se comunicam por APIs.  
**Vantagens:**  
- Escalabilidade granular.  
- Releases independentes para cada serviço.  
- Flexibilidade para uso de diferentes tecnologias.  
**Desafios:**  
- Comunicação distribuída aumenta a complexidade.  
- Latência nas interações entre serviços.  
- Dificuldade em gerenciar transações distribuídas.  

### 2.4 Arquitetura Orientada a Mensagens  
Utiliza filas de mensagens para comunicação assíncrona entre clientes e servidores.  
**Benefícios:**  
- Desacoplamento no espaço: cliente e servidor não precisam se conhecer.  
- Desacoplamento no tempo: clientes podem continuar funcionando mesmo se o servidor estiver fora do ar.  
Essa abordagem melhora a escalabilidade e resiliência do sistema.  

### 2.5 Arquitetura Publish/Subscribe  
Baseia-se na troca de eventos entre publicadores e assinantes, permitindo que múltiplos sistemas sejam notificados simultaneamente sobre um evento específico.  
**Diferente das Filas de Mensagens:**  
- Os eventos são distribuídos para múltiplos assinantes.  
- Assinantes recebem notificações assíncronas em tempo real.  
Exemplo: um sistema de reservas de passagens pode notificar diferentes serviços, como sistema de milhagens, contabilidade e marketing.  

### 2.6 Outros Padrões Arquiteturais  
- **Pipes & Filtros**: fluxo de dados processado em etapas independentes (exemplo: comandos Unix).  
- **Cliente/Servidor**: arquitetura clássica onde clientes solicitam serviços a um servidor remoto.  
- **Peer-to-Peer (P2P)**: sistemas descentralizados onde cada nó pode atuar como cliente e servidor (exemplo: torrents).  
