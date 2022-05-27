---
title: Bemanna ett projekt med kapacitet för kontraktpersonal och underleverantörer
description: I det här ämnet beskrivs hur projektkraven kan bemannas med kontraktpersonal eller underleverantörskapacitet i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a0efea80484dfca0a9dae8404837c3376dfecaed
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574664"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Bemanna ett projekt med kapacitet för kontraktpersonal och underleverantörer

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Allmänna projektteammedlemmar kan vara bemannade med anställda eller kontraktarbetare. När du bemannar ett projekt med kontraktarbetare kan du begränsa personalalternativen till vissa kontraktarbetare som är tilldelade till en underleverantörsrad. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Sök efter resurskrav för personal med kontraktarbetare som hör till en viss underleverantörsrad

Sök efter resurskrav för personal med kontraktarbetare som hör till en viss underleverantörsrad genom att ta följande steg:

1. Skapa en generisk projektteammedlem som refererar till en underleverantör och underleverantörsrad.
2. Generera ett resurskrav för den här generiska projektteammedlemmen med knappen **Generera krav** i underrutnätet för projektteammedlemmar.
3. Markera teammedlemsraden och välj knappen **Boka** i underrutnätet. 
4. Då öppnas schemaläggningstavlan med kravsammanhang. Tillsammans med andra attribut, t.ex. datum, roll och fält för organisationsenheter, fylls filtren i schemaläggningstavlan i automatiskt med fälten leverantör, underleverantör och underleverantörsrad från resurskraven.
5. Systemet söker efter resurser som uppfyller filtervillkoren och listar dem. 
6. Välj en av de filtrerade resurserna och boka resursen för kravet. 
7. En projektteammedlem skapas och uppdateras med referenser till en underleverantör och underleverantörsrad. Gå till **Projektuppskattningar** och välj **Uppdatera priser** för att se den uppdaterade kostnaden för resurstilldelningen. 

> [!NOTE]
> Det är inte alltid möjligt att uppdatera projektteammedlemmen med en referens till underleverantör och en underleverantörsrad under bokningen om resursen har tilldelats flera underleverantörsrader. Om systemet inte kan uppdatera projektteammedlemmen med en underleverantör och underleverantörsrad, öppnar du posten för projektteammedlemmen och uppdaterar fälten manuellt så att kostnadsberäkningen återspeglar underleverantörers kostnad.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Sök efter resurskrav vad gäller personal med en kontraktarbetare

Sök efter resurskrav vad gäller personal med en kontraktarbetare genom att ta följande steg:

1. Skapa en generisk projektteammedlem.
2. Generera ett resurskrav för den här generiska projektteammedlemmen med knappen **Generera krav** i underrutnätet för projektteammedlemmar.
3. Markera teammedlemsraden och välj knappen **Boka** i underrutnätet. 
4. Då öppnas schemaläggningstavlan med kravsammanhang. Tillsammans med andra attribut, t.ex. datum, roll och fält för organisationsenheter, fylls filtren i schemaläggningstavlan i automatiskt med fälten leverantör, underleverantör och underleverantörsrad från resurskraven. Eftersom det inte finns några ifyllda värden för underleverantör eller underleverantörsrad kommer dessa attribut att vara tomma i filterrutan.
5. Systemet söker efter resurser som uppfyller filtervillkoren och listar dem.
6. Uppdatera fältet **Arbetartyp** i filterfönstret till **Kontraktarbetare** för att begränsa sökningen till kontraktarbetare. Uppdatera **Leverantör** i filterfönstret för att välja en leverantör och begränsa sökningen så att den endast visar kontraktarbetare som tillhör ett specifikt leverantörsföretag.
7. Välj en kontraktarbetare i listan och boka resursen för kravet.
8. En projektteammedlem skapas. Projektteammedlemmen uppdateras emellertid inte med någon underleverantör eller underleverantörsrad och resurstilldelningen kommer därför inte att kostnadsföras med hjälp av underleverantörspriset. Uppdatera projektteamsmedlemmen manuellt med en underleverantörsrad och gå till **Projektuppskattningar** och välj **Uppdatera priser** för att se den uppdaterade kostnaden för resurstilldelningen.

> [!NOTE]
> Projektteammedlemmar som har **Arbetstyp** inställd på **Kontraktarbetare** men som inte har en underleverantörsreferens flaggas som **Ogiltiga** i rutnätet **Projektteammedlemmar**. Om det finns projektteammedlemmar med den här statusen öppnar du posten för projektteammedlemmen och uppdaterar fälten för underleverantör och underleverantörsrad manuellt så att kostnadsberäkningen återspeglar underleverantörers kostnad på fliken **Uppskattningar**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
