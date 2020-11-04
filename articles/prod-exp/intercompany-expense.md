---
title: Koncerninterna utgifter
description: En arbetare som är anställd av en juridisk person i en organisation kan utföra arbete för en annan juridisk person i samma organisation. I det här fallet kan du använda funktionen för koncernintern utgift för att tilldela arbetarens utgifter till den juridiska personen för vilken arbetet har utförts.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085691"
---
# <a name="intercompany-expenses"></a>Koncerninterna utgifter

[!include [banner](../includes/banner.md)]

En arbetare som är anställd av en juridisk person i en organisation kan utföra arbete för en annan juridisk person i samma organisation. I det här fallet kan du använda funktionen för koncernintern utgift för att tilldela arbetarens utgifter till den juridiska personen för vilken arbetet har utförts. Den juridiska personen där medarbetaren är anställd kallas utlånande juridisk person. Den juridiska personen för vilken medarbetaren ådrar sig utgifter kallas lånande juridisk person. 

Innan en medarbetare kan skapa och skicka in utgifter för arbete som utförs för en annan juridisk person går du till sidan **Parametrar för utgiftshantering** och väljer alternativet **Tillåt koncerninterna utgiftsrader**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Momsbokföring för koncerninterna utgifter

[!include [banner](../includes/banner.md)]

Om du vill använda momsgrupper som är associerade med den utlånande juridiska personen (källa) i stället för den lånande juridiska personen (mål) i utgiftsrapporten, måste du konfigurera detta i redovisningens momskonfiguration. När redovisningsparametern **Juridisk person för bokföring av koncernintern moms** är inställd på **Källa** och **Tillämpa skatteregler för moms** är inställd på **Nej** används momskombinationen för den utlånande juridiska personen. När samma parameter anges till **Destination** används momskombinationen för lånande juridisk person. För juridiska personer i USA, när parametern är inställd på **Källa** , måste också fältet **Momsfordran** konfigureras på sidan **Bokföringsgrupper i transaktionsregister**. Redovisningsmotorn använder informationen från det här fältet för momsrelaterade redovisningsposter.   
Beteendet är konsekvent för utgiftsrader som har bokförts med eller utan projekt.  
