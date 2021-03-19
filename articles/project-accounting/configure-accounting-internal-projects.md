---
title: Konfigurera redovisning för interna projekt
description: I det här ämnet finns information om hur du konfigurerar redovisningspraxis för interna projekt i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287620"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurera redovisning för interna projekt

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Med interna projekt kan företag spåra kostnader som är relaterade till aktiviteter som inte debiteras en kund. Exempel på interna projekt är:

- Utveckla en produkt, t.ex. en mobilapp, och spåra kostnaden för utvecklingen.
- Hantera tid och utgifter före köpet. Det här interna projektet före försäljning kan konverteras till ett fakturerbart projekt om offerten vinns.

Ett projekt som inte är associerat med ett kontrakt i Dynamics 365 Project Operations behandlas som internt. Projektkostnad och intäktsprofiler används inte för att bestämma redovisningsreglerna för projektet. Intern projektkostnad bokförs alltid med vinst och förlust-principer. Redovisningskonton för bokföringar definieras på sidan **Bokföringsinställningar för transaktionsregister**.

- Tidstransaktioner bokförs genom att debitera kontot **Kostnad** och kreditera kontot **Löneallokering**.
- Utgiftstransaktioner bokförs genom att debitera kontot **Kostnad** och kreditera **motkonto för utgift**.

När transaktioner har bokförts i projektet, om projektet är associerat med ett projektkontrakt, kommer systemet att återföra alla ackumulerade transaktioner och skapa nya fakturerbara transaktioner. De fakturerbara transaktionerna följer redovisningsreglerna som har definierats i respektive projektkostnads- och intäktsprofil.




[!INCLUDE[footer-include](../includes/footer-banner.md)]