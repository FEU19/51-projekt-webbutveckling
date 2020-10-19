# Web app: HAMSTERWARS
### Projekt webbutveckling, FEU19
#### Kompletterande uppgift

Du som av någon anledning inte har blivit godkänd på projektet ska göra en avskalad version av projektet och svara på frågor om hur man arbetar agilt. Uppgiften ska göras individuellt.


### Kursmål
I den här kursen ska du lära dig mer om hur man arbetar **agilt i team** och hur man bygger en större app, med både **backend webbserver + databas** och **frontend-ramverk**. Du ska använda allt vi har gått igenom i utbildningen hittills.


### Teknik
+ Backend: API med Node.js och Express.
+ Frontend: web app med valfritt ramverk (React, Vue eller Angular)

Bilder och JSON data finns i repot.

### Guider
Observera att guiderna är gjorda för projektgrupperna, du behöver anpassa dem efter ditt mindre projekt.
+ [Starta upp projektet](start-guide.md)
+ [Publicera online (deploy)](deploy.md)
+ [Att arbeta agilt](agile.md)


---
## Specifikation

|Route              | Vad ska visas |
|:------------------|-------------------------|
|/                  |Battle                   |

#### Battle
Två hamstrar ställs mot varandra. Bara en kan vinna. Två hamstrar ska slumpas av backend. Användaren röstar genom att klicka på den bild man tycker bäst om.

När man röstat ska resultatet visas i samma komponent. Man ska kunna se vad båda hamstrarna heter och hur många vinster och förluster de har var.


#### API

|Method |Route                   | Vad ska göras                   |
|:------|:-----------------------|---------------------------------|
|GET    |`/`                      |Serva den byggda index.html     |
|GET    |`/assets/hamster-1.jpg`  |Serva bildfiler med express.static |
|GET    |`/hamster`               |Skicka en slumpad hamster (JSON) |
|POST   |`/battle/:winner/:loser` |Spara vinst och förlust         |

Root URL, `/` ska serva index.html som du byggt med frontend-ramverket. (`npm run build`)

Alla hamsterbilder ska servas som en statisk mapp, dvs med funktionen express.static. Man skriver routes som börjar med `/assets/` för att komma åt dem. I frontend-appen kan det till exempel stå:
```html
<img src="/assets/hamster-7.jpg" />
```

Skicka AJAX GET request till `/hamster`, så ska backend returnera ett slumpat hamster-objekt.

Skicka AJAX POST request till `/battle` med id för två hamstrar som parametrar, för att spara resultatet av en match. (Alltså inte querystring.) Första parametern ska vara vinnaren. Hamster-objektets egenskap "wins" ska räknas upp med ett. Andra parametern ska vara förloraren, vars "defeats" räknas upp med ett.


---
---
## Level ups
Förslag på förbättringar (i ungefärlig svårighetsordning) som du kan göra för att demonstrera att projektet är värt ett högre betyg.

###### Wowfaktor
Använd CSS-animeringar eller ljudeffekter för att förhöja användarupplevelsen!

###### Databas
Använd MongoDB för att spara information om hamstrarna, i stället för att spara den som en variabel på servern.

###### Fler sidor
+ Startsida
+ Statistik - de 5 hamstrar som vunnit flest matcher
+ Ladda upp ny hamster

###### Mer statistik
Visa mer information på statistik-sidan. Till exempel vilka hamstrar som deltagit i minst antal strider och de senaste striderna.

###### Hamstergalleri
Bläddra igenom alla hamstrar som finns i databasen. *Se upp med dataanvändningen! Många bildöverföringar kan göra så att ni går över gratisgränsen för molntjänster.*

###### Rättvisare slumpning
Välj bland de hamstrar som haft minst antal matcher, när appen ska slumpa fram hamstrar.

###### Ladda upp bildfil
Formuläret för att lägga till ny hamster ska kunna ladda upp riktiga bilder.

###### Flera hamstrar i varje match
Ny form av strid, med tre eller fyra hamstrar. Användaren kan få fler än en röst.

###### Gladiatorspel
Nya strider, som äger rum i omgångar. En användare skapar en tävling med fyra (utvalda eller slumpade) hamstrar. Andra användare kan gå med i tävlingen. Alla får två röster var. När man lagt sina två röster får man se resultatet hittills.

###### Merch
Mer eller mindre funktionell webbshop för att beställa t-shirt med sidans logga m.m..

---

---
## Inlämning
1 Projektet ska lämnas in med ett textdokument, eller ett delat dokument. Skicka dokumentet eller länk till det till läraren via slack.

Innehåll:
> [Rubrik] Inlämning för [ditt namn] <br>
> GitHub-länk: ... <br>
> URL till publicerad app: ... <br>
> Jag har implementerat följande levelups: ...
>
> Här är mina svar på frågorna om hur man arbetar agilt
> 1. [Ditt svar på första frågan]
> 2. ...

2 Du ska svara på följande frågor om hur man arbetar *agilt*. Svara med egna ord.

1. Vilka frågor ska man ställa på ett *daily scrum*?
1. Varför ska man stå upp under *daily scrum*?
1. Hur lång ska en *daily scrum* vara?
1. Vad är syftet med *sprint planning*?
1. En sprint bör vara ungefär 2-4 veckor. Varför kan den inte vara längre?
1. När i sprinten kommer *sprint review* och *sprint retrospective*?
1. Om man använder Trello för att arbeta med scrum, vilka rubriker ska man då ha på sina listor?


---
## Bedömning
För *godkänt* krävs
+ du ska lämna in ett dokument enligt beskrivningen ovan
+ appen uppfyller kraven, på ett grundläggande sätt
+ appen använder teknikerna Express, Node.js, samt ett frontend-ramverk
+ appen ska publiceras online

För *väl godkänt* krävs dessutom
+ appen uppfyller kraven väl
+ genomtänkt gränssnitt och bra användarupplevelse (UI/UX)
+ du ska implementera level ups
