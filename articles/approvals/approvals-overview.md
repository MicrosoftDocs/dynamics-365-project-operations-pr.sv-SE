---
title: Översikt över godkännanden
description: Den här artikeln innehåller information om hur du arbetar med godkännande i Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: d5b5c93dc948992505054ef7b17579aafcdf8f8d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924728"
---
# <a name="approvals-overview"></a>Översikt över godkännanden

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Skicka in tid, utgifter och materialanvändning passerar ett godkännandearbetsflöde. När posterna har godkänts registreras transaktioner i schemat med verkliga värden och tid.

## <a name="approvals-workflow"></a>Arbetsflöde för godkännande
När du skapar och skickar en tids-, kostnad- eller materialanvändningspost skapas en godkännandepost. Projektgodkännaren eller chefen granskar och godkänner posten. Om posten är relaterad till ett projekt skapas de faktiska värdet när den godkänns. Det gör att kostnaden och faktureringen kan spåras.

## <a name="approve-an-entry"></a>Godkänna en post
På sidan **Godkännanden** kan du växla mellan olika vyer så att du kan visa de olika typerna av godkännanden.
  
1. Gå till sidan **Godkännanden** och välj **Utgifter**, **Tid**, **Materialanvändning** eller **Återkallade**.
2. Granska varje godkännande och markera de du vill godkänna.
3. Välj **Godkänn** om du vill godkänna de markerade posterna.
Systemet bearbetar posterna och skapar faktiska värden.

## <a name="reject-an-entry"></a>Avvisa en post
Som projektgodkännare kan du behöva skicka tillbaka en post till en användare för korrigering.
  
1. Gå till sidan **Godkännanden** och välj den post som ska avvisas. 
2. Välj **Avvisa**.
3. Valfritt, lägg till en kommentar i dialogrutan **Kommentarer till avvisning** för att informera användaren om varför posten avvisas.
4. Välj **OK**. Posten skickas tillbaka till användaren.
  
## <a name="cancel-approval"></a>Avbryt godkännandet
I vissa fall kan du behöva avbryta en post som godkänts tidigare. Om du avbryter en tidigare godkänd post får det ekonomiska effekter. 

## <a name="approving-recall-requests"></a>Återkalla godkännandebegäran
I vissa fall kan en konsult behöva godkänna en post som godkänts tidigare. Om du avbryter en tidigare godkänd post får det ekonomiska effekter. Projekt godkännaren krävs för att godkänna affären för att återställa transaktionen i Faktiska värden.

## <a name="specify-project-approvers"></a>Specificera projektgodkännare
Varje projekt har ett antal projektteammedlemmar. Du kan ange vilka teammedlemmar som också är projektgodkännare.

1. Gå till sidan **Projekt** och öppna projektet från listan.
2. Under fliken **Team** väljer du den teammedlem som ska vara projektgodkännare och trycker sedan på **Redigera**.
3. Sätt fältet **Projektgodkännare** på **Ja**.
4. Välj **Spara**.
5. Upprepa steg 2–4 om du vill lägga till ytterligare projektgodkännare.

## <a name="configure-the-users-manager"></a>Konfigurera användarens chef

1. Gå till **Inställningar** > **Säkerhet** > **Användare**.
2. Välj den användare som du vill tilldela en chef och välj sedan chef från listan i området **organisationsinformation**. 
3. Välj **Spara**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
