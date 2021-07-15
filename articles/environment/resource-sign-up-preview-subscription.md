---
title: Registrera dig för prenumerationer på förhandsversioner av Project Operations för resursbaserade/icke lagerbaserade scenarier
description: I det här ämnet finns information om hur du prenumererar på och distribuerar Project Operations för resursbaserade/icke lagerbaserade scenarier.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334849"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Registrera dig för prenumerationer på förhandsversioner av Project Operations för resursbaserade/icke lagerbaserade scenarier

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I ämne beskrivs hur du prenumererar på proverbjudandet och distribuerar Project Operations-miljön för resurs-/icke-lagerbaserade scenarier.

## <a name="prerequisites"></a>Förutsättningar
- Den användare som distribuerar förhandsversionen måste ha behörighet som global administratör av Azure-klient. Du kan skapa en klientorganisation under det första erbjudandet. 
- För att distribuera en Finance-miljö krävs en giltig Azure-prenumeration som ska faktureras per miljö. Du kan använda din organisations befintliga prenumeration eller använda en [Azure-utvärderingsversion](https://azure.microsoft.com/en-us/free/) för att komma i gång. CDS-miljön kommer att tillhandahållas gratis i en begränsad 30-dagarsperiod.

> [!IMPORTANT]
> Endast en person, klientadministratören, i en organisation behöver utföra den här uppgiften. Om du inte är prenumerant på den här versionen väntar du tills din organisation har registrerats och du har fått dina användarautentiseringsuppgifter.
> 
> Utvärderingsversioner används endast i klientorganisationen. Du kan bara köra en utvärderingsversion en gång. Vi rekommenderar att du skapar en ny klientorganisation för utvärderingsversionen.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) – Förhandsgranska utvärderingsversion 

Innan du börjar ska du kontrollera att du är inloggad i en webbläsare med användarkontot för arbete i klientorganisationen där du vill använda förhandsversionen av Project Operations.

1. Den första erbjudandekoden gäller **Dynamics 365 Project Operations** här [Provversion av Project Operations](https://aka.ms/try-po).
2. Bekräfta order.

  Du ser en bekräftelse på att erbjudandet har lösts in.

### <a name="dynamics-365-finance-preview-trial"></a>Utvärdering av förhandsversion av Dynamics 365 Finance

Gå till [Förhandsgranska utvärderingsversion av Dynamics 365 for Finance](https://aka.ms/trypoche) och upprepa stegen från föregående avsnitt med erbjudandet, Registrera dig för Cloud Hosted Environment.  

## <a name="assign-licenses"></a>Tilldela licenser

> [!IMPORTANT]
> Du måste ha administratörsbehörighet till organisationens Microsoft 365-portal för att kunna utföra följande steg.

1. Gå till [Microsoft 365 administratörscenter](https://portal.office.com/) för att tilldela licenser till dina användare.

2. På sidan **Aktiva användare** väljer du de användare som du vill tilldela en licens till.

3. Kontrollera att **Dynamics 365 Project Operations**-licensen har markerats och välj **Spara ändringar**.

> [!NOTE]
> Erbjudandet gällande utvärderingsversionen av Finance behöver inte tilldelas en användare.

## <a name="start-a-new-project-in-lcs"></a>Skapa ett nytt projekt i LCS

Skapa ett nytt LCS-projekt enligt beskrivningen i ämnet [Starta ett nytt projekt i LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Lägg till en Azure-prenumeration i ett LCS-projekt

Slutför uppgiften genom att följa stegen i ämnet [Lägga till en Azure-prenumeration i LCS-projekt](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Distribuera demomiljön av Finance med Project Operations för resursbaserade/icke lagerbaserade scenarier

Följ anvisningarna i ämnet [Etablera en ny miljö](resource-provision-new-environment.md) för att slutföra distributionen. Använd distributionstypen [Demomiljö](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) för förhandsgranskning. 

## <a name="install-cds-setup-and-configuration-data"></a>Installationsinställning av CDS och konfigurationsdata

Installationsinställlning av CDS och konfigurationsdata enligt beskrivningen i ämnet [Konfigurera och tillämpa konfigurationsdata i Common Data Service](resource-apply-pro-setup-config-data.md).
Slutför endast det här steget när Finance demonstrationmiljön har distribuerats och demonstrationsdata är klara.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
