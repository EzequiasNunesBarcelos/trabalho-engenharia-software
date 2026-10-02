# trabalho-engenharia-software

Trabalho de Engenharia de Software do Prof Henry em 2026-02



Este repositório é onde vou guardar meu trabalho da disciplina de Engenharia de Software.

## Diagrama UML

```mermaid
flowchart TD
   %% atores
    cliente["👨‍🦰 cliente"]
    garçom[" 💁‍♂️ garçom"]

    %% ações
    subgraph sistema
       comida["pedir comida"]
       vinho["pedir vinho"]
    end

     %% relacionamentos
    cliente -- "faz pedido" --- comida
    garçom -- "recebe pedido" --- comida

     vinho -. "estande" .-> comida

```


