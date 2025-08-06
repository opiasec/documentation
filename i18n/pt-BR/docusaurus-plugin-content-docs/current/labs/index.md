# Labs

## Visão Geral
*Labs* é um projeto open-source que fornece uma plataforma para aprender Segurança de Aplicações de forma prática. Oferece uma variedade de **labs efêmeros** e **exercícios** práticos que cobrem diferentes aspectos da segurança de aplicações.

### Recursos
- **Labs Práticos**: Labs interativos que permitem praticar suas habilidades em um ambiente seguro.
- **Ambientes Efêmeros**: Cada lab roda em seu próprio ambiente isolado, garantindo que seu trabalho não afete outros e possa ser facilmente resetado.
- **Avaliadores**: Ferramentas automatizadas que avaliam seu trabalho e fornecem feedback, ajudando você a aprender e melhorar.
- **Revisão Manual**: Além das avaliações automatizadas, alguns labs podem requerer revisão manual por instrutores ou colegas para tarefas mais complexas.

### Stack Tecnológica
O projeto *Labs* é construído usando uma stack que inclui:
- **Frontend**: Angular (com PrimeNG).
- **Backend**: Golang (com Echo).
- **API**: Golang (com Echo).
- **Orquestrador**: Kubernetes para gerenciar ambientes de lab.
- **Banco de Dados**: PostgreSQL, Redis e MongoDB.

--- 
## Arquitetura
O projeto *Labs* é projetado para ser modular e extensível, permitindo a fácil adição de novos labs e exercícios. A arquitetura inclui:
- **Frontend**: Uma interface amigável ao usuário, fornecendo acesso a labs e exercícios.
- **Backend**: Um servidor que desempenha o papel de BFF (Backend for Frontend), lidando com requisições do frontend e comunicando com a API do Cluster e banco de dados.
- **Banco de Dados**: Um banco de dados que armazena o progresso do usuário, configurações de lab e resultados de avaliação.
- **API do Cluster**: Uma API que gerencia o ciclo de vida dos ambientes de lab, incluindo criação, exclusão e atualizações de status.

![Diagrama de Arquitetura](/img/labs/architecture.png)
