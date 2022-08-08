---
title: Nyheter i februari 2021 – Project Operations för resurs-/icke-lagerbaserade scenarier
description: Denna artikel innehåller information om kvalitetsuppdateringarna som är tillgängliga i februari 2021-versionen av Project Operations för resurs-/icke-lagerbaserade scenarier.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1fe1e59a0a3674752fe62525349a50f00e11089b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029644"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i februari 2021 – Project Operations för resurs-/icke-lagerbaserade scenarier

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Denna artikel gäller följande Dynamics 365 Project Operations komponenter och versioner:

- Project Operations i Dataverse-miljö 4.7.0.95
- Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.16 

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| **Funktionsområde** | **Referensnummer** | **Kvalitetsuppdatering** |
| --- | --- | --- |
| **Fakturering och prissättning** | 2053736 | Fakturaraddetaljer är nu åtkomliga genom att gå till **Faktura** > **Relaterad information**. |
| **Fakturering och prissättning** | 2122613 | Åtgärderna **Aktivera** och **Inaktivera** togs bort från associationsentiteterna för **Prislista**. |
| **Fakturering och prissättning** | 2128606 | Löste problemet med **ullReferenceException** i plugin-programmet **GetEstimatesForProject**. |
| **Distribution och konfiguration** | 2139346 | Löste problemet med import av icke-hanterad **Dynamics365ProjectOperationsDualWrite**-lösning. |
| **Distribution och konfiguration** | 2140569 | Projektlösningen för får inte installeras i Teams-miljön för Dataverse. |
| **Distribution och konfiguration** | 2086991 | Begränsad anpassning av lokalisering av webbresurser. |
| **Administrering av affärsmöjligheter** | 2136794 | Visa rätt felmeddelande när processerna **Bekräfta faktura** eller **Markera fakturan som betalda** misslyckas. |
| **Administrering av affärsmöjligheter** | 2139330 | Ett byte av projektledaren för ett projekt får inte återställa det ägande företaget tillbaka till standardvärdet. |
| **Administrering av affärsmöjligheter** | 2146376 | Korrigerade skattebelopp i en faktisk icke-debiterbar skapas från fakturabekräftelse. |
| **Projektplanering och spårning** | 2099879 | Dataverse-miljödistributionen måste skapa en standardtransaktionskategori med ett statiskt ID och inte slumpmässigt generera en per miljö. |
| **Projektplanering och spårning** | 2128577 | Åtgärdade användarbehörigheten för Project Service för att uppdatera transaktionskategorin för en resurstilldelning. |
| **Projektplanering och spårning** | 2164035 | Åtgärdade problem med funktionen **Kopiera projekt**. |
| **Tidspost** | 2129161 | Hårdare begränsningar tillämpas för att säkerställa att användarna inte kan ändra och uppdatera en tidspost som har skickats eller godkänts. |
| **Tidspost** | 2103572 | Tidsgodkännande för icke-projekttidsposter får inte söka rollen som projektgodkännare. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektledning och redovisning i Dynamics 365 Finance 

Mer information om projekthantering och redovisning i Dynamics 365 Finance finns i [Nyheter i januari 2021 – Project Operations för resurs-/icke-lagerbaserade scenarier](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Regleringsuppdateringar

Information om regeluppdateringar för appar för ekonomi och drift finns i [Regeluppdateringar](/dynamics365/finance/localizations/regulatory-updates). Ett annat sätt att lära sig om regelverksrelaterade uppdateringar är att logga in på Lifecycle Services (LCS) och visa de planerade regeluppdateringarna med hjälp av verktyget för problemsökning. Med problemsökning kan du söka efter land, typ av funktion och utgåva.


[!INCLUDE[footer-include](../includes/footer-banner.md)]