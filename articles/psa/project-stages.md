---
title: Typer av projektstadier
description: I det här ämnet finns information om projektstadier.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: aa423979a794b07a8bd27440f47a29480b74b518
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123084"
---
# <a name="project-stage-types"></a>Typer av projektstadier 

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