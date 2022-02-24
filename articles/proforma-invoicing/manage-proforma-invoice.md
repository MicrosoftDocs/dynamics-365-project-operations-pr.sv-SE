---
title: Hantera en proforma-faktura
description: I det här ämnet finns information om hur man hanterar och arbetar med proforma-fakturor.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f3aab57f159dbb522ebe5d24dc3693034f6f81f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181474"
---
# <a name="manage-a-proforma-invoice"></a>Hantera en proforma-faktura

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

I Dynamics 365 Project Operations skapas proforma-fakturor som ett tillägg till fakturorna i Dynamics 365 Sales. Det finns emellertid många skillnader i faktureringsprocessen mellan Sales och Project Operations när det gäller fakturering. Det går till exempel inte att skapa en ny faktura från sidan **Fakturalista** i Project Operations, men det är möjligt att göra det i Sales. Dessa skillnader och tillägg används för att stödja faktureringsprocesser för projekt som skiljer sig från en typisk faktura för en försäljningsorder.

> [!IMPORTANT]
> På grund av skillnaderna bör du inte använda fakturor i Sales och Project Operations.

## <a name="invoice-header"></a>Fakturarubrik

Följande information finns tillgänglig i ett proforma-fakturahuvud i Project Operations.

| Fält | Plats | Beskrivning | Inverkan nedströms |
| --- | --- | --- | --- |
| **Faktura-ID** | Fliken **Sammanfattning** | Det ID som genereras automatiskt när en proforma-faktura skapas. Ett skrivskyddat fält som är låst för redigering. | Det här fältet används som referens för varje proforma-faktura. |
| **Namn** | Fliken **Sammanfattning** | Ange till namnet på projektkontraktet som standard. Det här fältet kan redigeras av användaren. | &nbsp;  |
| **Valuta** | Fliken **Sammanfattning** | Ange till valutan på projektkontraktet som standard. Ett skrivskyddat fält som är låst för redigering. |&nbsp; |
| **Prislista** | Fliken **Sammanfattning** | Ange till prislistan på projektkontraktet som standard. Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Affärsmöjlighet** | Fliken **Sammanfattning** | Referens till en kopplad affärsmöjlighet. Ett skrivskyddat fält som är låst för redigering. | &nbsp;  |
| **Kontrakt** | Fliken **Sammanfattning** | Referensen till det kopplade projektkontraktet. Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Kund** | Fliken **Sammanfattning** | Referensen till det kopplade projektkontraktet. Ett skrivskyddat fält som är låst för redigering. |&nbsp;  |
| **Beskrivning** | Fliken **Sammanfattning** | Textfältet som beskriver fakturan. Det här fältet kan redigeras av användaren. | &nbsp; |
| **Fakturera till** och relaterade fält | **Fliken Sammanfattning** | Standardvärden anges i projektkontraktets kund. Det här fältet kan redigeras av användaren.  | &nbsp; |
| **Status** | Fliken **Sammanfattning** | Anger följande alternativ: **aktiv**, **stängd**, **betald** och **avbruten** och kan redigeras av användaren. | Status för projektåtgärder som inte stöds omfattar **stängd** och **annullerad**. </br> Status är **aktiv** när fakturan skapas. </br>Statusen anges till **betald** endast efter att fakturan har bekräftats. |
| **Status för projektfaktura** | Fliken **Sammanfattning** | Anger följande alternativ: **Utkast**, **Granskning pågår** och **Bekräftad** och kan redigeras av användaren. | I både **Utkast** och **Granskning pågår** kan fakturan redigeras. Det går inte att redigera fakturan efter att den har bekräftats. |
| **Detaljbelopp** | Fliken **Sammanfattning** | Summan av beloppen på alla fakturarader efter förskott och avdrag. Ett skrivskyddat fält som är låst för redigering. | Fältet används för att beräkna slutbeloppet. |
| **Rabatt (%)** | Fliken **Sammanfattning** | Det här fältet kan redigeras för att ange en rabattprocent. Det här fältet stöds inte av Project Operations-funktioner. | Det här är ett fält som inte stöds. |
| **Rabattbelopp** | Fliken **Sammanfattning** | Det här fältet kan redigeras för att ange ett rabattbelopp. Det här fältet stöds inte av Project Operations-funktioner. | Det här är ett fält som inte stöds. |
| **Belopp före frakt** | **Fliken Sammanfattning** | Det totala fakturabeloppet efter att rabatterna har tillämpats. Ett skrivskyddat fält som är låst för redigering. | Fältet används för att beräkna slutbeloppet. |
| **Fraktbelopp** | Fliken **Sammanfattning** | Det här fältet kan redigeras för att ange ett fraktbelopp. Det här fältet stöds inte av Project Operations-funktioner. | Det här är ett fält som inte stöds. |
| **Total moms** | Fliken **Sammanfattning** | Den totala momsen från alla fakturarader på fakturan. Ett skrivskyddat fält som är låst för redigering. | Inga. |
| **Totalbelopp** | Fliken **Sammanfattning** | Summan av beloppet efter rabatter och moms. | Summan är det belopp kunden behöver betala. |

