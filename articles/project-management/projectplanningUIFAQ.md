---
title: Felsöka arbete i uppgiftsrutnätet
description: Den här artikeln innehåller felsökningsinformation som behövs när du arbetar i uppgiftsrutnätet.
author: ruhercul
ms.date: 04/05/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e6ab4f34fe3f6732f7bef252f298671e07a3c3ca
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911066"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Felsöka arbete i uppgiftsrutnätet 


_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier, Lite-distribution - affär med proforma-fakturering, Project for the Web_

Rutnätet Uppgift som utnyttjas av Dynamics 365 Project Operations är en värdbaserad iFrame i Microsoft Dataverse. Som ett resultat av den här användningen måste specifika krav uppfyllas för att säkerställa att autentiseringen och autentiseringen fungerar korrekt. I artikeln beskrivs vanliga problem som kan påverka möjligheten att rendera rutnät eller hantera uppgifter i uppdelad arbetsstruktur (WBS).

Vanliga problem omfattar:

- Fliken **Uppgift** i rutnätet Uppgift är tom.
- När du öppnar projektet läses inte projektet in och användargränssnittet (UI) har fastnat i rotationsytan.
- Administration av privilegier för **Project for the Web**.
- Ändringar sparas inte när du skapar, uppdaterar eller tar bort en uppgift.

## <a name="issue-the-task-tab-is-empty"></a>Problem: Fliken Uppgift är tom

### <a name="mitigation-1-enable-cookies"></a>Åtgärd 1: Aktivera cookies

För Project Operations krävs att tredjeparts-cookies aktiveras för att uppdelad arbetsstruktur ska kunna återges. När cookies från tredje part inte är aktiverade visas en tom sida i stället för uppgifter när du väljer fliken **Uppgifter** på sidan **Projekt**.

För Microsoft Edge eller Google Chrome-webbläsare beskriver följande förfaranden hur du uppdaterar dina webbläsarinställningar i syfte att aktivera cookies från tredje part.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Öppna din Edge-webbläsare.
2. I det övre högra hörnet väljer du **ellipsen** (...) och sedan **Inställningar**.
3. Under **Cookies och webbplatsbehörigheter** väljer du **Cookies och webbplatsdata**.
4. Inaktivera **Blockera cookies från tredje part**.
5. Uppdatera webbläsaren. 

#### <a name="google-chrome"></a>Google Chrome

1. Öppna Chrome-webbläsaren.
2. Välj de tre vertikala punkterna i det övre högra hörnet och välj sedan **Inställningar**.
3. Under **Sekretess och säkerhet** väljer du **Cookies och annan webbplatsdata**.
4. Välj **Tillåt alla cookies**.
5. Uppdatera webbläsaren. 

> [!NOTE]
> Om du blockerar cookies från tredje part blockeras alla cookies och webbplatsdata från andra webbplatser, även om webbplatsen är tillåten i undantagslistan.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Åtgärd 2: Verifiera att PEX slutpunkt har konfigurerats korrekt

För Project Operations krävs att en projektparameter refererar till PEX-slutpunkten. Denna slutpunkt krävs för att kommunicera med den tjänst som används för att återge uppdelad arbetsstruktur. Om parametern inte är aktiverad visas felmeddelandet "Projektparametern är inte giltig". Uppdatera PEX slutpunkt genom att följa stegen nedan.

1. Lägg till fältet **PEX-slutpunkt** på sidan **Projektparametrar**.
2. Identifiera vilken typ av produkt du använder. Det här värdet används när PEX-slutpunkt anges. Vid hämtningen är produkttypen redan definierad i PEX-slutpunkten. Behåll det värdet.
3. Uppdatera fältet med följande värde: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Följande tabell innehåller den typparameter som ska användas baserat på produkttypen.

      | **Produkttyp**                     | **Typparameter** |
      |--------------------------------------|--------------------|
      | Project for the Web i standardorganisation   | type=0             |
      | Project for the Web i namngiven CDS-organisation | type=1             |
      | Project Operations                   | type=2             |

4. Ta bort fältet från sidan **Projektparametrar**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Riskreducering 3: Logga in på project.microsoft.com.
Öppna en ny flik i din Microsoft Edge-webbläsare, gå till project.microsoft.com och logga in med hjälp av den användarroll du använder för att få åtkomst till Project Operations.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problem: Projektet läses inte in och användargränssnittet har fastnat i spinnern

