---
title: Lägg till en Azure-prenumeration i ett LCS-projekt
description: I det här ämnet finns information om hur du ansluter din Azure-prenumeration till ett LCS-projekt.
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a80c926ba67a1620e39d8c7677a05678454e6340
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880560"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="5c13c-103">Lägg till en Azure-prenumeration i ett LCS-projekt</span><span class="sxs-lookup"><span data-stu-id="5c13c-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="5c13c-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="5c13c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5c13c-105">Miljöer i molnet måste distribueras med hjälp av en befintlig Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="5c13c-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="5c13c-106">I det här ämnet beskrivs du ansluter din befintliga Azure-prenumeration till ett LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="5c13c-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="5c13c-107">Bevilja administratörsmedgivande</span><span class="sxs-lookup"><span data-stu-id="5c13c-107">Grant admin consent</span></span>

1. <span data-ttu-id="5c13c-108">I ditt LCS-projekt, i avsnittet **Miljöer**, väljer du **Microsoft Azure-inställningar**.</span><span class="sxs-lookup"><span data-stu-id="5c13c-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Inställningar för Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="5c13c-110">På sidan **Projektinsätllningar**, under fliken **Azure-anslutningsprogram**, väljer du **Auktorisera**.</span><span class="sxs-lookup"><span data-stu-id="5c13c-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="5c13c-111">Detta gör att miljöer kan distribueras till det här projektet.</span><span class="sxs-lookup"><span data-stu-id="5c13c-111">This allows environments to be deployed to this project.</span></span>

![Azure-anslutningsprogram](./media/2AzureConnectors.png)

3. <span data-ttu-id="5c13c-113">Välj **Auktorisera** igen för att ge administratörsmedgivande.</span><span class="sxs-lookup"><span data-stu-id="5c13c-113">Select **Authorize** again to provide admin consent.</span></span>

![Bevilja administratörsmedgivande](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="5c13c-115">Godkänn begäran om behörighet.</span><span class="sxs-lookup"><span data-stu-id="5c13c-115">Accept the permissions request.</span></span>

![Godkänn begäran om behörighet](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="5c13c-117">Auktoriseringen har slutförts.</span><span class="sxs-lookup"><span data-stu-id="5c13c-117">The authorization is now complete.</span></span> 

![Autentiseringen är klar](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="5c13c-119">Tillhandahåll åtkomst till Dynamics Deployment Services för din Azure-prenumeration</span><span class="sxs-lookup"><span data-stu-id="5c13c-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="5c13c-120">Gå till [Microsoft Azure-fakturering](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) och välj din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="5c13c-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="5c13c-121">Dynamics Deployment Services måste få åtkomst till den här prenumerationen för att kunna distribuera miljöer.</span><span class="sxs-lookup"><span data-stu-id="5c13c-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Information om Azure-prenumeration](./media/6AzureSubscription.png)

2. <span data-ttu-id="5c13c-123">Välj **Åtkomstkontroll (IAM)** i navigeringsfönstret och välj sedan **Lägg till rolltilldelning**.</span><span class="sxs-lookup"><span data-stu-id="5c13c-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="5c13c-124">I skjutreglaget till höger väljer du **Deltagarroll** och i listan som visas söker du efter och väljer **Dynamics Deployment Services**.</span><span class="sxs-lookup"><span data-stu-id="5c13c-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="5c13c-125">Välj **Spara**.</span><span class="sxs-lookup"><span data-stu-id="5c13c-125">Select **Save**.</span></span>

![Prenumerationsåtkomst](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="5c13c-127">Lägga till ett anslutningsprogram för prenumeration i ett LCS-projekt</span><span class="sxs-lookup"><span data-stu-id="5c13c-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="5c13c-128">I ditt LCS-projekt, på sidan **Microsoft Azure-inställningar**, väljer du **Lägg till** för att lägga till ett nytt anslutningsprogram.</span><span class="sxs-lookup"><span data-stu-id="5c13c-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="5c13c-129">Ange ditt ID för Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5c13c-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="5c13c-130">Du hittar ditt ID för Azure-prenumerationen i [Azure-portalen](https://ms.portal.azure.com/) under **Inställningar** längst ned till vänster på skärmen.</span><span class="sxs-lookup"><span data-stu-id="5c13c-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="5c13c-131">I fältet **Konfigurera för att använda Azure Resource Manager** väljer du **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5c13c-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="5c13c-132">Kontrollera att AAD-klientorganisationens domän för Azure-prenumerationen stämmer överens med den domänägande Azure-prenumerationen som du använder och välj **Nästa**.</span><span class="sxs-lookup"><span data-stu-id="5c13c-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="5c13c-133">På skärmen **Microsoft Azure-konfiguration** väljer du **Nästa** för att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="5c13c-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="5c13c-134">Om du får ett felmeddelande på den här sidan går du tillbaka till avsnittet [Tillhandahåll Dynamics Deployment Services åtkomst till Azure-prenumerationen](#provide) i det här ämnet och kontrollera att du har slutfört alla steg.</span><span class="sxs-lookup"><span data-stu-id="5c13c-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="5c13c-135">Ladda ner Azure Management Certificate till en lokal mapp på din dator.</span><span class="sxs-lookup"><span data-stu-id="5c13c-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="5c13c-136">Be administratören av din Azure-prenumeration att överföra certifikatet till Azure-hanteringsportalen genom att välja prenumerationen och gå till **Inställningar** > **Hantering av certifikat**.</span><span class="sxs-lookup"><span data-stu-id="5c13c-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="5c13c-137">Certifikatet gör att LCS kan kommunicera med Azure för din räkning.</span><span class="sxs-lookup"><span data-stu-id="5c13c-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="5c13c-138">Du kan hoppa över det här steget om din användare har åtkomst till prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5c13c-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="5c13c-139">Välj **Nästa**.</span><span class="sxs-lookup"><span data-stu-id="5c13c-139">Select  **Next**.</span></span>
8. <span data-ttu-id="5c13c-140">Välj Azure-regionen som du vill distribuera i och välj ett datacenter som är nära det ställe där du vill använda systemet.</span><span class="sxs-lookup"><span data-stu-id="5c13c-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="5c13c-141">Välj **Anslut**.</span><span class="sxs-lookup"><span data-stu-id="5c13c-141">Select  **Connect**.</span></span>

<span data-ttu-id="5c13c-142">Din Azure-prenumeration har upprättats.</span><span class="sxs-lookup"><span data-stu-id="5c13c-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="5c13c-143">Nu kan du distribuera Dynamics 365 Finance-miljöer i molnet.</span><span class="sxs-lookup"><span data-stu-id="5c13c-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
