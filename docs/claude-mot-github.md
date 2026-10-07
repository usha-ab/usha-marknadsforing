# Koppla din Claude till GitHub

Så att din Claude kan **skriva** i repot, inte bara läsa det.

## Läget

Repot är offentligt, så vilken Claude som helst kan läsa filerna genom att
öppna adressen. Det är därför Marianas Claude kunde läsa guiden direkt.

Att **ändra** något kräver inloggning. Det finns två vägar dit. Prova A först —
den tar några minuter. Fungerar den inte, ta B.

---

## Väg A: koppling i Claude

Om ditt Claude-abonnemang tillåter egna kopplingar (connectors) går det att
lägga till GitHub direkt.

1. Öppna **Inställningar → Kopplingar** (Settings → Connectors) i Claude
2. Leta efter GitHub i katalogen. Finns den: lägg till och logga in med ditt
   GitHub-konto
3. Finns den inte, välj **Lägg till egen koppling** och använd adressen
   `https://api.githubcopilot.com/mcp/`

Hittar du ingen av delarna har ditt abonnemang inte funktionen, och då är det
väg B som gäller. Det är inget fel på dig eller kontot.

**Säkerhet:** ger kopplingen dig valet att begränsa åtkomsten, välj bara
`usha-ab/usha-marknadsforing`. Din Claude behöver inte komma åt plattformens
kod.

---

## Väg B: Claude Code på din dator

Fungerar alltid, men tar en kvart att sätta upp. Claude Code är samma assistent
i ett terminalfönster, med tillgång till filerna och till GitHub.

Du behöver inte kunna programmera. Du kommer att skriva på svenska, precis som
i chatten.

**1. Installera Node** (om du inte har det): ladda ner från nodejs.org, version
18 eller senare. Nästa, nästa, klar.

**2. Installera Claude Code.** Öppna Terminal (Mac: tryck cmd+mellanslag, skriv
"Terminal") och klistra in:

    npm install -g @anthropic-ai/claude-code

**3. Installera GitHub CLI och logga in:**

    brew install gh
    gh auth login

Välj GitHub.com, HTTPS, och logga in via webbläsaren. Det är det som ger din
Claude rätt att skriva.

**4. Hämta hem repot:**

    gh repo clone usha-ab/usha-marknadsforing
    cd usha-marknadsforing

**5. Starta:**

    claude

Nu är du inne. Skriv på svenska.

---

## Vad du kan be din Claude om när det fungerar

- *"Läs innehallskalender.md och lägg till att 5 snabba släpps den 14 oktober,
  jag gör klippet"*
- *"Ge Pablo en uppgift om att bestämma vem som svarar på DM, märk den admin"*
- *"Jämför social-media-strategi.md med vad som faktiskt ligger i kalendern och
  säg vad som inte stämmer"*
- *"Skriv ett utkast till bildtext för Victoria-reveal och lägg det i copy/instagram"*

Din Claude gör ändringen, föreslår en rad om varför, och skickar upp den. Pablo
ser den i repots historik.

## Två saker att veta

**Repot är offentligt.** Allt du skriver här kan läsas av vem som helst. Riktig
korrespondens med namngivna personer, telefonnummer och personuppgifter hör
inte hemma här — se reglerna i README.

**Inget går sönder.** Varje version sparas. Blir något fel går det att läsa
tillbaka och återställa, och Pablo kan alltid rätta.

## Om du kör fast

Skriv i Usha Content, eller lägg en uppgift i repot med etiketten `beslut` och
Pablo som ansvarig. Fastnar du i steg B går det att ta tillsammans på en
kvart — det är mest klistra in och klicka.
