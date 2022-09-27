---
title: Registrera tid, utgifter och materialanvändning för underleverantörskomponenter
description: I den här artikeln förklaras hur tid, utgifter och materialanvändning som registrerats för projekt från underleverantörskomponenter spåras av Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522536"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Registrera tid, utgifter och materialanvändning i projekt för underleverantörskomponenter

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

I den här artikeln förklaras hur tid, utgifter och materialanvändning som registrerats för projekt från underleverantörskomponenter spåras av Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Kostnad för underleverantörers tid för projekt
I Project Operations kan kontraktanställda registrera tid för projekt på samma sätt som anställda. När en kontraktarbetare anger tid för projekt och/eller projektuppgifter kan han eller hon välja en viss underleverantör och underleverantörsrad.

När den tid som kontraktanställda har skickat in godkänns registreras projektkostnaden med hjälp av den enhetskostnad som har angetts för den kontraktarbetarresursen i avsnittet **Rollpriser** i inköpsprislistan i underleverantörskontraktet.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Kostnad för underleverantörers utgifter för projekt
När du anger utgifter för projekt kan du välja en underleverantör och en underleverantörsrad i utgiftsposten. 

När denna utgiftspost har skickats in och godkänts registreras utgiften i den projektbaserade enhetskostnad som har angetts för den transaktionskategorin i avsnittet **Kategoripriser** i inköpsprislistan i underleverantörskontraktet.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Kostnad för underleverantörers material för projekt
När du anger materialanvändning för projekt kan du välja en underleverantör och en underleverantörsrad i materialanvändningsloggen. När materialanvändningsloggen har skickats in och godkänts registreras materialkostnaden i den projektbaserade enhetskostnad som har angetts för den produkten i avsnittet **Prislisteposter** i prislistan i underleverantörskontraktet.

Materialanvändning kan även registreras för oregistrerade produkter i projekt. Den här typen av materialanvändning kan också länkas till en underleverantör och en underleverantörsrad. När du registrerar materialanvändning för produkter som inte finns i produktkatalogen måste du ange enhetskostnaden för den oregistrerade produkten. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
