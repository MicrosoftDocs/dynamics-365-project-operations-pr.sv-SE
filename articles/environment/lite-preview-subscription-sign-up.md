---
title: Registrera dig för förhandsversionsprenumeration - lite
description: I det här ämnet finns information om hur du prenumererar på och distribuerar Project Operations enkel distribution – avtal till proforma-fakturering.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334804"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registrera dig för förhandsversionsprenumeration 

I ämne hur du prenumererar på proverbjudandet och distribuerar Dynamics 365 Project Operations lite deployment – handlar om att fakturera proforma.

> [!NOTE]
> Processen kommer att ändras i kommande versioner av Project Operations.

## <a name="prerequisites"></a>Förutsättningar
- Den användare som distribuerar förhandsversionen måste ha behörighet som global administratör av Azure-klient. Du kan skapa en klientorganisation under det första erbjudandet.

> [!IMPORTANT]
> Endast en person, klientadministratören, i en organisation behöver utföra den här uppgiften. Om du inte är prenumerant på den här versionen väntar du tills din organisation har registrerats och du har fått dina användarautentiseringsuppgifter.
> 
> Utvärderingsversioner används endast i klientorganisationen. Du kan bara köra en utvärderingsversion en gång. Vi rekommenderar att du skapar en ny klientorganisation för utvärderingsversionen.

### <a name="dynamics-365-project-operations-trial"></a>Dynamics 365 Project Operations utvärderingsversion 

Innan du börjar ska du kontrollera att du är inloggad i en webbläsare med användarkontot för arbete i klientorganisationen där du vill använda förhandsversionen av Project Operations.

1. Gå till [Project Operations utvärderingsversion](https://aka.ms/try-po) för att lösa in den första erbjudandekoden, **Dynamics 365 Project Operations**.
2. Bekräfta order.

  Du ser att erbjudandet om bekräftelse löstes in.

## <a name="assign-licenses"></a>Tilldela licenser

> [!IMPORTANT]
> Du måste ha administratörsbehörighet till organisationens Microsoft 365-portal för att kunna utföra följande steg.


1. Gå till [Microsoft 365 administratörscenter](https://portal.office.com/) för att tilldela licenser till dina användare.
2. På sidan **Aktiva användare** väljer du de användare som du vill tilldela en licens till.
3. Kontrollera att **Dynamics 365 Project Operations**-licensen är markerad. 
4. Välj **Spara ändringar**.

## <a name="create-a-new-dataverse-environment"></a>Skapa en ny Dataverse-miljö

1. Tillhandahåll en ny distributionsmiljö för Project Operations Dataverse-distribution genom att följa anvisningarna i ämnet [Dataverse-distributionsmodell](lite-deployment.md). När du väljer miljötyp ska du se till att använda **Utvärdering (prenumerationsbaserad)**.

  ![Ny miljö](./media/19CreateEnvironment.png)

2. Välj inställningen **Aktivera Dynamics 365-appar** och låt **Distribuera dessa appar automatiskt** vara tomt.  
3. Välj **Spara** för att skapa miljön.

  ![Lägg till databas](./media/20CreateEnvironment1.png)

4. När miljön har skapats installerar du **Microsoft Dynamics 365 Project Operations**-lösningen. 

![Installera lösning](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Installera en CDS-konfiguration och konfigurera demodata

Installera CDS-konfigurationen och konfigurera demodata genom att följa anvisningarna i ämnet [Tillämpa demokonfiguration och konfigurationsdata](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
