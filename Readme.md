# Web app: HAMSTERWARS
### Projekt webbutveckling, FEU19

**Ert projekt är att bygga en fullstack lösning för kommande virala sensationen, webplatsen HAMSTERWARS.**
Webbplatsen är en spinoff på [Kittenwar](http://www.kittenwar.com), en hemsida där matcher mellan två bilder slumpas fram och besökarna röstar på den de finner gulligast. Poäng ska räknas, listor ska sammanställas.


### Kursmål
I den här kursen ska du lära dig mer om hur man arbetar **agilt i team** och hur man bygger en större app, med både **backend webbserver + databas** och **frontend-ramverk**. Du ska använda allt vi har gått igenom i utbildningen hittills.

Projektet ska utföras av grupper på 3-5 personer.

### Teknik
+ Backend: REST API med Node.js, Express och MongoDB.
+ Frontend: web app med valfritt ramverk (React, Vue eller Angular)
+ Metodik: scrum, agile

Bilder och JSON data finns i repot.

### Guider
+ [Starta upp projektet](start-guide.md)
+ [Publicera online (deploy)](deploy.md)
+ [Att arbeta agilt](agile.md)


---
## Specifikation

|Route | Vad ska visas|
|:------------------|----------------------------|
|/                  |Startsida                   |
|/battle            |Rösta på slumpade hamstrar  |
|/battle/:id1/:id2  |En specifik matchup         |
|/result/:id        |Resultatet av en match      |
|/stats             |Statistik                   |
|/upload            |Lägga till en ny tävlande   |

#### Startsida
Här ska du presentera idén med appen. Startsidan ska vara det första man ser när man laddar appen. Därifrån kan man gå till battle, statistik eller uppladdning.

#### Battle
Två hamstrar ställs mot varandra. Bara en kan vinna. Om det finns parametrar i URL ska de användas, annars ska två hamstrar slumpas av backend. Användaren röstar genom att klicka på den bild man tycker bäst om. När man röstat ska resultatet visas.

#### Resultat (matchup)
Visa resultatet av en match mellan två hamstrar. Man vill se så mycket information som möjligt om vinnaren - åtminstone bild och namn.

#### Statistik
Visa statistik om matcher och tävlande hamstrar.

+ totala antalet matcher
+ top 5 hamstrar som vunnit mest
+ top 5 hamstrar som förlorat mest

#### Ladda upp ny hamster
Här ska det finnas ett formulär för att fylla i all information om en tävlande hamster som databasen behöver. All information ska valideras så att den är informativ och användarvänlig. För G räcker det att hamsterbilden är en URL. För VG ska man kunna ladda upp en ny bildfil till assets-mappen.



---
---
## Level ups
Förslag på förbättringar (i ungefärlig svårighetsordning) som ni kan göra för att lära er mer, eller demonstrera att projektet är värt ett högre betyg.

###### Wowfaktor
Använd CSS-animeringar eller ljudeffekter för att förhöja användarupplevelsen!

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
1 Projektet ska lämnas in med ett meddelande från en av gruppens medlemmar, via slack:

> Inlämning för grupp Xyz <br>
> Medlemmar i gruppen: Anna, Bo, Cecilia <br>
> GitHub-länk: ... <br>
> URL till publicerad app: ... <br>
> Länk till Trello: ... <br>
> Länk till Figma-skisser: ... <br>
> Vi har implementerat följande levelups: ...

2 Varje gruppmedlem ska skicka in sin individuella projektrapport som ett delat dokument via slack.

#### Individuell projektrapport
Skriv kort om:
+ hur du har jobbat
+ hur arbetet har fungerat
+ vad har du jobbat mest med

Skriv särskilt om parprogrammering och annat som kan göra att din sanna arbetsinsats inte syns på GitHub eller i Trello.


---
## Bedömning
För *godkänt* krävs
+ du ska lämna in en individuell projektrapport
+ gruppen ska bygga webbappen "Hamsterwars"
+ gruppen ska arbeta agilt
+ appen uppfyller kraven, på ett grundläggande sätt
+ appen använder en ME*N stack (MongoDB, Express, Node.js, frontend-ramverk)
+ appen ska publiceras online

För *väl godkänt* krävs dessutom
+ appen uppfyller kraven väl
+ genomtänkt gränssnitt och bra användarupplevelse (UI/UX)
+ appens UI/UX ska anpassas efter feedback från användare
