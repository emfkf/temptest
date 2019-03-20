LF is replaced by CRLF in all files from the file folder. 

Imports are used with GOPATH so put ICA02 in go folder.

# ICA02
## Oppgave 1
Metoden `IterateOverASCIIStringLiteral(sl string)` itererer over elementene i en string gitt som parameter. Hvert element printes ut via print format string funksjonen fra 'fmt' pakken i 3 format: [ASCII-kode heksadesimalt][Dobbel-kvotet symbol for ASCII-kode][ASCII-kode binært] eller `"%X %q %b"`. 

IterateOverASCIIStringLiteral metoden itererer over en string literal gitt som parameter ved bruk av en range iterator. Den printer ut i format %X %q %b, men %q kan erstattes med %c dersom en ikke ønsker apostroffer rundt c. 
GenerateASCIIStringLiteral metoden genererer en ASCII string literal ved hjelp av en Buffer. Fra HEX verdi 00 til 7F, eller 0 til 127, skrives det assosierte ASCII tegnet til en string, før metoden returnerer stringen. 
GreetingASCII returnerer en string «Hello :-)». I tillegg printer den ut hvert tegn fra en byteslice av stringen. 
TestGreetingASCII bruker en range iterator over stringen gitt i retur av GreetingASCII, og sjekker om verdien til tegnene ligger under maksgrensen for ASCII tegn.
## Oppgave 2

Stringen brukt i oppgaven genereres fra en funksjon GenerateExtendedASCIIStringLiteral som returnerer en string. Metoden bruker en buffer fra bytes pakken sin WriteString metode i en iterator som går fra HEX 7F til FF, eller 127 til 255.
IterateOverASCIIStringLiteral er lik som metoden med samme funksjon i forrige oppgave. 
Test for GreetingExtendedASCII er imidlertid bare halveis gjort. Vi tester om tegnene i stringen returnert fra GreetingExtendedASCII() ligger mellom verdiene for extended ASCII, men kun for standard tegnsett. Det som kan legges til er at stringen sjekkes opp mot extended ASCII karaktersett for andre språk. 
