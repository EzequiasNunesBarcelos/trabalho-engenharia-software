# trabalho-engenharia-software

Trabalho de Engenharia de Software do Prof Henry em 2026-02



Este repositório é onde vou guardar meu trabalho da disciplina de Engenharia de Software.

## Diagrama UML

```mermaid

   classDiagram
    class Cliente["👤 Cliente"] {
        +int idCliente
        +string nome
        +string cpf
        +string telefone
        +string email
        +cadastrar()
        +atualizarDados()
    }

    class Animal["🐾 Animal"] {
        +int idAnimal
        +string nome
        +string especie
        +string raca
        +int idade
        +float peso
        +obterHistorico()
    }

    class Veterinario["👨‍⚕️ Veterinario"] {
        +int idVeterinario
        +string nome
        +string crmv
        +string especialidade
        +string telefone
        +atenderConsulta()
    }

    class Consulta["📅 Consulta"] {
        +int idConsulta
        +string dataHora
        +string motivo
        +string diagnostico
        +float valor
        +agendar()
        +cancelar()
        +finalizar()
    }

    class Receita["📄 Receita"] {
        +int idReceita
        +string dataEmissao
        +string instrucoes
        +gerarPDF()
    }

    class Medicamento["💊 Medicamento"] {
        +int idMedicamento
        +string nome
        +string dosagem
        +string posologia
    }

    class Exame["🔬 Exame"] {
        +int idExame
        +string nomeExame
        +string resultado
        +string dataExame
        +solicitarExame()
    }

    Cliente -- Animal
    Animal -- Consulta
    Veterinario -- Consulta
    Consulta -- Receita
    Consulta -- Exame
    Receita -- Medicamento
```

### Diagrama de Classe

```mermaid
classDiagram
    class Cliente {
        +idCliente: int
        +nome: string
        +cpf: string
        +telefone: string
        +email: string
        +cadastrar()
        +atualizarDados()
    }

    class Animal {
        +idAnimal: int
        +nome: string
        +especie: string
        +raca: string
        +idade: int
        +peso: float
        +obterHistorico()
    }

    class Veterinario {
        +idVeterinario: int
        +nome: string
        +crmv: string
        +especialidade: string
        +telefone: string
        +atenderConsulta()
    }

    class Consulta {
        +idConsulta: int
        +dataHora: string
        +motivo: string
        +diagnostico: string
        +valor: float
        +agendar()
        +cancelar()
        +finalizar()
    }

    class Receita {
        +idReceita: int
        +dataEmissao: string
        +instrucoes: string
        +gerarPDF()
    }

    class Medicamento {
        +idMedicamento: int
        +nome: string
        +dosagem: string
        +posologia: string
    }

    class Exame {
        +idExame: int
        +nomeExame: string
        +resultado: string
        +dataExame: string
        +solicitarExame()
    }

    Cliente -- Animal : possui
    Animal -- Consulta : realiza
    Veterinario -- Consulta : conduz
    Consulta -- Receita : gera
    Consulta -- Exame : solicita
    Receita -- Medicamento : contem
    

    

    
```
