---
title: Hantera en proforma projektbaserad faktura
description: Detta ämne ger information om hur du hanterar och arbetar med projektbaserade proforma-fakturor.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c61b0d887ae35988f1765d40de0447aa5fd7efd4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593772"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Hantera en proforma projektbaserad faktura

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

I Dynamics 365 Project Operations skapas proforma-fakturor som ett tillägg till fakturorna i Dynamics 365 Sales. Det finns emellertid många skillnader i faktureringsprocessen mellan Sales och Project Operations när det gäller fakturering. Det går till exempel inte att skapa en ny faktura från sidan **Fakturalista** i Project Operations, men det är möjligt att göra det i Sales. Dessa skillnader och tillägg används för att stödja faktureringsprocesser för projekt som skiljer sig från en typisk faktura för en försäljningsorder.

> [!IMPORTANT]
> På grund av skillnaderna bör du inte använda fakturor i Sales och Project Operations.

## <a name="invoice-header"></a>Fakturarubrik

Följande information finns tillgänglig i ett proforma-fakturahuvud i Project Operations.

| Fält | Plats | Beskrivning |
| --- | --- | --- | 
| **Faktura-ID** | Fliken **Sammanfattning** | Det ID som genereras automatiskt när en proforma-faktura skapas. Ett skrivskyddat fält som är låst för redigering. Det här fältet används som referens för varje proforma-faktura. |
| **Namn** | Fliken **Sammanfattning** | Ange till namnet på projektkontraktet som standard. Detta fält kan redigeras. | 
| **Valuta** | Fliken **Sammanfattning** | Ange till valutan på projektkontraktet som standard. Ett skrivskyddat fält som är låst för redigering. |
| **Prislista** | Fliken **Sammanfattning** | Ange till prislistan på projektkontraktet som standard. Ett skrivskyddat fält som är låst för redigering. | 
| **Affärsmöjlighet** | Fliken **Sammanfattning** | Referens till en kopplad affärsmöjlighet. Ett skrivskyddat fält som är låst för redigering. | 
| **Kontrakt** | Fliken **Sammanfattning** | Referensen till det kopplade projektkontraktet. Ett skrivskyddat fält som är låst för redigering. | 
| **Kund** | Fliken **Sammanfattning** | Referensen till det kopplade projektkontraktet. Ett skrivskyddat fält som är låst för redigering. |
| **Beskrivning** | Fliken **Sammanfattning** | Textfältet som beskriver fakturan. Detta fält kan redigeras. | 
| **Fakturera till** och relaterade fält | **Fliken Sammanfattning** | Standardvärden anges i projektkontraktets kund. Detta fält kan redigeras.  | 
| **Status** | Fliken **Sammanfattning** | Anger följande alternativ: **Aktiv**, **Stängd**, **Betald** och **Avbruten** och kan redigeras. Status för Project Operations som inte stöds omfattar **stängd** och **annullerad**. </br> Status är **aktiv** när fakturan skapas. </br>Statusen anges till **betald** endast efter att fakturan har bekräftats.  | 
| **Status för projektfaktura** | Fliken **Sammanfattning** | Anger följande alternativ: **Utkast**, **Granskning pågår** och **Bekräftad** och kan redigeras. I både **Utkast** och **Granskning pågår** kan fakturan redigeras. Det går inte att redigera fakturan efter att den har bekräftats. | 
| **Detaljbelopp** | Fliken **Sammanfattning** | Summan av beloppen på alla fakturarader efter förskott och avdrag. Ett skrivskyddat fält som är låst för redigering.  Fältet används för att beräkna slutbeloppet. | 
| **Rabatt (%)** | Fliken **Sammanfattning** | Det här fältet kan redigeras för att ange en avdragsprocent. Det här fältet stöds inte av Project Operations-funktioner. Det här är ett fält som inte stöds.|  
| **Rabattbelopp** | Fliken **Sammanfattning** | Det här fältet kan redigeras för att ange ett rabattbelopp. Det här fältet stöds inte av Project Operations-funktioner. Det här är ett fält som inte stöds. |  
| **Belopp före frakt** | **Fliken Sammanfattning** | Det totala fakturabeloppet efter att avdragen har tillämpats. Ett skrivskyddat fält som är låst för redigering. Fältet används för att beräkna slutbeloppet.  | 
| **Fraktbelopp** | Fliken **Sammanfattning** | Det här fältet kan redigeras för att ange ett fraktbelopp. Det här fältet stöds inte av Project Operations-funktioner. Det här är ett fält som inte stöds. |
| **Total moms** | Fliken **Sammanfattning** | Den totala momsen från alla fakturarader på fakturan. Ett skrivskyddat fält som är låst för redigering. | 
| **Totalbelopp** | Fliken **Sammanfattning** | Summan av beloppet efter avdrag och moms. Summan är det belopp kunden behöver betala. | 

