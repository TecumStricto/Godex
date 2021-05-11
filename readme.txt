Za UTF ispis:

File je nužno spremiti kao UTF-8
Kod ispisa isključivo koristiti BinaryReader tj. SendFileToPrinter
Naše znakove samo ukucati

a) za prozvati interni font, nužno je na kraju imati 0E prije text, jel to znači da ide UTF text
b) za pozvati Windows TTF, nužno je kroz GoLable, izabrati opciju Font Type/True Type Font/ Downloada TTF te izabrati npr. TB kao "ime fonta"
iz coda se poziva onda kao: ATB,60,118,68,68,0,0E,B,0,TB šđČĆŽ , ako je font definiran kao TB

U notepadu se naši znakovi vide ispravno.


-----------
Za CP852 ispis:
https://en.wikipedia.org/wiki/Code_page_852
File je nužno spremiti kao ANSI.

a) nužno dodati ^XSET,CODEPAGE,1 za 852 cp
b) interni font, ne treba na kraju imati E, sukladno standardu zamjeniti HR znakove sa "črčkama"
AF,68,56,1,1,0,0,ćç†Ź¬ź¦§ĐŃ
U notepadu se naši znakovi vide kao "črčke".


-----------
Za CP1250
http://www.orbus.be/bosanski_jezik/centraleuropeancode.htm
Za 1250 ispis:
File je nužno spremiti kao ANSI.

a) nužno dodati ^XSET,CODEPAGE,15 za 1250 cp
b) interni font, ne treba na kraju imati E, naše znakove samo ukucati
AF,68,56,1,1,0,0,ššŠŠđđĐĐččČČććĆĆžžŽŽ
U notepadu se naši znakovi vide ispravno.

RawPrint.exe šalje file na printer koji je defniran kao običan Generic/Text Only - Ne treba driver !
