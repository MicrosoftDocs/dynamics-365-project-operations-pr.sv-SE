---
title: Konfigurera underleverantörer som bokningsbara resurser
description: I det här ämnet beskrivs hur du konfigurerar och upprätthåller underleverantörsresurser som skapas från användare och kontaktpersoner i systemet, så att de kan associeras med underavtal i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6d2f250063afc24de99e308d8d7583d1822bcabb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597268"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Konfigurera underleverantörer som bokningsbara resurser

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Följ anvisningarna nedan för att konfigurera underleverantörer som bokningsbara resurser i Microsoft Dynamics 365 Project Operations.

1. Gå till **Projekt** \> **Resurser** och välj **Ny**.
2. Välj ett av följande alternativ i fältet **Resurstyp** på sidan **Ny bokningsbar resurs**:

    - **Användare** – Välj den här resurstypen om underleverantörerna måste ha åtkomst till Project Operations för att ange tid eller utgifter. Om du väljer **Användare** måste underleverantörerna ha en giltig licens för att få åtkomst till systemet.
    - **Kontakt** eller **Konto** – Välj en av dessa resurstyper om underleverantörer inte behöver ha tillgång till Project Operations, men måste vara tillgängliga för tilldelningar av uppgifter eller för bokningar i projekt. Ingen av dessa resurstyper ger åtkomst till systemet. Välj **Konto** om du vill representera leverantörens företag som en bokningsbar resurs. Välj **Kontakt** för att representera de enskilda anställda hos leverantören.

3. Beroende på vilken resurstyp du valt uppmanas du att välja motsvarande användar-, konto- eller kontaktpost.
4. Välj "Kontraktarbetare" i fältet **Typ av arbetare** om du vill konfigurera underleverantören som en bokningsbar resurs.

    > [!NOTE]
    > Om du lämnar fältet **Typ av arbetare** tomt betraktas den bokningsbara resursen som en anställd.

5. Om du valde **Kontraktarbetare** som typ av arbetare väljer du den leverantör resursen arbetar för.
6. Välj resursens tidszon och välj sedan **Spara**. Om du vill tilldela en arbetstimmarsmall till en bokningsbar resurs kan du välja **Ange kalender** på listsidan **Bokningsbar resurs**.

För att associeras med en underavtalsrad måste en bokningsbar resurs uppfylla följande villkor:

- Den bokningsbara resursen måste vara en kontraktarbetare.
- En bokningsbar resurs med resurstypen **Kontakt** måste associeras med leverantörskontot som en kontakt. En bokningsbar resurs med resurstypen **Användare** behöver inte associeras med leverantörskontot som en kontakt.
- Värdet för fältet **Leverantör** för den bokningsbara resursen måste matcha värdet för fältet **Leverantör** för underavtalet.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Uppdatera typen av arbetar- och leverantörsmappning för bokningsbara resurser

Fältet **Typ av arbetare** för en bokningsbar resurs avgör om den bokningsbara resursen är en kontraktarbetare eller en anställd. I fältet **Leverantör** definieras leverantörskontot som den bokningsbara resursen är associerad med. Genom att associera en bokningsbar resurs med en leverantör som en kontakt anger du att kontakten är en anställd på leverantörsföretaget.

Om fälten **Typ av arbetare** och **Leverantör** för en bokningsbar resurs ändras påverkar ändringarna eventuella framtida valideringar för nya poster som skapas av den bokningsbara resursen, till exempel tidsposter. Men ändringarna gör inte befintliga poster ogiltiga.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
