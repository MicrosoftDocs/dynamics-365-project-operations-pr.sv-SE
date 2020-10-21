---
title: Lägga till en Azure-prenumeration i LCS-projekt
description: I det här ämnet finns information om hur du ansluter din Azure-prenumeration till ett LCS-projekt.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949101"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a>Lägga till en Azure-prenumeration i LCS-projekt

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Miljöer i molnet måste distribueras med hjälp av en befintlig Azure-prenumeration. I det här ämnet beskrivs du ansluter din befintliga Azure-prenumeration till ett LCS-projekt. 

## <a name="grant-admin-consent"></a>Bevilja administratörsmedgivande

1. I ditt LCS-projekt, i avsnittet **Miljöer**, väljer du **Microsoft Azure-inställningar**.

![Inställningar för Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. På sidan **Projektinsätllningar**, under fliken **Azure-anslutningsprogram**, väljer du **Auktorisera**. Detta gör att miljöer kan distribueras till det här projektet.

![Azure-anslutningsprogram](./media/2AzureConnectors.png)

3. Välj **Auktorisera** igen för att ge administratörsmedgivande.

![Bevilja administratörsmedgivande](./media/3GrantAdminConsent.png)

4. Godkänn begäran om behörighet.

![Godkänn begäran om behörighet](./media/4AcceptPermissionRequest.png)

Auktoriseringen har slutförts. 

![Autentiseringen är klar](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Tillhandahåll åtkomst till Dynamics Deployment Services för din Azure-prenumeration

1. Gå till [Microsoft Azure-fakturering](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) och välj din prenumeration. Dynamics Deployment Services måste få åtkomst till den här prenumerationen för att kunna distribuera miljöer.

![Information om Azure-prenumeration](./media/6AzureSubscription.png)

2. Välj **Åtkomstkontroll (IAM)** i navigeringsfönstret och välj sedan **Lägg till rolltilldelning**.
3. I skjutreglaget till höger väljer du **Deltagarroll** och i listan som visas söker du efter och väljer **Dynamics Deployment Services**. 
4. Välj **Spara**.

![Prenumerationsåtkomst](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Lägga till ett anslutningsprogram för prenumeration i ett LCS-projekt

1. I ditt LCS-projekt, på sidan **Microsoft Azure-inställningar**, väljer du **Lägg till** för att lägga till ett nytt anslutningsprogram.
2. Ange ditt ID för Azure-prenumerationen. Du hittar ditt ID för Azure-prenumerationen i [Azure-portalen](https://ms.portal.azure.com/) under **Inställningar** längst ned till vänster på skärmen.
3. I fältet **Konfigurera för att använda Azure Resource Manager** väljer du **Ja**.
4. Kontrollera att AAD-klientorganisationens domän för Azure-prenumerationen stämmer överens med den domänägande Azure-prenumerationen som du använder och välj **Nästa**.
5. På skärmen **Microsoft Azure-konfiguration** väljer du **Nästa** för att bekräfta. Om du får ett felmeddelande på den här sidan går du tillbaka till avsnittet [Tillhandahåll Dynamics Deployment Services åtkomst till Azure-prenumerationen](#provide) i det här ämnet och kontrollera att du har slutfört alla steg.
6. Hämta Azure-hanteringscertifikatet till en lokal mapp på datorn och överför det sedan till Azure-hanteringsportalen genom att gå till **Inställningar** > **Hanteringscertifikat**. Med det här certifikatet kan LCS kommunicera med Azure åt dig. Du kan hoppa över det här steget om din användare har åtkomst till prenumerationen.
7. Välj **Nästa**.
8. Välj Azure-regionen som du vill distribuera i och välj ett datacenter som är nära det ställe där du vill använda systemet.
9.  Välj **Anslut**.

Din Azure-prenumeration har upprättats. Nu kan du distribuera Dynamics 365 Finance-miljöer i molnet.


