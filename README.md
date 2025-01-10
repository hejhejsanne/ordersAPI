# ordersAPI

#1

post /orders
- [x] ingen validering alls
- [x]  tar emot okänd fält för icke existerande objekt
- [x]   kastar inga felmeddelanden
- [x]    totalamount fungerar inte riktigt, tar inte med quantity men räknar ihop olika items

#2
 - [ ] ger inte korrekt information vid felmeddelande, tex vid inmatning av en String
 - [ ] säger order not found när man skickar in null, bör säga ange ett id eller id cannot be null
 - [ ] loggar inte fel för felsökning

#4

- [ ] hittar order men uppdaterar inte status eller updatedAt
- [ ] loggar inte listenerCount
- [ ] uppdaterar inte orders.json
- [ ] minnesanvändning går upp mycket vid många requests
- [ ] max eventListeners är 10, kanske lite lågt?
