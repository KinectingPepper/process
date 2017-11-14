Process
======================================

### Protocol

Er wordt altijd volgens het protocol gefilmd. Hieruit komen dus 3 exercises, welke de standaard 3 armbewegingen zijn.
Men kan ervan uitgaan dat de oefeningen/exercises deze betekennissen hebben:
1. Abdunctie(handen langs het lichaam, zijwaarts omhoog bewegen en zo hoog mogelijk proberen te komen. hierbij wordt de afwijking in de Z as bekeken)
2. voorwaartse abdunctie(handen langs het lichaam, voorlangs omhoog bewegen en zo hoog mogelijk proberen te komen. hierbij kan de afwijking in de X as worden bekeken)
3. flexion(ellebogen in de zij gedrukt houden en vuisten vooruit horizontaal opsteken, vervolgens met de vuisten zijwaarts bewegen en zo ver mogelijk naar achter proberen te komen. Hierbij kan de maximale rotatie worden bekeken.)



### Data opschonen

Bij het opschonen van de data gaan we ervan uit dat een persoon altijd 3 oefeningen heeft, als dit niet het geval is klopt de opname niet.
Mocht de opname niet kloppen dan wordt deze handmatig gescheiden zodat hier wel 3 opnames uitkomen.


### Roteren

Bij het roteren van de data zal als input een dataframe en een oefening worden meegegeven en als output komt hier een dataframe uit met geroteerde gegevens.(combined.csv opslaan als back-up)


### Herkennen

Bij het herkennen van de data zal als input een dataframe worden meegegeven en als output komt hier een dataframe uit met de kolom "eNum" ingevuld. Hierbij wordt een kolom toegevoegd aan het dataframe die beschrijft of de oefening is uitgevoerd met beide handen('lr'), of alleen een linker-('l') of rechterhand('r')


### Snijden

Bij het snijden van de opdrachten zal als input een dataframe(gefilterd met 1 persoon en 1 oefening) worden meegegeven en op basis van de waarden uit de nieuwe kolom(van het herkennen) komt hier als output een dataframe uit die de 'nutteloze' data weg heeft gefilterd.
Deze bijgesneden oefeningen zullen dan als een apart bestand worden opgeslagen zodat dit proces niet voor elke grafiek opnieuw moet worden uitgevoerd.


### Herbruikbaarheid
Uiteindelijk hebben we dus een proces waarbij de meest uitgevoerde acties eenvoudig te herbruiken zijn:
* Het toevoegen van een nieuw persoon(met 3 oefeningen) aan het CSV bestand.
* Het roteren van nieuwe data.
* Het bijsnijden van de nieuwe data per oefening.
* Het herkennen van de oefeningen.
* Het berekenen van hoeken voor een bepaalde input.


### Proces nieuw persoon:
1. Oefeningen worden als 3 aparte csv bestanden opgeslagen, is dit niet het geval dan moeten deze gesplitst worden.
2. Toevoegen aan back-up bestand 
3. Roteren
4. Snijden
5. Toevoegen aan bestaande dataset





### Hoeken berekenen
(Eventueel voor later)

Het berekenen van hoeken zal vaker nodig zijn, hier wordt dus een aparte methode voor aangemaakt. Deze methode heeft als input een dataframe(gefilterd voor 1 persoon & met alleen de gewenste oefening en alleen de gewenste zijde). Hieruit komt vervolgens een lijst met de berekende hoeken voor die persoon met een bepaalde exercise en een bepaalde zijde.
