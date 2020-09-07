# Uppstartsguide
[Tillbaka till huvudsidan](Readme.md)

### Första projektmötet
1. Planera
2. Skisser på gränssnitt


### Terminalen
```bash
# Börja med att välja frontend-ramverk!

# Exempel för React (ersätt "gruppnamn" med er grupps namn)
npx create-react-app hamsterwars-gruppnamn

# Exempel för Vue:
npx vue create hamsterwars-gruppnamn


# Fortsätt med att installera backend
cd hamsterwars-gruppnamn/
npm install express mongodb body-parser
mkdir server/

# Skapa en mapp för bilderna
mkdir assets/
```

Kontrollera att ni har filerna [`.gitignore`](https://github.com/FEU19/45-express-mongodb/blob/master/.gitignore) och [`.editorconfig`](https://github.com/FEU19/45-express-mongodb/blob/master/.editorconfig).

Skapa branch `dev` och *feature branches* för det ni jobbar med för stunden.

### Kom ihåg att:
1. göra `commit` och `push` i din feature branch ofta
2. göra merge till `dev` när andra gruppmedlemmar behöver din kod
3. göra merge från `dev` till `master` när ni har en fungerande version i `dev`)
