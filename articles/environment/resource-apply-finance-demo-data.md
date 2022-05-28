---
title: Använda demodata i en Finance molnvärdbaserad miljö
description: I detta ämne beskrivs hur du använder demodata från Project Operations till en miljö med Dynamics 365 Finance-moln som värd.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e4ccc7eb02fabdc0476fe454f33bff637ab8b835
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588988"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Använda demodata i en Finance molnvärdbaserad miljö

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

> [!IMPORTANT]
> Detta ämne gäller endast Microsoft Dynamics 365 Finance-version 10.0.13 och kan endast utföras i en molnvärdmiljö. Slutför stegen i det här ämnet **INNAN** du tillämpar kvalitetsuppdateringar av miljön.

1. I ditt LCS-projekt öppnar du sidan **Miljöinformation**. Observera att den innehåller den information som behövs för att ansluta till miljön med hjälp av RDP (Remote Desktop Protocol).

![Miljöinformation.](./media/1EnvironmentDetails.png)

Den första uppsättningen av markerade autentiseringsuppgifter är autentiseringsuppgifterna till det lokala kontot och innehåller en hyperlänk till anslutningen till fjärrskrivbordet. Autentiseringsuppgifterna inkluderar administratörens användarnamn och lösenord till miljön. Den andra uppsättningen autentiseringsuppgifter används för att logga in på SQL-servern i den här miljön.

2. Fjärranslutning till miljön genom hyperlänken i **Lokala konton** och använd **autentiseringsuppgifterna till det lokala kontot** för att autentisera.
3. Gå till **Internet Information Services** > **Programpooler** > **AOSService** och stoppa tjänsten. Du stoppar tjänsten i detta skede så att du kan fortsätta att byta ut SQL-databasen.

![Stoppa AOS.](./media/2StopAOS.png)

4. Gå till **Tjänster** och stoppa följande två artiklar:

- Microsoft Dynamics 365 Unified Operations : batchhanteringstjänst
- Microsoft Dynamics 365 Unified Operations: ramverk för import och export av data

![Stoppa tjänster.](./media/3StopServices.png)

5. Öppna Microsoft SQL Server Management Studio. Logga in med dina autentiseringsuppgifter till SQL-servern och använd axdb-administratörens användarnamn och lösenord från LCS-sidan **Information om miljöer**.

![SQL Server Management Studio.](./media/4SSMS.png)

6. I objektutforskaren, **Databaser** och lokalisera **AXDB**. Du ersätter databasen med en ny databas som finns i [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Kopiera zip-filen till den virtuella datorn som du har fjärråtkomst till och extrahera zip-innehåll.
8. I SQL Server Management Studio högerklickar du på **AxDB** och väljer sedan **Uppgifter** > **Återställ** > **Databas**.

![Återställa databas.](./media/5RestoreDatabase.png)

9. Välj **Källenhet** och navigera till filen som extraherades ur den zip du kopierade.

![Källenheter.](./media/6SourceDevice.png)

10. Välj **Alternativ** och välj sedan **Skriv över den befintliga databasen** och **Stäng befintliga anslutningar till måldatabasen**. 
11. Välj **OK**.

![Återställ inställningar.](./media/7RestoreSetting.png)

Du får en bekräftelse på att AXDB-återställningen har slutförts. När du har fått bekräftelsemeddelandet kan du stänga SQL Services Management Studio.

12. Gå tillbaka till **Internet Information Services** > **Programpooler** > **AOSService** och starta AOSService.
13. Gå till **Tjänster** och starta de två tjänster du stoppade tidigare.

14. Leta upp verktyget AdminUserProvisioning på den här virtuella datorn. Leta under K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Kör .ext-filen med din användaradress i fältet **E-postadress**. 
16. Välj **Skicka**.

![Användarförsörjning för administratör.](./media/8AdminUserProvisioning.png)

Det här tar några minuter att slutföra. Du bör få ett bekräftelsemeddelande om att administratörsanvändaren har uppdaterats.

17. Kör slutligen kommandotolken som administratör och utför iisreset

![IIS-återställning.](./media/9IISReset.png)

18. Avsluta sessionen på fjärrskrivbordet och använd LCS-sidan **Information om miljö** för att logga in på miljön och bekräfta att den fungerar som den ska.

![Finance and Operations.](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]