---
title: Typer av projektstadier
description: I det här ämnet finns information om projektstadier.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 7f893b5429dd61ae45ad9d536420c96b2f58605b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586872"
---
# <a name="project-stage-types"></a>Typer av projektstadier 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektstadier designas för att återspegla projektets status allt eftersom det fortlöper. Anpassningar kan användas för att automatiskt uppdatera stadier i flöden för affärsprocesser, Power Automate eller tillägg för plugin-program.

Följande stadier definieras i standardvärdet för BPF:

- Skapa
- Offert
- Planera
- Leverera
- Slutför
- Stäng 

## <a name="new"></a>Nytt

När du skapar ett projekt anges projektstadiet till **Nytt**. Om projektet skapades från en mall kan det finnas schema-, uppskattnings- och teamdata. I annat fall är det bara en disposition av projektet och resterande komponenter måste anges.

## <a name="quote"></a>Offert

När du associerar ett projekt med en offert eller när du skapar det från ett projekt från offert, anges projektstadiet som **Offert**, och de uppskattade start- och slutdatumen uppdateras. När projektet är i stadiet **Offert** visas information om offerten på fliken **Försäljning** fliken på sidan **Projektentitet**.

## <a name="plan"></a>Planera

När du vinner en offert som är associerad med ett projekt och projekt flyttas till fasen **Kontrakt** uppdateras projektfasen till **Planera**. När projektet är i stadiet **Planera** visas information om kontraktet på fliken **Projektentitet**.

## <a name="deliver"></a>Leverera

När projektplanen är klar och du är redo att starta projektet ska projektledaren uppdatera projektfasen till **Leverera** för att visar att projektet har påbörjats.

## <a name="complete"></a>Slutför 

När arbetet för projektet har slutförts kan projektledaren uppdatera fasen till att **slutföras**. Om du uppdaterar projektfasen till **Slutföra** anger projektledaren att arbetet är 100 procent klart, men att projektet hålls öppet så att väntande tid- eller utgiftsposter kan registreras.

## <a name="close"></a>Stäng

När alla transaktioner har registreras kan projektledaren uppdatera fasen till att **Stäng**. Vid den tidpunkten kan inga transaktioner registreras och projektet får värdet skrivskyddat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
