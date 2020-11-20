---
title: Arbetsflöde för utgiftshantering
description: I det här ämnet förklaras hur du kan använda arbetsflödessystemet i Microsoft Dynamics 365 Finance för att konfigurera en granskningsprocess för utgiftsrapporter i utgiftshantering.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085695"
---
# <a name="expense-management-workflow"></a>Arbetsflöde för utgiftshantering

[!include [banner](../includes/banner.md)]

Du kan använda arbetsflödessystemet för att konfigurera en granskningsprocess för utgiftsrapporter i utgiftshantering. Du kan konfigurera ett arbetsflöde som använder följande kriterier för att avgöra vem som godkänner utgiftsrapporter:

- Hierarkin för medarbetarrapporter och fördefinierade godkännandegränser
- Ett godkännande på flera nivåer som stöder interimistiska godkännare och en slutlig godkännare
- Ekonomiska dimensioner och projektansvar
- Tilldelning till specifika användare eller användargrupper

Du kan skapa arbetsflödesgodkännanden för utgiftsrapporter, reserekvisitioner, förskott och återbetalning av moms.

**Exempel**

Följande process är ett exempel på arbetsflödet för utgiftshantering för en utgiftsrapport.

1. En medarbetare skapar och sparar en utgiftsrapport.
2. Medarbetaren skickar in utgiftsrapporten för godkännande. Godkännaren identifieras utifrån de regler som definierades när arbetsflödet konfigurerades.
3. Godkännaren får ett meddelande om att en utgiftsrapport är klar för godkännande. Godkännaren granskar utgiftsrapporten och kontrollerar att följande villkor uppfylls:

    - Utgifterna strider inte mot några utgiftsprinciper. Om en utgift bryter mot en princip verifierar godkännaren att utgiftsrapporten innehåller en giltig affärsmotivering.
    - Elektroniska kvitton bifogas utgiftsrapporten.

4. Godkännaren godkänner utgiftsrapporten.
5. Utgiftsrapporten tilldelas koordinatorn för bokföring i leverantörsreskontra.
6. Ett av följande steg inträffar, beroende på om automatisk bokföring är konfigurerad:

    - Om automatisk bokföring är konfigurerad bearbetas utgiftsrapporten för betalningen och utgiftsrapportens status uppdateras.
    - Om automatisk bokföring inte är konfigurerad verifierar koordinatorn för leverantörsreskontra att alla ursprungliga kvitton har skickats in och att kvittona stämmer överens med utgifterna i utgiftsrapporten. Alla momskoder som anges i utgiftsrapporten måste också verifieras som riktiga.

När dessa krav har verifierats bokförs utgiftsrapporten.

När utgiftsrapporten har bokförts auktoriseras betalningen för utgiftsrapporten och medarbetaren återbetalas.