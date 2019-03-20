LF is replaced by CRLF in all files from the file folder. 

Imports are used with GOPATH so put ICA02 in go folder.

# ICA02
## Oppgave 1
Metoden `IterateOverASCIIStringLiteral(sl string)` itererer over elementene i en string gitt som parameter. Hvert element printes ut via print format string funksjonen fra 'fmt' pakken i 3 format: [ASCII-kode heksadesimalt][Dobbel-kvotet symbol for ASCII-kode][ASCII-kode binært] eller `"%X %q %b"`. 

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg1iterate.PNG)

Metoden `GenerateASCIIStringLiteral() string` genererer og returnerer en ASCII string literal gjennom en for loop fra HEX verdi 00 til 7F, eller 0 til 127. For hver verdi skrives det assosierte ASCII tegnet inn i en string gjennom `WriteString(s string)` metoden gjennom en buffer fra bytes pakken. 

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg1generate.PNG)

Metoden `GreetingASCII() string` returnerer en string "Hello :-)". Den printer ut hvert tegn fra en byteslice av stringen formatert til tegn. 

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg1greeting.PNG)

Testen `TestGreetingASCII(t *testing.T)` itererer over alle tegn i en string returnert fra `GreetingASCII() string` metoden, og tester at verdien til hvert tegn ligger under maksgrensen for verdier i ASCII tabellen. 

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg1test.PNG)

### Main og Terminal

`Main()` metoden kjører `IterateOverASCIIStringLiteral(ascii.ASCII)` og `GenerateASCIIStringLiteral()`.

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg1main.PNG)

![Output](https://github.com/emfkf/temptest/blob/master/pictures/opg1terminal1.PNG)
![Output](https://github.com/emfkf/temptest/blob/master/pictures/opg1terminal2.PNG)
![Output](https://github.com/emfkf/temptest/blob/master/pictures/opg1terminal3.PNG)

## Oppgave 2A
Metoden `IterateOverASCIIStringLiteral(sl string)` itererer over elementene i en string gitt som parameter. Hvert element printes ut via print format string funksjonen fra 'fmt' pakken i 3 format: [ASCII-kode heksadesimalt][Dobbel-kvotet symbol for ASCII-kode][ASCII-kode binært] eller `"%X %q %b"`. 

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg2iterate.PNG)

Metoden `GenerateExtendedASCIIStringLiteral() string` genererer og returnerer en ASCII string literal gjennom en for loop fra HEX verdi 80 til FF, eller 128 til 255. For hver verdi skrives det assosierte ASCII tegnet inn i en string gjennom `WriteString(s string)` metoden gjennom en buffer fra bytes pakken. 

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg2generate.PNG)

Metoden `GreetingASCII() string` returnerer en string "Salut, ça va °-) Ça coute ​ €50​". Den printer ut hvert tegn fra en byteslice av stringen formatert til tegn. 

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg2greeting.PNG)

### Main og Terminal
`Main()` metoden kjører `IterateOverASCIIStringLiteral(ascii.ASCII)` og `GenerateASCIIStringLiteral()`.

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg2main.PNG)

![Output](https://github.com/emfkf/temptest/blob/master/pictures/opg2terminal1.PNG)
![Output](https://github.com/emfkf/temptest/blob/master/pictures/opg2terminal2.PNG)
![Output](https://github.com/emfkf/temptest/blob/master/pictures/opg2terminal3.png)

## OPPGAVE 2B
Testen `TestGreetingExtendedASCII(t *testing.T)` itererer over alle tegn i en string returnert fra `GreetingASCII() string` metoden, og tester at verdien til hvert tegn ligger over maksgrensen for normale verdier i ASCII tabellen og under maksgrensen for verdier i den utvidede ASCII tabellen. Testen er ikke helt fullført, da den kun sjekker mot det standard tegnsettet. Det kan legges til sjekking opp mot utvidet ASCII tegnsett for andre språk.

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg2test.PNG)

## Oppgave 3
![Output](https://github.com/emfkf/temptest/blob/master/pictures/opg3treasure.PNG)

## 3B

## Oppgave 3c
Metoden `PrintTreasureUTF8(treasureString string)` tar en string literal som parameter. Ved bruk av `strings.Replace()` metoden erstatter vi alle tilfeller av UTF-16 enkoding med UTF-8 enkoding. Stringen dekodes ved hjelp av hex pakkens `DecodeString(str string)` metode, og printes deretter ut.

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg3printtreasureutf8.PNG)

### Output




## Oppgave 4
Metoden `Translate(expression string, language string)` oversetter en string ("nord og sør") til enten islandsk eller japansk basert på 

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg4translate.PNG)

## Oppgave 5

Metoden `AllocateVar(b int) []byte` returnerer en slice av lengden gitt som parameter `b`. 

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg5allocatevar.PNG)

Metoden `AllocateMake(b int) []byte` returnerer en slice av lengden gitt som parameter `b`. 

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg5allocatemake.PNG)

Metoden `Reslice(slc []byte, lidx int, uidx int) []byte` initierer en ny slice via `AllocateMake(b int)` metoden, setter denne slicen til en slice med `[lidx:uidx]` og returnerer slicen. 

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg5reslice.PNG)

Metoden `CopySlice(slice []byte) []byte` returnerer en kopi av slicen gitt som parameter `slice`.

![Metoden](https://github.com/emfkf/temptest/blob/master/pictures/opg5copyslice.PNG)