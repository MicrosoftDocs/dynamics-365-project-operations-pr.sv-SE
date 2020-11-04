---
title: Registrera dig för en förhandsversionsprenumeration
description: I det här ämnet finns information om hur du prenumererar på och distribuerar Project Operations enkel distribution – avtal till proforma-fakturering.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5342466f308ab62a9f73a85fbd838d7c33bb1f47
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085403"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Registrera dig för en förhandsversionsprenumeration för enkel distribution – avtal till proforma-fakturering

I det här ämnet beskrivs hur du prenumererar partnererbjudandet för förhandsversion och distribuerar Dynamics 365 Project Operations enkel distribution – avtal till proforma-fakturering.

> [!NOTE]
> Processen kommer att ändras i kommande versioner av Project Operations.

## <a name="prerequisites"></a>Förutsättningar

- Du får ett e-postmeddelande med en inbjudan att delta i förhandsversionen. Du kan begära en förhandsversion på [webbplatsen för Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Den användare som distribuerar förhandsversionen måste ha behörighet som global administratör av Azure-klient.
- Granska alla villkor.

## <a name="subscribe"></a>Prenumerera

När du får ett godkännande av en [begäran av förhandsversion](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) får du två erbjudanden från Microsoft via e-post. Med de här erbjudandena kan du distribuera förhandsversionen av Project Operations:

- Dynamics 365 Project Operations (CRM) – utvärdering av förhandsversion
- Office 365 Project Operations – utvärdering av förhandsversion

> [!IMPORTANT]
> Endast en person, klientadministratören, i en organisation behöver utföra den här uppgiften. Om du inte är prenumerant på den här versionen väntar du tills din organisation har registrerats och du har fått dina användarautentiseringsuppgifter.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – utvärdering av förhandsversion 

Innan du börjar ska du kontrollera att du är inloggad i en webbläsare med användarkontot för arbete i klientorganisationen där du vill använda förhandsversionen av Project Operations.

1. Lös in den första erbjudandekoden, **Dynamics 365 Project Operations (CRM) – utvärdering av förhandsversion** genom att klistra in den i webbläsarens URL.

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

3. Kontrollera att licenserna för **förhandsversion av Dynamics 365 Project Operations (CRM)** och **Office 365 Project Operations – förhandsversion** har valts. 
4. Välj **Spara ändringar**.

## <a name="create-a-new-cds-environment"></a>Skapa en ny CDS-miljö

1. Tillhandahåll en ny distributionsmiljö för Project Operations CDS-distribution genom att följa anvisningarna i ämnet [CDS-distributionsmodell](lite-deployment.md). När du väljer miljötyp ska du se till att använda **Utvärdering (prenumerationsbaserad)**.
![Ny miljö](./media/19CreateEnvironment.png)

2. Välj inställningen **Aktivera Dynamics 365-appar** och låt **Distribuera dessa appar automatiskt** vara tomt.  
3. Välj **Spara** för att skapa miljön.

![Lägg till databas](./media/20CreateEnvironment1.png)

4. När miljön har skapats installerar du lösningen **Microsoft Dynamics 365 Project Operations**. 

![Installera lösning](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Installera en CDS-konfiguration och konfigurera demodata

Installera CDS-konfigurationen och konfigurera demodata genom att följa anvisningarna i ämnet [Tillämpa demokonfiguration och konfigurationsdata](lite-apply-demo-setup-config-data.md).
