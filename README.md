# ordersAPI

#1

post /orders
- [x] ingen validering alls
- [x]  tar emot okänd fält för icke existerande objekt
- [x]   kastar inga felmeddelanden
- [x]    totalamount fungerar inte riktigt, tar inte med quantity men räknar ihop olika items

#2
 - [x] ger inte korrekt information vid felmeddelande, tex vid inmatning av en String
 - [x]  säger order not found när man skickar in null, bör säga ange ett id eller id cannot be null
 - [x] loggar inte fel för felsökning


#3
- [x] Ingen validering alls - status borde vara en enum, validering borde ske på servern (modeller för detta) Price och totalamount hänger inte ihop 
- [x] Saknar funtionallitet för att spara till fil, men ger ok - lägg till write to file
- [x] Finns ingen kontroll av ordningen utav sparande - Vi borde se till att låsa processen för att spara och skapa en kö för efterföljande uppdateringar

#4
- [ ] loggar inte listenerCount
- [x] uppdaterar inte orders.json
- [x] minnesanvändning går upp mycket vid många requests
- [ ] max eventListeners är 10, kanske lite lågt?

#5
- [x] man kan inte köra flera samtidigt
- [x] calculate fel, är 10000 istället fär längd
- [ ] lägg till   writeOrdersToFile(orders) på slutet för att spara till orders.json

#7
- [ ] findIndex används istället för find
- [x] ändringen man gör loggas i funktionen men sparas inte i order objektet i "orders"

#8
- [x] funktionen loopar igenom orders som redan har processed true och sätter dom till processed true, den borde bara loopa igenom och sätta processed true på de funktionerna som inte redan har processed true
- [x] ingen rollback 






** 17 Poäng **

