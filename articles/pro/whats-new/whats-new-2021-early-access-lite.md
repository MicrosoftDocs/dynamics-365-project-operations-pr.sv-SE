---
title: Nyheter i tidig åtkomst för 2021 års lanseringsvåg 2 – Project Operations lite-distribution
description: Detta ämne innehåller information om de funktioner som är tillgängliga i den tidiga åtkomstversionen för 2021 års lanseringsvåg 2 för Project Operations Lite-distribution.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a201e3e4333b8892eea72387222d64e18b74d71b
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323933"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Nyheter i tidig åtkomst för 2021 års lanseringsvåg 2 – Project Operations lite-distribution

_Gäller: Lite-distribution – avtal till proforma-fakturering_

Detta ämne gäller för följande Dynamics 365 Project Operations-komponenter och -versioner:

  - Project Operations i Dataverse-miljöversion 4.23.0.4

Utgåvan tillämpas endast om en miljö har [anmälts för tidig åtkomst](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

[Underleverantörshantering](../subcontracting/subcontracting_EA_scope.md) – Denna funktion ger bättre synlighet och kontroll över samtliga aspekter av arbetet med ett projekt. I förhandsgranskningen av underleverantörshanteringen ingår följande funktioner:

  - En projektledare kan skapa ett underavtal med en leverantör. Som standard används de prislistor som är kopplade till leverantörsposten för underavtalet. Leverantörskontot har relationstypen **Leverantör** eller **Leverantör**.
  - En projektledare kan specificera samtliga inköp som radobjekt i underavtalet. Underavtalsrader kan vara för tid, utgifter eller produkter. Underavtalsradens transaktionsklass avgör vad raden avser.
  - Leverantörskontoansvarig och projektledaren kan iterera över underavtalet. Prissättningen kan justeras i inköpsprislistor som är kopplade till underavtalet.
  - Under själva kan leverantörskontoansvarig – om underavtalsraden avser tid – associera leverantörskontakterna med respektive underavtalsrad. Den här associationen ger information till den projektledare som arbetar med underavtalet. När en leverantörskontakt associeras med en underavtalsrad skapar systemet automatiskt en bokningsbar resurs från kontakten (om en bokningsbar resurs inte redan finns).
  - Faktureringsmetoden för respektive underavtalsrad kan ha ett fast pris eller tid och material. För underavtalsrader med fast pris skapas ett milstolpebaserat fakturaschema.
