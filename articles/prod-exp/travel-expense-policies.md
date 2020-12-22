---
title: Konfigurera utgiftsprinciper
description: Du kan konfigurera utgiftsprinciper som medarbetarna måste följa när de registrerar och skickar in utgiftsrapporter och reserekvisitioner i Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6240a7be175800ce6f3b066de9e935ab370629ef
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650116"
---
# <a name="set-up-expense-policies"></a>Konfigurera utgiftsprinciper

[!include [banner](../includes/banner.md)]

Du kan definiera policyer som medarbetarna måste följa när de registrerar och skickar utgiftsrapporter och reserekvisitioner.         
Med hjälp av utgiftspolicyer kan du effektivt hantera utgifter.         

Du kan till exempel ange en policy för hotellutgifter i New York City, vilket anger att utgiftskostnaden per natt inte får överskrida 250 USD.       
Om en arbetare skickar in en utgiftsrapport eller en reserekvisition där rumskostnaden överstiger det här beloppet meddelar systemet        
medarbetaren som policybeloppet för utgiften har överskridits. Du kan konfigurera meddelandet som medarbetaren får när du        
definierar policy.      
        
Du kan definiera tre typer av policyer:         
        
- Varning – Låter medarbetaren skicka in en utgiftsrapport eller reserekvisition men kostnaden markeras för alla godkännare och        
  för senare rapportering.        

- Fel – Kräver att medarbetaren ändrar utgifterna för att följa principen innan han eller hon skickar in utgiftsrapporten eller reserekvisitionen.       
 
 - Motivering – Kräver att arbetaren eller chefen anger en motivering för att principbeloppet överskrids innan utgiftsrapporten eller reserekvisitionen skickas in.        

## <a name="policy-tips"></a>Policytips
Här följer några förslag som kan hjälpa dig när du skapar nya principer för utgiftshantering. 
* Principer är datumeffektiva och börjar inte gälla om principen skapas med ett datum efter det datum då kostnaden inträffade. Om du till exempel skapar en ny princip i dag för att införa en maximal måltidsutgift på 50 dollar, kontrolleras inte några befintliga utgifter som anges i igår mot den här principen.
* När du skapar en policy för en utgiftskategori som kan specificeras bör du lägga till ett villkor för utgiftsradtypen. Vissa principer, t.ex. krav på kvitton, kanske inte fungerar för specificerade rader och ska endast användas på rubrikraden eller en rad som inte har specificerats. 
* Utgiftshanteringspolicye utvärderas mot källentiteten som standard. För koncerninterna scenarier kan du ange att policyn ska utvärderas mot målentiteten (lånande entitet) i stället. Om du vill köra principer mot målentiteten aktiverar du funktionen "Utvärdera utgiftspolicy mot låntagande juridisk person" på arbetsytan **Funktionshantering**.

## <a name="when-to-evaluate-policies"></a>När policyer utvärderas

I parametrar för utgiftshantering finns ett alternativ att antingen utvärdera principer för utgiftshantering när en rad sparas eller när en utgiftsrapport skickas in. Om du väljer att utvärdera när en rad sparas säkerställer detta att användare får tidigare insyn i vad de behöver göra för att slutföra sina utgiftsrapporter samtidigt. Annars kan du försena utvärdering av principer och spara tid genom att validera i slutet, under överföringen till arbetsflödet.
