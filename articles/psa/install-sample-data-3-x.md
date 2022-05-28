---
title: Installation av exempeldata
description: I det här ämnet finns information om hur du installerar exempeldata i Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: johnmichalak
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 952f3c3c037bb8459bdd1400288c4ea8604ce282
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581858"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Installationen av exempeldata data för Project Service-programmet

[!include [banner](../includes/psa-now-project-operations.md)]

För att hjälpa dig att bygga upp dina egna demo-miljöer tillhandahåller Microsoft hämtningsbara exempeldatapaket som visar upp funktionerna i appen. Det finns två typer av exempeldatapaketen:
- referens/installationsdata
- demodata (referens/installations- och transaktionsdata såsom arbetsorder och projekt)

Exempeldatapaket **referens** kan hämtas i tre olika paket så att du endast kan installera data för Project Service, eller bara för Field Service eller du kan installera exempeldata för båda programmen på samma gång.

Exempeldatapaketen inställning/referens är:

- [**V902PSMasterData** - endast Project Service version 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - endast Field Service version 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x och Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Det senaste **demonstrations** datapaketet är:

 - [**FPSDemoData** - Field Service 8.x och Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Installationsinstruktioner skiljer sig något i användare för att skapa och konfigurera avsnittet men resten är desamma som i föregående [**blogginlägg**](https://aka.ms/fpsdemodatablog). Det här paketet har en lägre demonstrationsdatauppsättning och tar cirka tre timmar att installera.

Dessa exempeldatapaket finns endast tillgängliga på engelska.

> [!IMPORTANT]
> **Det går inte att avinstallera exempeldata.** Du bör endast installera dessa paket på demonstration, evaluation, träning och testsystem. Observera att installera ett individuellt paket och installerar sedan det andra individuella paketet stöds inte. (Med andra ord, du kan inte installera **FSMasterData** följt av **PSMasterData**, eller tvärtom.) Om du tycker att du behöver exempeldata för båda programmen när som helst i framtiden bör du installera paketet **v902FPSMasterData**.

När du installerar exempeldatapaket utför installationsprocessen följande åtgärder:

- Skapar eller anger standardparametrar för att använda Project Service, Field Service eller båda programmen (om tillämpligt).

- Importerar exempeldata program såsom bokningsbara resurser, programspecifika roller, försäljning och kostnadsprislistor, organisationsenheter, försäljningsprocessposter och andra entiteter för att demonstrera viktiga funktioner.  

Med **demonstrationsdata** paketet får du ovan och ytterligare transaktionsdata såsom arbetsorder och projekt.

Undrar du vilka funktioner du kan demonstrera med exempeldata? Se Fabrikam Robotics fiktiva scenario i [tekniska anteckningar](#technical-notes).

Om du har frågor om hur du installerar exempeldatapaketen [skicka ett e-postmeddelande till fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Krav

Installationsprotokollet förutsätter följande om din målinstans (org):

- Grundspråk är engelska och basvalutan amerikanska dollar (USD, $)

- Organisationen har ingen Project Service- eller Field Service-data redan eller har bara enkla standarddata som ingår i alla nya organisationer

- Rätt version av affärsprogrammet är redan installerat:
       
    - **För FPSDemoData eller v902FPSMasterData:** organisationen har Field Service version 8.x och Project Service version 3.x installerat.

    - **För v902PSMasterData:** organisationen har Project Service version 3.x installerat.

    - **För v902FSMasterData:** organisationen har Field Service version 8.x installerat.

> [!NOTE]
> Om du behöver installera exempeldata ovanpå en befintlig utvärderingsversion eller demomiljö av Project Service och Field Service som redan innehåller data (vilket inte rekommenderas) måste du avbryta säkerhetsprövningarna som utförs av installationsprogrammet. Mer information finns i tekniska anteckningar nedan.

## <a name="prepare-for-installation"></a>Förbered installation

Du måste köra installationsprogrammet på en dator med den senaste versionen av Windows (helst Windows 10).

Du bör planera för datorn att vara ansluten till ett nätverk och för att installationen ska köras i upp till **1 timme** för **inställning/referensdata**. (Installationen tar normalt ungefär 30 minuter för **FPSMasterData**, som innehåller exempeldata för båda programmen.) För **FPSDemoData** tar installationen runt **3 timmar**.

Datorn bör ha funktionen skärmsläckare avstängd. I annat fall kan sessionens autentiseringsuppgifter för installationen förloras när skärmsläckaren aktiveras (såvida inte du håller sessionen aktiv).

> [!div class="mx-imgBorder"]
> ![Bild på inställningar för skärmsläckare med skärmsläckaren avstängd.](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Hämta och packa upp

Installationsprogrammet för Project Service och Field Service exempeldata distribueras som en självextraherande körbar fil. Filnamnen kan variera beroende på exempeldatapaketet men annars är stegen desamma oavsett vilka paket du installerar.

När du har hämtat ett paket, kör exe.-filen och acceptera villkoren för att packa upp komprimerade zip-filen. Du måste sedan extrahera innehållet till den filen till en mapp som du väljer på din dator.

Beroende på operativsystem och säkerhetsinställningar kan behöva utföra följande steg när du packat upp zip-filen:

1. Söka efter och högerklicka på **FPSDemoData.dll**-file i mappen **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Välj **avblockera**.

3. Välj **tillämpa**.

4. Välj **OK**.


## <a name="create-or-configure-users"></a>Skapa eller konfigurera användare

**FPSDemoData**-paketet kräver sex användare när **FPSMasterData**-paketet kräver en användare. Referera till korrekt för ditt exempeldatapaketet.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Skapa eller konfigurera användare - inställning/referensdatapaket

**FPSMasterData**-paketet har utformats för att installera med en användare med namnet Spencer Low med inställningar som beskrivs här. Om du vill installera paketet korrekt behöver du skapa (eller tillfälligt byta namn) användare i din miljö så att de matchar konfigurationen för inkommande konfiguration av exempeldata.

Skapa eller konfigurera användare genom att gå till **inställningar** > **säkerhet** > **användare** och gör följande:

1. Ange UserFullname=”Spencer Low” med användarnamn ”spencerl” (**gemener**) till rollerna Projektledare och Metodansvarig.

2. Välj användaren **Spencer Low** och välj sedan **Hantera roller**. Leta upp och markera roll **systemadministratören** och markera **OK** ge fullständig administratörsrättigheter till Spencer Low. Det här steget är nödvändigt för att säkerställa att exempelposter skapas med rätt ägarskap och därför fyller i vyer på rätt sätt.

3. Från det nedladdade paketet måste du uppdatera en datamappningsfil med e-postadresser till standardanvändarkontext. Det gör du genom att öppna **PkgFolder**, hitta och öppna **ImportUserMapFile.xml**-filen i Notepad (eller Visual Studio eller en annan XML-redigerare). Ange fältet **DefaultUserToMapTo =** till Spencer Low användarens e-postadress.

4. Om du inte använder Spencer Low med användarnamn **spencerl**, måste du uppdatera en ytterligare fil. Öppna **DemoDataPreImportConfig.xml**-filen och sök **userstocreateandconfigure**-etiketten. Uppdatera etiketten **\<login\>** med användarnamnet för din Spencer Low användare. Mer information finns i [tekniska anteckningar](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Skapa eller konfigurera användare - demonstrationsdatapaket

Demonstrationsdatapaketet kräver sex användare. För att uppdateringen ska installeras på rätt sätt, gör du följande:

 1. Skapa eller tillfälligt byta namn på befintliga användare så att de överensstämmer med konfiguration av inkommande exempeldata genom att gå till **inställningar** > **eller** > **användare**.
 
    Dessa två roller behövs endast för personbaserade demonstrationer.  
    - Användarens fullständiga namn ="David So" som Field Service-tekniker   
    - Användarens fullständiga namn = ”Johan Reding” som Customer Service och Field Service-avsändare   
    - Användarens fullständiga namn = ”Molly Clark” som kontohanterare   
    - Användarens fullständiga namn = ”Spencer Low” som övare och projektledare  
    - Användarens fullständiga namn = ”Veronica Quek” som Teammedlem   
    - Användarens fullständiga namn = ”William Contoso”
  
2. Tilldela de sex användarna ovanför administratörsrollen i syfte att importera demonstrationsdata så att provposter importeras korrekt. 

3. Öppna **PkgFolder** och sök efter och öppna **ImportUserMapFile.xml**. Uppdatera fälten **ny=** till e-postadresser för motsvarande användare i systemet.

   > [!div class="mx-imgBorder"]
   > ![Skärmbild av UserMapFile.](media/sample-data-7.png)

4. Om användarens fullständiga namn ”Spencer Low” har en annan användare än **”spencerl”** måste du uppdatera en ytterligare fil. Öppna **DemoDataPreImportConfig.xml** och sök **userstocreateandconfigure**-etiketten. Uppdatera etiketten **\<login\>** med loginId (skiftlägeskänsligt). 

5. Den första användarens kalender (i etiketten **userstocreateandconfigure**) används för att fylla arbetstimmarna för alla bokningsbara resurser på import av demodata. Gå till **inställningar** > **säkerhet** > **användare**, hitta användaren ”Spencer Low” och öppna alternativet ”arbetstimmar”. Redigera befintliga arbetstimmar genom att välja alternativet **hela återkommande veckoschema från början till slut**. Kontrollera att **arbetstid anges till 8:00 - 17:00 (9 timmar) måndag till fredag och den tidszon som har angetts till Pacific Time (USA och Kanada)**. Detta görs för att säkerställa att alla projekt och schematavlor visas som förväntat.

**Rekommendation:** Överväg att skapa en säkerhetskopia av organisationen nu, om du skulle behöva återställa till en utgångspunkt om något går fel under installationen av exempeldata. Mer information finns i [Säkerhetskopiera och återställ instanser](/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Kör Package Deployer

1. Sök efter och kör **PackageDeployer.exe** i mappen **v902FPSMasterData** ELLER **PackageDeployer_FPSDemoData**.

2. Acceptera villkoren

3. I nästa fönster:

   a. Välj distributionstyp **Office 365**.

   b. Använd användare och lösenord för systemadministratören som konfigurerats i ”Skapa eller konfigurera användare” (”Spencer Low” med ”spencerl” användarnamn).

   c. Kontrollera att **Visa listan över tillgängliga organisationer** är markerad.

      > [!div class="mx-imgBorder"]
      > ![Bild på Package Deployer-fönstret med ”visa listan över tillgängliga företag” markerad](media/sample-data-2.png)

4. Välj organisation när du vill installera exempeldata.

5. Välj **nästa** tills du ser dialogrutan **Inställning av demonstrationsdata**.

   > [!div class="mx-imgBorder"]
   > ![Bild på statusfönstret för installation av demonstrationsdata.](media/sample-data-3.png)

6. Innan du fortsätter, observera att installera exempeldata kan ta upp till en timme (normalt ~ 10 minuter). Du måste se till att datorn fortfarande är på och ansluten till ett nätverk under installationsprocessen och att sessionen är fortfarande aktiv.   

7. När du är klar klickar du på **nästa** för att starta installationsprocessen för exempeldata. När dina exempeldata är laddade, klicka på **Slutför**.

## <a name="verify-the-sample-data-installation"></a>Kontrollera installationen av exempeldata

För en sundhetskontroll kontrollerar du att antalet poster och typer av entiteter som visas i Fabrikam Robotics fiktiva scenario visas som förväntat.

När dina exempeldata helt laddats, logga in som användaren Spencer Low och kontrollera följande:

- Om Project Service-programmet är installerat, går du till **Project Service** > **inställningar** > **prislistor**. Bekräfta att det finns fakturataxa och kostnader med rätt valuta, för varje land/region i datauppsättningen.

- Om Project Service-programmet är installerat, går du till **Universal Resource Scheduling** > **Inställningar** > **Organisationsenheter**. Kontrollera att en prislista för kostnad med rätt valuta har associerats med varje organisationsenhet (utom poster för ort). Om något saknas kan du söka efter och associera rätt kostnadsprislista.

- Om Field Service-programmet är installerat, går du till **Project Service** > **inställningar** > **prislistor**. Kontrollera att faktureringstariffer och kostnader finns. Gå till **Field Service** > **inställningar** > **prislistor** och kontrollera att det finns fakturataxa och kostnader med rätt valuta, för varje land/region i datauppsättningen.

  > [!div class="mx-imgBorder"]
  > ![Bild på aktiva prislistor.](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Bild på aktiva organisationsenheter.](media/sample-data-5.png)

## <a name="technical-notes"></a>Tekniska anteckningar

Nedan följer mer teknisk information om installationen av dessa data.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Installera exempeldata ovanför befintliga data (rekommenderas inte)

Om du behöver installera exempeldata ovanpå en befintlig utvärderingsversion eller demomiljö av Field Service och Project Service som redan innehåller data måste du avbryta säkerhetsprövningarna som utförs av installationsprogrammet.

Gör det genom att gå till mappen **PkgFolder** och sök och öppna filen **DemoDataPreImportConfig.xml** med Notepad (eller ett annat XML-redigerare).

Leta upp följande värde och ändra inställningen från sant till falskt:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Den här ändringen kommer att leda till att installationsprogrammet kringgår vissa viktiga säkerhetskontroll kontroller, inklusive:

- Bekräfta att det finns fler än en aktiv post för **organisationsenhet** och sedan byta namn på den till **Fabrikam USA**.

- Bekräfta att det finns fler än en aktiv post för **arbetsmall**.

- Bekräfta att det finns fler än en aktiv post för **Projektparameter** och sedan byta namn på den till **Parametrar**.

### <a name="configuration-components"></a>Konfigurationskomponenter

Det finns ett antal andra konfigurationskomponenter i konfigurationsfilen för förimport. För tekniska användare kan några dessa omfatta:

- **\<RequiredSolutions\>** anger nödvändiga lösningsinstallationer och deras versionsnummer.

- **\<InstallSampleData\>** kontrollerar om medföljande exempeldata för appar har installerats.

    - falskt - hoppar över installation av dessa inbyggda data (som kan tas bort).

    - sant - installerar den inbyggda data samtidigt med installationen av FS och PSA exempeldata.

- **\<PreImportDataCollection\>** anger datamappningar med platt fil och associerade poster som ska importeras före den huvudsakliga installationen av exempeldata.

- **\<EntitiesToEnableScheduling\>** anger vilka entiteter som ska aktiveras för bokning i Microsoft Dynamics Scheduling (även kallat Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** anger Bokningsbara resurser som kommer att skapas (om de inte redan finns) innan importen av exempeldata körs. Observera att Bokningsbara resurser för källsystemets exempeldata överensstämmer med målsystemets Bokningsbara poster på fullständigt namn och inloggningsnamnet för varje resurs. Därför är det INTE möjligt att byta namn i förkonfigureringsfilen om du inte först importerar exempeldata till ett målsystem med dessa namn och sedan byter namn på Bokningsbara resurser till det önskade namnet tillsammans med Aktiverade användarposter och exporterar data igen för import till systemet till din slutliga destination (uppdaterar **ImportUserMapFile.xml** gamla och nya poster i enlighet med detta).

- **\<PluginsToDisable\>** anger mycket diskret radobjekt plugin-program som måste inaktiveras under importen av exempeldata och sedan återaktiveras efteråt.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Fabrikam Robotics fiktivt scenario

Field Service och Project Service exempeldatapaket referens installerar **Lösningen Fabrikam Manufacturing Master Data (v3.0.0.0)**, tillsammans med cirka 4 000 poster och ungefär 40 olika entiteter. Separat exempeldatapaket för Field Service eller Project Service innehåller en deluppsättning av exempeldata **v902FPSMasterData** för programmet. Paketet **demodata** installeras på **lösningen Fabrikam Manufacturing demodata (v3.0.0.7)** med ungefär 22 000 poster över 148 entiteter.

Det fiktiva företaget Fabrikam Robotics, är en tillverkare av elektroniska enheter med monteringsbandrobotar och är kända för sina produkters kvalitet, innovation och solida kundtjänst, inklusive installationsplanering, implementering och löpande underhållstjänster. Fabrikam har sitt säte i USA (Fabrikam USA) och använder projektbaserade tjänståtgärder i Frankrike, Indien, Österrike och Schweiz.

Field Service-åtgärder är centrerade i USA, mest i Seattle-området. Företaget fokuserar på att dra nytta av IoT-anslutning (sakernas internet) för att övervaka kundtillgångprestanda och leverera proaktiva tjänster på plats.

En översikt på hög nivå om exempeldata är följande:

- Vanliga exempeldataelement (ingår i båda programmen)

    - 1 användare.

    - 71 konton

    - 137 kontakter

    - Olika transaktionstyper och kategorier

    - 50 produkter ed 1 prislista för produkt

    - 14 pris-/kostnadslistor

    - 31 egenskaper (resursfärdigheter) i 2 klassificeringsmodeller med 3 nivåer (klassificeringsvärden)

- Project Service

    - 8 organisationsenheter

    - 6 rollspecifika utnyttjandenivåer

    - 2,8 k + rollprisspecifikationer

- Field Service

    - 4 områden

    - 5 arbetsordertyper

    - 22 kundtillgångar

    - 9 incidenttyper med ett urval av associerade resursegenskaper (9), tjänster (13) och serviceuppgifter (13)
   
Paketet **demodata** installerar ungefär 179 arbetsorder 12 projekt och associerade transaktionsdata. 

### <a name="change-the-work-hours-for-sample-resources"></a>Ändra arbetstider/drifttider för exempelresurser

Som standard har alla bokningsbara resurser en standardarbetskalender på 24 timmar.

Om du behöver ändra arbetstider/drifttider för exempelbokningsbara resurser går du till **Universal Resource Scheduling** > **schemaläggning** > **resurser**.

Välj en användare (till exempel Spencer Low) och ändra Spencers arbetstider till de timmar som du vill koppla till flera användare. Gå till **Universal Resource Scheduling** > **inställningar** > **arbetstidsmallar** och redigera posten **standardarbetsmall**. I fältet **mallresurs** väljer du en användare med arbetstimmar som du vill koppla till andra resurser. Gå till **Universal Resource Scheduling** > **schemaläggning** > **resurser** > **aktiva bokningsbara resurser**. Markera de resurser som du vill ändra och välj sedan **ange kalender**. På listrutan **arbetsmall**, välj mallen **standardarbetstid** eller en annan mall med korrekt mallresurs. När du börjar schemaläggningstavlan bör du kunna se att resurserna nu har uppdaterat dina arbetstider.

> [!div class="mx-imgBorder"]
> ![Bild på aktiva bokningsbara resurser.](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]