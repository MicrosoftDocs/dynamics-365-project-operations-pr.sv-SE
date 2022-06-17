---
title: Koncerninterna utgifter
description: Den här artikeln innehåller information om hur du använder kostnader för att tilldela en arbetares utgifter till den juridiska enhet som arbetet utfördes för.
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
ms.openlocfilehash: 1c58fb1510c9ba75bc81a4dc07b91f1b6a60355d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932410"
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
