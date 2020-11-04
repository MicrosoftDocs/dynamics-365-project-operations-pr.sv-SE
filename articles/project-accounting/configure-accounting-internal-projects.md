---
title: Konfigurera redovisning för interna projekt
description: I det här ämnet finns information om hur du konfigurerar redovisningspraxis för interna projekt i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085474"
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