För autentisering måste popup-fönster aktiveras för att uppgiftsrutnätet ska kunna läsas in. Om popup-fönster inte är aktiverade fastnar skärmen i inläsningsspinnern. Följande bild visar URL:en med en blockerad popup-etikett i adressfältet. Detta resulterar i att spinnern fastnar när han försöker läsa in sidan. 

   ![Fastnande spinner och popup-block.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Åtgärd 1: Aktivera popup-fönster

När ditt projekt har fastnat i spinner är det möjligt att popup-fönster inte är aktiverade.

#### <a name="microsoft-edge"></a>Microsoft Edge

Det finns två sätt att aktivera popup-fönster i Edge-webbläsaren.

1. Välj meddelandet längst upp till höger i webbläsaren i edge-webbläsaren.
2. Välj **Tillåt alltid popup-fönster och om omdirigerar från** den specifika Dataverse miljön.
 
     ![Popup-fönster har blockerats.](media/enablepopups.png)

Alternativt kan du slutföra följande steg.

1. Öppna din Edge-webbläsare.
2. I det övre högra hörnet väljer du **ellips** (...) och välj **Inställningar** > **Webbplatsbehörigheter** > **Popup-fönster och omdirigera**.
3. Växla **popup-fönster och om omdirigerar** för att blockera popup-fönster, eller växla på för att tillåta popup-fönster på enheten.
4. Uppdatera webbläsaren när du har aktiverat popup-fönster. 

#### <a name="google-chrome"></a>Google Chrome
1. Öppna Chrome-webbläsaren.
2. Navigera till en sida där popup-fönster blockeras.
3. Välj **Blockerad av popup-fönster** i adressfältet.
4. Markera länken för det popup-fönster du vill visa.
5. Uppdatera webbläsaren när du har aktiverat popup-fönster. 

> [!NOTE]
> Om du vill att popup-fönster för webbplatsen alltid ska visas väljer du **Tillåt alltid popup-fönster och om omdirigerar från [webbplatsen]** och väljer sedan **Klar**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problem 3: Administration av privilegier för Project for the Web.

Project Operations förlitar sig på en extern schemaläggningstjänst. Tjänsten kräver att en användare har tilldelats flera roller som gör att användaren kan läsa och skriva till entiteter som är relaterade till WBS. Dessa entiteter omfattar projektuppgifter, resurstilldelningar och aktivitetsberoenden. Om en användare inte kan återge WBS när de navigerar till fliken **Uppgifter** beror det förmodligen på att **Projekt** för **Project Operations** inte har aktiverats. En användare kan få antingen ett säkerhetsrollsfel eller ett fel relaterat till nekad åtkomst.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Åtgärd 1: Verifiera programanvändaren och slutanvändaren

1. Gå till **Inställning** > **Säkerhet** > **Användare** > **Programanvändare**.  

   ![Programläsare.](media/applicationuser.jpg)
   
2. Dubbelklicka på programanvändarposten och kontrollera följande:

     - Användaren har åtkomst till projektet. Det gör du genom att kontrollera att användaren har säkerhetsroll **Projektledare**.
     - Microsoft Project-programmets användare finns och är korrekt konfigurerad.
 
3. Om den här användaren inte finns skapar du en ny användarpost. 
4. Välj **Nya användare**, ändra postformuläret till **Programanvändare** och lägg sedan till **Program-ID**.

   ![Information om programanvändare.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problem 4: Ändringar sparas inte när du skapar, uppdaterar eller tar bort en uppgift

När du gör en eller flera uppdateringar av WBS misslyckas ändringarna och sparas inte. Ett fel uppstår i schemarutnätet med ett meddelande om att en nyligen genomförd ändring inte kunde sparas.

### <a name="mitigation-1-validate-the-license-assignment"></a>Åtgärd 1: Verifiera licenstilldelningen

1. Kontrollera att användaren har tilldelats rätt licens och att tjänsten är aktiverad i serviceplaninformationen för licensen.  
2. Kontrollera att användaren kan öppna **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Åtgärd 2: Valideringskonfiguration för projektprogramanvändaren
1. Kontrollera att projektprogrammets användare har skapats.
2. Tillämpa följande säkerhetsroller på användaren:
  
  - Dataverse-användare eller basanvändare
  - Project Operations-systemet
  - Projektsystem
  - Dubbelskrivning till Project Operations. Denna roll krävs för resurs-/icke-lagerbaserade scenarier för Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
