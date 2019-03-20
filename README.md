LF is replaced by CRLF in all files from the file folder. 

Imports are used with GOPATH so put ICA02 in go folder.

# ICA02
## Oppgave 1
Metoden `IterateOverASCIIStringLiteral(sl string)` itererer over elementene i en string gitt som parameter. Hvert element printes ut via print format string funksjonen fra 'fmt' pakken i 3 format: [ASCII-kode heksadesimalt][Dobbel-kvotet symbol for ASCII-kode][ASCII-kode binært] eller `"%X %q %b"`. 

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg1iterate.PNG)

Metoden `GenerateASCIIStringLiteral() string` genererer og returnerer en ASCII string literal gjennom en for loop fra HEX verdi 00 til 7F, eller 0 til 127. For hver verdi skrives det assosierte ASCII tegnet inn i en string gjennom `WriteString(s string)` metoden gjennom en buffer fra bytes pakken. 

Metoden `GreetingASCII() string` returnerer en string "Hello :-)". Den printer ut hvert tegn fra en byteslice av stringen formatert til tegn. 

Testen `TestGreetingASCII(t *testing.T)` itererer over alle tegn i en string returnert fra `GreetingASCII() string` metoden, og tester at verdien til hvert tegn ligger under maksgrensen for verdier i ASCII tabellen. 

## Oppgave 2
Metoden `IterateOverASCIIStringLiteral(sl string)` itererer over elementene i en string gitt som parameter. Hvert element printes ut via print format string funksjonen fra 'fmt' pakken i 3 format: [ASCII-kode heksadesimalt][Dobbel-kvotet symbol for ASCII-kode][ASCII-kode binært] eller `"%X %q %b"`. 

Metoden `GenerateExtendedASCIIStringLiteral() string` genererer og returnerer en ASCII string literal gjennom en for loop fra HEX verdi 80 til FF, eller 128 til 255. For hver verdi skrives det assosierte ASCII tegnet inn i en string gjennom `WriteString(s string)` metoden gjennom en buffer fra bytes pakken. 

Metoden `GreetingASCII() string` returnerer en string "Salut, ça va °-) Ça coute ​ €50​". Den printer ut hvert tegn fra en byteslice av stringen formatert til tegn. 

Testen `TestGreetingExtendedASCII(t *testing.T)` itererer over alle tegn i en string returnert fra `GreetingASCII() string` metoden, og tester at verdien til hvert tegn ligger over maksgrensen for normale verdier i ASCII tabellen og under maksgrensen for verdier i den utvidede ASCII tabellen. Testen er ikke helt fullført, da den kun sjekker mot det standard tegnsettet. Det kan legges til sjekking opp mot utvidet ASCII tegnsett for andre språk.

## Oppgave 3

## Oppgave 4
Metoden `Translate(expression string, language string)` oversetter en string ("nord og sør") til enten islandsk eller japansk basert på 


## Oppgave 5