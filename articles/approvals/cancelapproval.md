---
title: Avbryt godkännande av tidigare godkända poster
description: I detta ämne beskrivs hur en projektledare kan annullera godkännande av tidigare godkända poster för tid, utgifter eller materialanvändning.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584802"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Avbryt godkännande av tidigare godkända poster

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

En projektledare eller godkännare som tidigare dokänt poster för tid, utgifter eller materialanvändning kan annullera sitt godkännande av dessa poster. 

Följ stegen nedan om du vill avbryta godkännandet av en tidigare godkänd post för tid, utgift eller materialanvändning.

1. Gå till **Projekt** \> **Mitt arbete** \> **Godkännanden**.
2. Listsidan **Godkännanden** visar alla tidsposter som väntar på godkännande. Ändra vyn till **Mina tidigare godkännanden**.
3. Välj tidpunkt, utgift eller materialgodkännande som ska annulleras. I åtgärdsfönstret väljer du sedan **Annullera godkännande**.
4. Välj **OK** för att bekräfta åtgärden i den meddelanderuta för bekräftelse som vitas.

> [!IMPORTANT]
> Du kan inte annullera godkännande av en tidigare godkänd tids-, utgifts- och materialanvändningspost som redan har fakturerats kunden. Om du försöker göra detta får du ett meddelande om att godkännandet inte kan annulleras eftersom det redan har fakturerats. I så fall kan du endast annullera godkännandet om en korrigeringsfaktura används för att utfärda en fullständig kreditering eller återbetalning till kunden för den ursprungliga fakturan.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Effekt av att annullera godkännande av en tidigare godkänd post

När ett godkännande har annullerats finns det både driftseffekter och ekonomiska effekter.

### <a name="operational-impact"></a>Driftseffekter

Om godkännande av en post annulleras markeras godkännandeposten som **Skickad**. Postens status ändras till **Skickad**. I det här stadiet kan en projektteammedlem återkalla posten utan att skicka in en begäran återkallelse.

Godkännaren kan ändra värdena för **Fakturerbar kvantitet** och **Faktureringstyp** och sedan godkänna posten en gång till.

### <a name="financial-impact"></a>Finansiella effekter

Om godkännandet av en post annulleras kommer motsvarande faktiska värden för kostnad och försäljning att uppdateras på följande sätt:

- Fältet **Justeringsstatus** uppdateras till **Justerad**.
- Fältet **Faktureringsstatus** uppdateras till **Annullerad**.

Sedan skapas återföringsposter i tabellen faktiska värden. Om du vill skapa återföringsposter kopieras systemet över fältvärdena från de ursprungliga värdena. De enda värden som inte kopieras över är antalet värden. De här värdena återförs i stället. Återförda faktiska värden skapas både för **kostnad** och för **fakturerade försäljningsvärden**. Fältet **justeringsstatus** på de återförda verkliga värdena ställs till att värdet **inte justerat** och fält **faktureringsstatus** är **annullerad**. På grund av dessa ändringar tar de registrerade utgifterna och den totala förväntande omsättningen kommer inte längre att räknas för de belopp som dessa faktiska värden representerar.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
