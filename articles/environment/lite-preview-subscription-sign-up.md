---
title: Registrera dig för förhandsversionsprenumeration - lite
description: I det här ämnet finns information om hur du prenumererar på och distribuerar Project Operations enkel distribution – avtal till proforma-fakturering.
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4de51277e5a08690cc16497e3916f40498b39fb8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997443"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registrera dig för förhandsversionsprenumeration - lite 

Detta ämne förklarar hur du prenumererar på förhandsgranskning av partnererbjudandet och distribuerar Dynamics 365 Project Operations Lite-distribuerar – hantera proformafakturering.

> [!NOTE]
> Processen kommer att ändras i kommande versioner av Project Operations.

## <a name="prerequisites"></a>Förutsättningar

- Du får ett e-postmeddelande med en inbjudan att delta i förhandsversionen. Du kan begära en förhandsversion på [webbplatsen för Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Den användare som distribuerar förhandsversionen måste ha behörighet som global administratör av Azure-klient.
- Granska alla villkor.

## <a name="subscribe"></a>Prenumerera

När du får ett godkännande av en [begäran av förhandsversion](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) får du två erbjudanden från Microsoft via e-post. Med de här erbjudandena kan du distribuera förhandsversionen av Project Operations:

- Utvärderingsversion av Dynamics 365 Project Operations (CRM)
- Office 365 Project Operations – utvärdering av förhandsversion

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

## <a name="assign-licenses"></a>Tilldela licenser

> [!IMPORTANT]
> Du måste ha administratörsbehörighet till organisationens Microsoft 365-portal för att kunna utföra följande steg.


1. Gå till [Microsoft 365 administratörscenter](https://portal.office.com/) för att tilldela licenser till dina användare.

![Startsida för administratörscenter](./media/14AdminPortal.png)

2. På sidan **Aktiva användare** väljer du de användare som du vill tilldela en licens till.

![Tilldela licenser](./media/15AssignLicenses.png)

3. Kontrollera att licenser **Dynamics 365 Project Operations (CRM) förhandsgranskning** och **Office 365 Project Operations - förhandsgranskning** markeras. 
4. Välj **Spara ändringar**.

## <a name="create-a-new-cds-environment"></a>Skapa en ny CDS-miljö

1. Tillhandahåll en ny distributionsmiljö för Project Operations CDS-distribution genom att följa anvisningarna i ämnet [CDS-distributionsmodell](lite-deployment.md). När du väljer miljötyp ska du se till att använda **Utvärdering (prenumerationsbaserad)**.
![Ny miljö](./media/19CreateEnvironment.png)

2. Välj inställningen **Aktivera Dynamics 365-appar** och låt **Distribuera dessa appar automatiskt** vara tomt.  
3. Välj **Spara** för att skapa miljön.

![Lägg till databas](./media/20CreateEnvironment1.png)

4. När miljön har skapats installerar du **Microsoft Dynamics 365 Project Operations**-lösningen. 

![Installera lösning](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Installera en CDS-konfiguration och konfigurera demodata

Installera CDS-konfigurationen och konfigurera demodata genom att följa anvisningarna i ämnet [Tillämpa demokonfiguration och konfigurationsdata](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]