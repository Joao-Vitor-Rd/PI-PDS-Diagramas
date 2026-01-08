# Diagrama de Classes - Projeto Procuradoria da Mulher

Este documento apresenta a modelagem arquitetural do sistema desenvolvida como parte da disciplina de **Projeto Integrado 1**.

O objetivo deste diagrama é representar a estrutura estática e o fluxo de comunicação entre os componentes principais do backend da aplicação, focando em manutenibilidade e separação de responsabilidades.

##  Arquitetura Adotada

O sistema segue uma arquitetura robusta baseada em **Camadas** e no padrão de projeto **Mediator**. A estrutura foi desenhada para desacoplar a interface (IPC/Electron) da regra de negócio.

O fluxo de dados segue a seguinte hierarquia:

`Orquestrador (IPC) ➡️ Mediator ➡️ Controller ➡️ Service ➡️ Repository ➡️ Database`

* **IpcOrchestrator:** Ponto central que recebe as requisições do frontend e delega para o mediador correto.
* **Mediators:** Isolam a complexidade e orquestram chamadas para controladores ou repositórios.
* **Controllers/Services:** Contêm as regras de negócio e validações.
* **Repositories:** Responsáveis pela persistência de dados (PostgreSQL) e interfaces de contrato.


## Ferramenta Utilizada para o Diagrama de Classe:
* **Modelagem:** Astah UML

## Autores

Trabalho desenvolvido por:

* **@Joao-Vitor-Rd**
* **@cauanrricardo**


---
*Projeto desenvolvido na [Universidade Federal do Ceará] - 2026.*
