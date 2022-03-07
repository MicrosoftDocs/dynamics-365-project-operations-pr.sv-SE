---
title: Hantering av underkontrakt i Project Operations
description: Det här ämnet ger en översikt över den fullständiga processen för underavtalshantering i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994253"
---
# <a name="subcontract-management-in-project-operations"></a>Hantering av underkontrakt i Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Underkontraktering i Microsoft Dynamics 365 Project Operations stöder följande affärsprocessflöde.

![Processflöde för underkontraktering](../media/SubcontractingProcessFlow.png)

Här är en steg-för-steg-beskrivning av underkontrakteringsprocessen.

1. Projektledaren skapar ett underavtal med en leverantör. Som standard används de prislistor som är kopplade till leverantörsposten för underavtalet. Leverantörskontot har relationstypen **Leverantör** eller **Leverantör**.
2. Projektledaren kan specificera alla inköp som radobjekt i underavtalet. Underavtalsrader kan vara för tid, utgifter eller produkter. Den transaktionsklass som väljs på varje underavtalsrad avgör vad raden gäller för.
3. Leverantörskontoansvarig och projektledaren kan iterera över underavtalet. Prissättningen kan justeras i inköpsprislistor som är kopplade till underavtalet.
4. Vid den här punkten eller senare i processen, om underavtalsraden gäller tid, associerar leverantörskontoansvarig kontakterna med varje underavtalsrad. Den här associationen ger information till den projektledare som arbetar med underavtalet. När en kontakt associeras med en underavtalsrad skapas automatiskt en bokningsbar resurs från kontakten, om en bokningsbar resurs inte redan finns.
5. Faktureringsmetoden för varje underavtalsrad kan vara **Fast pris** eller **Tid och material**. För underavtalsrader med fast pris kan du skapa ett milstolpebaserat fakturaschema.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
