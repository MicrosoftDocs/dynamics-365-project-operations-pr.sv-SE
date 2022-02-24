---
title: Skapa en ny mall för arbetstid
description: Ämnet beskriver hur du skapar en mall för arbetstid i Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981277"
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
3. Välj resursens flik **Arbetstider** och följ instruktionerna i [Ange arbetstider för en resurs](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) för att konfigurera kalenderreglerna.

**Skapa en ny kalendermall**

1. Gå till **Inställningar** \> **Kalendermall**.
2. Välj **Ny** och ange namn, beskrivning och mallresurs.


> [!NOTE]
> När en resurs refereras till i en kalendermall associeras en kopia av resursens kalender med kalendermallen. Om du ändrar arbetstider i den kopierade mallen överförs inte ändringarna till kalendermallen.


### <a name="see-also"></a>Se även  
 [Konfigurera resurser](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
