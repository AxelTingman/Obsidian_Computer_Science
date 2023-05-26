#Kurs/Datorsystem #Kurs/Datorsystem/Föreläsning/4 
***

# Operationer
### Aritmetic
- add
- addi
- sub
- subbi
- mul
- muli
- div
- divi

### Logic
- and
- andi
- or
- ori
- xor
- xori
- nor
- (...)

### Data
- mov
- movi
	- Används för att initiera variabler: `movi r1, 0` är detsamma som `int i = 0;`
- movia
- ldb
- ldw
- stb
- stw
- (...)

### Flow control
- br
- beg
- bit
- jmp
- jmpi
- call
- ret
- (...)

# Kontrollinstruktioner
### Branch
- Fortsätter exekveringen på en angiven minnesaddress
- Kan kombineras med villkor

### Jump
- Flytta exekveringen ett angivet antal rader
- Kombineras inte med villkor

### Skip
- Hoppar över till nästkommande instruktion
- Kombineras med villkor
- Finns **inte** på Altera Nios II.