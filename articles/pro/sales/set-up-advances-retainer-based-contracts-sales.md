---
title: Förskott och arvodesbaserade kontrakt – Lite
description: I det här ämnet finns information om arvodesbaserade kontrakteringsmodeller och förskott i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 912b235af5e561349fdfb481e5f5b7c5514669c3
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180889"
---
# <a name="advances-and-retainer-based-contracts---lite"></a>Förskott och arvodesbaserade kontrakt – Lite


_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Dynamics 365 Project Operations stöder arvode-baserade kontrakt. Ett arvodebaserat kontrakt är en förhandlad uppsättning lika fördelade utbetalningar som kunden ska faktureras för under hela projektets varaktighet. Den här typen av kontrakt används vanligtvis för faktureringsmodeller som grundas på tid och material eller förbrukning, där det finns ett behov av att ge kunden en förutsägbar faktura och en betalningsplan. Faktiska intäkter för varje period stäms av mot den betalning som tas emot från kunden i början av perioden. I enlighet med faktureringsmodellen som grundar sig på tid och material kan intäktsvärden som har ökat i varje period variera beroende på kostnaderna. Om den ökade intäkten överstiger det belopp som erhållits i början av perioden kan projektleveransföretaget göra följande:

- Endast fakturera kunden för överskottet 
- Senarelägga avstämningen av intäkten till nästa faktureringsperiod och utföra en sista faktura i slutet av projektet för eventuella kvarvarande ej avstämda intäkter

Den huvudsakliga skillnaden mellan en arvodesbaserad kontraktmodell och en med fast pris i Project Operations är att fakturabeloppet i kontraktmodellen med fast pris inte är länkat eller knutet till ådragna kostnader. Fakturering följer en milstolpe-baserad metod som är justerad mot de kostnader som uppstår för perioden. I ett arvodebaserat kontrakt registreras intäkter som kan faktureras utifrån faktureringsmetoden på kontraktraden. När faktureringsmetoden är tid och material är faktureringsbara intäkter knutna till kostnader som uppstår under en given period och kan variera från period till period. Kunden faktureras dock bara för beloppet på det periodiska arvodet. I systemet används en ny faktura i slutet av perioden för att stämma av den fakturerade intäkten som registrerats under perioden mot det belopp kunden fakturerades för i början av perioden.

Fördelen med den här metoden är att kundens kostnader blir förutsägbara i arvodesschemat i motsats till en typisk tids- och materialmodell. Organisationen som levererar projektet har också utrymme för att täcka risken för att kostnaderna som uppstår till följd av ökningar av omfattningen av en modell med fast pris inte skulle ha tillåtits.

Utöver ett periodiskt arvodesbaserat schema kan Project Operations registrera ett engångsförskott från en kund och stämma av mot de olika projektkostnadskomponenterna.

Arvodet i Project Operations är inte tillgängligt för användning förrän det faktureras till kunden. Detta indikeras av följande fält i underrutnätet för förskott och arvoden.

| Fält | Beskrivning | Inverkan nedströms |
| --- | --- | --- |
| Disponibelt belopp | Det belopp som är tillgängligt för användning på en arvodes- eller förskottspost. | Innan förskottet eller arvodet faktureras är det inte tillgängligt att använda, vilket innebär att det tillgängliga beloppet blir noll. |
| Använt belopp | Det belopp som redan använts av arvodet eller förskottet. | Ett förskott eller arvode kan avstämmas delvis på en faktura med faktiska kostnader som gör att någon del markeras som redan använd eller förbrukad. Resten av förskottet eller arvodet är tillgängligt att stämma av på en framtida faktura med faktiska kostnader. |
