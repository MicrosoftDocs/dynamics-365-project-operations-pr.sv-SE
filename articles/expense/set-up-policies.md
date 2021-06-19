---
title: Definiera utgiftspolicyer
description: Du kan definiera utgiftspolicyer som medarbetarna måste följa när de registrerar och skickar utgiftsrapporter och reserekvisitioner.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa108db9aa0d2a22c35d2d046917ddae1f3842c1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001898"
---
# <a name="define-expense-policies"></a>Definiera utgiftspolicyer

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Du kan definiera policyer som medarbetarna måste följa när de registrerar och skickar utgiftsrapporter och reserekvisitioner.         
Med hjälp av utgiftspolicyer kan du effektivt hantera utgifter.         

Du kan till exempel ange en policy för hotellutgifter i New York City, vilket anger att utgiftskostnaden per natt inte får överskrida 250 USD.       
Om en arbetare skickar en utgiftsrapport eller en reserekvisition där rumskostnaden överstiger det här beloppet meddelar systemet         
medarbetaren som policybeloppet för utgiften har överskridits. Du kan konfigurera meddelandet som medarbetaren får när du        
definierar policy.      
        
Du kan definiera tre typer av policyer:         
        
- **Varning**: kan medarbetaren skicka en utgiftsrapport eller reserekvisition men kostnaden markeras för alla godkännare och         
  för senare rapportering.        

- **Fel**: kräver att medarbetaren ändrar utgifterna för att följa principen innan du skickar utgiftsrapporten eller reserekvisitionen.        
 
 - **Motivering**: kräver att arbetaren eller chefen anger en motivering för att policybeloppet överskrids innan utgiftsrapporten skickas eller reserekvisitionen skickas.        

## <a name="policy-tips"></a>Policytips
Här följer några förslag som kan hjälpa dig när du skapar nya policyer för utgiftshantering: 

- Policyer är datumeffektiva vilket innebär att en policy inte börjar gälla om den skapas med ett datum efter det datum då kostnaden inträffade. Du kan till exempel skapa en ny policy i dag för att upprätthålla en maximal måltidsutgift på 50 USD. Alla befintliga utgifter som angavs i igår kontrolleras inte mot den här policyn.
- När du skapar en policy för en utgiftskategori som kan specificeras bör du lägga till ett villkor för utgiftsradtypen. Vissa policyer, t.ex. krav på kvitton, kanske inte passar för specificerade rader. I det här fallet gäller policyn endast för rubrikraden eller en rad som inte har specificerats. 
- Utgiftshanteringspolicye utvärderas mot källentiteten som standard. För koncerninterna scenarier kan du ange att policyn ska utvärderas mot målentiteten (lånande entitet) i stället. Om du vill köra policyer mot målentiteten aktiverar du funktionen **Utvärdera utgiftspolicy mot låntagande juridisk person** på arbetsytan **Funktionshantering**.

## <a name="when-to-evaluate-policies"></a>När policyer utvärderas

I parametrar för utgiftshantering kan du välja om du vill utvärdera policyer för utgiftshantering när en rad sparas eller när en utgiftsrapport skickas. Om du väljer att utvärdera när en rad sparas får användarna tidigare insyn i vad de behöver göra för att slutföra sina utgiftsrapporter samtidigt. Annars kan du försena utvärdering av policyer och spara tid genom att validera i slutet, under överföringen till arbetsflödet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]