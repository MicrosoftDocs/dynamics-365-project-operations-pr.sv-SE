---
title: Registrera dig för prenumerationer på förhandsversioner av Project Operations för resursbaserade/icke lagerbaserade scenarier
description: I det här ämnet finns information om hur du prenumererar på och distribuerar Project Operations för resursbaserade/icke lagerbaserade scenarier.
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1b8c8982ede83191ce346e76718322d47abf0dd8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000458"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Registrera dig för prenumerationer på förhandsversioner av Project Operations för resursbaserade/icke lagerbaserade scenarier

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I det här ämnet beskrivs hur du prenumererar på förhandsversioner/partnererbjudanden och distribuerar Project Operations-miljöer för resursbaserade/icke lagerbaserade scenarier.

## <a name="prerequisites"></a>Förutsättningar

- Du får ett e-postmeddelande med en inbjudan att delta i förhandsversionen. Du kan begära en förhandsversion på [webbplatsen för Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Den användare som distribuerar förhandsversionen måste ha behörighet som global administratör av Azure-klient.
- För att distribuera en Finance-miljö krävs en giltig Azure-prenumeration som ska faktureras per miljö. Du kan använda din organisations befintliga prenumeration eller använda en [Azure-utvärderingsversion](https://azure.microsoft.com/en-us/free/) för att komma i gång. CDS-miljön kommer att tillhandahållas gratis i en begränsad 30-dagarsperiod.

## <a name="subscribe"></a>Prenumerera

När din [begäran av förhandsversion](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) godkänns får du tre erbjudanden från Microsoft via e-post. Med de här erbjudandena kan du distribuera förhandsversionen av Project Operations:

- Utvärderingsversion av Dynamics 365 Project Operations (CRM)
- Office 365 Project Operations – utvärdering av förhandsversion
- Dynamics 365 Finance – utvärdering av förhandsversion

> [!IMPORTANT]
> Endast en person, klientadministratören, i en organisation behöver utföra den här uppgiften. Om du inte är prenumerant på den här versionen väntar du tills din organisation har registrerats och du har fått dina användarautentiseringsuppgifter.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Utvärderingsversion av Dynamics 365 Project Operations (CRM) 

Innan du börjar ska du kontrollera att du är inloggad i en webbläsare med användarkontot för arbete i klientorganisationen där du vill använda förhandsversionen av Project Operations.

1. Lös in den första erbjudandekoden, **Dynamics 365 Project Operations (CRM) - Utvärderingsversion** genom att klistra in den i webbläsarens webbadress.

![Hämta erbjudande](./media/16RedeemFirstOfferNew.png)

2. Bekräfta order.

![Bekräfta order](./media/17ConfirmOrderNew.png)

Du ser en bekräftelse på att erbjudandet har lösts in.

![Bekräftelse](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations – utvärdering av förhandsversion

Upprepa samma steg som med den första erbjudandekoden. Se till att du lägger till den andra erbjudandekoden med samma användarkonto som användes tillsammans med koden för den första erbjudandet.

### <a name="dynamics-365-finance-preview-trial"></a>Utvärdering av förhandsversion av Dynamics 365 Finance

Upprepa samma steg med det senaste erbjudandet från välkomstmeddelandet.

## <a name="assign-licenses"></a>Tilldela licenser

> [!IMPORTANT]
> Du måste ha administratörsbehörighet till organisationens Microsoft 365-portal för att kunna utföra följande steg.

1. Gå till [Microsoft 365 administratörscenter](https://portal.office.com/) för att tilldela licenser till dina användare.

![Startsida för administratörscenter](./media/14AdminPortal.png)

2. På sidan **Aktiva användare** väljer du de användare som du vill tilldela en licens till.

![Tilldela licenser](./media/15AssignLicenses.png)

3. Kontrollera att licensen för **utvärderingsversionen av Dynamics 365 Project Operations (CRM)** samt för **utvärderingsversionen av Office 365 Project Operations** har valts, och välj sedan **Spara ändringar**.

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
Slutför endast det här steget efter att demonstrationsmiljön av Finance har distribuerats och demonstrationsdata i FO är klara.


[!INCLUDE[footer-include](../includes/footer-banner.md)]