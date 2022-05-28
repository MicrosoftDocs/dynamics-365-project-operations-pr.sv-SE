---
title: Koncerninterna utgifter
description: Detta ämne innehåller information om hur du använder koncerninterna utgifter för att tilldela en medarbetares utgifter till den juridiska person som arbetet utförts för.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6788a590879bd839ebb9dedc45895dc047cc9f15
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684256"
---
# <a name="intercompany-expenses"></a>Koncerninterna utgifter

En arbetare som är anställd av en juridisk person i en organisation kan utföra arbete för en annan juridisk person i samma organisation. Du kan använda koncerninterna utgifter för att tilldela en medarbetares utgifter till den juridiska person som arbetet utförts för. Den juridiska personen där medarbetaren är anställd kallas utlånande juridisk person. Den juridiska personen för vilken medarbetaren ådrar sig utgifter kallas lånande juridisk person. 

Innan en anställd kan skapa och skicka in koncerninterna utgifter, måste du aktivera koncerninterna kostnadsrader. På sidan **Parametrar för utgiftshantering** i den utlånande juridiska entiteten väljer du **Tillåt koncerninterna utgiftsrader**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Momsbokföring för koncerninterna utgifter

[!include [banner](../includes/banner.md)]

Innan du kan använda momsgrupper som är associerade med den utlånande (källrelaterade) juridiska entiteten i stället för den lånande juridiska personen (associerad med destination) i utgiftsrapporten måste du aktivera funktionen i momskonfigurationen för huvudboken. När parametern **Juridisk entitet för momsbokföring** har angetts som **Källa** och **Tillämpa momsregler** har angetts som **Nej** används momskombinationen för den lånande juridiska entiteten. När samma parameter anges till **Destination** används momskombinationen för lånande juridisk person. För juridiska personer i USA, när parametern är inställd på **Källa**, måste också fältet **Momsfordran** konfigureras på sidan **Bokföringsgrupper i transaktionsregister**. Redovisningsmotorn använder informationen från det här fältet för momsrelaterade redovisningsposter.   
Beteendet är konsekvent för utgiftsrader som har bokförts med eller utan projekt.  

## <a name="new-expense-expression-builder"></a>Nytt uttrycksverktyg för utgifter

Den nya uttrycksverktyget löser problem med koncerninterna kostnadsscenarier som använder projekt. När du skapar en koncernintern utgift kan du använda den här funktionen för att säkerställa att utgiftspolicyn verifieras korrekt mot det projekt som valts på utgiftsraden och att utgiftsrapporten kan skickas korrekt.

För att funktionen för uttrycksverktyget för utgifter ska fungera måste den vara aktiverad. Dessutom bör den utgiftspolicy som har ett projekt-ID konfigureras.

Om du redan har konfigurerat principer som verifierar projekt-ID:t på utgiftsraden måste de principerna dras tillbaka. Sedan kan du aktivera funktionen och konfigurera om principerna.

Aktivera funktionen genom att följa stegen nedan.

1. Gå till **Arbetsytor** \> **Funktionshantering**.
2. Välj **Nytt uttrycksverktyg som löser problem med koncerninterna kostnadsscenarier som använder projekt**. Välj sedan **Aktivera nu**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
