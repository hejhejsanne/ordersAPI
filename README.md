# ordersAPI

#1

post /orders
- [ ] ingen validering alls
- [ ]  tar emot okänd fält för icke existerande objekt
- [ ]   kastar inga felmeddelanden
- [ ]    totalamount fungerar inte riktigt, tar inte med quantity men räknar ihop olika items

#2
 - [ ] ger inte korrekt information vid felmeddelande, tex vid inmatning av en String
 - [ ] säger order not found när man skickar in null, bör säga ange ett id eller id cannot be null
 - [ ] loggar inte fel för felsökning


#3
- [ ] Ingen validering alls - status borde vara en enum, validering borde ske på servern (modeller för detta) Price och totalamount hänger inte ihop 
- [ ] Saknar funtionallitet för att spara till fil, men ger ok - lägg till write to file
- [ ] Finns ingen kontroll av ordningen utav sparande - Vi borde se till att låsa processen för att spara och skapa en kö för efterföljande uppdateringar

#4
- [ ] hittar order men uppdaterar inte status eller updatedAt
- [ ] loggar inte listenerCount
- [ ] uppdaterar inte orders.json
- [ ] minnesanvändning går upp mycket vid många requests
- [ ] max eventListeners är 10, kanske lite lågt?

#5
- [ ] man kan inte köra flera samtidigt
- [ ] calculate fel, är 10000 istället fär längd
- [ ] lägg till   writeOrdersToFile(orders) på slutet för att spara till orders.json

#7
- [ ] findIndex används istället för find
- [ ] ändringen man gör loggas i funktionen men sparas inte i order objektet i "orders"

#8
- [ ] funktionen loopar igenom orders som redan har state processed och sätter dom till processed, den borde bara loopa igenom och sätta process på de funktionerna som inte har state "processed"
