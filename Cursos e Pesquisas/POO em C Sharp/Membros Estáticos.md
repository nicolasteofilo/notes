Um membro estático é um componente de um classe que pertence sempre a própria classe e não a suas instâncias (objetos que são criados). Isso significa que eu posso acessar esses membros sem nem ao menos instanciar a classe, sem a necessidade da criação de um objeto.

Eles são definidos usando a palavra-chave **`static`** e compartilham o mesmo estado entre todas as instâncias da classe (ou nenhum estado, no caso de métodos).

- Não é necessário instanciar a classe para acessar um membro estático
- O membro estático é compartilhado entre todas as instâncias da classe, isso se houver instâncias
- Um membro estático só pode acessar outros membros estáticos da classe
- São úteis para **funcionalidade globais**, **configurações** ou **contadores**

Exemplo:
```C#
class Math  
{  
    // Campo estático  
    public static double Pi = 3.14159;  
  
    // Método estático  
    public static double CalcularAreaDoCirculo(double raio)  
    {  
        return Pi * raio * raio;  
    }  
}
```