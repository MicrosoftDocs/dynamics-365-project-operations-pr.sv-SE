---
title: Felsöka arbete i uppgiftsrutnätet
description: Detta ämne ger felsökningsinformation som behövs när du arbetar i uppgiftsrutnätet.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031559"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Felsöka arbete i uppgiftsrutnätet 

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Detta ämne beskriver hur du åtgärdar problem som kan uppstå när du arbetar med kostnadshantering.

## <a name="enable-cookies"></a>Aktivera cookies

För Project Operations krävs att tredjeparts-cookies aktiveras för att den uppdelade arbetsstrukturen ska kunna återges. När cookies från tredje part inte är aktiverade visas en tom sida i stället för uppgifter när du väljer fliken **Uppgifter** på sidan **Projekt**.

![Tom flik när cookies från tredje part inte är aktiverade](media/blankschedule.png)


### <a name="workaround"></a>Lösning
För Microsoft Edge eller Google Chrome-webbläsare beskriver följande förfaranden hur du uppdaterar dina webbläsarinställningar i syfte att aktivera cookies från tredje part.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Öppna din Edge-webbläsare.
2. I det övre högra hörnet väljer du **ellipsen** (...) och sedan **Inställningar**.
3. Under **Cookies och webbplatsbehörigheter** väljer du **Cookies och webbplatsdata**.
4. Inaktivera **Blockera cookies från tredje part**.

#### <a name="google-chrome"></a>Google Chrome

1. Öppna Chrome-webbläsaren.
2. Välj de tre vertikala punkterna i det övre högra hörnet och välj sedan **Inställningar**.
3. Under **Sekretess och säkerhet** väljer du **Cookies och annan webbplatsdata**.
4. Välj **Tillåt alla cookies**.

> [!IMPORTANT]
> Om du blockerar cookies från tredje part blockeras alla cookies och webbplatsdata från andra webbplatser, även om webbplatsen är tillåten i undantagslistan.

## <a name="pex-endpoint"></a>PEX-slutpunkt

För Project Operations krävs att en projektparameter refererar till PEX-slutpunkten. Denna slutpunkt krävs för att kommunicera med den tjänst som används för att återge den uppdelade arbetsstrukturen. Om parametern inte är aktiverad visas felmeddelandet "Projektparametern är inte giltig". 

### <a name="workaround"></a>Lösning
 ![Fältet för PEX-slutpunkt i projektparametern](media/projectparameter.png)

1. Lägg till fältet **PEX-slutpunkt** på sidan **Projektparametrar**.
2. Uppdatera fältet med följande värde: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Ta bort fältet från sidan **Projektparametrar**.

## <a name="privileges-for-project-for-the-web"></a>Privilegier för projekt för webben

Project Operations förlitar sig på en extern schemaläggningstjänst. Tjänsten kräver att en användare har flera roller tilldelade för att att läsa och skriva till entiteter relaterade till den uppdelade arbetsstrukturen. Dessa entiteter omfattar projektuppgifter, resurstilldelningar och aktivitetsberoenden. Om en användare inte kan rendera den uppdelade arbetsstrukturen när han eller hon går till fliken **Uppgifter** beror detta förmodligen på att Project Operations inte har aktiverats. En användare kan få antingen ett säkerhetsrollsfel eller ett fel relaterat till nekad åtkomst.


## <a name="workaround"></a>Lösning

1. Gå till **Inställning > Säkerhet > Användare > Programanvändare**.  

   ![Programläsare](media/applicationuser.jpg)
   
2. Dubbelklicka på programanvändarposten för att bekräfta följande:

 - Användaren har åtkomst till projektet. Verifieringen sker oftast genom att användaren innehar säkerhetsrollen **Projektansvarig**.
 - Microsoft Project-programmets användare finns och är korrekt konfigurerad.
 
3. Om denna användare inte finns kan du skapa en ny användarpost. Välj **Ny användare**. Ändra postformuläret till **Programanvändare** och lägg sedan till **Program-ID**.

   ![Information om programanvändare](media/applicationuserdetails.jpg)

4. Kontrollera att användaren har tilldelats rätt licens och att tjänsten är aktiverad i serviceplaninformationen för licensen.
5. Kontrollera att användaren kan öppna project.microsoft.com.
6. Kontrollera genom projektparametrarna att systemet pekar på rätt projektslutpunkt.
7. Kontrollera att projektprogrammets användare har skapats.
8. Tillämpa följande säkerhetsroller på användaren:

  - Användare av Dataverse
  - Project Operations-systemet
  - Projektsystem

## <a name="error-when-updating-the-work-breakdown-structure"></a>Fel vid uppdatering av uppdelad arbetsstruktur

När en eller flera uppdateringar görs i den uppdelade arbetsstrukturen misslyckas ändringarna och sparas inte. Ett fel uppstår i schemarutnätet och meddelandet "Det gick inte att spara den senaste ändringen du har gjort" visas.

### <a name="workaround"></a>Lösning

1. Kontrollera att användaren har tilldelats rätt licens och att tjänsten är aktiverad i serviceplaninformationen för licensen.
2. Kontrollera att användaren kan öppna project.microsoft.com.
3. Kontrollera att systemet pekar på rätt projektslutpunkt.
4. Kontrollera att projektprogrammets användare har skapats.
5. Tillämpa följande säkerhetsroller på användaren:
  
  - Dataverse-användare eller basanvändare
  - Project Operations-systemet
  - Projektsystem
  - Dubbelskrivningssystem för Project Operations (denna roll krävs om du distribuerar det resurs-/icke-lagerbaserade scenariot för Project Operations.)
