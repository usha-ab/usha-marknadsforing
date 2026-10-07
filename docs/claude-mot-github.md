# Låt din Claude skriva i repot

Din Claude kan redan **läsa** allt här — repot är offentligt, så den behöver
bara adressen. För att den ska kunna **ändra** något krävs inloggning.

## Varför kopplingen i webbläsaren inte räcker

Du kopplade ditt GitHub-konto till Claude, och det gick bra. Men
organisationen `usha-ab` kunde inte länkas:

> *usha-ab — You need to be an owner of this organization on GitHub to link it.*

Att länka en organisation kräver ägarbehörighet, och ägare i `usha-ab` kan
radera plattformens källkod och hantera bolagets fakturering. Det är mycket
mer än det här handlar om, så vi gör inte så.

**Claude Code går runt problemet.** Där loggar du in som dig själv, och din
skrivrätt på det här repot är allt som behövs. Ingen organisationskoppling.

Claude Code ingår i Claude Pro, som du redan har.

---

## Sätt upp det

Ungefär en kvart. Du behöver inte kunna programmera — du kommer att skriva på
svenska, precis som i chatten. Det här är bara installationen.

### 1. Öppna Terminal

**Mac:** tryck `cmd` + mellanslag, skriv "Terminal", enter.
**Windows:** sök efter "PowerShell" i startmenyn.

Ett fönster med textrader öppnas. Du klistrar in en rad i taget och trycker
enter. Vänta tills den blir klar innan du tar nästa.

### 2. Node

Behövs för att köra Claude Code. Ladda ner från **nodejs.org**, välj versionen
som står som LTS, och installera som vilket program som helst.

Kontrollera att det tog:

    node --version

Står det `v18` eller högre är du klar.

### 3. Claude Code

    npm install -g @anthropic-ai/claude-code

### 4. GitHub CLI

Det är det här steget som ger din Claude rätt att skriva.

**Mac:**

    brew install gh

Har du inte brew: hämta installeraren på **cli.github.com**.

**Windows:**

    winget install GitHub.cli

Logga sedan in:

    gh auth login

Välj **GitHub.com**, sedan **HTTPS**, och svara ja på att autentisera via
webbläsaren. Ett fönster öppnas där du loggar in som vanligt.

### 5. Hämta hem repot

    gh repo clone usha-ab/usha-marknadsforing
    cd usha-marknadsforing

### 6. Starta

    claude

Nu är du inne. Logga in med ditt Claude-konto när den frågar, och skriv sedan
på svenska.

---

## Vad du kan be den om

- *"Läs innehallskalender.md och lägg till att 5 snabba släpps den 14 oktober,
  jag gör klippet"*
- *"Ge Pablo en uppgift om att bestämma vem som svarar på DM, märk den admin"*
- *"Jämför social-media-strategi.md med vad som faktiskt ligger i kalendern och
  säg vad som inte stämmer"*
- *"Skriv ett utkast till bildtext för Victoria-reveal och lägg det i
  copy/instagram"*

Den gör ändringen, föreslår en rad om varför, och skickar upp den. Pablo ser
den i repots historik.

Be den gärna förklara vad den tänker göra innan den gör det, tills du känner
dig trygg.

---

## Två saker att veta

**Repot är offentligt.** Allt du skriver kan läsas av vem som helst. Riktig
korrespondens med namngivna personer, telefonnummer och personuppgifter hör
inte hemma här — se reglerna i README.

**Inget går sönder.** Varje version sparas. Blir något fel går det att läsa
tillbaka och återställa, och Pablo kan alltid rätta.

## Om du kör fast

Skriv i Usha Content. Installationen är mest klistra in och klicka, och fastnar
du på ett steg går det snabbt att ta tillsammans.
