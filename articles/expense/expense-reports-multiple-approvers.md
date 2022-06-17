---
title: Utgiftsrapporter och flera godkännare
description: Den här artikeln innehåller information om utgiftsrapporter som kräver godkännande av flera personer.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 88f42535e4826d1f618bd542eec3b26a6fde1a97
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914480"
---
# <a name="expense-reports-and-multiple-approvers"></a>Utgiftsrapporter och flera godkännare

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Beroende på organisationens godkännandeprinciper för utgifter kan fler än en person behöva godkänna en skickad utgiftsrapport. När du konfigurerar arbetsflödesprocessen för godkännande av utgiftsrapporter kan du lägga till arbetsflödeselement som innehåller uppgifter eller steg för en eller flera godkännare av utgiftsrapporter. Du kan till exempel kräva att alla utgiftsrapporter ska godkännas av två olika personer, chefen för den medarbetare som skickade rapporten och koordinatorn för leverantörsreskontra.

Om du vill kräva flera godkännare för utgiftsrapporter kan du lägga till arbetsflödeselementen på något av följande sätt:

- Lägg till ett godkännandeelement som har ett steg. Steget kan till exempel kräva att en utgiftsrapport tilldelas en användargrupp och att den godkänns med 50 procent av användargruppens medlemmar.
- Lägg till ett godkännandeelement som har flera steg. Godkännandeelementet kan till exempel innehålla följande steg:

    1. Chefen för den medarbetare som skickade utgiftsrapporten godkänner den.
    2. Leverantörsreskontra ansvarig verifierar inleveranserna och objekt för utgiftsrapport.
    3. Budgetägaren godkänner utgiftsrapporten.

- Lägg till flera godkännandeelement, som vart och ett har ett steg. Du kan till exempel lägga till ett separat godkännandeelement för vart och ett av följande steg:

    1. Medarbetarens chef godkänner utgiftsrapporten.
    2. Budgetägaren godkänner utgiftsrapporten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]