---
title: Project Operations-integration med dubbelriktad skrivning
description: Ämnet innehåller en översikt över Project Operations-integration med dubbelriktad skrivning.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998703"
---
# <a name="project-operations-dual-write-integration-overview"></a>Översikt över Project Operations-integration med dubbelriktad skrivning

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Project Operations använder [funktioner för dubbelriktad skrivning](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) för att synkronisera data mellan Microsoft Dataverse och Dynamics 365 Finance.

Följande illustrerar hur data synkroniseras som en del av integrationen mellan Dataverse och Ekonomi.

![Översikt över Project Operations dataflöden](./media/ProjectOperationsFlows.jpg)

Project Operations i Dataverse har ett modernt användargränssnitt (UI) och är enkelt att utöka med lite eller ingen kod med hjälp av funktionerna i Power Platform. Projektansvariga, resursansvariga, projektteammedlemmar och andra personer på kontoret utför sina aktiviteter i Project Operations i Dataverse.

Project Operations i Ekonomi har stöd för projektredovisning och intäktsidentifiering. Project Operations ansluter till det ekonomiska ramverket i Ekonomi för momsberäkning, växelkurser, rapportering av ekonomiska mått med mera. Projektredovisaren är till största delen baserad i Ekonomi.

Project Operations-integration består av följande komponentintegration:


- [Inställning och konfiguration av Project Operations för dataintegration](resource-dual-write-setup-integration.md) 
- [Projektberäkningar och faktiska värden](resource-dual-write-estimates-actuals.md)
- [Projektfaktura](resource-dual-write-project-invoice.md)
- [Utgiftshantering](resource-dual-write-expense.md)
- [Leverantörsfaktura](resource-dual-write-vendor-invoice.md)
