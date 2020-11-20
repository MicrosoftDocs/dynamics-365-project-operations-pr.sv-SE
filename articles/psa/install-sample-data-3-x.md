---
title: Installation av exempeldata
description: I det här ämnet finns information om hur du installerar exempeldata i Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 3c9cca7aa9d85bb38e48820b361ba07923ceddbd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132445"
---
# <a name="sample-data-installation-for-the-project-service-application"></a><span data-ttu-id="32618-103">Installationen av exempeldata data för Project Service-programmet</span><span class="sxs-lookup"><span data-stu-id="32618-103">Sample data installation for the Project Service application</span></span>

<span data-ttu-id="32618-104">För att hjälpa dig att bygga upp dina egna demo-miljöer tillhandahåller Microsoft hämtningsbara exempeldatapaket som visar upp funktionerna i appen.</span><span class="sxs-lookup"><span data-stu-id="32618-104">To help you build your own demo environments, Microsoft provides downloadable sample data packages that showcase the capabilities of your apps.</span></span> <span data-ttu-id="32618-105">Det finns två typer av exempeldatapaketen:</span><span class="sxs-lookup"><span data-stu-id="32618-105">There are two types of sample data packages:</span></span>
- <span data-ttu-id="32618-106">referens/installationsdata</span><span class="sxs-lookup"><span data-stu-id="32618-106">reference/setup data</span></span>
- <span data-ttu-id="32618-107">demodata (referens/installations- och transaktionsdata såsom arbetsorder och projekt)</span><span class="sxs-lookup"><span data-stu-id="32618-107">demo data (reference/setup and transactional data such as work orders and projects)</span></span>

<span data-ttu-id="32618-108">Exempeldatapaket **referens** kan hämtas i tre olika paket så att du endast kan installera data för Project Service, eller bara för Field Service eller du kan installera exempeldata för båda programmen på samma gång.</span><span class="sxs-lookup"><span data-stu-id="32618-108">The sample **reference** data packages are downloadable in three different packages, so you can install data only for Project Service, or only for Field Service, or you can install sample data for both applications at once.</span></span>

<span data-ttu-id="32618-109">Exempeldatapaketen inställning/referens är:</span><span class="sxs-lookup"><span data-stu-id="32618-109">The sample setup/reference data packages are:</span></span>

