---
title: Nyheter i februari 2021 – Project Operations för resursscenarier/icke-lagerbaserade scenarier
description: I det här ämnet finns information om de kvalitetsuppdateringar som är tillgängliga i utgåvan av Project Operations för februari 2021 för resursscenarier/icke-lagerbaserade scenarier.
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 12708a9b847f1f87ee0f5f45688adf48638d709f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291911"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i februari 2021 – Project Operations för resursscenarier/icke-lagerbaserade scenarier

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Detta ämne gäller för följande Dynamics 365 Project Operations-komponenter och -versioner:

- Project Operations i Dataverse-miljö 4.7.0.95
- Projektledning och redovisning i Dynamics 365 Finance-miljö version 10.0.16 

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

Mer information om projektledning och redovisning i Dynamics 365 Finance finns i [Nyheter i januari 2021 – Project Operations för resurs-/icke lagerbaserade scenarier](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Regleringsuppdateringar

Mer information om regleringsuppdateringar för Finance and Operations-appar finns i [regleringsuppdateringar](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Ett annat sätt att lära sig om regelverksrelaterade uppdateringar är att logga in på Lifecycle Services (LCS) och visa de planerade regeluppdateringarna med hjälp av verktyget för problemsökning. Med problemsökning kan du söka efter land, typ av funktion och utgåva.


[!INCLUDE[footer-include](../includes/footer-banner.md)]