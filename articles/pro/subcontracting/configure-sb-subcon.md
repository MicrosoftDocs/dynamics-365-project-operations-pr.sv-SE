---
title: Konfigurera schemaläggningstavlan så att kapaciteten för kontraktarbetare och underleverantörer visas
description: Den här artikeln beskriver hur du konfigurerar schemaläggningstavlan i Microsoft Dynamics 365 Project Operations så att underkontrakterad resurskapacitet visas när du bemannar projektresurskraven.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262239"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurera schemaläggningstavlan så att kapaciteten för kontraktarbetare och underleverantörer visas 

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

Schemaläggningstavlan i Microsoft Dynamics 365 Project Operations kan användas för att söka efter resurser på två sätt:

- Allmän resurssökning utan att det finns några specifika projektbaserade resurskrav.
- Kravspecifik resurssökning där projektkraven ger sammanhang för de resurser som föreslås.

Om du vill meddela schemaläggningstavlan om underkontrakterad resurskapacitet och kontraktarbetare måste du göra uppdateringar av inställningarna för schemaläggningstavlan. Bland uppdateringarna finns: 
- Uppdatera inställningarna för schemaläggningstavlan för allmän resurssökning.
- Uppdatera inställningarna för schemaläggningstavlan för kravbaserad resurssökning.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Uppdatera inställningarna för schemaläggningstavlan för allmän resurssökning
### <a name="update-filters-for-general-resource-search"></a>Uppdatera filter för allmän resurssökning
När du söker efter en resurs bör de filter som finns tillgängliga på schemaläggningstavlan uppdateras så att du även kan söka efter externa resurser genom att ange något av eller allt av det följande:
  - Arbetartyp, om de resurser som visas ska vara kontraktarbetare eller anställda.
  - Leverantörsföretag som en resurs ska tillhöra.
  - Resurser som tillhör en viss underleverantör eller underleverantörsrad.
    
### <a name="update-retrieve-resource-query"></a>Uppdatera fråga för resurshämtning
Frågan som används för sökning bör också uppdateras så att dessa ytterligare filterattribut används. Uppdatera schemaläggningstavlans konfiguration för allmän resurssökning genom att följa stegen nedan:  
1. Öppna **Inställningar för schemaläggninstavlan** för en viss schemaläggningstavla.
2. Öppna fliken **Allmänna inställningar** och bläddra till **Andra inställningar**.
3. I listan över inställningar i det här avsnittet uppdaterar du **Filterlayout** till **Standardfilterlayout för Project Operations Lite**.
4. Uppdatera **Hämta resursfråga** till **Standardfråga för att hämta resurs för Project Operations Lite**.

![Uppdatera inställningarna för schemaläggningstavlan för allmän resurssökning](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Uppdatera inställningarna för schemaläggningstavlan för kravbaserad resurssökning
### <a name="update-filters-for-requirement-specific-resource-search"></a>Uppdatera filter för kravspecifik resurssökning 
När du söker efter en resurs bör de filter som finns tillgängliga på schemaläggningstavlan uppdateras så att du även kan söka efter externa resurser genom att ange något av eller allt av det följande:
 - Arbetartyp, om de resurser som visas ska vara kontraktarbetare eller anställda.
 - Leverantörsföretag som en resurs ska tillhöra.
 - Resurser som tillhör en viss underleverantör eller underleverantörsrad.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Uppdatera hämta resursfråga för kravspecifik resurssökning 
Frågan som används för sökning bör också uppdateras så att dessa ytterligare filterattribut används. Uppdatera schemaläggningstavlans konfiguration för kravspecifik resurssökning genom att följa stegen nedan:

1. Öppna **Inställningar för schemaläggningstavla** för en specifik schemaläggningstavla och välj sedan **Öppna standardinställningar** för att öppna inställningarna för kravspecifik sökning.
2. Öppna fliken **Allmänna inställningar** och bläddra till **Andra inställningar**.
3. I listan över inställningar i det här avsnittet uppdaterar du **Filterlayout** till **Standardfilterlayout för Project Operations Lite**.
4. Uppdatera **Hämta resursfråga** till **Standardfråga för att hämta resurs för Project Operations Lite**.
5. Öppna fliken **Schematyper** och gå till **Projekt**.
6. Under inställningarna för **Projekt**, uppdatera **Fråga för resurshämtning för schemaläggningsassistenten** till **Standardfråga för att hämta resurs för Project Operations Lite** och uppdatera **Fråga för begränsningshämtning för schemaläggningsassistenten** till **Standardfråga för att hämta begränsningar för Project Operations**.

![Uppdatera inställningarna för schemaläggningstavlan för kravbaserad resurssökning](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
