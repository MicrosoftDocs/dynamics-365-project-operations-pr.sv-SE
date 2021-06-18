---
title: Använda demodata i en Finance molnvärdbaserad miljö
description: I det här ämnet beskrivs hur du använder demodata från Project Operations i en Dynamics 365 Finance-miljö i molnet.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7d8a198b3bfd71ae08bc338d17896519b5ffd6b8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000188"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="c2dff-103">Använda demodata i en Finance molnvärdbaserad miljö</span><span class="sxs-lookup"><span data-stu-id="c2dff-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="c2dff-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="c2dff-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2dff-105">Det här ämnet gäller endast Microsoft Dynamics 365 Finance-versionen 10.0.13 och kan endast utföras i en molnbaserad miljö.</span><span class="sxs-lookup"><span data-stu-id="c2dff-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="c2dff-106">Slutför stegen i det här ämnet **INNAN** du tillämpar kvalitetsuppdateringar av miljön.</span><span class="sxs-lookup"><span data-stu-id="c2dff-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="c2dff-107">I ditt LCS-projekt öppnar du sidan **Miljöinformation**.</span><span class="sxs-lookup"><span data-stu-id="c2dff-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="c2dff-108">Observera att den innehåller den information som behövs för att ansluta till miljön med hjälp av RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="c2dff-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![ miljöinformation](./media/1EnvironmentDetails.png)

<span data-ttu-id="c2dff-110">Den första uppsättningen av markerade autentiseringsuppgifter är autentiseringsuppgifterna till det lokala kontot och innehåller en hyperlänk till anslutningen till fjärrskrivbordet.</span><span class="sxs-lookup"><span data-stu-id="c2dff-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="c2dff-111">Autentiseringsuppgifterna inkluderar administratörens användarnamn och lösenord till miljön.</span><span class="sxs-lookup"><span data-stu-id="c2dff-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="c2dff-112">Den andra uppsättningen autentiseringsuppgifter används för att logga in på SQL-servern i den här miljön.</span><span class="sxs-lookup"><span data-stu-id="c2dff-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="c2dff-113">Fjärranslutning till miljön genom hyperlänken i **Lokala konton** och använd **autentiseringsuppgifterna till det lokala kontot** för att autentisera.</span><span class="sxs-lookup"><span data-stu-id="c2dff-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="c2dff-114">Gå till **Internet Information Services** > **Programpooler** > **AOSService** och stoppa tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c2dff-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="c2dff-115">Du stoppar tjänsten i detta skede så att du kan fortsätta att byta ut SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="c2dff-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Stoppa AOS](./media/2StopAOS.png)

4. <span data-ttu-id="c2dff-117">Gå till **Tjänster** och stoppa följande två artiklar:</span><span class="sxs-lookup"><span data-stu-id="c2dff-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="c2dff-118">Microsoft Dynamics 365 Unified Operations : batchhanteringstjänst</span><span class="sxs-lookup"><span data-stu-id="c2dff-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="c2dff-119">Microsoft Dynamics 365 Unified Operations: ramverk för import och export av data</span><span class="sxs-lookup"><span data-stu-id="c2dff-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Stoppa tjänster](./media/3StopServices.png)

5. <span data-ttu-id="c2dff-121">Öppna Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="c2dff-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="c2dff-122">Logga in med dina autentiseringsuppgifter till SQL-servern och använd axdb-administratörens användarnamn och lösenord från LCS-sidan **Information om miljöer**.</span><span class="sxs-lookup"><span data-stu-id="c2dff-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="c2dff-124">I objektutforskaren, **Databaser** och lokalisera **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="c2dff-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="c2dff-125">Du ersätter databasen med en ny databas som finns i [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="c2dff-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="c2dff-126">Kopiera zip-filen till den virtuella datorn som du har fjärråtkomst till och extrahera zip-innehåll.</span><span class="sxs-lookup"><span data-stu-id="c2dff-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="c2dff-127">I SQL Server Management Studio högerklickar du på **AxDB** och väljer sedan **Uppgifter** > **Återställ** > **Databas**.</span><span class="sxs-lookup"><span data-stu-id="c2dff-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Återställa databas](./media/5RestoreDatabase.png)

9. <span data-ttu-id="c2dff-129">Välj **Källenhet** och navigera till filen som extraherades ur den zip du kopierade.</span><span class="sxs-lookup"><span data-stu-id="c2dff-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Källenheter](./media/6SourceDevice.png)

10. <span data-ttu-id="c2dff-131">Välj **Alternativ** och välj sedan **Skriv över den befintliga databasen** och **Stäng befintliga anslutningar till måldatabasen**.</span><span class="sxs-lookup"><span data-stu-id="c2dff-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="c2dff-132">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2dff-132">Select **OK**.</span></span>

![Återställ inställningar](./media/7RestoreSetting.png)

<span data-ttu-id="c2dff-134">Du får en bekräftelse på att AXDB-återställningen har slutförts.</span><span class="sxs-lookup"><span data-stu-id="c2dff-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="c2dff-135">När du har fått bekräftelsemeddelandet kan du stänga SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="c2dff-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="c2dff-136">Gå tillbaka till **Internet Information Services** > **Programpooler** > **AOSService** och starta AOSService.</span><span class="sxs-lookup"><span data-stu-id="c2dff-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="c2dff-137">Gå till **Tjänster** och starta de två tjänster du stoppade tidigare.</span><span class="sxs-lookup"><span data-stu-id="c2dff-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="c2dff-138">Leta upp verktyget AdminUserProvisioning på den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c2dff-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="c2dff-139">Leta under K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="c2dff-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="c2dff-140">Kör .ext-filen med din användaradress i fältet **E-postadress**.</span><span class="sxs-lookup"><span data-stu-id="c2dff-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="c2dff-141">Välj **Skicka**.</span><span class="sxs-lookup"><span data-stu-id="c2dff-141">Select **Submit**.</span></span>

![Användarförsörjning för administratör](./media/8AdminUserProvisioning.png)

<span data-ttu-id="c2dff-143">Det här tar några minuter att slutföra.</span><span class="sxs-lookup"><span data-stu-id="c2dff-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="c2dff-144">Du bör få ett bekräftelsemeddelande om att administratörsanvändaren har uppdaterats.</span><span class="sxs-lookup"><span data-stu-id="c2dff-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="c2dff-145">Kör slutligen kommandotolken som administratör och utför iisreset</span><span class="sxs-lookup"><span data-stu-id="c2dff-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS-återställning](./media/9IISReset.png)

18. <span data-ttu-id="c2dff-147">Avsluta sessionen på fjärrskrivbordet och använd LCS-sidan **Information om miljö** för att logga in på miljön och bekräfta att den fungerar som den ska.</span><span class="sxs-lookup"><span data-stu-id="c2dff-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]