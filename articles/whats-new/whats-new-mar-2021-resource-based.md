---
title: Nyheter i mars 2021 – Project Operations för resurs-/icke-lagerbaserade scenarier
description: Denna artikel innehåller information om kvalitetsuppdateringarna som är tillgängliga i mars 2021-versionen av Project Operations för resurs-/icke-lagerbaserade scenarier.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e93b4eaad98267f163bad4aff3e4fdcc661e2ab0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028436"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i mars 2021 – Project Operations för resurs-/icke-lagerbaserade scenarier

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Denna artikel gäller följande Dynamics 365 Project Operations komponenter och versioner:

- Project Operations i Dataverse-miljöversion 4.8.0.91 
- Projekthantering och redovisning i Dynamics 365 Finance-miljö, version 10.0.16 

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse


| **Funktionsområde** | **Referensnummer** | **Kvalitetsuppdatering** |
| --- | --- | --- |
| Fakturering och prissättning | 2133873 | Åtgärdad visning av valutasymbolen **Enhetens försäljningspris** i rutnätet **Utgiftsberäkningar**. |
| Fakturering och prissättning | 2174616 | När en offert har vunnits refereras den anpassade kontraktprislistan till kontraktradsinformation som kopieras från offerten. |
| Administrering av affärsmöjligheter | 2167475 | Fast momsbelopp i korrigeringsfakturan som ursprungligen kom från en icke fakturerad faktisk post. |
| Administrering av affärsmöjligheter | 2176285 | Momsbelopp får inte kopieras från information om försäljningskontrakt/offertrad till information om kostnadskontrakt/offertrad. |
| Administrering av affärsmöjligheter | 2188079 | Regel för delad fakturering får inte skapas för kontrakt som inte är arbetsbaserade. |
| Planering och spårning | 2125274 | Attributet **Dubbelskrivning till karta för projekt** för **Mappning av projektets startdatum** uppdaterats från **msdyn\_taskearlieststart** till **msdyn\_actualstart**. |
| Planering och spårning | 2138853 | Projektkopieringsfunktionen har uppdaterats för att säkerställa att utläggsberäkningsrader som referensuppgifter kopieras till målprojektet. |
| Planering och spårning | 2154306 | Åtgärdade problem med att ta bort kostnader i Project Operations för resursbaserade scenarier. |
| Planering och spårning | 2173259 | Funktionen projektkopiering har uppdaterats så att felmeddelandet **Kopierar WBS** visas i vissa situationer. |
| Tid och utgift | 2148910 | Åtgärdade visningsproblem med sidan **Redigera post** i rutnätet **Tidspost**. |
| Tid och utgift | 2159798 | Försedd med kontroller som säkerställer att godkända utgiftsposter inte kan redigeras. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektledning och redovisning i Dynamics 365 Finance

För mer information, se [Nyheter i januari 2021 - Project Operations för resurs-/icke-lagerbaserade scenarier](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Regleringsuppdateringar

Information om regeluppdateringar för appar för ekonomi och drift finns i [Regeluppdateringar](/dynamics365/finance/localizations/regulatory-updates). Ett annat sätt att lära sig om regelverksrelaterade uppdateringar är att logga in på LCS och visa de planerade regeluppdateringarna med hjälp av verktyget för problemsökning. Med problemsökning kan du söka efter land, typ av funktion och utgåva.


[!INCLUDE[footer-include](../includes/footer-banner.md)]