## <a name="project-based-invoice-lines"></a>Projektbaserade kontraktrader

I Project Operations finns det alltid en faktura rad för varje projektkontraktrad. Fakturaraden skapas även om det inte finns några verkliga värden. Följande information finns tillgänglig i ett proforma-fakturarad.

| Fält | Plats | Beskrivning | 
| --- | --- | --- |
| **Faktura-ID** | Fliken **Allmänt** | Referens till faktura-ID. Ett skrivskyddat fält som är låst för redigering. Länken faktura-ID kan användas för att navigera tillbaka till fakturahuvudet. | 
| **Namn** | Fliken **Allmänt** | Namnet på fakturaraden som standard anges i kontraktradnamnet. Detta fält kan redigeras. |
| **Project** | Fliken **Allmänt** | Projektet på den relaterade projektkontraktraden. Ett skrivskyddat fält som är låst för redigering. Projektlänken kan användas för att navigera till projektet. | 
| **Faktureringsmetod** | Fliken **Allmänt** | Faktureringsmetoden på den relaterade projektkontraktraden. Ett skrivskyddat fält som är låst för redigering. |
| **Belopp på kontraktrad** | Fliken **Allmänt** | Kontraktsbeloppet på den relaterade projektkontraktsraden. Ett skrivskyddat fält som är låst för redigering. | 
| **Fakturerat till datum** | Fliken **Allmänt** | Summan av beloppen på alla fakturaraddetaljer för den här fakturan. Ett skrivskyddat fält som är låst för redigering. | 
| **Belopp** | Fliken **Allmänt** | Summan av beloppen på alla debiterbara fakturaraddetaljer för den här fakturan. Ett skrivskyddat fält som är låst för redigering. Fältet används för att beräkna slutbeloppet på fakturahuvudet. | 
| **Moms** | Fliken **Allmänt** | Summan av skattebeloppen på alla fakturaraddetaljer för den här fakturaraden. Ett skrivskyddat fält som är låst för redigering. Fältet används för att beräkna slutliga skattebeloppet på fakturahuvudet. | 
| **Utökat belopp** | Fliken **Allmänt** | Summan av totala belopp (**Skatt + belopp**) på alla debiterbara fakturaraddetaljer för den här fakturaraden. Ett skrivskyddat fält som är låst för redigering. Fältet används för att beräkna slutbeloppet på fakturahuvudet. |

## <a name="invoice-line-details"></a>Information om fakturarad

Varje fakturarad i en projektfaktura inkluderar fakturaraddetaljer. Dessa raddetaljer är relaterade till fakturerad faktisk försäljning och milstolparna som relaterar till den kontraktrad som fakturaraden refererar till. Alla dessa transaktioner är markerade som **Klara för fakturering**.

För raden **Tid- och materialfaktura** grupperas fakturaradinformationen på sidan **Debiterbar**, **Ej debiterbar** och **Kostnadsfritt** på **Fakturarad**. Informationen i **debiterbar fakturarad** läggs till summan för fakturaraden. **Kostnadsfritt** och **Faktiskt icke debiterbart** läggs inte till i fakturaradens summa.

För en rad för **Fast prisfaktura** skapas fakturadetaljer från milstolpar som är markerade som **Klar att fakturera** på den relaterade kontraktraden. När fakturaradinformationen har skapats från en milstolpe uppdateras faktureringsstatusen på milstolpen till **kundfakturan som skapats**.

### <a name="edit-invoice-line-details"></a>Redigera information om fakturarad

Följande fält är tillgängliga på fakturaraddetaljer som backas upp av fakturerad faktiskt försäljning.