## <a name="project-based-invoice-lines"></a>Projektbaserade kontraktrader

I Project Operations finns det alltid en faktura rad för varje projektkontraktrad. Fakturaraden skapas även om det inte finns några verkliga värden. Följande information finns tillgänglig i ett proforma-fakturarad.

| Fält | Plats | Beskrivning | Inverkan nedströms |
| --- | --- | --- | --- |
| **Faktura-ID** | Fliken **Allmänt** | Referens till faktura-ID. Ett skrivskyddat fält som är låst för redigering. | Länken faktura-ID kan användas för att navigera tillbaka till fakturahuvudet. |
| **Namn** | Fliken **Allmänt** | Namnet på fakturaraden som standard anges i kontraktradnamnet. Det här fältet kan redigeras av användaren. | &nbsp; |
| **Project** | Fliken **Allmänt** | Projektet på den relaterade projektkontraktraden. Ett skrivskyddat fält som är låst för redigering. | Projektlänken kan användas för att navigera till projektet. |
| **Faktureringsmetod** | Fliken **Allmänt** | Faktureringsmetoden på den relaterade projektkontraktraden. Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Belopp på kontraktrad** | Fliken **Allmänt** | Kontraktsbeloppet på den relaterade projektkontraktsraden. Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Fakturerat till datum** | Fliken **Allmänt** | Summan av beloppen på alla fakturaraddetaljer för den här fakturan. Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Belopp** | Fliken **Allmänt** | Summan av beloppen på alla debiterbara fakturaraddetaljer för den här fakturan. Ett skrivskyddat fält som är låst för redigering. | Fältet används för att beräkna slutbeloppet på fakturahuvudet. |
| **Moms** | Fliken **Allmänt** | Summan av skattebeloppen på alla fakturaraddetaljer för den här fakturaraden. Ett skrivskyddat fält som är låst för redigering. | Fältet används för att beräkna slutliga skattebeloppet på fakturahuvudet. |
| **Utökat belopp** | Fliken **Allmänt** | Summan av totala belopp (**Skatt + belopp**) på alla debiterbara fakturaraddetaljer för den här fakturaraden. Ett skrivskyddat fält som är låst för redigering. | Fältet används för att beräkna slutbeloppet på fakturahuvudet. |

## <a name="invoice-line-details"></a>Information om fakturarad

Varje fakturarad i en projektfaktura inkluderar fakturaraddetaljer. Dessa raddetaljer är relaterade till fakturerad faktisk försäljning och milstolparna som relaterar till den kontraktrad som fakturaraden refererar till. Alla dessa transaktioner är markerade som **Klara för fakturering**.

