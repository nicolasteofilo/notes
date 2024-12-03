Os membros constantes são atributos da nossa classe, ou seja, variáveis, que uma vez que foram inicializados, não podem ser alterados novamente. Eles são como ***"constantes"*** dentro de uma classe.

Vantagens:
- Impossibilidade de alteração acidental
- Melhora na legibilidade do código escrito: Pois identifica facilmente valores que não mudam e não podem ser mudados

Exemplo:

```C#
namespace OPP;  
  
public class CartItem  
{  
    public static int CartItemsCount; // shared with all instances  
    
    private const int DEFAULT_QUANTITY = 1;  
    private const decimal DEFAULT_PRICE = decimal.Zero;  
      
    private string _name;  
    public string Name  
    {  
        get => _name;  
        set  
        {  
            if(string.IsNullOrEmpty(value)) throw new ArgumentNullException(nameof(Name));  
            _name = value;  
        }  
    }
    public int Quantity { get; private set; }  
    
    private decimal _price;  
    public decimal Price  
    {  
        get => _price;  
        set  
        {  
            if(value < 0) throw new ArgumentException("Price cannot be negative");  
            _price = value;  
        }  
    }
    
    public CartItem(string name, decimal price = DEFAULT_PRICE, int quantity = DEFAULT_QUANTITY)  
    {  
        Name = name;  
        Quantity = quantity;  
        Price = price;  
        CartItemsCount++;  
    }  
}
```
No exemplo acima os membros constantes foram usados para definir ***configurações*** de quantidade padrões e preços padrões, que são valores que não devem mudar constantemente, e no caso são acessíveis somente dentro da classe, pois estão com o modificador de acesso *private*.