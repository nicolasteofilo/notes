[Artigo: O que é OPP - Kipper](https://dev.to/fernandakipper/programacao-orientada-objetos-e-programacao-procedural-qual-a-diferenca-22lj)
### O que é a Programação Orientada a Objetos e Qual a diferença para a PC (Programação Procedural)
Na POO a ideia principal é que tudo dentro do nosso programa são classes e objetos, onde as classes são os agrupadores de funcionalidade e informações, e os objetos são os participantes desses grupos.

Os métodos que são criados dentro das classes são abstrações que servem para expor somente as funções que operam os nossos dados e esconder esses dados em si, pois quem está usando essa classe não precisa e nem deve ter acesso a lógica interna da classe.

Já a PC é basicamente um programa que não possui essas separações mais bem definidas, mas sim se resume a modularizar instruções de execução do programa em procedimentos, com chamadas de funções e métodos. Deferente da programação funcional a procedural pode modificar algo de fora do seu escopo e não necessariamente precisam retornar algo, já na funcional, a função sempre retorna algo(mesmo que seja ***void***) e não modifica nada fora de seu escopo.

As modificações que ocorrem fora do escopo na PC, são chamados de ***efeitos colaterais***.

A Orientação a Objetos normalmente deixa o programa mais coeso, pois é mais atrelado ao mundo real, onde cada objeto representa entidades do mundo real ou abstrações.
Cada objeto possou ***dados(atributos)*** e ***comportamentos(métodos)***.

### Os 4 pilares da programação Orientada a Objetos
- Encapsulamento: Protege os dados, expondo normalmente somente os métodos que manipulam e exibem os dados, expondo somente o necessário.
- Herança: Permite que uma classe derive da outra, o que gera um bom reaproveitamento de código e de lógicas.
- Polimorfismo: Permite tratar **objetos** de forma diferente, dependendo do contexto em que ele está inserido
- Abstração: Simplifica a complexidade, focando apenas nos aspectos essenciais

### Diferenças entre Programação Funcional(PF),  Programação Procedural(PC) e Orientada a Objetos(POO)
1. **Funcional**:
    - Baseada em funções puras, sem alterar estados ou variáveis externas.
    - Enfatiza a **imutabilidade** e a **composição de funções**.
    - Exemplos: Haskell, Elixir, JavaScript (quando usado funcionalmente).
2. **Procedural**:
    - Baseada na execução de **procedimentos** (funções ou sub-rotinas).
    - Geralmente organiza o código em **sequências de instruções**, manipulando diretamente os dados.
    - Foco em **estrutura linear** e **fluxo de controle**.
    - Exemplos: C, Pascal.
3. **Orientada a Objetos**:
    - Estrutura o código em **objetos** interagindo entre si.
    - Usa conceitos como herança, encapsulamento e polimorfismo.
    - Exemplos: Java, C#, Python (POO).

***Resumo***
- **Funcional**: Matemática e declarativa, sem estados.
- **Procedural**: Sequencial e focada em funções, altera os estados globais.
- **POO**: Abstrata, modular e centrada em objetos.