För raden **Tid- och materialfaktura** grupperas fakturaraddetaljer i **debiterbar**, **icke-debiterbar** och **kostnadsfri** på sidan **Fakturarad**. Informationen i **debiterbar fakturarad** läggs till summan för fakturaraden. **Kostnadsfritt** och **Faktiskt icke debiterbart** läggs inte till i fakturaradens summa.

För raden **Faktura med fast pris** skapas fakturaraddetaljer från milstolpar som är markerade som **klara för fakturering** på den relaterade kontraktraden. När fakturaradinformationen har skapats från en milstolpe uppdateras faktureringsstatusen på milstolpen till **kundfakturan som skapats**.

### <a name="edit-invoice-line-details"></a>Redigera information om fakturarad

Följande fält är tillgängliga på fakturaraddetaljer som backas upp av fakturerad faktiskt försäljning.

| Fält | Beskrivning | Inverkan nedströms |
| --- | --- | --- |
| **Fakturarad** | En referens till **Fakturarad-ID**. Skrivskyddat fält, låst för redigering. | Denna länk kan användas för att navigera tillbaka till fakturahuvudet. |
| **Beskrivning** | En beskrivning av fakturaraddetaljen. Anges som standard i fältet **Interna kommentarer** i **Tidspost** och från fältet **Beskrivning** på **Utgiftspost**. Det här fältet kan redigeras av användaren.| &nbsp; |
| **Extern beskrivning** | En beskrivning av fakturaraddetaljen. Anges som standard i fältet **Externa kommentarer** i **Tidspost** och från fältet **Beskrivning** på **Utgiftspost**. Det här fältet kan redigeras av användaren. | Beskrivningen kan användas för att avgöra vad som ska vara på den utskrivna fakturan som ska skickas till kunden. I Project Operations en proforma-faktura inte alla funktioner som krävs för att konfigurera utskriftsinställningar för en faktura. |
| **Startdatum** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | Fältet kan redigeras på en ny fakturaraddetalj som inte har säkerhetskopierats av en faktisk källa. |
| **Project** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | Ange som standard projektet på den tillhörande kontraktsraden. |
| **Uppgift** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | Fältet kan redigeras på en ny fakturaraddetalj som inte har säkerhetskopierats av en faktisk källa. I en nedrullningsbar lista visas alla uppgifter som är associerade med den relaterade projektkontraktraden.  |
| **Transaktionskategori** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | Fältet kan redigeras på en ny fakturaraddetalj som inte har säkerhetskopierats av en faktisk källa. |
| **Roll** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | Fältet kan redigeras på en ny fakturaraddetalj som inte har säkerhetskopierats av en faktisk källa. |
| **Bokningsbar resurs** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | Fältet kan redigeras på en ny fakturaraddetalj som inte har säkerhetskopierats av en faktisk källa. |
| **Resursföretag** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | Fältet kan redigeras på en ny fakturaraddetalj som inte har säkerhetskopierats av en faktisk källa. |
| **Resursenhet** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | Fältet kan redigeras på en ny fakturaraddetalj som inte har säkerhetskopierats av en faktisk källa. |
| **Antal** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | Fältet kan redigeras på en ny fakturaraddetalj som inte har säkerhetskopierats av en faktisk källa. |
| **Enhetsschema** | För fakturarad för tid anges det här värdet alltid värdet till tid och kan inte redigeras. För utgifter anges detta som standard från den faktiska källkostnaden. Ett skrivskyddat fält som är låst för redigering. | Ange som standard till **tid** på en ny fakturaraddetalj som inte har säkerhetskopierats med ett faktiskt värde. |
| **Enhet** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | Fältet kan redigeras på en ny fakturaraddetalj som inte har säkerhetskopierats av en faktisk källa |
| **Pris** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | Fältet kan redigeras på en ny fakturaraddetalj som inte har säkerhetskopierats av en faktisk källa. Om inget värde anges kommer värdet att anges som standard när du har **sparat**. |
| **Valuta** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | Anges som standard i fakturahuvudet när du skapar en ny fakturainformation utan faktisk uppbackning.  Ett skrivskyddat fält som är låst för redigering. |
| **Belopp** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | Beräknat som ett **antal \* pris** för att skapa en ny fakturadetalj utan att behöva säkerhetskopiera. Det beräknas efter **Spara**. Ett skrivskyddat fält som är låst för redigering. |
| **Moms** | Anges som standard från faktiska källan. Det här fältet kan redigeras av användaren | Fältet kan redigeras av användaren när du skapar en ny fakturaraddetalj utan att behöva säkerhetskopiera. |
| **Utökat belopp** | Ett beräknat fält, beräknat som **belopp + moms**. Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Faktureringstyp** | Anges som standard från faktiska källan. Det här fältet kan redigeras av användaren. | Om du väljer **debiterbar** läggs raden till i total summan för fakturaraden. **Kostnadsfritt** och **icke-debiterbar** tas de bort från fakturaradens totala summa. |
| **Transaktionstyp** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | Ange som standard till **fakturerad försäljning** och låst när du skapar en ny **fakturaraddetalj** utan att behöva säkerhetskopiera.  |
| **Transaktionsklass** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | Ange som standard baserat på om användaren väljer att skapa en fakturraddetalj **Tid**, **Utgift** eller **Avgift** samtidigt som du också skapar en ny **fakturraddetalj** utan en faktisk uppbackning. Låst från redigering. |

