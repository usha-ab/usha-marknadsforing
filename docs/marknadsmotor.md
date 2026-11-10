# Marknadsmotorn

Lärdomen från *The Startup Ideas Podcast* (Cody Schneider, nov 2026): det som
gör marknadsföring med AI-agenter bra är inte prompten utan **miljön** –
agenten läser riktiga data, får en rytm, producerar volym, och en människa
med smak godkänner innan något går ut. Vi har redan datan (UTM på varje
bokning, GA4, kortlänkar) och mallarna. Det här dokumentet är rytmen.

Fokus: **The Lab torsdagar** på Bacchi Syre (strategidokumentets "måndagar"
är inaktuellt sedan oktober 2026).

## Fyra rutiner, en vecka

| När | Rutin | Vad den gör | Vem godkänner |
| --- | --- | --- | --- |
| Måndag 07:30 | **Måndagsrapporten** | Läser förra veckans bokningar per kanal (utm_source/medium/campaign) och sidvisningar. Säger vad som konverterade och vad som var tyst. Mejl till Pablo och Mariana. | Ingen – den läser bara. |
| Måndag 08:00 | **Veckobatchen** | Fem inläggsvarianter + två reelsmanus för torsdagens Lab, ur värdekartan och veckans tema. Poängsatta mot creative director-checklistan. Mejl till Pablo och Mariana. | Pablo säger ja (eller ändrar). Mariana postar. |
| Tisdag 08:00 | **Outreach-batchen** | Fem lokaler/arrangörer/kreatörer ur CRM:et som inte kontaktats, personliga utkast enligt copy/outreach, lagda som **utkast i Gmail** – aldrig skickade. | Pablo läser och skickar själv. |
| Löpande | **Swipe-biblioteket** | `media/swipe/` – referenser vi vill likna, som batchen mäts mot. | Mariana fyller på. |

Rutinerna körs som Claude-molnrutiner (claude.ai/code/routines) med tillgång
till det här repot, Supabase (läsning) och Gmail. Ingen rutin publicerar eller
skickar något själv. Det är regeln: **manus → Pablos ja → först då ut**.

## Vad vi mäter

- Bokningar per kanal från `bookings.utm_*` (kanalen bärs länk → cookie →
  Stripe → bokning, se docs/utm-rutin.md). Kortlänkarna sätter kanalen:
  usha.se/thelab/insta, /thelab/chatt, /taxi/insta osv.
- Sidvisningar på /event/the-lab-torsdag och /thelab från Vercel Analytics.
- Inte: likes, följare, räckvidd. De säger inget om kvällen.

## Volym och gallring

Fem varianter per vecka är poängen, inte ett perfekt inlägg. Det som fick
klick och bokningar enligt måndagsrapporten görs mer av; det som var tyst
läggs ner utan diskussion. Efter fyra veckor har vi tjugo varianter och vet
vilken vinkel som faktiskt tar folk till torsdagen.

## Nästa steg (kräver beslut)

Ett litet annonstest på Meta (t.ex. 500 kr/vecka i fyra veckor, fem
varianter, mätt mot bokningar via UTM). Manus och bilder förbereds i batchen;
inget spenderas förrän Pablo säger till.
