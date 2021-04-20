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
ms.openlocfilehash: 65d05e3a6321dc32aee55c28b3eaa4bd0bae2f86
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858000"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurera redovisning för interna projekt

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Med interna projekt kan företag spåra kostnader som är relaterade till aktiviteter som inte debiteras en kund. Exempel på interna projekt är:

- Utveckla en produkt, t.ex. en mobilapp, och spåra kostnaden för utvecklingen.
- Hantera tid och utgifter före köpet. Det här interna projektet före försäljning kan konverteras till ett fakturerbart projekt om offerten vinns.

Ett projekt som inte är associerat med ett kontrakt i Dynamics 365 Project Operations behandlas som internt. Projektkostnad och intäktsprofiler används inte för att bestämma redovisningsreglerna för projektet. Intern projektkostnad bokförs alltid med vinst och förlust-principer. Redovisningskonton för bokföringar definieras på sidan **Bokföringsinställningar för transaktionsregister**.

- Tidstransaktioner bokförs genom att debitera kontot **Kostnad** och kreditera kontot **Löneallokering**.
- Utgiftstransaktioner bokförs genom att debitera kontot **Kostnad** och kreditera **motkonto för utgift**.
- Artikeltransaktioner bokförs genom att debitera kontot **Kostnad** och kreditera kontot **Kostnad - artikel**.

När transaktioner har bokförts i projektet, om projektet är associerat med ett projektkontrakt, kommer systemet att återföra alla ackumulerade transaktioner och skapa nya fakturerbara transaktioner. De fakturerbara transaktionerna följer redovisningsreglerna som har definierats i respektive projektkostnads- och intäktsprofil.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
