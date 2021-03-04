---
title: Vanliga frågor om resurshantering
description: Det här ämnet innehåller svar på vanliga frågor om resurshantering.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d335a12a9b478bff63b6c93809c89dac9718a4be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144390"
---
# <a name="resource-management-faq"></a>Vanliga frågor om resurshantering

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Vad är det för skillnad på en teammedlem och ett resurskrav?

En projektteammedlem kan tilldelas uppgifter, bokas eller överbokas och ställas in som godkännare. Ett resurskrav kan existera utan en projektteammedlem som ett utkast till efterfrågan. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Vad är det för skillnad på föreslagna och preliminärbokade timmar?

Föreslagna timmar och preliminärbokade timmar skiljer sig åt i synbarheten. Föreslagna timmar visas endast för resursansvariga och projektledare som initierat behovet genom att använda en resursbegäran. De preliminärbokade timmarna är synliga för alla som har till gång till schemaläggningstavlan.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Hur kan jag visa de preliminärbokade timmarna för resurser i ett team?

Preliminärbokningar kan göras när du bokar ett resurskrav. Resurser som är preliminärbokade i ett projektteam visas som teammedlemmar med preliminärbokade timmar. De visas också på schemaläggningstavlan.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Hur ändrar jag de begärda timmarna och start- och slutdatumen för en resurs (generiskt eller namngivet) som jag bokade?

När du har bokat resurser väljer du **Underhåll bokningar** för att göra nödvändiga ändringar.

## <a name="what-resources-types-does-project-service-automation-support"></a>Vilka resurstyper stöder Project Service Automation?

**Användare** och **kontakt** är de enda resurstyper som stöds i Dynamics 365 Project Service Automation. Du kan skapa andra typer av resurser (t.ex. **utrustning** och **grupp**), men det finns inget fullständigt användningsfall som stöds för dem.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Vad är det för skillnad på en tilldelning och en bokning?

Tilldelningar är tilldelningen av resurser till projektuppgifter i projektschemat. Resurserna kan antingen vara riktiga eller generiska resurser. Bokningar är en fast eller preliminär allokering av resurser till ett projekt. Fasta bokningar förbrukar en resurs kapacitet. För verkliga resurser bör bokningarna och tilldelningarna godkännas eftersom de inte skiljer sig åt. PSA tvingar emellertid inte detta avtal. I vyn avstämning visas en projektledare där resursens bokningar och tilldelningar inte godkänner varandra.
