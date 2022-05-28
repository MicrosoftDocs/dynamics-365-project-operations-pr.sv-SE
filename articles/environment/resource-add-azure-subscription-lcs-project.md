---
title: Lägg till en Azure-prenumeration i ett LCS-projekt
description: I det här ämnet finns information om hur du ansluter din Azure-prenumeration till ett LCS-projekt.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 839c510838b0bccb718b8ca8a4f71a1c46e7ea3f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595934"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Lägg till en Azure-prenumeration i ett LCS-projekt

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Miljöer i molnet måste distribueras med hjälp av en befintlig Azure-prenumeration. I det här ämnet beskrivs du ansluter din befintliga Azure-prenumeration till ett LCS-projekt. 

## <a name="grant-admin-consent"></a>Bevilja administratörsmedgivande

1. I ditt LCS-projekt, i avsnittet **Miljöer**, väljer du **Microsoft Azure-inställningar**.

![Inställningar för Microsoft Azure.](./media/1MicrosoftAzureSettings.png)

2. På sidan **Projektinsätllningar**, under fliken **Azure-anslutningsprogram**, väljer du **Auktorisera**. Detta gör att miljöer kan distribueras till det här projektet.

![Azure-anslutningsprogram.](./media/2AzureConnectors.png)

3. Välj **Auktorisera** igen för att ge administratörsmedgivande.

![Bevilja administratörsmedgivande.](./media/3GrantAdminConsent.png)

4. Godkänn begäran om behörighet.

![Godkänn begäran om behörighet.](./media/4AcceptPermissionRequest.png)

Auktoriseringen har slutförts. 

![Autentiseringen är klar.](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Tillhandahåll åtkomst till Dynamics Deployment Services för din Azure-prenumeration

1. Gå till [Microsoft Azure-fakturering](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) och välj din prenumeration. Dynamics Deployment Services måste få åtkomst till den här prenumerationen för att kunna distribuera miljöer.

![Information om Azure-prenumeration.](./media/6AzureSubscription.png)

2. Välj **Åtkomstkontroll (IAM)** i navigeringsfönstret och välj sedan **Lägg till rolltilldelning**.
3. I skjutreglaget till höger väljer du **Deltagarroll** och i listan som visas söker du efter och väljer **Dynamics Deployment Services**. 
4. Välj **Spara**.

![Prenumerationsåtkomst.](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Lägga till ett anslutningsprogram för prenumeration i ett LCS-projekt

1. I ditt LCS-projekt, på sidan **Microsoft Azure-inställningar**, väljer du **Lägg till** för att lägga till ett nytt anslutningsprogram.
2. Ange ditt ID för Azure-prenumerationen. Du hittar ditt ID för Azure-prenumerationen i [Azure-portalen](https://ms.portal.azure.com/) under **Inställningar** längst ned till vänster på skärmen.
3. I fältet **Konfigurera för att använda Azure Resource Manager** väljer du **Ja**.
4. Kontrollera att AAD-klientorganisationens domän för Azure-prenumerationen stämmer överens med den domänägande Azure-prenumerationen som du använder och välj **Nästa**.
5. På skärmen **Microsoft Azure-konfiguration** väljer du **Nästa** för att bekräfta. Om du får ett felmeddelande på den här sidan går du tillbaka till avsnittet [Tillhandahåll Dynamics Deployment Services åtkomst till Azure-prenumerationen](#provide) i det här ämnet och kontrollera att du har slutfört alla steg.
6. Ladda ner Azure Management Certificate till en lokal mapp på din dator. Be administratören av din Azure-prenumeration att överföra certifikatet till Azure-hanteringsportalen genom att välja prenumerationen och gå till **Inställningar** > **Hantering av certifikat**. Certifikatet gör att LCS kan kommunicera med Azure för din räkning. Du kan hoppa över det här steget om din användare har åtkomst till prenumerationen.
7. Välj **Nästa**.
8. Välj Azure-regionen som du vill distribuera i och välj ett datacenter som är nära det ställe där du vill använda systemet.
9.  Välj **Anslut**.

Din Azure-prenumeration har upprättats. Du kan nu distribuera Dynamics 365 Finance-tjänster som finns i molnet.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
