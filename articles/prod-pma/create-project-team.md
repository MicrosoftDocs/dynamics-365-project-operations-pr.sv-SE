---
title: Skapa ett projektteam
description: I det här ämnet finns information om hur du skapar och hanterar projektteam.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7eb9101352afd27b527bf6b8acc6f92198f44ea
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085705"
---
# <a name="create-a-project-team"></a>Skapa ett projektteam

[!include [banner](../includes/banner.md)]

För att du ska kunna använda rollerna som har ställts in tidigare i ett projekt måste en projektledare associera rollerna med projektet. Flera roller kan tilldelas för ett projekt. För att undvika förvirring märks rollerna automatiskt under reservation. Om projektledaren t.ex. kräver tre programmerare är det tre programmerare som har **programmerare 1** , **programmerare 2** och **programmerare 3** när deras etiketter genereras automatiskt. Om rollegenskaperna tidigare har angetts för rollen används de som ett filter vid sökning efter en resurs. Ytterligare kännetecken kan läggas till som krävs för att sökningen ska kunna förfinas ytterligare.

Vyinställningar kan också anpassas så att du får en bättre bild av resurstillgängligheten. Det finns alternativ för att visa tim-, dygns-, vecko-, månads-, kvartals- och årstillgänglighet. Det finns även ett alternativ för att visa tillgänglig och återstående kapacitet för resurser. Det här alternativet är användbart vid tidshantering när du uppskattar tillgänglig tid för aktiviteter eller resurstillgänglighet.

Projektledaren kan välja en roll på sidan och om det finns en tillgänglig resurs som passar för kravet väljer du om du vill reservera en resurs som ska fylla rollen. Observera att resurserna inte behöver reserveras vid den här tidpunkten i planeringsfasen. När du skapar en struktur kan du ersätta roller med personalresurser för projektet. Om roller ersätts med personalresurser i WBS uppdateras projektets teamlista och schemaläggning automatiskt i resursinställningarna.

[![Projektteamlistor som innehåller både roller och faktiska resurser](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektledaren har olika alternativ för att boka en resurs för ett projekt, till exempel **återstående kapacitet** , **full kapacitet** , **kapacitetsprocent** och **ange timmar**. De här bokningsalternativen kan när som helst annulleras om resurstilldelningar ändras. Två typer av bokningar stöds:

- **Fast bokning** – resursreservationen har godkänts och bekräftats för att arbeta med åtagandet för den angivna varaktigheten.
- **Mjuk bokning** – resursreservationerna har godkänts och preliminärt angetts till att arbeta med åtagandet för den angivna varaktigheten.

Följande procedur förklarar hur du skapar ett projektteam.

## <a name="create-a-project-team"></a>Skapa ett projektteam

1. På listsidan **Alla projekt** välj ett projekt och välj sedan **Redigera**.
2. På fliken **Projektteam och schemaläggning** i fältet **Schemalägg slutdatum** ange startdatum för schemaläggning plus en månad. Om exempelvis schemats startdatum är 24 juni 2017 (24/06/2017) anger du **24/07/2017**.
3. Markera **Lägg till**.
4. I fältet **Lägg till roller i projekt** i fältet **Roll** väljer du **chefsprojektledare**.
5. Välj **nödvändig kompetens**.
6. På sidan **Välj egenskaper** är de egenskaper som du tidigare angett för rollen chefsprojektledare markerad som standard. Välj **OK**.
7. På sidan **Lägg till roller i projekt** i fältet **Antal resurser** ange **1**.
8. I fältet **resurs** visas alla resurser som har nödvändig kompetens i sökningen. Välj **Daniel Goldschmidt** och välj sedan **Skapa**.
9. På sidan **Projekt** välj **Lägg till**.
10. I fältet **Lägg till roller i projekt** i fältet **Roll** väljer du **teammedlem**. Ange **5** i fältet **Antal resurser**.
11. Välj **Skapa**.
12. På sidan **projekt** väljer du **uppfylla resurser**.

## <a name="monitor-project-teams"></a>Övervaka projektteam
1. På sidan **All projekt** välj länken **projekt-ID** för projekt **XYZ uppgradering fas 2**.
2. Snabbflik **Projektgrupp och schemaläggning** , verifiera att de projektresurser som anges är korrekta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]