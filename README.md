# DEV2 - Herhalingsoefening 20-21


## Opgave
Maak een webapplicatie waarmee je boeken volgens auteur kan opzoeken. Je kan de data ophalen via de volgende API call:

```http://openlibrary.org/search.json?author=AUTEUR_NAAM``` 

Een voorbeeld van een API call is 

```http://openlibrary.org/search.json?author=george%20orwell```

(je vindt de boeken terug in de `docs` property van de response)

Zorg ervoor dat een gebruiker zelf een auteur kan ingeven, wanneer hij op de knop duwt, toon je de `title`, de eerste `author`, `first_publish_year` en de book cover van de gevonden boeken. 

Al deze data vind je terug per object in de `docs` array, alleen de book cover is niet aanwezig. De book cover kan je ophalen door de volgende link te genereren: ```http://covers.openlibrary.org/b/id/COVER_I-L.jpg```, de ```cover_i``` vind je terug in de data. Een voorbeeld van een correcte cover is het volgende: 

```http://covers.openlibrary.org/b/id/8748936-L.jpg.```

Voordat je de boekenlijst toont maak je enkele aanpassingen aan de data. Je moet de boekenlijst sorteren op `first_publish_year` van laag naar hoog (gebruik hiervoor de sort functie). Zorg er ook voor dat je maximaal 10 boeken toont. Helaas hebben sommige boeken geen cover_i, deze boeken moet je eruit filteren (gebruik hiervoor de filter functie).

Wanneer de data nog aan het laden is, toon je een loading message. Wanneer de ingegeven auteur geen boeken heeft toon je de volgende error message: 
`"No books for author AUTEUR_NAAM"`

> :warning: **Deze oefening staat niet op punten; maar voor jullie inzicht alsnog een mogelijke puntenverdeling


## Criteria

#### Geimplementeerde functionaliteiten

- Toon een loading message wanneer de API call nog bezig is <i>1 punt</i>
- Toon de titel, auteur, book cover en published date van de gevonden boeken op basis van de ingegeven auteur <i>4 punten</i>
- Sorteer de boeken op first_publish_year van laag naar hoog <i>2 punten</i>
- Zorg ervoor dat boeken zonder cover_i uitgefilterd worden.<i>1 punt </i>
- Toon maximaal 10 boeken <i>1 punt</i>
- Toon de volgende message als er geen boeken gevonden zijn voor de ingegeven auteur "No books for author AUTEUR_NAAM" <i>1 punt </i>

#### Code qualiteit

Pas op, je moet voldoende code en geïmplementeerde functionaliteiten hebben om punten te halen op code qualiteit

- De code is volledig objectgeoriënteerd geschreven <i>4 punten</i>
- Er wordt geen code herhaalt. <i>2 punten</i>

Totaal: 16 punten