Följande fält är tillgängliga på fakturaraddetaljer som backas upp av en milstolpe:

| Fält | Beskrivning | Inverkan nedströms |
| --- | --- | --- |
| **Fakturarad** | Referens till **Fakturarad-ID**. Ett skrivskyddat fält som är låst för redigering. | Länken kan användas för att navigera tillbaka till fakturahuvudet. |
| **Beskrivning** | Beskrivning av fakturaraddetaljen. Ange som standard i beskrivningen av källmilstolpen. | &nbsp; |
|**Extern beskrivning** | Beskrivning av fakturaradinformationen som anges som standard från beskrivningen av källmilstolpen. | Fältet kan användas för att avgöra vad som ska vara på den utskrivna fakturan som ska skickas till kunden. En proforma-faktura i Project Operations har inte alla funktioner som krävs för att konfigurera utskriftsinställningar för en faktura. |
| **Startdatum** | Anges som standard från datumet för **milstolpe** på källmilstolpe. Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Project** | Anges som standard från källmilstolpe. Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Uppgift** | Anges som standard från källmilstolpe. Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Transaktionskategori** | Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Roll** | Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Bokningsbar resurs** | Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Resursenhet** | Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Enhetsschema** | Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Enhet** | Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Pris** | Ange som standard i beloppet i källmilstolpen. Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Valuta** | Anges som standard från källmilstolpe. Ett skrivskyddat fält som är låst för redigering. |&nbsp; |
| **Belopp** | Ange som standard i beloppet i källmilstolpen. Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Moms** | Ange som standard från momsbeloppet i källmilstolpen. Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Utökat belopp** | Ange som standard från utökat belopp i källmilstolpen. Det här fältet kan redigeras av användaren | &nbsp; |
| **Faktureringstyp** | Anges alltid som standard till **debiterbar**. Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Transaktionstyp** | Anges som standard från källmilstolpe. Ett skrivskyddat fält som är låst för redigering. | &nbsp; |
| **Transaktionsklass** | Anges som standard från källmilstolpe. Ett skrivskyddat fält som är låst för redigering. | &nbsp; |

## <a name="refresh-invoice-transactions"></a>Uppdatera fakturatransaktioner

Om du har verkliga värden som följde efter att fakturan skapades kan du ta med dessa faktiska värden på fakturan.

1. I **eftersläpad fakturavy**, markera data som **Klar att fakturera**.   
2. Öppna proforma-utkastfakturan och i menyfliksområdet **Åtgärder** klicka på **Uppdatera transaktioner på fakturaraden**.

  Detta skapar fakturaradinformation för alla faktiska som är tidigare daterade och markerade som **Klar att fakturera** men som inte ingår i fakturan.
