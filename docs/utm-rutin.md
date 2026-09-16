# UTM-rutin: så vet vi vad som sålde biljetten

Utan kampanjparametrar i länken vet vi att en biljett såldes, men inte vad som sålde den. Omdirigeringen till Stripe och tillbaka raderar all referrer, så GA4 kan inte lista ut det på egen hand.

Sedan 16 september 2026 bär plattformen kanalen hela vägen: parametern fångas i en cookie när besökaren landar, följer med som metadata genom kassan, och skrivs som kolumner på bokningen. Kanalen är alltså en uppgift i databasen, inte en gissning i ett rapportverktyg.

## Så bygger du en länk

Grundform:

```
https://usha.se/event/the-lab-tarraxo-urban-kizomba?utm_source=instagram&utm_medium=social&utm_campaign=thelab
```

Fyra parametrar, varav de tre första alltid ska vara med:

| Parameter | Vad den svarar på | Våra värden |
|---|---|---|
| `utm_source` | Var låg länken? | `instagram`, `facebook`, `linkedin`, `tiktok`, `newsletter`, `qr`, `flyer` |
| `utm_medium` | Vilken sorts yta? | `social`, `story`, `bio`, `email`, `print`, `dm` |
| `utm_campaign` | Vilken insats? | `thelab`, `klippkort`, `partner`, `epassi` |
| `utm_content` | Vilken variant? (valfri) | `reel`, `carousel`, `post`, `a`, `b` |

Regler som gör datan användbar:

- **Gemener, inga mellanslag, inga å ä ö.** Systemet tvingar ned till gemener och kastar värden med konstiga tecken, men skriv rätt från början.
- **Samma ord varje gång.** `instagram` och `Instagram` blir samma sak, men `ig` blir en egen rad i rapporten. Håll dig till tabellen.
- **Kampanjen är insatsen, inte datumet.** Alla Lab-inlägg har `utm_campaign=thelab`, hela hösten. Vill du skilja veckor åt, använd `utm_content`.
- **Länka till sidan personen ska till**, inte till startsidan. En kväll, en kurs, en profil.

## Kombinera med partnerlänken

Partnerkoden och kampanjen bor på varsin parameter och krockar inte:

```
https://usha.se/event/the-lab-tarraxo-urban-kizomba?ref=B6CA24&utm_source=instagram&utm_medium=story&utm_campaign=thelab
```

Då vet vi både vem som värvade och var länken låg.

## Var du lägger länken

- **Instagram:** i bion (en länk, byt när kampanjen byter) och i story-stickers. Bildtexter är inte klickbara, så där räcker `usha.se`.
- **Facebook:** i inlägget och i eventets biljettlänk.
- **LinkedIn:** i första kommentaren, inte i brödtexten.
- **Nyhetsbrev och mejl:** alltid, med `utm_medium=email`.
- **QR-koder på plats:** `utm_source=qr&utm_medium=print&utm_campaign=<var koden sitter>`.

## Vad som mäts automatiskt

Detta skickas till GA4 utan att någon behöver göra något:

| Händelse | När |
|---|---|
| `purchase` | Köpet är genomfört. Bär belopp, biljettyp, antal, kanal och eventuell partnerkod. Bokningens id används som transaktions-id, så en omladdad kvittosida inte räknas som ett extra köp. |
| `begin_checkout` | Någon trycker på köpknappen. Skillnaden mot `purchase` visar hur många som hoppar av i kassan. |
| `pass_purchase` | Ett klippkort köptes. |
| `follow` | Någon började följa en kreatör med konto. |
| `follow_email` | Någon följde via e-post, utan konto. |
| `sign_up` | Nytt konto. |

## Vad du kan fråga databasen om

Kanalen ligger på bokningen som `utm_source`, `utm_medium`, `utm_campaign` och `utm_content`. Det gör det möjligt att svara på "hur många biljetter kom från Instagram i september" med en säker siffra, även för gästköp där GA4 tappar spåret.

Null betyder okänd kanal, inte direkttrafik. En länk utan parametrar ger null.
