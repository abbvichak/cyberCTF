# cyberCTF
Ett projekt där vi ska göra en "Capture The Flag" uppgift där någon behöver "bryta" eller "hacka" din uppgift för att lösa den och få "flaggan"

## Planering
### Uppgiften
Cookie Decrypter

### Medverkande
Victor Håkonsen

### Beskrivning
Uppgiften går ut på att man ska hitta ett lösenord för att kunna logga in på hemsidan, lösenordet finns gömt på hemsidan och man måste använda basic Web Exploration för att komma åt den.
Nyckeln i sig är encryptad med en mängd olika metoder som man behöver decoda för att få fram nyckeln. 

### Lösningsförslag
För att lösa uppgiften ska man först och främst använda sig av webbläsarens inspektör för att hitta hemsidans cookies, där får man användarnamnet (Ben Dover) och det encrypterade lösenordet, sedan ska man använda en hex decoder ([Hex (Base16) encoder & decoder, a simple online tool 🔧 (hexator.com)](https://www.hexator.com/)) för att göra den första decryptionen av lösenordet, sedan ska man använda base64 ([Base64 Decode and Encode - Online](https://www.base64decode.org/)) med först UTF16 och sedan UTF8 för att få ut en massa siffror där man behöver använda Encrypter / Decrypter ([franklin.edu](https://cs.franklin.edu/~whittakt/ITEC136/examples/encrypter.html)) för att få ASCII nummer som till sist ger lösenordet	 massvisMedFlaggor och då kan man logga in och får flaggan.

#### Svårighetsnivå
Svårighetsnivån beror på om man använder hintsen eller inte, utan hints skulle jag säga i princip 0 men med hints så kanske 0.7 eftersom man får hjälp med hur många decryptions vilka encryption methoder som används. 
