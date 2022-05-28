---
title: Varför kan jag inte ta bort poster från entiteten Faktiska värden?
description: I det här ämnet finns information om varför det inte går att ta bort poster från entiteten verkliga värden.
author: JPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
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
ms.openlocfilehash: ff2c951905324d5d05722f399057c03d22f1a1c9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584434"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Varför kan jag inte ta bort poster från entiteten Faktiska värden?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Med Project Service Automation (PSA) kan du inte ta bort faktiska värden eftersom de fungerar som källa till sanningen för transaktioner som har ekonomiska effekter för underordnade system, t.ex. redovisningen. Om verkliga värden kan tas bort kan det krävas att den ekonomiska rapporttransaktionens integritet ifrågasätts. För att kunna upprätta en granskningskedja bör kunderna använda journaler för att skapa kompensationstransaktioner.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
