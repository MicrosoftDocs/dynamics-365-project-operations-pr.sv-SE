---
title: Säkerhetsmodul
description: I det här ämnet finns information om säkerhetsmodellen i Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: b01f3d88dd021895933bc863b762f019ae50eed6
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642925"
---
# <a name="security-model"></a>Säkerhetsmodell

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Project Operations innehåller en unik säkerhetsmodell som möjliggör en rollbaserad affärsmodell för verksamhetssäkerhet som samarbetar med Microsoft Office-grupper. 


## <a name="security-roles"></a>Säkerhetsroller
Klientdesfunktioner i Projet Operations innehåller följande roller:

| Roll                          | Beskrivning                                                                                                                                                                 | Omfång |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Metodansvarig              | Stöder rapportering mellan projekt.                                                                                                            | Affärsenhet              |
| Projektgodkännare              | Godkänner tid och utgifter mot ett projekt.                                                                                                                              | Affärsenhet |
| Debiteringsadministratör för projekt | Skapar fakturaförslaget.                                                                                                                                                 | Affärsenhet |
| Projektledare               | Skapar projektplanen och begär resurser.                                                                                                                              | Affärsenhet |
| Projektresurs              | Gruppmedlemmar som kan bokas och rapportera tid.                                                                                                          | Affärsenhet|
| Resurshanterare              | Alla resurshanteringsfunktioner, t.ex. uppfyllande av resursbegäranden och bokningar, avgränsade med stöd för en hybridkonfiguration av projektledare + resurshanterare och en enskild och centraliserad resurshanteringsroll. | Affärsenhet |


Microsoft Project for the Web innehåller följande roller:

| Roll           | Beskrivning                                                                                                        | Omfång  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Projektanvändare   | Samarbetande användare av Project som kan skapa sina egna projekt och visa projekt som delas med dem. | Användare   |
| Projektsystem | Roll som används för programsammanhang. Kunderna bör inte använda den här systemrollen.                                    | Global |

## <a name="security-enforcement"></a>Säkerhet
Åtgärder som utförs på projektnivå utförs i den inloggade användarens kontext. Det innebär att om du ska kunna skapa, öppna eller ta bort ett projekt måste användaren ha åtkomst tillgänglig i CDS. Åtkomst i CDS kan beviljas via alla tänkbara mekanismer som ingår i plattformen. En användare med större omfång kan till exempel komma åt projektet eller om en uttrycklig åtgärd för projektdelning har utförts som ger användaren åtkomst.

Det är viktigt att tänka på detta när du skapar projekt i Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Modernt gruppsamarbete med Project Operations
Project for the Web och Project Operations har stöd för moderna grupper för samarbete. Användare som har lagts till i projektet via en grupp kan redigera projektplanen.

Project for the Web lägger automatiskt till användare i gruppen vid tilldelning.

Med grupper kan projektets behörigheter och stödjande samarbetsartefakter arbetas på kollektivt. Följande diagram illustrerar de händelser och tillståndsändringar som inträffar under grupptilldelningsprocessen.

Project Operations innebär inte att en grupp skapas genom en implicit åtgärd och utförs endast med hjälp av en uttrycklig åtgärd av att trycka på grupper.

Sökning efter gruppmedlem i dialogrutan **Grupp hantering** är begränsad till dem som har angetts som en del av miljöns säkerhetsgrupp. Läs mer: [Styra användarnas åtkomst till miljöer: säkerhetsgrupper och licenser](https://docs.microsoft.com/power-platform/admin/control-user-access).

![Gruppläge](./media/groupsmode.png)

1. Projektet skapas och ägs av användaren som skapar.
2. Projektägaren uppdateras till teamet.
3. Ägarteamet är mappat till den angivna eller skapade Office-gruppen.
4. Projektets ursprungliga ägare läggs till i Office-gruppen.

## <a name="deployment-recommendation"></a>Distributionsrekommendation
När modellen för gruppsamarbete utvecklas för Office-grupper kommer funktionerna att läggas till för att ge mer detaljerad kontroll över tid. Kunder som distribuerar Project Operations i dag uppmuntras att fokusera på en traditionell Microsoft Dynamics 365-säkerhetsmodell.

Mer information finns i [Säkerhet i Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operations och Microsoft Dynamics 365 Finance-säkerhet
Project Operations omfattar följande roller:

- Projektledare
- Projektrevisor

Mer information om säkerhet i Finance finns i [Rollbaserad säkerhet](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


