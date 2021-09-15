---
title: underavtalering i den tidiga åtkomstversionen i oktober 2021
description: Detta ämne ger en översikt över de underleverantörsfunktioner i Project Operations som ingår i den tidiga åtkomstversionen från oktober 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383717"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>underavtalering i den tidiga åtkomstversionen i oktober 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Detta ämne ger en översikt över de underleverantörsfunktioner i Dynamics 365 Project Operations som ingår i den tidiga åtkomstversionen för oktober 2021. Denna funktionsuppsättning är inte klar för produktion eller live-miljöer, varför dessa funktioner finns kvar i den tidiga åtkomstversionen tills den fullständiga funktionsuppsättningen har släppts. Vi rekommenderar att du inte använder underleverantörsfunktionen för live-produktionsscenarier förrän förhandsgranskningsbanderollen har tagits bort. 

Följande lista innehåller en översikt över vad som för närvarande är tillgängligt i den tidiga åtkomstversionen i oktober 2021:

1. Projektledaren skapar ett underavtal med en leverantör. Som standard används de prislistor som är kopplade till leverantörsposten för underavtalet. Leverantörskontot har relationstypen **Leverantör** eller **Leverantör**.

2. Projektledaren kan specificera alla inköp som radobjekt i underavtalet. Underavtalsrader kan vara för tid, utgifter eller produkter. Underavtalsradens transaktionsklass avgör vad raden avser.

3. Leverantörskontoansvarig och projektledaren kan iterera över underavtalet. Prissättningen kan justeras i inköpsprislistor som är kopplade till underavtalet.

4. Om underavtalsraden avser tid kommer leverantörskontoansvarig vid denna tidpunkt eller senare i processen att associera leverantörskontakter med respektive underavtalsrad. Den här associationen ger information till den projektledare som arbetar med underavtalet. När en leverantörskontakt associeras med en underavtalsrad skapar systemet automatiskt en bokningsbar resurs från kontakten (om en bokningsbar resurs inte redan finns).

5. Faktureringsmetoden för varje underavtalsrad kan vara **Fast pris** eller **Tid och material**. För underavtalsrader med fast pris skapas ett milstolpebaserat fakturaschema.

De återstående steg i affärsprocessflöden för underavtal som beskrivs i översikten är för närvarande inte tillgängliga. När nya funktioner läggs till uppdateras detta ämne. 

I följande illustration visas lanseringen av tidig åtkomst för underavtal, i jämförelse med den kompletta affärsprocessen ("end to end").

![Processflöde för underavtalering](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Kvantitetsbaserade och arbetsbaserade underavtalsrader för tidig åtkomst
I den tidiga åtkomst utgåvan för oktober 2021 stöds endast kvantitetsbaserade underavtalsrader. Det betyder att en underavtalsrad kan användas för att köpa tid, utgifter eller material från en leverantör men inte ett fullständigt arbete. Det innebär också att den kvantitet som köps (enheter bestående av tid, utgifter eller kvantiteter av material) på en underavtalsrad kan användas för alla projekt i systemet.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
