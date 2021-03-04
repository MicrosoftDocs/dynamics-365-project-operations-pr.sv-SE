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
ms.openlocfilehash: ea04178d4327ccd701ab431f172463a13a55154e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132400"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurera redovisning för interna projekt

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Med interna projekt kan företag spåra kostnader som är relaterade till aktiviteter som inte debiteras en kund. Exempel på interna projekt är:

- Utveckla en produkt, t.ex. en mobilapp, och spåra kostnaden för utvecklingen.
- Hantera tid och utgifter före köpet. Det här interna projektet före försäljning kan konverteras till ett fakturerbart projekt om offerten vinns.

Alla projekt som inte är associerade med ett kontrakt i Dynamics 365 Project Operations behandlas som interna. Projektkostnad och intäktsprofiler används inte för att bestämma redovisningsreglerna för projektet. Intern projektkostnad bokförs alltid med vinst och förlust-principer. Redovisningskonton för bokföringar definieras på sidan **Bokföringsinställningar för transaktionsregister**.

- Tidstransaktioner bokförs genom att debitera kontot **Kostnad** och kreditera kontot **Löneallokering**.
- Utgiftstransaktioner bokförs genom att debitera kontot **Kostnad** och kreditera **motkonto för utgift**.

När transaktioner har bokförts i projektet, om projektet är associerat med ett projektkontrakt, kommer systemet att återföra alla ackumulerade transaktioner och skapa nya fakturerbara transaktioner. De fakturerbara transaktionerna följer redovisningsreglerna som har definierats i respektive projektkostnads- och intäktsprofil.




[!INCLUDE[footer-include](../includes/footer-banner.md)]