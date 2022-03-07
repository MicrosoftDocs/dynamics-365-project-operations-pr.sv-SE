---
title: Använd tillägget Project Service för att planera ditt arbete i Microsoft Project | Microsoft-dokument
description: I den här ämnet finns information om hur du lägger till, konfigurerar och använder Microsoft Project-tillägget för Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d988419ae5a9d57532902d2553cd7de147e27c1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085670"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Använd Project Service Automation-tillägget för att planera ditt arbete i Microsoft Project

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gör det enklare för dig att göra din projektplanering inklusive uppskattningar. Du kan definiera arbetet så att utgifter, arbete och försäljningsvärde är tydliga när det slutliga förslaget skickas in.  

 Nu kan du installera [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] och göra planeringen i den välkända miljön i Microsoft Project [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Använd de stabila funktionerna för planering och hantering av [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och uppdatera projektplanen i Project Service Automation.  

> [!IMPORTANT]
> - För att använda SharePoint-dokumenthanteringsfunktionen i dina [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filer för [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt kommer din [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] administratör att aktivera dokumenthantering. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] är endast kompatibelt med [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Ladda ned och installera tillägg  
 Ha din [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-inloggningsinformation tillgänglig. Du behöver denna information för att ansluta från [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Från hämtningscenter kan du hämta tillägget för den version av Project Service som stöds antingen [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) eller [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Klicka på hämtningslänken.  

3.  När hämtningen är klar klickar du på **Ja** för att installera tillägget.  

## <a name="configure-the-add-in"></a>Konfigurera tillägget  

1. Öppna [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och klicka på fliken **Project Service**.  

2. Klicka på **Anslut**.  

3. Ange din inloggningsinformation och klicka sedan på **logga in**.  

   Nu kan du börja använda tillägget.  

## <a name="read-from-a-template"></a>Läsa från en mall  
 Läsa från en mall som du skapat i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] och kopierat till [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] för att starta din projektplanering. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Skapa en projektmall (Project Service Automation)](../psa/create-project-template.md)  

1.  Från fliken **Project Service** klickar du på **Läs** > **Project Service Automation-projektmall**.  

2.  Välj en projektmall i listan och klicka sedan på **öppna**.  

    > [!NOTE]
    >  Som standard ställs aktiviteter som kopieras från mallen till projekt in som manuellt schemalagda.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Tilldela [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-roller till projektresurser  

1.  Öppna ett projekt och klicka på menyfliksområdet **Aktivitet**.  

2.  Klicka på **Gantt-schemat** -menyn och välj sedan **Resurslista**.  

3.  Klicka på Resurslista i listrutan **Resursroller för Project Service** och välj en roll för Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Bemanna dina projektet med resurser  

1.  Från fliken Project Service väljer du en rad och klickar på **Hitta resurser**.  

2.  På skärmen **Boka resurs** väljer du den resurs som du vill använda för projektet.  

3.  Klicka på **Boka** och sedan på **OK**.  

## <a name="publish-your-project"></a>Publicera dina projekt  
När din projektplanering är klar är nästa steg är att importera och publicera projektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projektet kommer att importeras till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Prissättning och teamgenerationsprocess tillämpas. Öppna projektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] för att se att teamet, projektuppskattningar och uppdelad arbetsstruktur har genererats. I följande tabell visas var du hittar resultatet:


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Redigera diagram**   | Importera till skärmen [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **uppdelad arbetsstruktur**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Resursark** |   Importera till skärmen [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektteammedlemmar**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Använd användning**    |    Importerar till skärmen [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektberäkningar**.     |

**Importera och publicera projektet**  
1. Från fliken **Project Service** klickar du på **Publicera** > **Nytt Project Service Automation-projekt**.  

2. På dialogrutan **publicera ett nytt projekt i Project Service** anger du **projektnamnet** och väljer **kund**.  

3. Du kan också kontrollera **länka projektplanen i Project Service Automation** till länka planen Projektfil till Project Service Automation.  

4. Klicka på **Publicera**.  

   Länka projektfilen till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gör projektfilen till huvudfilen och anger uppdelad arbetsstruktur i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] till skrivskyddad.  Om du vill göra ändringar i projektplanen, måste du göra dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och publicera dem som uppdateringar till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Redigera ett projekt som har importerats  
 Om du vill göra ändringar i en projektplan som importeras till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] har du två alternativ:  

- Öppna huvudfilen och redigera den i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Ta bort länken från huvudfilen och redigera direkt i Project Service. Som standard är ett projekt som har överförts från [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och kan endast redigeras i Project. Redigera filen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], filens länk har tagits bort.  

### <a name="edit-in-pn_microsoft_project"></a>Redigera i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. I huvudmenyn klickar du på **Project Service** > **Projekt**.  

2. I listan över projekt öppnar du det som du skapade i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Klicka på **öppen i MS Project** från menyfliken. Detta kommer att öppna den länkade huvudfilen i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Ta bort en fil och redigera i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. I huvudmenyn klickar du på **Project Service** > **Projekt**.  

2. I listan över projekt öppnar du det som du skapade i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Klicka på **Ta bort länk från MS Project** från menyfliken.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Skicka en projektfil till SharePoint eller Office-grupper  
 Du kan överföra din projektfil till SharePoint och hitta den under den associerade dokument för ditt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.  Din administratör måste konfigurera dokumenthantering för SharePoint och aktivera den för projektentiteten. 

 Du kan också överföra projektfilen till [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] om du har Office-grupper inställda.

### <a name="upload-a-file-for-sharepoint"></a>Ladda upp en fil för SharePoint  

1. I huvudmenyn klickar du på **Project Service** > **Överför**.  

2. Välj **Till projektdokument i Project Service Automation**.  

3. I dialogrutan **Aktivera öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** väljer du **Ja** eller **Nej**.  

   - När du klickar på **Ja** kommer du att kunna klicka på knappen **Öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**-knappen i Project Service Automation och starta [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och läsa in projektfilen från SharePoint-dokumentbiblioteket.  

   - När du klickar på **Nej** kommer länken för knappen **Öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** inte att fungera.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen finns i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **dokument** för särskilda [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.  

### <a name="upload-a-file-for-office-groups"></a>Överför en fil för Office Group  

1. I huvudmenyn klickar du på **Project Service** > **Överför**.  

2. Välj **Till projektdokument i Project Service Automation**.  

3. I dialogrutan **Aktivera öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** väljer du **Ja** eller **Nej**.  

   - När du klickar på **Ja** kommer du att kunna klicka på knappen **Öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**-knappen i Project Service Automation och starta [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och läsa in projektfilen från SharePoint-dokumentbiblioteket.  

   - När du klickar på **Nej** kommer länken för knappen **Öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** inte att fungera.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen finns i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **dokument** för särskilda [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.  

## <a name="publish--your-project-as-a-template"></a>Publicera dina projekt som en mall  
 Du kan spara projektet och återanvända det genom att spara det som en projektmall i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Projektmallar är återanvändbara projektplaner i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Skapa en projektmall (Project Service Automation)](../psa/create-project-template.md)  

1. Från fliken **Project Service** klickar du på **Publicera** > **Ny Project Service Automation-mall**.  

2. På dialogrutan **publicera ett nytt projekt i Project Service-mall** anger du **Namn på projektmall**.  

3. Du kan också kontrollera **länka projektplanen i Project Service Automation** till länka Projektfil till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Klicka på **Publicera**.  

Länka projektfilen till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gör projektfilen till huvudfilen och anger uppdelad arbetsstruktur i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-mallen till skrivskyddad.  Om du vill göra ändringar i projektplanen, måste du göra dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och publicera dem som uppdateringar till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

### <a name="see-also"></a>Se även  
 [Guiden för projektledare](../psa/project-manager-guide.md)
