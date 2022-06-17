---
title: Nyheter i tidig åtkomst för 2021 års lanseringsvåg 2 – Project Operations lite-distribution
description: Denna artikel innehåller information om funktionerna som är tillgängliga i utgivningscykel 2 för 2021 tidig åtkomst av Project Operations Lite för oktober 2021.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d245868c8bd9ff332707a81c074d6c7ae3649378
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924130"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Nyheter i tidig åtkomst för 2021 års lanseringsvåg 2 – Project Operations lite-distribution

_Gäller: Lite-distribution – avtal till proforma-fakturering_

Denna artikel gäller följande Dynamics 365 Project Operations komponenter och versioner:

  - Project Operations i Dataverse-miljöversion 4.23.0.4

Utgåvan tillämpas endast om en miljö har [anmälts för tidig åtkomst](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

[Underleverantörshantering](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview) – Denna funktion ger bättre synlighet och kontroll över samtliga aspekter av arbetet med ett projekt. I förhandsgranskningen av underleverantörshanteringen ingår följande funktioner:

  - En projektledare kan skapa ett underavtal med en leverantör. Som standard används de prislistor som är kopplade till leverantörsposten för underavtalet. Leverantörskontot har relationstypen **Leverantör** eller **Leverantör**.
  - En projektledare kan specificera samtliga inköp som radobjekt i underavtalet. Underavtalsrader kan vara för tid, utgifter eller produkter. Underavtalsradens transaktionsklass avgör vad raden avser.
  - Leverantörskontoansvarig och projektledaren kan iterera över underavtalet. Prissättningen kan justeras i inköpsprislistor som är kopplade till underavtalet.
  - Under själva kan leverantörskontoansvarig – om underavtalsraden avser tid – associera leverantörskontakterna med respektive underavtalsrad. Den här associationen ger information till den projektledare som arbetar med underavtalet. När en leverantörskontakt associeras med en underavtalsrad skapar systemet automatiskt en bokningsbar resurs från kontakten (om en bokningsbar resurs inte redan finns).
  - Faktureringsmetoden för respektive underavtalsrad kan ha ett fast pris eller tid och material. För underavtalsrader med fast pris skapas ett milstolpebaserat fakturaschema.
