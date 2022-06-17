---
title: Skapa en ny mall för arbetstid
description: Denna artikel beskriver hur du skapar en mall för arbetstimmar i Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8f3ac17a29e79f86f7c3ce127edb4b02ca63ea04
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916080"
---
# <a name="create-a-work-hours-template-project-service"></a>Skapa en mall för arbetstid (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

För att skapa och hantera ett projekt måste du använda en kalendermall för projektet. Kalendermallen definierar följande projektattribut:

- Arbetstider, inklusive start- och sluttid
- Arbetsdagar
- Kalenderundantag, som lediga dagar

Kalendermallen som används för ett projekt är en kopia av kalendermallen som har definierats i organisationens inställningar.

> [!NOTE]
> Om du ändrar kalendermallen överförs inte ändringarna till projektets arbetstider. För att ändra projektets arbetstider måste en ny mall användas.

Det finns två viktiga krav om du vill skapa en kalendermall för organisationen:

- Ange mallens önskade arbetstider med hjälp av en ny eller befintlig bokningsbar resurs.
- Skapa en ny kalendermall och associera mallen med den bokningsbara resursen.

**Definiera arbetstider i mallen**

1. Gå till **Resurser** \> **Resurser**.
2. Skapa en ny resurs att referera till i kalendermallen eller välj en befintlig resurs.
3. Välj resursens flik **Arbetstider** och följ instruktionerna i [Ange arbetstider för en resurs](/dynamics365/field-service/set-work-hours-resource) för att konfigurera kalenderreglerna.

**Skapa en ny kalendermall**

1. Gå till **Inställningar** \> **Kalendermall**.
2. Välj **Ny** och ange namn, beskrivning och mallresurs.


> [!NOTE]
> När en resurs refereras till i en kalendermall associeras en kopia av resursens kalender med kalendermallen. Om du ändrar arbetstider i den kopierade mallen överförs inte ändringarna till kalendermallen.


### <a name="see-also"></a>Se även  
 [Konfigurera resurser](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
