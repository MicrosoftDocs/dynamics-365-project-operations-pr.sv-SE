---
title: Översikt över godkännanden
description: I det här ämne finns information om hur du arbetar med godkännanden i Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a7573b95998387453b72dbcb73c3de977ed7d913
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290381"
---
# <a name="approvals-overview"></a>Översikt över godkännanden

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Tids-och utgiftsöverföringar rör sig genom ett arbetsflöde för godkännande. När posterna har godkänts registreras transaktioner i schemat med verkliga värden och tid.

## <a name="approvals-workflow"></a>Arbetsflöde för godkännande
När du skapar och skickar en tid- eller utgiftspost skapas en godkännandepost. Projektgodkännaren eller din chef granskar och godkänner posten. Om posten är kopplad till ett projekt, skapas de faktiska värdena när den har godkänts. Det gör att kostnaden och faktureringen kan spåras. 

## <a name="approve-an-entry"></a>Godkänna en post
Med formuläret **Godkännanden** kan du växla mellan olika vyer så att du kan visa olika typer av godkännanden.
  
1. Gå till formuläret **Godkännanden** och välj **Utgifter**, **Tid** eller **Återkallanden**.
2. Granska varje godkännande och markera de du vill godkänna.
3. Välj **Godkänn** om du vill godkänna de markerade posterna.
Posterna kommer att bearbetas och verkliga värden och bokningar skapas.

## <a name="reject-an-entry"></a>Avvisa en post
Som projektgodkännare kan du behöva skicka tillbaka en post till en användare för korrigering.
  
1. Gå till formuläret **Godkännanden** och markera den post du vill avvisa. 
2. Välj **Avvisa**.
3. Valfri – Lägg till en kommentar i dialogrutan **Avvisade kommentarer** om du vill meddela användaren varför posten har avvisats.
4. Välj **OK**. Posten skickas tillbaka till användaren.
  
## <a name="recall-entries"></a>Återkalla poster
Du kan behöva återkalla en post som du har skickat. Om posten inte har godkänts returneras den omedelbart. En godkänd post kan emellertid ha en väsentlig inverkan. Projektgodkännaren måste godkänna återkallningen för att kunna återföra transaktionen i faktiska värden.

## <a name="specify-project-approvers"></a>Specificera projektgodkännare
Varje projekt har ett antal projektteammedlemmar. Du kan ange vilka teammedlemmar som också är projektgodkännare.

1. Gå till formuläret **Projekt** och öppna projektet från listan.
2. Under fliken **Team** väljer du den teammedlem som ska vara projektgodkännare och trycker sedan på **Redigera**.
3. Sätt fältet **Projektgodkännare** på **Ja**.
4. Välj **Spara**.
5. Upprepa steg 2–4 om du vill lägga till ytterligare projektgodkännare.

## <a name="configure-the-users-manager"></a>Konfigurera användarens chef

1. Gå till **Inställningar** > **Säkerhet** > **Användare**.
2. Välj den användare som du vill tilldela en chef och välj sedan chef från listan i området **organisationsinformation**. 
3. Välj **Spara**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]