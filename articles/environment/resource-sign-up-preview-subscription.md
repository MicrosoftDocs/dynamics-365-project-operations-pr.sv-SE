---
title: Registrera dig för prenumerationer på förhandsversioner av Project Operations för resursbaserade/icke lagerbaserade scenarier
description: I det här ämnet finns information om hur du prenumererar på och distribuerar Project Operations för resursbaserade/icke lagerbaserade scenarier.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949102"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Registrera dig för prenumerationer på förhandsversioner av Project Operations för resursbaserade/icke lagerbaserade scenarier

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

I det här ämnet beskrivs hur du prenumererar på förhandsversioner/partnererbjudanden och distribuerar Project Operations-miljöer för resursbaserade/icke lagerbaserade scenarier.

## <a name="prerequisites"></a>Förutsättningar

- Du får ett e-postmeddelande med en inbjudan att delta i förhandsversionen. Du kan begära en förhandsversion på [webbplatsen för Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Den användare som distribuerar förhandsversionen måste ha behörighet som global administratör av Azure-klient.
- För att distribuera en Finance-miljö krävs en giltig Azure-prenumeration som ska faktureras per miljö. Du kan använda din organisations befintliga prenumeration eller använda en [Azure-utvärderingsversion](https://azure.microsoft.com/en-us/free/) för att komma i gång. CDS-miljön kommer att tillhandahållas gratis i en begränsad 30-dagarsperiod.

## <a name="subscribe"></a>Prenumerera

När din [begäran av förhandsversion](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) godkänns får du två erbjudanden från Microsoft via e-post. Med de här erbjudandena kan du distribuera förhandsversionen av Project Operations:

- Dynamics 365 Project Operations – utvärdering av förhandsversion
- Utvärdering av förhandsversion av Dynamics 365 for Finance and Operations.

> [!IMPORTANT]
> Endast en person, klientadministratören, i en organisation behöver utföra den här uppgiften. Om du inte är prenumerant på den här versionen väntar du tills din organisation har registrerats och du har fått dina användarautentiseringsuppgifter.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – utvärdering av förhandsversion

1. Hämta det första erbjudandet, **Utvärdering av Dynamics 365 Project Operations**, med URL tillhandahållen i ditt välkomstmeddelande.

![Första erbjudandet](./media/1FirstOffer.png)

2. Kontrollera att du är inloggad som den användare som tillhör organisationen som ska prenumerera på tjänsten.
3. Fortsätt att hämta erbjudandet. 
4. Välj **Ja, lägg till det i mitt konto**.

![Hämta erbjudande](./media/2RedeemFirstOffer.png)

![Bekräfta erbjudandet](./media/3ConfirmFirstOffer.png)

![Erbjudande hämtat](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Utvärdering av förhandsversion av Dynamics 365 Finance

Upprepa samma steg med det andra erbjudandet från välkomstmeddelandet.

## <a name="assign-licenses"></a>Tilldela licenser

> [!IMPORTANT]
> Du måste ha administratörsbehörighet till organisationens Office 365-portal för att kunna utföra följande steg.

1. Gå till [Microsoft 365 administratörscenter](https://portal.office.com/) för att tilldela licenser till dina användare.

![Administrationsportalen för Office](./media/5OfficeAdminPortal.png)

2. På sidan **Aktiva användare** väljer du de användare som du vill tilldela en licens till.

![Tilldela licenser](./media/6AssignLicenses.png)

3. Kontrollera att licensen för Project Operations har valts och välj **Spara ändringar**. 

> [!NOTE]
> Erbjudandet gällande utvärderingsversionen av Finance behöver inte tilldelas en användare.

## <a name="start-a-new-project-in-lcs"></a>Skapa ett nytt projekt i LCS

Skapa ett nytt LCS-projekt enligt beskrivningen i ämnet [Starta ett nytt projekt i LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Lägg till en Azure-prenumeration i ett LCS-projekt

Slutför uppgiften genom att följa stegen i ämnet [Lägga till en Azure-prenumeration i LCS-projekt](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Distribuera demomiljön av Finance med Project Operations för resursbaserade/icke lagerbaserade scenarier

Följ anvisningarna i ämnet [Etablera en ny miljö](resource-provision-new-environment.md) för att slutföra distributionen. Använd distributionstypen [Demomiljö](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) för förhandsgranskning.

## <a name="install-cds-setup-and-configuration-data"></a>Installationsinställning av CDS och konfigurationsdata

Installationsinställlning av CDS och konfigurationsdata enligt beskrivningen i ämnet [Konfigurera och tillämpa konfigurationsdata i Common Data Service](resource-apply-pro-setup-config-data.md).