| Fält | Beskrivning |
| --- | --- | 
| **Fakturarad** | En referens till **Fakturarad-ID**. Fältet är skrivskyddad och låst för redigering. Denna länk kan användas för att navigera tillbaka till fakturahuvudet. | 
| **Beskrivning** | En beskrivning av fakturaraddetaljen. Anges som standard i fältet **Interna kommentarer** i **Tidspost** och från fältet **Beskrivning** på **Utgiftspost**. Detta fält kan redigeras.| 
| **Extern beskrivning** | En beskrivning av fakturaraddetaljen. Anges som standard i fältet **Externa kommentarer** i **Tidspost** och från fältet **Beskrivning** på **Utgiftspost**. Detta fält kan redigeras. Beskrivningen kan användas för att avgöra vad som ska vara på den utskrivna fakturan som ska skickas till kunden. I Project Operations en proforma-faktura inte alla funktioner som krävs för att konfigurera utskriftsinställningar för en faktura. | 
| **Startdatum** | Det här fältet är skrivskyddad som anges som standard från källan. |
| **Project** | Det här är ett skrivskyddad fält som anges som standard från den faktiska källan till projektet på den relaterade kontraktraden. |  
| **Uppgift** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. |
| **Transaktionskategori** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | 
| **Roll** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. |  
| **Bokningsbar resurs** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | 
| **Resursföretag** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | 
| **Resursenhet** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | 
| **Antal** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. |  
| **Enhetsschema** | För fakturarad för tid anges det här värdet alltid värdet till tid och kan inte redigeras. För utgifter anges detta som standard från den faktiska källkostnaden. Ett skrivskyddat fält som är låst för redigering. | 
| **Enhet** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. |  
| **Pris** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. |
| **Valuta** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | 
| **Belopp** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | 
| **Moms** | Anges som standard från faktiska källan. Detta fält kan redigeras.| 
| **Beräknat belopp** | Ett beräknat fält, beräknat som **belopp + moms**. Ett skrivskyddat fält som är låst för redigering. | 
| **Faktureringstyp** | Anges som standard från faktiska källan. Detta fält kan redigeras. Om du väljer **debiterbar** läggs raden till i total summan för fakturaraden. **Kostnadsfritt** och **icke-debiterbar** tas de bort från fakturaradens totala summa.| 
| **Välj produkt** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. |
| **Produkt** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | 
| **Produktnamn** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. |  
| **Beskrivning av oregistrerad** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. |
| **Transaktionstyp** | Det här fältet är skrivskyddad som anges som standard från källan till **Fakturerad försäljning**. |  
| **Transaktionsklass** | Anges som standard från faktiska källan. Ett skrivskyddat fält som är låst för redigering. | 

Följande fält är tillgängliga på fakturaraddetaljer som backas upp av en milstolpe.

| Fält | Beskrivning |
| --- | --- | 
| **Fakturarad** | Referens till **Fakturarad-ID**. Ett skrivskyddat fält som är låst för redigering. Länken kan användas för att navigera tillbaka till fakturahuvudet.  | 
| **Beskrivning** | Beskrivning av fakturaraddetaljen. Ange som standard i beskrivningen av källmilstolpen. | 
|**Extern beskrivning** | Beskrivning av fakturaradinformationen som anges som standard från beskrivningen av källmilstolpen. Fältet kan användas för att avgöra vad som ska vara på den utskrivna fakturan som ska skickas till kunden. En proforma-faktura i Project Operations har inte alla funktioner som krävs för att konfigurera utskriftsinställningar för en faktura. | 
| **Startdatum** | Anges som standard från datumet för **milstolpe** på källmilstolpe. Ett skrivskyddat fält som är låst för redigering. | 
| **Project** | Anges som standard från källmilstolpe. Ett skrivskyddat fält som är låst för redigering. |
| **Uppgift** | Anges som standard från källmilstolpe. Ett skrivskyddat fält som är låst för redigering. | 
| **Transaktionskategori** | Ett skrivskyddat fält som är låst för redigering. |
| **Roll** | Ett skrivskyddat fält som är låst för redigering. | 
| **Bokningsbar resurs** | Ett skrivskyddat fält som är låst för redigering. | 
| **Resursenhet** | Ett skrivskyddat fält som är låst för redigering. | 
| **Enhetsschema** | Ett skrivskyddat fält som är låst för redigering. | 
| **Enhet** | Ett skrivskyddat fält som är låst för redigering. | 
| **Pris** | Ange som standard i beloppet i källmilstolpen. Ett skrivskyddat fält som är låst för redigering. |
| **Valuta** | Anges som standard från källmilstolpe. Ett skrivskyddat fält som är låst för redigering. |
| **Belopp** | Ange som standard i beloppet i källmilstolpen. Ett skrivskyddat fält som är låst för redigering. | 
| **Moms** | Ange som standard från momsbeloppet i källmilstolpen. Ett skrivskyddat fält som är låst för redigering. |
| **Utökat belopp** | Ange som standard från utökat belopp i källmilstolpen. Detta fält kan redigeras. | 
| **Faktureringstyp** | Anges alltid som standard till **debiterbar**. Ett skrivskyddat fält som är låst för redigering. |
| **Transaktionstyp** | Anges som standard från källmilstolpe. Ett skrivskyddat fält som är låst för redigering. | 
| **Transaktionsklass** | Anges som standard från källmilstolpe. Ett skrivskyddat fält som är låst för redigering. | 

## <a name="refresh-invoice-transactions"></a>Uppdatera fakturatransaktioner

Om du har verkliga värden som följde efter att fakturan skapades kan du ta med dessa faktiska värden på fakturan.

1. I **eftersläpad fakturavy**, markera data som **Klar att fakturera**.   
2. Öppna proforma-utkastfakturan på menyfliksområdet **Åtgärder**, välj **Uppdatera transaktioner på fakturaraden**.

  Fakturaraddetaljer skapas för alla faktiska som är föråldrade och markerade som **Redo att fakturera**, men som inte finns med på fakturan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
