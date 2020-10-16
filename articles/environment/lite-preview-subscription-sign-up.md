---
title: Registrera dig för en förhandsversionsprenumeration
description: I det här ämnet finns information om hur du prenumererar på och distribuerar Project Operations enkel distribution – avtal till proforma-fakturering.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949099"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Registrera dig för en förhandsversionsprenumeration för enkel distribution – avtal till proforma-fakturering

I det här ämnet beskrivs hur du prenumererar partnererbjudandet för förhandsversion och distribuerar Dynamics 365 Project Operations enkel distribution – avtal till proforma-fakturering.

> [!NOTE]
> Processen kommer att ändras i kommande versioner av Project Operations.

## <a name="prerequisites"></a>Förutsättningar

- Du får ett e-postmeddelande med en inbjudan att delta i förhandsversionen. Du kan begära en förhandsversion på [webbplatsen för Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Den användare som distribuerar förhandsversionen måste ha behörighet som global administratör av Azure-klient.
- Den användare som distribuerar förhandsversionen kommer att behöva ett telefonnummer och ett giltigt kreditkort. Under registreringen får du inga avgifter för kortet i sex månader. Efter sex månader måste du avbryta prenumerationen. 
- Granska alla villkor.

## <a name="subscribe"></a>Prenumerera

När du får ett godkännande av en [begäran av förhandsversion](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) får du två erbjudanden från Microsoft via e-post. Med de här erbjudandena kan du distribuera förhandsversionen av Project Operations:

- Utvärdering av förhandsversionen av Dynamics 365 Customer Service – engångskod
- Dynamics 365 Project Operations – utvärdering av förhandsversion

### <a name="dynamics-365-customer-service-paid-offer"></a>Betalprenumeration på Dynamics 365 Customer Service

1. Använd ett InPrivate-/inkognitofönster i webbläsaren, använd den första erbjudandekoden för Dynamics 365 Customer Service. Du behöver följande om du vill registrera dig för Customer Service:

- Ett telefonnummer
- Ett kreditkort. När du registrerar dig får du inga avgifter för kortet i sex månader. Efter sex månader måste du avbryta prenumerationen.
- Granska alla villkor.

2. Tillhandahåll kontaktuppgifter.

![Kontaktinformation](./media/1ContactInformation.png)

3. Ange uppgifter om ny klientorganisation.

![Skapa användar-ID](./media/2CreateUserID.png)

4. Verifiera din identitet, spara ditt nya användar-ID och välj sedan **Konfigurera**.

![Spara information](./media/3SaveInfo.png)

5. Slutför registreringen av kreditkortet och granska alla villkor. 

![Slutför kreditkort](./media/4CompleteCreditCard.png)

![Utcheckning med kreditkort](./media/5CreditCardCheckout.png)

![Spara order](./media/6SaveOrder.png)

![Kreditkortsbekräftelse](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>Avbryt erbjudandet gällande Dynamics 365 Customer Service Enterprise

Erbjudandet gällande Dynamics 365 Customer Service Enterprise är gratis i sex månader. Erbjudandet ska förnyas till fullpris efter sex månader. Följ instruktionerna nedan om du vill avbryta innan förnyelsedatumet. 

> [!NOTE]
> När du har slutfört de här stegen kommer du inte längre att kunna använda miljön i den allmänt tillgängliga förhandsversionen av Project Operations.

1. Gå till [Administratörsportal](https://admin.microsoft.com/) och under **Fakturering** väljer du **Dina produkter**.

![Administratörsportalen, sidan Dina produkter](./media/8AdminPortal.png)

2. Välj **Erbjudande gällande Dynamics 365 Customer Service Enterprise**.

![Avbryta prenumerationen](./media/9CancelSubscription.png)

3. Välj **Inställningar** > **Åtgärder** > **Avbryt prenumeration**.
4. I formuläret **Avbryt prenumeration** anger du information i de obligatoriska fälten.
5. Välj **Avbryt** > **Prenumeration.**

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – utvärdering av förhandsversion

1. Hämta det andra erbjudandet, Utvärdering av Dynamics 365 Project Operations med URL tillhandahållen i ditt välkomstmeddelande.

![Hämta erbjudande 2](./media/10RedeemOffer2.png)

2. Kontrollera att du är inloggad som en användare som tillhör samma organisation som prenumererade genom den första erbjudandekoden och fortsätt sedan med att hämta erbjudandet. 
3. Välj **Ja, lägg till det i mitt konto**.

![Lägg till i konto](./media/11AddToAccount.png)

![Skärmen Prova nu](./media/12TryNow.png)

![Orderinformation](./media/13Confirmation.png)

## <a name="assign-licenses"></a>Tilldela licenser

> [!IMPORTANT]
> Du måste ha administratörsbehörighet till organisationens Office 365-portal för att kunna utföra följande steg.

1. Gå till [Microsoft 365 administratörscenter](https://portal.office.com/) för att tilldela licenser till dina användare.

![Startsida för administratörscenter](./media/14AdminPortal.png)

2. På sidan **Aktiva användare** väljer du de användare som du vill tilldela en licens till.

![Tilldela licenser](./media/15AssignLicenses.png)

3. Kontrollera att licensen för **Customer Service Enterprise** och **Project Operations** har valts och välj **Spara ändringar**.

## <a name="create-a-new-cds-environment"></a>Skapa en ny CDS-miljö

Tillhandahåll en ny distributionsmiljö för Project Operations CDS-distribution genom att följa anvisningarna i ämnet [CDS-distributionsmodell](lite-deployment.md).

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Installera en CDS-konfiguration och konfigurera demodata

Installera CDS-konfigurationen och konfigurera demodata genom att följa anvisningarna i ämnet [Tillämpa demokonfiguration och konfigurationsdata](lite-apply-demo-setup-config-data.md).
