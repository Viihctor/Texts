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
  
