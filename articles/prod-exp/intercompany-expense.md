---
title: Koncerninterna utgifter
description: Detta ämne innehåller information om hur du använder koncerninterna utgifter för att tilldela en medarbetares utgifter till den juridiska person som arbetet utförts för.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005093"
---
# <a name="intercompany-expenses"></a>Koncerninterna utgifter

En arbetare som är anställd av en juridisk person i en organisation kan utföra arbete för en annan juridisk person i samma organisation. Du kan använda koncerninterna utgifter för att tilldela en medarbetares utgifter till den juridiska person som arbetet utförts för. Den juridiska personen där medarbetaren är anställd kallas utlånande juridisk person. Den juridiska personen för vilken medarbetaren ådrar sig utgifter kallas lånande juridisk person. 

Innan en anställd kan skapa och skicka in koncerninterna utgifter, måste du aktivera koncerninterna kostnadsrader. På sidan **Parametrar för utgiftshantering** i den utlånande juridiska entiteten väljer du **Tillåt koncerninterna utgiftsrader**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Momsbokföring för koncerninterna utgifter

[!include [banner](../includes/banner.md)]

Innan du kan använda momsgrupper som är associerade med den utlånande (källrelaterade) juridiska entiteten i stället för den lånande juridiska personen (associerad med destination) i utgiftsrapporten måste du aktivera funktionen i momskonfigurationen för huvudboken. När parametern **Juridisk entitet för momsbokföring** har angetts som **Källa** och **Tillämpa momsregler** har angetts som **Nej** används momskombinationen för den lånande juridiska entiteten. När samma parameter anges till **Destination** används momskombinationen för lånande juridisk person. För juridiska personer i USA, när parametern är inställd på **Källa**, måste också fältet **Momsfordran** konfigureras på sidan **Bokföringsgrupper i transaktionsregister**. Redovisningsmotorn använder informationen från det här fältet för momsrelaterade redovisningsposter.   
Beteendet är konsekvent för utgiftsrader som har bokförts med eller utan projekt.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]