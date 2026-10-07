# Arbetsrutin: Pablo och Mariana

Hur vi jobbar med innehåll till Instagram och övriga kanaler, så att saker blir
gjorda och inte bara pratade.

## Problemet vi löser

Vi tänker bra tillsammans i WhatsApp. Men i ett röstmeddelande låter ett beslut
likadant som en fundering, och nästa dag vet ingen vad som faktiskt bestämdes.

Exempel från 2 oktober: frågan om vilken dag Victoria-reveal skulle släppas
diskuterades fram och tillbaka — måndag, tisdag, "onsdag är sent", "två släpp
före torsdagen" — och utbytet slutade utan ett datum. Två nya idéer (Kizomba
Basics-videor och intresseanmälan i appen) kom dessutom in mitt i ett svar om
något helt annat, och fanns ingenstans dagen efter.

**WhatsApp är inte problemet.** Att tänka högt funkar för oss. Det som saknades
var ett ställe dit besluten tar vägen.

## Reglerna

**WhatsApp är där vi tänker. `innehallskalender.md` är där vi bestämmer.**

1. **Ett utbyte är inte klart förrän något flyttats till kalendern.** Antingen
   som *Bestämt*, eller som *Öppet* med namn på den som ska avgöra.

2. **En idé som dyker upp mitt i ett svar om något annat går direkt till
   Idébanken.** Den ska inte behöva överleva i en chatt för att vara kvar.

3. **Tre tillstånd, inget mer.**
   - **Bestämt** — datum, kanal, format, vem som gör vad. Går att börja på i dag.
   - **Öppet** — vi vet vad frågan är och vem som ska svara. Alltid ett namn.
   - **Idébank** — bra, men inte schemalagt. Ingen skuld.

4. **"Jag lutar åt måndag" är inte ett beslut.** Det är en åsikt. Beslutet är
   ett datum i kalendern. Den som äger frågan sätter det.

5. **Ingen status i chatten.** Är något klart eller försenat syns det i
   kalendern, inte i ett meddelande som rullar bort.

## Uppgifter och löpande ansvar

Kalendern hanterar innehåll som ska ut ett visst datum. Men mycket av arbetet
har inget släppdatum: svara på DM, uppdatera profiltext, byta länk, bestämma
något. Mariana påpekade att det inte passar i Bestämt/Öppet/Idébank, och hon
har rätt.

**Sådant blir en uppgift (Issue) i stället.** En uppgift har en ansvarig, en
etikett och ingen tidsplan — den stängs när den är gjord.

Så skapar du en: gå till fliken **Issues** på github.com, tryck **New issue**,
skriv vad som ska göras, välj vem under **Assignees** och sätt en etikett.
Fungerar från mobilen. Vem som helst av oss kan ge vem som helst en uppgift.

| Etikett | Vad |
|---|---|
| `admin` | Löpande ansvar för kontot: DM, profiltext, länkar |
| `content` | Produktion: inlägg, video, design, copy |
| `beslut` | Väntar på ett beslut — den som ska avgöra står som assignee |
| `plattformen` | Rör usha.se och behöver byggas av Pablo eller Claude |

**Skillnaden mot kalendern:** kalendern svarar på *vad går ut när*. Uppgifterna
svarar på *vad behöver någon göra*. En idé som blir ett inlägg bor i kalendern;
att någon ska svara på DM:en bor i en uppgift.

Öppna frågor kan ligga båda ställena. Hör den ihop med ett släpp, lägg den
under **Öppet** i kalendern. Står den för sig själv, gör en uppgift med
etiketten `beslut` och sätt den som ska avgöra som assignee.

## Rytmen

**Veckoavstämning, tjugo minuter.** Vi går igenom Öppet och de öppna
uppgifterna, bestämmer det som går att bestämma, och flyttar det som är moget
från Idébank till Bestämt. Tjugo minuter räcker om vi gjort punkt 1 under
veckan.

**Löpande under veckan:** fritt i WhatsApp. Allt som landar förs in i kalendern
av den som fick svaret.

## Claudes roll

Claude kan inte läsa WhatsApp — det finns inget sätt att koppla in en assistent
i en vanlig gruppchatt, och Business-API:t är byggt för kundtjänst, inte för
intern dialog.

Bryggan är enkel: **Pablo klistrar in utbytet**, så omvandlar Claude det till
rader i kalendern — vad som bestämdes, vad som blev en uppgift, och vad som
fortfarande är öppet och väntar på vem. Det är inte lika smidigt som en
integration, men det fungerar och det är ärligt.

Claude skriver också copy, sätter mätlänkar enligt `utm-rutin.md` och håller
kalendern uppdaterad.

## Var saker bor

| Vad | Var |
|---|---|
| Vad som ska ut och när | `docs/innehallskalender.md` |
| Uppgifter och löpande ansvar | Issues här i repot |
| Strategi och långsiktig plan | `docs/social-media-strategi.md` |
| Innehållsplan för plattformen | `docs/innehallsplan-plattformen.md` |
| Färdiga texter och mallar | `copy/` |
| Bild, video, ljud, manus | `media/` (stora original i Drive, länkas) |
| Mätlänkar | `docs/utm-rutin.md` |
| Riktig korrespondens med namngivna personer | Gmail och CRM, aldrig här |

## Att redigera från telefonen

Kalendern är en vanlig textfil. På github.com: öppna filen, tryck pennan,
skriv, tryck "Commit changes". Det går från mobilen och kräver ingen
installation.

Hellre en slarvig rad i kalendern än en välformulerad i chatten.
