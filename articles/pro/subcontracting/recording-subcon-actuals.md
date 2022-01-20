---
title: Registrera tid, utgifter och materialanvändning för underleverantörskomponenter
description: I det här ämnet förklaras hur tid, utgifter och materialanvändning som registrerats för projekt från underleverantörskomponenter spåras av Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 04c78dd48367c3720b8f5ad5d924ed106da6a128
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903540"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Registrera tid, utgifter och materialanvändning i projekt för underleverantörskomponenter

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

I det här ämnet förklaras hur tid, utgifter och materialanvändning som registrerats för projekt från underleverantörskomponenter spåras av Microsoft Dynamics 365 Project Operations.

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