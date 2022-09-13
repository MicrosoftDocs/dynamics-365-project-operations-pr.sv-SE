---
title: Registrera dig för förhandsversionsprenumeration
description: Den här artikeln innehåller information om hur du prenumererar på och distribuerar Project Operations lite driftsättning - affär till proforma-fakturering.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 29bf31cd1bc9c1c5ac757de989154b4c7acc53fe
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410098"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registrera dig för förhandsversionsprenumeration 

Den här artikeln förklarar hur du prenumererar på testerbjudandet och distribuerar det Dynamics 365 Project Operations lite driftsättning - affär till proforma-fakturering.

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


1. Gå till [administrationscentret för Microsoft 365](https://portal.office.com/) om du vill tilldela licenserna till användarna.
2. På sidan **Aktiva användare** väljer du de användare som du vill tilldela en licens till.
3. Kontrollera att **Dynamics 365 Project Operations**-licensen är markerad. 
4. Välj **Spara ändringar**.

## <a name="create-a-new-dataverse-environment"></a>Skapa en ny Dataverse-miljö

1. Etablera en ny Project Operations Dataverse distributionsmiljö genom att följa instruktionerna i artikeln, [Dataverse distributionsmodellen](lite-deployment.md). När du väljer miljötyp ska du se till att använda **Utvärdering (prenumerationsbaserad)**.

  ![Ny miljö.](./media/19CreateEnvironment.png)

2. Välj inställningen **Aktivera Dynamics 365-appar** och låt **Distribuera dessa appar automatiskt** vara tomt.  
3. Välj **Spara** för att skapa miljön.

  ![Lägg till databas.](./media/20CreateEnvironment1.png)

4. När miljön har skapats installerar du **Microsoft Dynamics 365 Project Operations**-lösningen. 

![Installera lösning.](./media/21InstallSolution.png)

## <a name="set-up-demo-data"></a>Konfigurera demodata

Konfigurera demodata genom att följa instruktionerna i artikeln, [Installera demoinstallations- och konfigurationsdata](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
