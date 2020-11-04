---
title: Privata utgifter i en utgiftsrapport
description: I det här ämnet beskrivs de två metoderna för att hantera en arbetares privata utgifter i Microsoft Dynamics 365 Finance.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085689"
---
# <a name="personal-expenses-on-an-expense-report"></a>Privata utgifter i en utgiftsrapport

[!include [banner](../includes/banner.md)]

Under en affärsresa kan arbetstagarna ibland debitera företagets kreditkort för privata utgifter. Om du inte definierar en process för hantering av privata utgifter kan godkännandeprocessen för utgiftsrapporter störas när arbetstagarna skickar in sina specificerade utgiftsrapporter. 

Det finns två sätt att hantera en arbetares privata utgifter:

- **Betalas av medarbetare** – din organisation betalar inte privata utgifter som visas på fakturan för företagskreditkortet. I stället skapas en rapport som visar privata utgifter tillsammans med de företagsutgifter som debiterades företagskreditkortet.
- **Betalas av företaget** – organisationen betalar hela fakturan för företagets kreditkort och debiterar sedan arbetarens konto för privata utgifter.

Du kan välja vilken metod som ska användas av organisationen på sidan **Parametrar för utgiftshantering**.
