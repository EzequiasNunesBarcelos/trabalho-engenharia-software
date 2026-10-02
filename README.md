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

### Diagrama de Classe

```mermaid
classDiagram
    class Veterinário  {
        %%atrbutos: caracteristicas que serão
        %% armazenadas no sistema
        -CPF: string
        %% métodos: ações que serão desempenhadas
        %% por essa entidade no sistema
        +darCPF() string
        +atenderAnimal(animal: Animal) void
    }
    Veterinário -- Animal
    Animal -- Cliente
    class Animal {
        - dono: Cliente
        - nome: string
        - raça: string
        - peso: float
        - cor: string
        - sexo: string

    }

    class Cliente {
        -nome: string
        -cpf: string
        -email: string

    }


    

    

    
```
