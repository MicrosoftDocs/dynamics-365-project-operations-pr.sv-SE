---
title: Korrigera redovisning i utkast till projektfakturaförslag
description: I ämne beskrivs hur du ändrar redovisningsrelaterad information i ett utkast till fakturaförslag.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bf0a3d6b97880920b133cb3b30389adf0c83111c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575096"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Korrigera redovisning i utkast till projektfakturaförslag

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

*Verksamhetsinformationen* för projektfakturor underhålls av projektledaren på en proforma-faktura. Den här informationen omfattar beslut om de timmar, utgifter, material eller milstolpar som måste faktureras, priser och användning av förskotts- och kvarhållarbelopp. När du har bekräftat den ursprungliga proforma-fakturan kan du justera driftinformationen genom att skapa och bekräfta en [korrigerande proforma-faktura](../proforma-invoicing/corrective-invoices.md).

*Redovisningsinformation* för projektfakturor hanteras i ett kundriktad fakturadokument. Den här informationen omfattar momsberäkningen och de ekonomiska mått som tillämpats på fakturan. Den ämne innehåller information om hur dessa redovisningsuppgifter kan justeras efter ett utkast till projektfakturaförslag.

## <a name="adjust-sales-tax"></a>Justera momsbelopp

Standardfaktureringsmomsgrupper och artikelförsäljningsgrupper kan justeras direkt i fakturaförslagsdokumentet. Välj för att justera dessa grupper **Redigera** och ange sedan ett nytt värde på varje projektförslagsrad i fältet **Momsgrupp** eller **Momsgrupp för artikelförsäljning**.

## <a name="adjust-financial-dimensions"></a>Justera ekonomiska dimensioner

### <a name="header-dimensions"></a>Rubrikmått

Som standard hämtas ekonomiska fakturamått från de icke-fakturerade projekttransaktionsposter som faktureras. Med systeminställningarna kan du emellertid använda ekonomiska mått i sidhuvudet för projektfakturaförslag i syfte att publicera kundsaldon. Om du vill aktivera den här funktionen väljer du **Tillåt uppdateringar av projektmått för kundreskontra** på fliken **Ekonomi** på sidan **Projekthanterings- och redovisningsparametrar**.

Ekonomiska mått i fakturahuvuden kan redigeras innan en faktura bokförs. På sidan **Projektfakturaförslag** växlar du till vyn **Sidhuvud** och redigerar sedan värdena på fliken **Ekonomiska mått**.

Vyn **Sidhuvud** är endast tillgänglig när systemadministratören aktiverar funktionen **Använd fakturaföslag och fakturajournalformulär för projekt med vynd för sidhuvud och rader** i arbetsytan **Funktionshantering**. För den här funktionen krävs Ekonomiuppdatering 10.0.25 eller senare.

### <a name="line-dimensions"></a>Radmått

Ekonomiska dimensioner kan inte redigeras direkt på en förslagsrad för projektfaktura. Följ i stället de här stegen om du vill justera ekonomiska dimensioner på ett projektfakturaförslag.

1. I projektfakturaförslaget markerar du **Ta bort alla** om du vill ta bort projektfakturaförslagsraderna.

    Knappen **Radera alla** är endast tillgänglig efter att systemadministratören aktiverar funktionen **Ta bort rader för fakturaförslag när du använder Project Operations för resursbaserade/icke-lagerbaserade scenarier** i arbetsytan **Funktionshantering**.

2. Justera ekonomiska dimensioner:

    - **Transaktioner på konto (faktureringsmilstolpar):** Gå till **Alla projekt** \> **Hantera** \> **Transaktioner på konto** och välj den milstolpe som kräver justering. På fliken **Ekonomiska dimensioner** uppdaterar du sedan värdena efter behov.
    - **Tid, utgifter och materialtransaktioner:** På sidan **Upplagda projekttransaktioner**, välj **Justera bokföring** för att uppdatera de ekonomiska dimensionerna.

3. När du har justerat de ekonomiska dimensionsvärdena går du till **Projektledning och redovisning** \> **Periodisk** \> **Integrering av Project Operations** och välj **Importera från mellanlagringstabell** för att köra den periodiska processen. I den processen används de uppdaterade ekonomiska värdena för att skapa projektfakturaförslagsraderna på nytt. De uppdaterade värdena används sedan i projektundersänkaren och huvudboken när projektfakturan läggs upp.
