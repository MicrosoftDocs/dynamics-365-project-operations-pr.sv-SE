---
title: Projektstadier
description: Den här artikeln ger information om projektstadierna som är tillgängliga i Microsoft Dynamics Project Operations.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b146174583fdea45481b87375158ebe83ed63418
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911158"
---
# <a name="project-stages"></a>Projektstadier

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Projektstadier designas för att återspegla projektets status allt eftersom det fortlöper. Anpassningar kan användas för att automatiskt uppdatera stadier i flöden för affärsprocesser, Power Automate eller tillägg för plugin-program.

Följande stadier definieras i standardvärdet för affärsprocessflöde:

- Skapa
- Offert
- Planera
- Leverera
- Slutför
- Stängning 

## <a name="new"></a>Skapa

När du skapar ett projekt anges projektstadiet till **Nytt**. Om projektet skapades från en mall kan det finnas schema-, uppskattnings- och teamdata. I annat fall är det en disposition av projektet och resterande komponenter måste anges.

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