- [<span data-ttu-id="32618-110">**V902PSMasterData** - endast Project Service version 3.x</span><span class="sxs-lookup"><span data-stu-id="32618-110">**V902PSMasterData** - Project Service version 3.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [<span data-ttu-id="32618-111">**V902FSMasterData** - endast Field Service version 8.x</span><span class="sxs-lookup"><span data-stu-id="32618-111">**V902FSMasterData** - Field Service version 8.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [<span data-ttu-id="32618-112">**V902FPSMasterData** - Field Service 8.x och Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="32618-112">**V902FPSMasterData** - Field Service 8.x and Project Service 3.x</span></span>](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

<span data-ttu-id="32618-113">Det senaste **demonstrations** datapaketet är:</span><span class="sxs-lookup"><span data-stu-id="32618-113">The latest **demo** data package is:</span></span>

 - [<span data-ttu-id="32618-114">**FPSDemoData** - Field Service 8.x och Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="32618-114">**FPSDemoData** - Field Service 8.x and Project Service 3.x</span></span>](https://aka.ms/fpsdemodatapackage)

   <span data-ttu-id="32618-115">Installationsinstruktioner skiljer sig något i användare för att skapa och konfigurera avsnittet men resten är desamma som i föregående [**blogginlägg**](https://aka.ms/fpsdemodatablog).</span><span class="sxs-lookup"><span data-stu-id="32618-115">Installation instructions differ slightly in the users to create and configure section but the rest is the same as in the previous [**blog post**](https://aka.ms/fpsdemodatablog).</span></span> <span data-ttu-id="32618-116">Det här paketet har en lägre demonstrationsdatauppsättning och tar cirka tre timmar att installera.</span><span class="sxs-lookup"><span data-stu-id="32618-116">This package features a reduced demo data set and takes approximately 3 hours to install.</span></span>

<span data-ttu-id="32618-117">Dessa exempeldatapaket finns endast tillgängliga på engelska.</span><span class="sxs-lookup"><span data-stu-id="32618-117">These sample data packages are available in English only.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32618-118">**Det går inte att avinstallera exempeldata.**</span><span class="sxs-lookup"><span data-stu-id="32618-118">**There is no way to uninstall the sample data.**</span></span> <span data-ttu-id="32618-119">Du bör endast installera dessa paket på demonstration, evaluation, träning och testsystem.</span><span class="sxs-lookup"><span data-stu-id="32618-119">You should only install these packages on demonstration, evaluation, training, or test systems.</span></span> <span data-ttu-id="32618-120">Observera att installera ett individuellt paket och installerar sedan det andra individuella paketet stöds inte.</span><span class="sxs-lookup"><span data-stu-id="32618-120">Also note that installing an individual package, and then installing the other individual package, is not supported.</span></span> <span data-ttu-id="32618-121">(Med andra ord, du kan inte installera **FSMasterData** följt av **PSMasterData**, eller tvärtom.) Om du tycker att du behöver exempeldata för båda programmen när som helst i framtiden bör du installera paketet **v902FPSMasterData**.</span><span class="sxs-lookup"><span data-stu-id="32618-121">(In other words, you can't install **FSMasterData** followed by **PSMasterData**, or vice versa.) If you see yourself needing sample data for both applications at any point in the future, you should install the **v902FPSMasterData** package.</span></span>

<span data-ttu-id="32618-122">När du installerar exempeldatapaket utför installationsprocessen följande åtgärder:</span><span class="sxs-lookup"><span data-stu-id="32618-122">When you install any of the sample data packages, the installation process performs the following actions:</span></span>

- <span data-ttu-id="32618-123">Skapar eller anger standardparametrar för att använda Project Service, Field Service eller båda programmen (om tillämpligt).</span><span class="sxs-lookup"><span data-stu-id="32618-123">Creates or sets default parameters for using Project Service, Field Service, or both applications (if applicable).</span></span>

- <span data-ttu-id="32618-124">Importerar exempeldata program såsom bokningsbara resurser, programspecifika roller, försäljning och kostnadsprislistor, organisationsenheter, försäljningsprocessposter och andra entiteter för att demonstrera viktiga funktioner.</span><span class="sxs-lookup"><span data-stu-id="32618-124">Imports sample data for the applications, such as bookable resources, application-specific roles, sales and cost price lists, organizational units, sales process records, and other entities to demonstrate key capabilities.</span></span>  

<span data-ttu-id="32618-125">Med **demonstrationsdata** paketet får du ovan och ytterligare transaktionsdata såsom arbetsorder och projekt.</span><span class="sxs-lookup"><span data-stu-id="32618-125">With the **demo data** package, you get the above and additional transactional data such as work orders and projects.</span></span>

<span data-ttu-id="32618-126">Undrar du vilka funktioner du kan demonstrera med exempeldata?</span><span class="sxs-lookup"><span data-stu-id="32618-126">Wondering what capabilities you can demo with the sample data?</span></span> <span data-ttu-id="32618-127">Se Fabrikam Robotics fiktiva scenario i [tekniska anteckningar](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="32618-127">See the Fabrikam Robotics fictitious scenario in [Technical notes](#technical-notes).</span></span>

<span data-ttu-id="32618-128">Om du har frågor om hur du installerar exempeldatapaketen [skicka ett e-postmeddelande till fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="32618-128">If you have questions about installing these sample data packages, [send us an email at fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span></span>

## <a name="requirements"></a><span data-ttu-id="32618-129">Krav</span><span class="sxs-lookup"><span data-stu-id="32618-129">Requirements</span></span>

<span data-ttu-id="32618-130">Installationsprotokollet förutsätter följande om din målinstans (org):</span><span class="sxs-lookup"><span data-stu-id="32618-130">The installation protocol assumes the following about your target instance (org):</span></span>

- <span data-ttu-id="32618-131">Grundspråk är engelska och basvalutan amerikanska dollar (USD, $)</span><span class="sxs-lookup"><span data-stu-id="32618-131">Base language is English and base currency is US dollar (USD,$).</span></span>

- <span data-ttu-id="32618-132">Organisationen har ingen Project Service- eller Field Service-data redan eller har bara enkla standarddata som ingår i alla nya organisationer</span><span class="sxs-lookup"><span data-stu-id="32618-132">The org has no Project Service or Field Service data already, or only has barebones default data that comes with any new org.</span></span>

- <span data-ttu-id="32618-133">Rätt version av affärsprogrammet är redan installerat:</span><span class="sxs-lookup"><span data-stu-id="32618-133">The correct version of the business application is already installed:</span></span>
       
    - <span data-ttu-id="32618-134">**För FPSDemoData eller v902FPSMasterData:** organisationen har Field Service version 8.x och Project Service version 3.x installerat.</span><span class="sxs-lookup"><span data-stu-id="32618-134">**For FPSDemoData or v902FPSMasterData:** The org has Field Service version 8.x and Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="32618-135">**För v902PSMasterData:** organisationen har Project Service version 3.x installerat.</span><span class="sxs-lookup"><span data-stu-id="32618-135">**For v902PSMasterData:** The org has Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="32618-136">**För v902FSMasterData:** organisationen har Field Service version 8.x installerat.</span><span class="sxs-lookup"><span data-stu-id="32618-136">**For v902FSMasterData:** The org has Field Service version 8.x installed.</span></span>

> [!NOTE]
> <span data-ttu-id="32618-137">Om du behöver installera exempeldata ovanpå en befintlig utvärderingsversion eller demomiljö av Project Service och Field Service som redan innehåller data (vilket inte rekommenderas) måste du avbryta säkerhetsprövningarna som utförs av installationsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="32618-137">If you need to install the sample data on top of an existing Project Service and Field Service trial or demo environment that already has data (not recommended), you'll need to suspend the safety prechecks performed by the installer.</span></span> <span data-ttu-id="32618-138">Mer information finns i tekniska anteckningar nedan.</span><span class="sxs-lookup"><span data-stu-id="32618-138">For more information, see the technical notes below.</span></span>

## <a name="prepare-for-installation"></a><span data-ttu-id="32618-139">Förbered installation</span><span class="sxs-lookup"><span data-stu-id="32618-139">Prepare for installation</span></span>

<span data-ttu-id="32618-140">Du måste köra installationsprogrammet på en dator med den senaste versionen av Windows (helst Windows 10).</span><span class="sxs-lookup"><span data-stu-id="32618-140">You need to run the installer on a computer with a recent version of Windows (Windows 10 preferred).</span></span>

<span data-ttu-id="32618-141">Du bör planera för datorn att vara ansluten till ett nätverk och för att installationen ska köras i upp till **1 timme** för **inställning/referensdata**.</span><span class="sxs-lookup"><span data-stu-id="32618-141">You should plan for the computer to remain connected to a network, and for the installation to run for up to **1 hour** for **setup/reference data**.</span></span> <span data-ttu-id="32618-142">(Installationen tar normalt ungefär 30 minuter för **FPSMasterData**, som innehåller exempeldata för båda programmen.) För **FPSDemoData** tar installationen runt **3 timmar**.</span><span class="sxs-lookup"><span data-stu-id="32618-142">(Normally the installation takes around 30 minutes for **FPSMasterData**, which includes sample data for both applications.) For the **FPSDemoData**, the installation will take around **3 hours**.</span></span>

<span data-ttu-id="32618-143">Datorn bör ha funktionen skärmsläckare avstängd.</span><span class="sxs-lookup"><span data-stu-id="32618-143">The computer should have the screen saver function turned off.</span></span> <span data-ttu-id="32618-144">I annat fall kan sessionens autentiseringsuppgifter för installationen förloras när skärmsläckaren aktiveras (såvida inte du håller sessionen aktiv).</span><span class="sxs-lookup"><span data-stu-id="32618-144">Otherwise, session credentials for the installation may be lost when the screen saver engages (unless you keep your session active throughout).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="32618-145">![Bild på inställningar för skärmsläckare med skärmsläckaren avstängd](media/sample-data-1.png)</span><span class="sxs-lookup"><span data-stu-id="32618-145">![Screenshot of screen saver settings, with screen saver turned off](media/sample-data-1.png)</span></span>

## <a name="download-and-unpack"></a><span data-ttu-id="32618-146">Hämta och packa upp</span><span class="sxs-lookup"><span data-stu-id="32618-146">Download and unpack</span></span>

<span data-ttu-id="32618-147">Installationsprogrammet för Project Service och Field Service exempeldata distribueras som en självextraherande körbar fil.</span><span class="sxs-lookup"><span data-stu-id="32618-147">The Project Service and Field Service sample data installer is distributed as a self-extracting executable.</span></span> <span data-ttu-id="32618-148">Filnamnen kan variera beroende på exempeldatapaketet men annars är stegen desamma oavsett vilka paket du installerar.</span><span class="sxs-lookup"><span data-stu-id="32618-148">The file names may vary depending on the sample data package, but otherwise the steps are the same no matter which package you install.</span></span>

<span data-ttu-id="32618-149">När du har hämtat ett paket, kör exe.-filen och acceptera villkoren för att packa upp komprimerade zip-filen.</span><span class="sxs-lookup"><span data-stu-id="32618-149">After downloading a package, run the .exe file, and then accept terms and conditions to unpack the compressed zip file.</span></span> <span data-ttu-id="32618-150">Du måste sedan extrahera innehållet till den filen till en mapp som du väljer på din dator.</span><span class="sxs-lookup"><span data-stu-id="32618-150">You then need to extract contents of that file to a folder on the computer.</span></span>

<span data-ttu-id="32618-151">Beroende på operativsystem och säkerhetsinställningar kan behöva utföra följande steg när du packat upp zip-filen:</span><span class="sxs-lookup"><span data-stu-id="32618-151">Depending on the operating system and security settings, you may need to perform the following steps after unpacking the zip file:</span></span>

1. <span data-ttu-id="32618-152">Söka efter och högerklicka på **FPSDemoData.dll**-file i mappen **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="32618-152">Find and right-click the **FPSDemoData.dll** file in the **v902FPSMasterData** / **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="32618-153">Välj **avblockera**.</span><span class="sxs-lookup"><span data-stu-id="32618-153">Choose **Unblock**.</span></span>

3. <span data-ttu-id="32618-154">Välj **tillämpa**.</span><span class="sxs-lookup"><span data-stu-id="32618-154">Select **Apply**.</span></span>

4. <span data-ttu-id="32618-155">Välj **OK**.</span><span class="sxs-lookup"><span data-stu-id="32618-155">Select **OK**.</span></span>


## <a name="create-or-configure-users"></a><span data-ttu-id="32618-156">Skapa eller konfigurera användare</span><span class="sxs-lookup"><span data-stu-id="32618-156">Create or configure users</span></span>

<span data-ttu-id="32618-157">**FPSDemoData**-paketet kräver sex användare när **FPSMasterData**-paketet kräver en användare.</span><span class="sxs-lookup"><span data-stu-id="32618-157">The **FPSDemoData** package requires six users while **FPSMasterData** packages require one user.</span></span> <span data-ttu-id="32618-158">Referera till korrekt för ditt exempeldatapaketet.</span><span class="sxs-lookup"><span data-stu-id="32618-158">Refer to the correct one for your sample data package.</span></span>

## <a name="create-or-configure-users---setupreference-data-packages"></a><span data-ttu-id="32618-159">Skapa eller konfigurera användare - inställning/referensdatapaket</span><span class="sxs-lookup"><span data-stu-id="32618-159">Create or configure users - setup/reference data packages</span></span>

<span data-ttu-id="32618-160">**FPSMasterData**-paketet har utformats för att installera med en användare med namnet Spencer Low med inställningar som beskrivs här.</span><span class="sxs-lookup"><span data-stu-id="32618-160">The **FPSMasterData** package is designed to install with one user named Spencer Low with the settings described here.</span></span> <span data-ttu-id="32618-161">Om du vill installera paketet korrekt behöver du skapa (eller tillfälligt byta namn) användare i din miljö så att de matchar konfigurationen för inkommande konfiguration av exempeldata.</span><span class="sxs-lookup"><span data-stu-id="32618-161">To install the package correctly, you need to create (or temporarily rename) users in your environment to match the incoming sample data configuration.</span></span>

<span data-ttu-id="32618-162">Skapa eller konfigurera användare genom att gå till **inställningar** > **säkerhet** > **användare** och gör följande:</span><span class="sxs-lookup"><span data-stu-id="32618-162">To create or configure users, go to **Settings** > **Security** > **Users**, and do the following:</span></span>

1. <span data-ttu-id="32618-163">Ange UserFullname=”Spencer Low” med användarnamn ”spencerl” (**gemener**) till rollerna Projektledare och Metodansvarig.</span><span class="sxs-lookup"><span data-stu-id="32618-163">Set UserFullname="Spencer Low" with username "spencerl" (**lowercase**) to the Project Manager and Practice Manager roles.</span></span>

2. <span data-ttu-id="32618-164">Välj användaren **Spencer Low** och välj sedan **Hantera roller**.</span><span class="sxs-lookup"><span data-stu-id="32618-164">Select the **Spencer Low** user, and then select **Manage Roles**.</span></span> <span data-ttu-id="32618-165">Leta upp och markera roll **systemadministratören** och markera **OK** ge fullständig administratörsrättigheter till Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="32618-165">Find and select the **System Administrator** role, and then select **OK** to grant full admin rights to Spencer Low.</span></span> <span data-ttu-id="32618-166">Det här steget är nödvändigt för att säkerställa att exempelposter skapas med rätt ägarskap och därför fyller i vyer på rätt sätt.</span><span class="sxs-lookup"><span data-stu-id="32618-166">This step is necessary to ensure that sample records are created with the correct user ownership and therefore populate views correctly.</span></span>

3. <span data-ttu-id="32618-167">Från det nedladdade paketet måste du uppdatera en datamappningsfil med e-postadresser till standardanvändarkontext.</span><span class="sxs-lookup"><span data-stu-id="32618-167">From the downloaded package, you need to update a data mapping file with email addresses of the default user context.</span></span> <span data-ttu-id="32618-168">Det gör du genom att öppna **PkgFolder**, hitta och öppna **ImportUserMapFile.xml**-filen i Notepad (eller Visual Studio eller en annan XML-redigerare).</span><span class="sxs-lookup"><span data-stu-id="32618-168">To do this, open **PkgFolder**, and then find and open the **ImportUserMapFile.xml** file in Notepad (or Visual Studio or another XML editor).</span></span> <span data-ttu-id="32618-169">Ange fältet **DefaultUserToMapTo =** till Spencer Low användarens e-postadress.</span><span class="sxs-lookup"><span data-stu-id="32618-169">Set the **DefaultUserToMapTo=** field to the email address of the Spencer Low user.</span></span>

4. <span data-ttu-id="32618-170">Om du inte använder Spencer Low med användarnamn **spencerl**, måste du uppdatera en ytterligare fil.</span><span class="sxs-lookup"><span data-stu-id="32618-170">If you aren't using Spencer Low with username **spencerl**, you need to update an additional file.</span></span> <span data-ttu-id="32618-171">Öppna **DemoDataPreImportConfig.xml**-filen och sök **userstocreateandconfigure**-etiketten.</span><span class="sxs-lookup"><span data-stu-id="32618-171">Open the **DemoDataPreImportConfig.xml** file, and then find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="32618-172">Uppdatera etiketten **\<login\>** med användarnamnet för din Spencer Low användare.</span><span class="sxs-lookup"><span data-stu-id="32618-172">Update the **\<login\>** tag with the username of your Spencer Low user.</span></span> <span data-ttu-id="32618-173">Mer information finns i [tekniska anteckningar](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="32618-173">For additional details, see [Technical notes](#technical-notes).</span></span>

## <a name="create-or-configure-users---demo-data-package"></a><span data-ttu-id="32618-174">Skapa eller konfigurera användare - demonstrationsdatapaket</span><span class="sxs-lookup"><span data-stu-id="32618-174">Create or configure users - demo data package</span></span>

<span data-ttu-id="32618-175">Demonstrationsdatapaketet kräver sex användare.</span><span class="sxs-lookup"><span data-stu-id="32618-175">The demo data package requires six users.</span></span> <span data-ttu-id="32618-176">För att uppdateringen ska installeras på rätt sätt, gör du följande:</span><span class="sxs-lookup"><span data-stu-id="32618-176">For the package to install correctly, do the following:</span></span>

 1. <span data-ttu-id="32618-177">Skapa eller tillfälligt byta namn på befintliga användare så att de överensstämmer med konfiguration av inkommande exempeldata genom att gå till **inställningar** > **eller** > **användare**.</span><span class="sxs-lookup"><span data-stu-id="32618-177">Create or temporarily rename existing users to match incoming sample data configuration by going to **Settings** > **Security** > **Users**.</span></span>
 
    <span data-ttu-id="32618-178">Dessa två roller behövs endast för personbaserade demonstrationer.</span><span class="sxs-lookup"><span data-stu-id="32618-178">These roles are only needed for persona-based demos.</span></span>  
    - <span data-ttu-id="32618-179">Användarens fullständiga namn ="David So" som Field Service-tekniker</span><span class="sxs-lookup"><span data-stu-id="32618-179">User Fullname="David So" as Field Service Technician</span></span>   
    - <span data-ttu-id="32618-180">Användarens fullständiga namn = ”Johan Reding” som Customer Service och Field Service-avsändare</span><span class="sxs-lookup"><span data-stu-id="32618-180">User Fullname="Jamie Reding" as Customer Service & Field Service Dispatcher</span></span>   
    - <span data-ttu-id="32618-181">Användarens fullständiga namn = ”Molly Clark” som kontohanterare</span><span class="sxs-lookup"><span data-stu-id="32618-181">User Fullname="Molly Clark" as Account Manager</span></span>   
    - <span data-ttu-id="32618-182">Användarens fullständiga namn = ”Spencer Low” som övare och projektledare</span><span class="sxs-lookup"><span data-stu-id="32618-182">User Fullname="Spencer Low" as Practice and Project Manager</span></span>  
    - <span data-ttu-id="32618-183">Användarens fullständiga namn = ”Veronica Quek” som Teammedlem</span><span class="sxs-lookup"><span data-stu-id="32618-183">User Fullname="Veronica Quek" as Team Member</span></span>   
    - <span data-ttu-id="32618-184">Användarens fullständiga namn = ”William Contoso”</span><span class="sxs-lookup"><span data-stu-id="32618-184">User Fullname="William Contoso"</span></span>
  
2. <span data-ttu-id="32618-185">Tilldela de sex användarna ovanför administratörsrollen i syfte att importera demonstrationsdata så att provposter importeras korrekt.</span><span class="sxs-lookup"><span data-stu-id="32618-185">For the purposes of demo data import, assign the six users above the Administrator role so sample records import correctly.</span></span> 

3. <span data-ttu-id="32618-186">Öppna **PkgFolder** och sök efter och öppna **ImportUserMapFile.xml**.</span><span class="sxs-lookup"><span data-stu-id="32618-186">Open **PkgFolder** and then find and open **ImportUserMapFile.xml**.</span></span> <span data-ttu-id="32618-187">Uppdatera fälten **ny=** till e-postadresser för motsvarande användare i systemet.</span><span class="sxs-lookup"><span data-stu-id="32618-187">Update the **New=** fields to the email addresses of corresponding Users in your system.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="32618-188">![Skärmbild av UserMapFile](media/sample-data-7.png)</span><span class="sxs-lookup"><span data-stu-id="32618-188">![Screen shot of UserMapFile](media/sample-data-7.png)</span></span>

4. <span data-ttu-id="32618-189">Om användarens fullständiga namn ”Spencer Low” har en annan användare än **”spencerl”** måste du uppdatera en ytterligare fil.</span><span class="sxs-lookup"><span data-stu-id="32618-189">If your "Spencer Low" full name user has a different user ID than **"spencerl"**, then you need to update an additional file.</span></span> <span data-ttu-id="32618-190">Öppna **DemoDataPreImportConfig.xml** och sök **userstocreateandconfigure**-etiketten.</span><span class="sxs-lookup"><span data-stu-id="32618-190">Open **DemoDataPreImportConfig.xml** and find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="32618-191">Uppdatera etiketten **\<login\>** med loginId (skiftlägeskänsligt).</span><span class="sxs-lookup"><span data-stu-id="32618-191">Update the **\<login\>** tag with the loginId (case-sensitive).</span></span> 

5. <span data-ttu-id="32618-192">Den första användarens kalender (i etiketten **userstocreateandconfigure**) används för att fylla arbetstimmarna för alla bokningsbara resurser på import av demodata.</span><span class="sxs-lookup"><span data-stu-id="32618-192">The first user's calendar (in the **userstocreateandconfigure** tag) is used to populate the work hours for all bookable resources on import of demo data.</span></span> <span data-ttu-id="32618-193">Gå till **inställningar** > **säkerhet** > **användare**, hitta användaren ”Spencer Low” och öppna alternativet ”arbetstimmar”.</span><span class="sxs-lookup"><span data-stu-id="32618-193">Navigate to **Settings** > **Security** > **Users**, find your "Spencer Low" user, and open the "Work Hours" option.</span></span> <span data-ttu-id="32618-194">Redigera befintliga arbetstimmar genom att välja alternativet **hela återkommande veckoschema från början till slut**.</span><span class="sxs-lookup"><span data-stu-id="32618-194">Edit the existing work hours, selecting the **Entire recurring weekly schedule from start to end** option.</span></span> <span data-ttu-id="32618-195">Kontrollera att **arbetstid anges till 8:00 - 17:00 (9 timmar) måndag till fredag och den tidszon som har angetts till Pacific Time (USA och Kanada)**.</span><span class="sxs-lookup"><span data-stu-id="32618-195">Ensure the **Work hours are set to 8 AM - 5 PM (9 Hours), Monday to Friday and with the Timezone set to Pacific Time (US & Canada)**.</span></span> <span data-ttu-id="32618-196">Detta görs för att säkerställa att alla projekt och schematavlor visas som förväntat.</span><span class="sxs-lookup"><span data-stu-id="32618-196">This is needed to ensure that the Project and Schedule board show as expected.</span></span>

<span data-ttu-id="32618-197">**Rekommendation:** Överväg att skapa en säkerhetskopia av organisationen nu, om du skulle behöva återställa till en utgångspunkt om något går fel under installationen av exempeldata.</span><span class="sxs-lookup"><span data-stu-id="32618-197">**Recommendation:** Consider creating a backup of your org now, in case you need to revert to your starting point if something goes wrong during the sample data installation.</span></span> <span data-ttu-id="32618-198">Mer information finns i [Säkerhetskopiera och återställ instanser](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span><span class="sxs-lookup"><span data-stu-id="32618-198">For more information, see [Backup and restore instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).</span></span>

## <a name="run-the-package-deployer"></a><span data-ttu-id="32618-199">Kör Package Deployer</span><span class="sxs-lookup"><span data-stu-id="32618-199">Run the Package Deployer</span></span>

1. <span data-ttu-id="32618-200">Sök efter och kör **PackageDeployer.exe** i mappen **v902FPSMasterData** ELLER **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="32618-200">Find and run **PackageDeployer.exe** in the **v902FPSMasterData** OR **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="32618-201">Acceptera villkoren</span><span class="sxs-lookup"><span data-stu-id="32618-201">Accept the terms and conditions.</span></span>

3. <span data-ttu-id="32618-202">I nästa fönster:</span><span class="sxs-lookup"><span data-stu-id="32618-202">On the next window:</span></span>

   <span data-ttu-id="32618-203">a.</span><span class="sxs-lookup"><span data-stu-id="32618-203">a.</span></span> <span data-ttu-id="32618-204">Välj distributionstyp **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="32618-204">Select deployment type **Office 365**.</span></span>

   <span data-ttu-id="32618-205">b.</span><span class="sxs-lookup"><span data-stu-id="32618-205">b.</span></span> <span data-ttu-id="32618-206">Använd användare och lösenord för systemadministratören som konfigurerats i ”Skapa eller konfigurera användare” (”Spencer Low” med ”spencerl” användarnamn).</span><span class="sxs-lookup"><span data-stu-id="32618-206">Use the user and password of the system administrator user configured in "Create or configure users" ("Spencer Low" with "spencerl" username).</span></span>

   <span data-ttu-id="32618-207">c.</span><span class="sxs-lookup"><span data-stu-id="32618-207">c.</span></span> <span data-ttu-id="32618-208">Kontrollera att **Visa listan över tillgängliga organisationer** är markerad.</span><span class="sxs-lookup"><span data-stu-id="32618-208">Make sure **Display list of available organizations** is selected.</span></span>

      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="32618-209">![Bild på Package Deployer-fönstret med ”visa listan över tillgängliga företag” markerad](media/sample-data-2.png)</span><span class="sxs-lookup"><span data-stu-id="32618-209">![Screenshot of Package Deployer window with "Display list of available organizations" selected](media/sample-data-2.png)</span></span>

4. <span data-ttu-id="32618-210">Välj organisation när du vill installera exempeldata.</span><span class="sxs-lookup"><span data-stu-id="32618-210">Select the organization where you want to install the sample data.</span></span>

5. <span data-ttu-id="32618-211">Välj **nästa** tills du ser dialogrutan **Inställning av demonstrationsdata**.</span><span class="sxs-lookup"><span data-stu-id="32618-211">Select **Next** until you see the **Demo Data Setup** dialog.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="32618-212">![Bild på statusfönstret för installation av demonstrationsdata](media/sample-data-3.png)</span><span class="sxs-lookup"><span data-stu-id="32618-212">![Screenshot of the demo data installer status window](media/sample-data-3.png)</span></span>

6. <span data-ttu-id="32618-213">Innan du fortsätter, observera att installera exempeldata kan ta upp till en timme (normalt ~ 10 minuter).</span><span class="sxs-lookup"><span data-stu-id="32618-213">Before proceeding, note that installing sample data could take up to one hour (normally ~10 minutes).</span></span> <span data-ttu-id="32618-214">Du måste se till att datorn fortfarande är på och ansluten till ett nätverk under installationsprocessen och att sessionen är fortfarande aktiv.</span><span class="sxs-lookup"><span data-stu-id="32618-214">You'll need to make sure the computer remains on and connected to a network throughout the installation process, and that your session remains active.</span></span>   

7. <span data-ttu-id="32618-215">När du är klar klickar du på **nästa** för att starta installationsprocessen för exempeldata.</span><span class="sxs-lookup"><span data-stu-id="32618-215">When you're ready, click **Next** to start the sample data installation process.</span></span> <span data-ttu-id="32618-216">När dina exempeldata är laddade, klicka på **Slutför**.</span><span class="sxs-lookup"><span data-stu-id="32618-216">After the sample data is loaded, click **Finish**.</span></span>

## <a name="verify-the-sample-data-installation"></a><span data-ttu-id="32618-217">Kontrollera installationen av exempeldata</span><span class="sxs-lookup"><span data-stu-id="32618-217">Verify the sample data installation</span></span>

<span data-ttu-id="32618-218">För en sundhetskontroll kontrollerar du att antalet poster och typer av entiteter som visas i Fabrikam Robotics fiktiva scenario visas som förväntat.</span><span class="sxs-lookup"><span data-stu-id="32618-218">For a sanity check, verify that the number of records and types of entities listed in Fabrikam Robotics fictitious scenario appear as expected.</span></span>

<span data-ttu-id="32618-219">När dina exempeldata helt laddats, logga in som användaren Spencer Low och kontrollera följande:</span><span class="sxs-lookup"><span data-stu-id="32618-219">After the sample data completely loads, sign in as the Spencer Low user and confirm the following:</span></span>

- <span data-ttu-id="32618-220">Om Project Service-programmet är installerat, går du till **Project Service** > **inställningar** > **prislistor**.</span><span class="sxs-lookup"><span data-stu-id="32618-220">If the Project Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="32618-221">Bekräfta att det finns fakturataxa och kostnader med rätt valuta, för varje land/region i datauppsättningen.</span><span class="sxs-lookup"><span data-stu-id="32618-221">Confirm that bill rates and costs rates exist with the appropriate currency for each country/region in the data set.</span></span>

- <span data-ttu-id="32618-222">Om Project Service-programmet är installerat, går du till **Universal Resource Scheduling** > **Inställningar** > **Organisationsenheter**.</span><span class="sxs-lookup"><span data-stu-id="32618-222">If the Project Service application is installed, go to **Universal Resource Scheduling** > **Settings** > **Organizational Units**.</span></span> <span data-ttu-id="32618-223">Kontrollera att en prislista för kostnad med rätt valuta har associerats med varje organisationsenhet (utom poster för ort).</span><span class="sxs-lookup"><span data-stu-id="32618-223">Confirm that a cost price list with the appropriate currency has been associated with each org unit (excluding city entries).</span></span> <span data-ttu-id="32618-224">Om något saknas kan du söka efter och associera rätt kostnadsprislista.</span><span class="sxs-lookup"><span data-stu-id="32618-224">If any are missing, find and associate the correct cost price list.</span></span>

- <span data-ttu-id="32618-225">Om Field Service-programmet är installerat, går du till **Project Service** > **inställningar** > **prislistor**.</span><span class="sxs-lookup"><span data-stu-id="32618-225">If the Field Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="32618-226">Kontrollera att faktureringstariffer och kostnader finns.</span><span class="sxs-lookup"><span data-stu-id="32618-226">Confirm that bill rates and costs rates exist.</span></span> <span data-ttu-id="32618-227">Gå till **Field Service** > **inställningar** > **prislistor** och kontrollera att det finns fakturataxa och kostnader med rätt valuta, för varje land/region i datauppsättningen.</span><span class="sxs-lookup"><span data-stu-id="32618-227">Go to **Field Service** > **Settings** > **Price Lists** and check that bill rates and costs rates exist, with the appropriate currency, for each country/region in the data set.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="32618-228">![Bild på aktiva prislistor](media/sample-data-4.png)</span><span class="sxs-lookup"><span data-stu-id="32618-228">![Screenshot of active price lists](media/sample-data-4.png)</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="32618-229">![Bild på aktiva organisationsenheter](media/sample-data-5.png)</span><span class="sxs-lookup"><span data-stu-id="32618-229">![Screenshot of active organizational units](media/sample-data-5.png)</span></span>

## <a name="technical-notes"></a><span data-ttu-id="32618-230">Tekniska anteckningar</span><span class="sxs-lookup"><span data-stu-id="32618-230">Technical notes</span></span>

<span data-ttu-id="32618-231">Nedan följer mer teknisk information om installationen av dessa data.</span><span class="sxs-lookup"><span data-stu-id="32618-231">See below for more technical details on the installation of this data.</span></span>

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a><span data-ttu-id="32618-232">Installera exempeldata ovanför befintliga data (rekommenderas inte)</span><span class="sxs-lookup"><span data-stu-id="32618-232">Installing sample data on top of existing data (not recommended)</span></span>

<span data-ttu-id="32618-233">Om du behöver installera exempeldata ovanpå en befintlig utvärderingsversion eller demomiljö av Field Service och Project Service som redan innehåller data måste du avbryta säkerhetsprövningarna som utförs av installationsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="32618-233">If you need to install sample data on top of an existing Field Service or Project Service trial or demo environment that already has data, you'll need to suspend the safety prechecks performed by the installer.</span></span>

<span data-ttu-id="32618-234">Gör det genom att gå till mappen **PkgFolder** och sök och öppna filen **DemoDataPreImportConfig.xml** med Notepad (eller ett annat XML-redigerare).</span><span class="sxs-lookup"><span data-stu-id="32618-234">To do this, go to the **PkgFolder** folder to find and open the **DemoDataPreImportConfig.xml** file with Notepad (or another XML editor).</span></span>

<span data-ttu-id="32618-235">Leta upp följande värde och ändra inställningen från sant till falskt:</span><span class="sxs-lookup"><span data-stu-id="32618-235">Find the following value, and then change the setting from true to false:</span></span>

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

<span data-ttu-id="32618-236">Den här ändringen kommer att leda till att installationsprogrammet kringgår vissa viktiga säkerhetskontroll kontroller, inklusive:</span><span class="sxs-lookup"><span data-stu-id="32618-236">This change causes the installer to bypass some important safety checks, including:</span></span>

- <span data-ttu-id="32618-237">Bekräfta att det finns fler än en aktiv post för **organisationsenhet** och sedan byta namn på den till **Fabrikam USA**.</span><span class="sxs-lookup"><span data-stu-id="32618-237">Confirming that there is no more than one active **Organizational Unit** record, and then renaming it to **Fabrikam US**.</span></span>

- <span data-ttu-id="32618-238">Bekräfta att det finns fler än en aktiv post för **arbetsmall**.</span><span class="sxs-lookup"><span data-stu-id="32618-238">Confirming that there is no more than one active **Work Template** record.</span></span>

- <span data-ttu-id="32618-239">Bekräfta att det finns fler än en aktiv post för **Projektparameter** och sedan byta namn på den till **Parametrar**.</span><span class="sxs-lookup"><span data-stu-id="32618-239">Confirming that there is no more than one active **Project Parameter** record, and then renaming that entry to **Parameters**.</span></span>

### <a name="configuration-components"></a><span data-ttu-id="32618-240">Konfigurationskomponenter</span><span class="sxs-lookup"><span data-stu-id="32618-240">Configuration components</span></span>

<span data-ttu-id="32618-241">Det finns ett antal andra konfigurationskomponenter i konfigurationsfilen för förimport.</span><span class="sxs-lookup"><span data-stu-id="32618-241">There are a number of other configuration components in this pre-import configuration file.</span></span> <span data-ttu-id="32618-242">För tekniska användare kan några dessa omfatta:</span><span class="sxs-lookup"><span data-stu-id="32618-242">For technical users, some of these include:</span></span>

- <span data-ttu-id="32618-243">**\<RequiredSolutions\>** anger nödvändiga lösningsinstallationer och deras versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="32618-243">**\<RequiredSolutions\>** specifies prerequisite solution installations and their version numbers.</span></span>

- <span data-ttu-id="32618-244">**\<InstallSampleData\>** kontrollerar om medföljande exempeldata för appar har installerats.</span><span class="sxs-lookup"><span data-stu-id="32618-244">**\<InstallSampleData\>** controls whether out-of-the-box sample data for the apps is installed.</span></span>

    - <span data-ttu-id="32618-245">falskt - hoppar över installation av dessa inbyggda data (som kan tas bort).</span><span class="sxs-lookup"><span data-stu-id="32618-245">false - skips installation of this built-in data (which is removable)</span></span>

    - <span data-ttu-id="32618-246">sant - installerar den inbyggda data samtidigt med installationen av FS och PSA exempeldata.</span><span class="sxs-lookup"><span data-stu-id="32618-246">true - installs the built-in data concurrent with installation of the FS and PSA sample data</span></span>

- <span data-ttu-id="32618-247">**\<PreImportDataCollection\>** anger datamappningar med platt fil och associerade poster som ska importeras före den huvudsakliga installationen av exempeldata.</span><span class="sxs-lookup"><span data-stu-id="32618-247">**\<PreImportDataCollection\>** specifies flat-file Data Maps and associated Records to be imported ahead of the main sample data installation.</span></span>

- <span data-ttu-id="32618-248">**\<EntitiesToEnableScheduling\>** anger vilka entiteter som ska aktiveras för bokning i Microsoft Dynamics Scheduling (även kallat Universal Resource Scheduling).</span><span class="sxs-lookup"><span data-stu-id="32618-248">**\<EntitiesToEnableScheduling\>** specifies which entities should be enabled for Booking in Microsoft Dynamics Scheduling (aka Universal Resource Scheduling).</span></span>

- <span data-ttu-id="32618-249">**\<UsersToCreateAndConfigure\>** anger Bokningsbara resurser som kommer att skapas (om de inte redan finns) innan importen av exempeldata körs.</span><span class="sxs-lookup"><span data-stu-id="32618-249">**\<UsersToCreateAndConfigure\>** specifies Bookable Resources that will be created (if they don't exist already) before the sample data import executes.</span></span> <span data-ttu-id="32618-250">Observera att Bokningsbara resurser för källsystemets exempeldata överensstämmer med målsystemets Bokningsbara poster på fullständigt namn och inloggningsnamnet för varje resurs.</span><span class="sxs-lookup"><span data-stu-id="32618-250">Note that the source system sample data Bookable Resource match with the target system Bookable Resource records on the FullName and login of each resource.</span></span> <span data-ttu-id="32618-251">Därför är det INTE möjligt att byta namn i förkonfigureringsfilen om du inte först importerar exempeldata till ett målsystem med dessa namn och sedan byter namn på Bokningsbara resurser till det önskade namnet tillsammans med Aktiverade användarposter och exporterar data igen för import till systemet till din slutliga destination (uppdaterar **ImportUserMapFile.xml** gamla och nya poster i enlighet med detta).</span><span class="sxs-lookup"><span data-stu-id="32618-251">Therefore, it is NOT possible to change the names in this preconfiguration file unless you first import sample data into a target system using these names, then rename the Bookable Resources to your desired name set along with the Enabled User records, and then export the data again for import into your final destination system (updating the **ImportUserMapFile.xml** Old and New entries accordingly).</span></span>

- <span data-ttu-id="32618-252">**\<PluginsToDisable\>** anger mycket diskret radobjekt plugin-program som måste inaktiveras under importen av exempeldata och sedan återaktiveras efteråt.</span><span class="sxs-lookup"><span data-stu-id="32618-252">**\<PluginsToDisable\>** specifies very discrete line-item plug-ins that must be disabled during the sample data import and then reenabled afterwards.</span></span>

### <a name="fabrikam-robotics-fictitious-scenario"></a><span data-ttu-id="32618-253">Fabrikam Robotics fiktivt scenario</span><span class="sxs-lookup"><span data-stu-id="32618-253">Fabrikam Robotics fictitious scenario</span></span>

<span data-ttu-id="32618-254">Field Service och Project Service exempeldatapaket referens installerar **Lösningen Fabrikam Manufacturing Master Data (v3.0.0.0)**, tillsammans med cirka 4 000 poster och ungefär 40 olika entiteter.</span><span class="sxs-lookup"><span data-stu-id="32618-254">The Field Service and Project Service sample reference data packages install the **Fabrikam Manufacturing Master Data (v3.0.0.0) solution**, along with approximately 4,000 records and approximately 40 different entities.</span></span> <span data-ttu-id="32618-255">Separat exempeldatapaket för Field Service eller Project Service innehåller en deluppsättning av exempeldata **v902FPSMasterData** för programmet.</span><span class="sxs-lookup"><span data-stu-id="32618-255">The separate sample data packages for Field Service or Project Service contain a subset of the **v902FPSMasterData** sample data for that application.</span></span> <span data-ttu-id="32618-256">Paketet **demodata** installeras på **lösningen Fabrikam Manufacturing demodata (v3.0.0.7)** med ungefär 22 000 poster över 148 entiteter.</span><span class="sxs-lookup"><span data-stu-id="32618-256">The **Demo Data** package installs the **Fabrikam Manufacturing Demo Data (v3.0.0.7) solution** with approximately 22,000 records across 148 entities.</span></span>

<span data-ttu-id="32618-257">Det fiktiva företaget Fabrikam Robotics, är en tillverkare av elektroniska enheter med monteringsbandrobotar och är kända för sina produkters kvalitet, innovation och solida kundtjänst, inklusive installationsplanering, implementering och löpande underhållstjänster.</span><span class="sxs-lookup"><span data-stu-id="32618-257">The fictional company, Fabrikam Robotics, is a manufacturer of electronic device assembly line robots and is known for their product quality, innovation, and solid customer service, including installation planning, implementation, and ongoing maintenance services.</span></span> <span data-ttu-id="32618-258">Fabrikam har sitt säte i USA (Fabrikam USA) och använder projektbaserade tjänståtgärder i Frankrike, Indien, Österrike och Schweiz.</span><span class="sxs-lookup"><span data-stu-id="32618-258">Fabrikam is headquartered in the United States (Fabrikam US), and has project-based service operations in France, India, the United Kingdom, and Switzerland.</span></span>

<span data-ttu-id="32618-259">Field Service-åtgärder är centrerade i USA, mest i Seattle-området.</span><span class="sxs-lookup"><span data-stu-id="32618-259">Field service operations are centered in the United States, mostly in the greater Seattle area.</span></span> <span data-ttu-id="32618-260">Företaget fokuserar på att dra nytta av IoT-anslutning (sakernas internet) för att övervaka kundtillgångprestanda och leverera proaktiva tjänster på plats.</span><span class="sxs-lookup"><span data-stu-id="32618-260">The company is focused on leveraging Internet of Things (IoT) connectivity to monitor customer asset performance and deliver increasingly proactive onsite services.</span></span>

<span data-ttu-id="32618-261">En översikt på hög nivå om exempeldata är följande:</span><span class="sxs-lookup"><span data-stu-id="32618-261">A high-level overview of the sample data is as follows:</span></span>

- <span data-ttu-id="32618-262">Vanliga exempeldataelement (ingår i båda programmen)</span><span class="sxs-lookup"><span data-stu-id="32618-262">Common sample data elements (included for both applications)</span></span>

    - <span data-ttu-id="32618-263">1 användare.</span><span class="sxs-lookup"><span data-stu-id="32618-263">1 user</span></span>

    - <span data-ttu-id="32618-264">71 konton</span><span class="sxs-lookup"><span data-stu-id="32618-264">71 accounts</span></span>

    - <span data-ttu-id="32618-265">137 kontakter</span><span class="sxs-lookup"><span data-stu-id="32618-265">137 contacts</span></span>

    - <span data-ttu-id="32618-266">Olika transaktionstyper och kategorier</span><span class="sxs-lookup"><span data-stu-id="32618-266">Various transaction types and categories</span></span>

    - <span data-ttu-id="32618-267">50 produkter ed 1 prislista för produkt</span><span class="sxs-lookup"><span data-stu-id="32618-267">50 products with 1 product price list</span></span>

    - <span data-ttu-id="32618-268">14 pris-/kostnadslistor</span><span class="sxs-lookup"><span data-stu-id="32618-268">14 price/cost lists</span></span>

    - <span data-ttu-id="32618-269">31 egenskaper (resursfärdigheter) i 2 klassificeringsmodeller med 3 nivåer (klassificeringsvärden)</span><span class="sxs-lookup"><span data-stu-id="32618-269">31 characteristics (resource skills) in 2 rating models with 3 levels (rating values)</span></span>

- <span data-ttu-id="32618-270">Project Service</span><span class="sxs-lookup"><span data-stu-id="32618-270">Project Service</span></span>

    - <span data-ttu-id="32618-271">8 organisationsenheter</span><span class="sxs-lookup"><span data-stu-id="32618-271">8 organizational units</span></span>

    - <span data-ttu-id="32618-272">6 rollspecifika utnyttjandenivåer</span><span class="sxs-lookup"><span data-stu-id="32618-272">6 role-specific utilization levels</span></span>

    - <span data-ttu-id="32618-273">2,8 k + rollprisspecifikationer</span><span class="sxs-lookup"><span data-stu-id="32618-273">2.8k+ role-price specifications</span></span>

- <span data-ttu-id="32618-274">Field Service</span><span class="sxs-lookup"><span data-stu-id="32618-274">Field Service</span></span>

    - <span data-ttu-id="32618-275">4 områden</span><span class="sxs-lookup"><span data-stu-id="32618-275">4 territories</span></span>

    - <span data-ttu-id="32618-276">5 arbetsordertyper</span><span class="sxs-lookup"><span data-stu-id="32618-276">5 work order types</span></span>

    - <span data-ttu-id="32618-277">22 kundtillgångar</span><span class="sxs-lookup"><span data-stu-id="32618-277">22 customer assets</span></span>

    - <span data-ttu-id="32618-278">9 incidenttyper med ett urval av associerade resursegenskaper (9), tjänster (13) och serviceuppgifter (13)</span><span class="sxs-lookup"><span data-stu-id="32618-278">9 incident types with a range of associated resource characteristics (9), services (13) and service tasks (13)</span></span>
   
<span data-ttu-id="32618-279">Paketet **demodata** installerar ungefär 179 arbetsorder 12 projekt och associerade transaktionsdata.</span><span class="sxs-lookup"><span data-stu-id="32618-279">The **Demo Data** package installs approximately 179 work orders, 12 projects, and associated transactional data.</span></span> 

### <a name="change-the-work-hours-for-sample-resources"></a><span data-ttu-id="32618-280">Ändra arbetstider/drifttider för exempelresurser</span><span class="sxs-lookup"><span data-stu-id="32618-280">Change the work hours for sample resources</span></span>

<span data-ttu-id="32618-281">Som standard har alla bokningsbara resurser en standardarbetskalender på 24 timmar.</span><span class="sxs-lookup"><span data-stu-id="32618-281">By default, all bookable resources have a 24 work hours calendar.</span></span>

<span data-ttu-id="32618-282">Om du behöver ändra arbetstider/drifttider för exempelbokningsbara resurser går du till **Universal Resource Scheduling** > **schemaläggning** > **resurser**.</span><span class="sxs-lookup"><span data-stu-id="32618-282">If you need to change the work hours for sample bookable resources, go to **Universal Resource Scheduling** > **Scheduling** > **Resources**.</span></span>

<span data-ttu-id="32618-283">Välj en användare (till exempel Spencer Low) och ändra Spencers arbetstider till de timmar som du vill koppla till flera användare.</span><span class="sxs-lookup"><span data-stu-id="32618-283">Select a user (for example, Spencer Low) and change Spencer's work hours to the hours you want to apply to multiple users.</span></span> <span data-ttu-id="32618-284">Gå till **Universal Resource Scheduling** > **inställningar** > **arbetstidsmallar** och redigera posten **standardarbetsmall**.</span><span class="sxs-lookup"><span data-stu-id="32618-284">Go to **Universal Resource Scheduling** > **Settings** > **Work Hour Templates** and edit the **Default Work Template** record.</span></span> <span data-ttu-id="32618-285">I fältet **mallresurs** väljer du en användare med arbetstimmar som du vill koppla till andra resurser.</span><span class="sxs-lookup"><span data-stu-id="32618-285">In the **Template Resource** field, select a user with work hours that you want to apply to other resources.</span></span> <span data-ttu-id="32618-286">Gå till **Universal Resource Scheduling** > **schemaläggning** > **resurser** > **aktiva bokningsbara resurser**.</span><span class="sxs-lookup"><span data-stu-id="32618-286">Go to **Universal Resource Scheduling** > **Scheduling** > **Resources** > **Active Bookable Resources**.</span></span> <span data-ttu-id="32618-287">Markera de resurser som du vill ändra och välj sedan **ange kalender**.</span><span class="sxs-lookup"><span data-stu-id="32618-287">Select the resources you want to change, and then select **Set Calendar**.</span></span> <span data-ttu-id="32618-288">På listrutan **arbetsmall**, välj mallen **standardarbetstid** eller en annan mall med korrekt mallresurs.</span><span class="sxs-lookup"><span data-stu-id="32618-288">On the **Work Template** drop-down list, select the **Default Work Hour** template or another template with the correct templating resource.</span></span> <span data-ttu-id="32618-289">När du börjar schemaläggningstavlan bör du kunna se att resurserna nu har uppdaterat dina arbetstider.</span><span class="sxs-lookup"><span data-stu-id="32618-289">When you go to the schedule board, you should see that the resources now have updated work hours.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="32618-290">![Bild på aktiva bokningsbara resurser](media/sample-data-6.png)</span><span class="sxs-lookup"><span data-stu-id="32618-290">![Screenshot of active bookable resources](media/sample-data-6.png)</span></span>
