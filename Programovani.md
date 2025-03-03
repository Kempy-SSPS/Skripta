# Programování
## Algoritmizace
- sadu pokynů, kterými se program řídí
- Bez schopnosti tvorby algoritmů nemůžeme napsat kvalitní kód.
- Jednoduchý algoritmus napsaný v pseudokódu:
    ```python
    Vstup: heslo
    Pokud heslo == 1234:
        Vypiš "Správné heslo"
    Jinak:
        Vypiš "Špatné heslo"
    ```

## Datové typy
- každý programovací jazyk má v sobě zabudované základní datové typy
- nejzákladnější datové typy:
	
    ```
    int - celá čísla
	
    double - desetinná čísla
	
    string - textové řetězce
	
    char - jeden znak
	
    bool - true/false
    ```
## Syntaxe
- **Syntaxe** - sada pravidel, při jejímž porušení nebude program fungovat (např. v C# vše musí končit ";")
- Jednoduchý kód pro vypsání textu do konzole 
  - v jazyce Python
  
    ```python
    print("Hello, World!") 
    ```

  - v jazyce C
  
    ```c
    #include <stdio.h>

    int main()
    {
        printf("Hello, World!");
        return 0;
    }
    ```

## Komentáře

- Část kódu, která se nevykonává, ale slouží k vysvětlení kódu, jeho zpřehlednění, či k zapsání poznámek (např. TODO)
- Komentáře v Pythonu

    ```python
    # Toto je   komentář

    """
    Toto je komentář
    na více řádků
    """
    ```

- Komentáře v C

    ```c 
    // Toto je komentář

    /*
    Toto je komentář
    na více řádků
    */
    ```

- Jednoduchý program, který bude zdravit uživatele
  - v jazyce Python
  
    ```python
    name = input("Zadej své jméno: ")
    print("Ahoj " + name)
    ```
    
  - v jazyce C

    ```c
    #include <stdio.h>

    int main()
    {
        char name[50];
        printf("Zadej své jméno: ");
        scanf("%s", name);
        printf("Ahoj %s", name);
        return 0;
    }
    ```

## Podmínky (if/else statements)
- Umožňují vykonat část kódu, pokud je splněna určitá podmínka
- Příklad if/else statementu
  - v jazyce Python

    ```python
    # if, elif, else
    age = 18
    if age < 18:
        print("Jsi dítě")
    elif age >= 65:
        print("Jsi důchodce")
    else:
        print("Jsi dospělý")
    ```

  - v jazyce C

    ```c
    #include <stdio.h>

    int main()
    {
        int age = 18;
        if (age < 18)
        {
            printf("Jsi dítě");
        }
        else if (age >= 65)
        {
            printf("Jsi důchodce");
        }
        else
        {
            printf("Jsi dospělý");
        }
        return 0;
    }
    ```

## Cykly (for/while loops)
### For loop
- Umožnuje opakovat stejnou část kodu po stanovenou dobu
- Příklad for loopu
  - v jazyce Python

    ```python
    for i in range(10):
        print(i)
    ```

  - v jazyce C

    ```c
    #include <stdio.h>

    int main()
    {
        for (int i = 0; i < 10; i++)
        {
            printf("%d\n", i);
        }
        return 0;
    }
    ```

### While loop
- Opakuje část kódu, dokud je splněna určitá podmínka
- Příklad while loopu
  - v jazyce Python

    ```python
    i = 0
    while i < 10:
        print(i)
        i += 1
    ```

    - v jazyce C

    ```c
    #include <stdio.h>

    int main()
    {
        int i = 0;
        while (i < 10)
        {
            printf("%d\n", i);
            i++;
        }
        return 0;
    }
    ```

## Pole (arrays)
- Umožňuje ukládat více hodnot do jedné proměnné
- Příklad pole
  - v jazyce Python

    ```python
    pole = [1, 2, 3, 4, 5]
    print(pole[0]) #Vypíše první prvek pole
    print(pole[3]) #Vypíše čtvrtý prvek pole
    print(len(pole)) #Vypíše délku pole
    ```

    - v jazyce C

    ```c
    #include <stdio.h>

    int main()
    {
        int pole[] = {1, 2, 3, 4, 5};
        printf("%d\n", pole[0]); //Vypíše první prvek pole
        printf("%d\n", pole[3]); //Vypíše čtvrtý prvek pole
        printf("%d\n", sizeof(pole) / sizeof(pole[0])); //Vypíše délku pole
        return 0;
    }
    ```

## Metody/funkce
- Kus kódu, který lze využívat opakovaně (stačí ji zavolat a ona se vykoná, zavolat ji lze opakovaně)
- Program pozdravení s využitím metody/funkce
    - v jazyce Python

    ```python
    def pozdrav(name):
        print("Ahoj " + name)
    
    print("Zadej své jméno: ")
    name = input()
    pozdrav(name)
    ```

    - v jazyce C

    ```c
    #include <stdio.h>

    void pozdrav(char name[])
    {
        printf("Hi %s\n", name);
    }

    int main()
    {
        char name[50];
        printf("Zadej své jméno: ");
        scanf("%s", name);
        pozdrav(name);
        return 0;
    }
    ```

## Jednoduchá kalkulačka
- V jazyce Python

```python
while True: #Program se bude stále opakovat- Jednoduchá kalkulačka za použití while loopu a if/else statementů
    print("Kalkulačka V1")
    inputString = input("Chcete sčítat (+) nebo odčítat (-)?") #Načte uživatelský vstup

    if inputString == "+": #Pokud je uživatelný vstup roven "+", čísla se budou sčítat
        numberOne = input("Zadejte první číslo: ")
        numberTwo = input("Zadejte druhé číslo: ")
        result = int(numberOne) + int(numberTwo) #Sečte proměnné a výsledek zapíše do proměnné result
        print("Výsledek součtu čísel je: " + str(result)) #Vypíše výsledek a vrátí se na začátek

    elif inputString == "-": #Pokud je uživatelný vstup roven "-", čísla se budou odčítat
        numberOne = input("Zadejte první číslo: ")
        numberTwo = input("Zadejte druhé číslo: ")
        result = int(numberOne) - int(numberTwo) #Odečte proměnné a výsledek zapíše do proměnné result
        print("Výsledek rozdílu čísel je: " + str(result)) #Vypíše výsledek a vrátí se na začátek

    else:
        print("Neplatný vstup") #V případe, že by uživatel zadal něco jiného než "+" nebo "-", bude jeho vstup vyhodnocen jako neplatný a vrátí se na začátek

```

- V jazyce C

```c
#include <stdio.h>

int main()
{
    while (1) //Program se bude stále opakovat- Jednoduchá kalkulačka za použití while loopu a if/else statementů
    {
        char operation;
        float numberOne;
        float numberTwo;

        printf("Zadejte operaci (+, -, *, /): ");
        scanf(" %c", &operation);
        printf("Zadejte první číslo: ");
        scanf("%f", &numberOne);
        printf("Zadejte druhé číslo: ");
        scanf("%f", &numberTwo);

        float result;

        if (operation == '+') //Pokud je uživatelný vstup roven "+", čísla se budou sčítat
        {
            result = numberOne + numberTwo; //Sečte proměnné a výsledek zapíše do proměnné result
            printf("Výsledek součtu čísel je: %f\n", result);
        }
        else if (operation == '-') //Pokud je uživatelný vstup roven "-", čísla se budou odčítat
        {
            result = numberOne - numberTwo; //Odečte proměnné a výsledek zapíše do proměnné result
            printf("Výsledek rozdílu čísel je: %f\n", result); //Vypíše výsledek a vrátí se na začátek
        }
        else if (operation == '*')
        {
            result = numberOne * numberTwo; //Vynásobí proměnné a výsledek zapíše do proměnné result
            printf("Výsledek rozdílu čísel je: %f\n", result); //Vypíše výsledek a vrátí se na začátek
        }
        else if (operation == '/')
        {
            result = numberOne / numberTwo; //Vydělí proměnné a výsledek zapíše do proměnné result
            printf("Výsledek rozdílu čísel je: %f\n", result); //Vypíše výsledek a vrátí se na začátek
        }
        else
        {
            printf("Neplatný vstup\n"); //V případe, že by uživatel zadal něco jiného než "+" nebo "-", bude jeho vstup vyhodnocen jako neplatný a vrátí se na začátek
        }
    }
}
```
