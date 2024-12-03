## Abstração
A **abstração** consistem em esconder os detalhes internos e expor somente as características essenciais de um objeto. Basicamente é a a habilidade de representamos um objeto do mundo real com seus atributos e comportamentos que são relevantes somente para o contexto, ignorando aspectos desnecessários.

#### *Classes Abstratas*
As Classes Abstratas são um tipo de classe que não podem ser instanciadas, ele serve somente como um modelo e como uma abstração de funcionalidades que serão compartilhadas entre suas classes derivadas, que usam da ***Herança***.  Elas podem conter ***métodos abstratos(sem implementação)*** e ***métodos concretos(com implementação)***.

#### *Interfaces*
As Interfaces definem um contrato, um modelo definido que as classes devem seguir, diferente das classes abstratas, as interfaces não possuem nenhuma implementação, servem somente como um modelo que como a nossa classe deve ser construída e estruturada.

## Encapsulamento
O encapsulamento consistem em proteger os nossos dados, proteger os dados de um objeto, restringindo o acesso direto a esses dados. Com uma estratégia de encapsulamento nós deixaremos de exibir esses dados e será exposto métodos e propriedade que espoem esses dados de maneira segura e controlada.

- A principal ideia é que um objeto deve controlar como suas informações internas são acessadas ou modificadas, promovendo maior **segurança**, **organização** e **manutenção** no código.

Dentro do C# o encapsulamento é implementado usando ***modificadores de acesso***, como:
- **`public`**: O membro é acessível de qualquer lugar.
- **`private`**: O membro só é acessível dentro da própria classe.
- **`protected`**: O membro é acessível dentro da classe e em classes derivadas.
- **`internal`**: O membro é acessível dentro do mesmo assembly/projeto.

Exemplo de classe:
```C#
namespace OPP;  
  
public class BankAccount  
{  
    private decimal Balance; // private field  
    public string Holder { get; private set; }  
  
    public BankAccount(decimal balance, string holder)  
    {  
        Balance = balance;  
        Holder = holder;  
    }  
    public decimal GetBalance() => Balance;  
      
    public void Deposit(decimal amount)  
    {  
        if (amount <= 0)  
            throw new ArgumentException("Deposit amount must be greater than zero");  
          
        Balance += amount;  
        Console.WriteLine($"Deposited {amount:C}");  
    }  
  
    public void Withdraw(decimal amount)  
    {  
        if (amount <= 0)  
            throw new ArgumentException("Deposit amount must be greater than zero");  
          
        Balance -= amount;  
        Console.WriteLine($"Withdrawn {amount:C}");  
    }  
}
```
Os ***atributos*** da nossa classe são as variáveis, como *Balance* e *Holder*. Os ***modificadores de acesso*** nos meus atributos é o que define quem pode acessar e como serão modificados os nossos atributos.

O ***get*** permite que a variável que é pública possa ser ***lida*** de fora da classe. Já o `private set;` Restringe a modificação desse atributo somente para dentro da classe, então ele não pode ser modificado de fora da classe. Ou seja, esse valor só pode ser modificado no construtor e em métodos internos da classe. 
Essa combinação é útil quando eu desejo que um atributo seja **somente leitura** para o código externo, mas permita alterações controladas internamente.