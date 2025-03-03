# Kryptografie
- Obor zabývající se šifrováním
- V kontextu kybernetické bezpečnosti využívána k ochraně dat - zašifrování dle vybraného algoritmu

## Šifrování vs kódovani
- Oboje transformace dat do jiné podoby
- Ačkoliv se to tak může zdát, opravdu se nejedná o stejnou věc

## Šifrování
- Pro přeměnu dat využíván klíč
- Klíč dle druhu algoritmu buď symetrický nebo asymetrický
	- **Symetrický**
    	- Jeden klíč pro šifrování a dešifrování
    	- Příklady symetrických algoritmů: AES, Caesarova šifra, Vigenèrova šifra
	- **Asymetrický**
    	- 2 klíče - veřejný (sloužící k zašifrování) a soukromý (sloužící k dešifrování)
    	- Příklady asymetrických algoritmů: RSA, Lizard, ECC

## Kódování
- Reprezentace dat dle předem stanoveného kódu
- Využívá se pro obfuskaci, jejíž cílem je znečitelnit kód pro člověka
- Při kódování není zadáván žádný klíč -> velmi jednoduché zjistit původní obsah
- Text "SSPS" zakódovaný pomocí Base64:

	```
	U1NQUw==
	```

- Nástroje pro kódování a dekódování: 
    - https://gchq.github.io/CyberChef/
    - https://www.dcode.fr/en


## Hashovací funkce
- Jednosměrná matematická funkce
- Hash
  - Výsledek hashovací funkce po zadání vstupních dat
  - Jedná se tzv. o “Otisk prstu” dat
  - Neměnný a unikátní (může se však stát tzv. kolize)
  - Kolize - jeden hash náleží dvěma různým vstupním datům (stává se zřídka)
- Příklady hashovacích funkcí: md5, SHA512, Blake2
- Příklady využití: integrita dat, zabezpečení hesel
- Nelze dešifrovat, ale lze ho prolomit pomocí takzvaných "rainbow tables" (dlouhý seznam slov, která se zahashují a výsledný hash je porovnán)
- Příklad hashe MD5: ```769ef95f8741c399409e69b409e7f808``` (vstupní data - slovo "SSPS" )
- Nástroje na prolomení (cracknutí) hashů: Hashcat, JohnTheRipper, https://crackstation.net/
