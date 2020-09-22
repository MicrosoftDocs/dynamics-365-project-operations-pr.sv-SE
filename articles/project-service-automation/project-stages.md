---
title: Projektstadier
description: I det här ämnet finns information om projektstadier.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3756190"
---
# <a name="project-stages"></a>Projektstadier 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektstadier uppdateras för att återspegla projektets status allt eftersom det fortlöper. Standardaffärsprocessflödet uppdaterar automatiskt vissa stadier i projekt, medan andra uppdateras manuellt av projektledaren. 

Följande stadier definieras i standardvärdet för BPF:

- Nytt
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
