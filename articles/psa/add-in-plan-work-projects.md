---
title: Planera ditt arbete i Microsoft Project med tillägget Project Service
description: I den här artikeln finns information om hur du använder Microsoft Project-tillägget för Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 779d83a896dd7d92c6584e6f1c57b1ea567e9051
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911020"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Planera ditt arbete i Microsoft Project med tillägget Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gör det enklare för dig att göra din projektplanering inklusive uppskattningar. Du kan definiera arbetet så att utgifter, arbete och försäljningsvärde är tydliga när det slutliga förslaget skickas in.  

Du kan installera [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] och göra planeringen i den välkända miljön i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Använd de stabila funktionerna för planering och hantering av [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och uppdatera projektplanen i Project Service Automation.  

> [!IMPORTANT]
> - För att använda SharePoint-dokumenthanteringsfunktionen i dina [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filer för [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt kommer din [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] administratör att aktivera dokumenthantering. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] är endast kompatibelt med [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Ladda ned och installera tillägg  
 Ha din [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-inloggningsinformation tillgänglig. Du behöver denna information för att ansluta från [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Från hämtningscenter kan du hämta tillägget för den version av Project Service som stöds antingen [V2.X](/dynamics365/project-operations/psa/overview#guidance-for-earlier-versions-app-version-2x-or-1x) eller [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Välj hämtningslänken.  

3.  När hämtningen är klar väljer du **Ja** för att installera tillägget.  

## <a name="configure-the-add-in"></a>Konfigurera tillägget  

1. Öppna [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och välj fliken **Project Service**.  

2. Välj **Anslut**.  

3. Ange din inloggningsinformation och välj sedan **Logga in**.  

   Nu kan du börja använda tillägget.  

## <a name="read-from-a-template"></a>Läsa från en mall  
 Läsa från en mall som du skapat i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] och kopierat till [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] för att starta din projektplanering. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Skapa en projektmall (Project Service Automation)](../psa/create-project-template.md)  

1.  Från fliken **Project Service** väljer du **Läs** > **Projektmall för Project Service Automation**.  

2.  Välj en projektmall i listan och välj sedan **Öppna**.  

    > [!NOTE]
    >  Som standard ställs uppgifter som kopieras från mallen till projekt in som manuellt schemalagda.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Tilldela [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-roller till projektresurser  

1.  Öppna ett projekt och markera menyfliksområdet **Uppgift**.  

2. Välj menyn **Gantt-schema** och välj sedan **Resurslista**.  

3. Markera listrutan **Resursroller för Project Service** i resurslistan och välj en roll för Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Bemanna dina projektet med resurser  

1.  Från fliken Project Service väljer du en rad och sedan **Hitta resurser**.  

2.  På skärmen **Boka resurs** väljer du den resurs som du vill använda för projektet.  

3.  Välj **Boka** och välj sedan **OK**.  

## <a name="publish-your-project"></a>Publicera dina projekt  
När din projektplanering är klar är nästa steg är att importera och publicera projektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projektet kommer att importeras till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Prissättning och teamgenerationsprocess tillämpas. Öppna projektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] för att se att teamet, projektuppskattningar och uppdelad arbetsstruktur har genererats. I följande tabell visas var du hittar resultaten:


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Redigera diagram**   | Importera till skärmen [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **uppdelad arbetsstruktur**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Resursark** |   Importera till skärmen [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektgruppmedlemmar**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Använd användning**    |    Importerar till vyn [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projektuppskattningar**.     |

**Importera och publicera projektet**  
1. I fliken **Project Service** går du till **Publicera** > **Nytt Project Service Automation-projekt**.  

2. I dialogrutan **Publicera ett nytt projekt i Project Service** anger du **projektnamnet** och väljer **Kund**.  

3. Du kan också välja **Länka projektplan till Project Service Automation** (valfritt) för att länka planens projektfil till Project Service Automation.  

4. Välj **Publicera**.  

   Länka projektfilen till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gör projektfilen till huvudfilen och anger uppdelad arbetsstruktur i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] till skrivskyddad.  Om du vill göra ändringar i projektplanen, måste du göra dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och publicera dem som uppdateringar till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Redigera ett projekt som har importerats  
 Om du vill göra ändringar i en projektplan som importeras till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] har du två alternativ:  

- Öppna huvudfilen och redigera den i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Ta bort länken från huvudfilen och redigera direkt i Project Service. Som standard är ett projekt som har överförts från [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och kan endast redigeras i Project. Redigera filen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], filens länk har tagits bort.  

### <a name="edit-in-pn_microsoft_project"></a>Redigera i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. I huvudmenyn går du till **Project Service** > **Projekt**.  

2. I listan över projekt öppnar du det som du skapade i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Markera **Öppna i MS Project** i menyfliksområdet. Detta kommer att öppna den länkade huvudfilen i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Ta bort en fil och redigera i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. I huvudmenyn går du till **Project Service** > **Projekt**.  

2. I listan över projekt öppnar du det som du skapade i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Markera **Ta bort länk från MS Project** i menyfliksområdet.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Skicka en projektfil till SharePoint eller Office-grupper  
 Du kan överföra din projektfil till SharePoint och hitta den under den associerade dokument för ditt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.  Din administratör måste konfigurera dokumenthantering för SharePoint och aktivera den för projektentiteten. 

 Du kan också överföra projektfilen till [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] om du har Office-grupper inställda.

### <a name="upload-a-file-for-sharepoint"></a>Ladda upp en fil för SharePoint  

1. I huvudmenyn går du till **Project Service** > **Överför**.  

2. Välj **Till projektdokument i Project Service Automation**.  

3. I dialogrutan **Aktivera öppnande i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**-dialogrutan väljer du **Ja** eller **Nej**.  

   - Om du väljer **Ja** kommer du att kunna välja **Öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** i Project Service Automation samt starta [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och läsa in projektfilen från SharePoint-dokumentbiblioteket.  

   - Om du väljer **Nej** fungerar inte länken **Öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** i.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen finns i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **dokument** för särskilda [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.  

### <a name="upload-a-file-for-office-groups"></a>Överför en fil för Office Group  

1. I huvudmenyn går du till **Project Service** > **Överför**.  

2. Välj **Till projektdokument i Project Service Automation**.  

3. I dialogrutan **Aktivera öppnande i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**-dialogrutan väljer du **Ja** eller **Nej**.  

   - Om du väljer **Ja** kommer du att kunna välja **Öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** i Project Service Automation samt starta [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och läsa in projektfilen från SharePoint-dokumentbiblioteket.  

   - Om du väljer **Nej** fungerar inte länken **Öppna i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** i.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen finns i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **dokument** för särskilda [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projekt.  

## <a name="publish--your-project-as-a-template"></a>Publicera dina projekt som en mall  
 Du kan spara projektet och återanvända det genom att spara det som en projektmall i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Projektmallar är återanvändbara projektplaner i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Mer information finns i [Skapa en projektmall (Project Service Automation)](../psa/create-project-template.md). 

1. I fliken **Project Service** går du till **Publicera** > **Ny Project Service Automation-mall**.  

2. I dialogrutan **Publicera ett nytt projekt i Project Service-mall** anger du **Namn på projektmall**.  

3. Du kan också välja **Länka projektplan i Project Service Automation** för att länka projektfilen till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Välj **Publicera**.  

Länka projektfilen till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gör projektfilen till huvudfilen och anger uppdelad arbetsstruktur i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-mallen till skrivskyddad.  Om du vill göra ändringar i projektplanen, måste du göra dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] och publicera dem som uppdateringar till [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Läs ett resursinläst schema

När du läser ett projekt från Project Service Automation synkroniseras inte resursens kalender till skrivbordsklienten. Om det finns skillnader i uppgifternas varaktighet, arbetsinsats eller slut beror detta förmodligen på att resurserna och skrivbordsklienten inte har samma mallkalender för arbetstimmar tillämpade på projektet.


## <a name="data-synchronization"></a>Datasynkronisering
Tabellerna i det här avsnittet innehåller information om synkroniseringen av entitetsdata mellan Project Service Automation och Microsoft Project-tilläggsprogrammet.

### <a name="project-task-entity-table"></a>Entitetstabell för projektaktivitet
I följande tabell beskrivs hur data för projektuppgifter synkroniseras mellan Project Service Automation och det stationära Microsoft Project-tillägget.

| **Entitet** | **Fält** | **Microsoft Project till Project Service Automation** | **Project Service Automation till Microsoft Project** |
| --- | --- | --- | --- |
| Projektuppgift | Förfallodatum | Synkroniserad | Ej synkroniserat |
| Projektuppgift | Beräknad insats | Synkroniserad | Ej synkroniserat |
| Projektuppgift | Klient-ID för MS Project | Synkroniserad | Ej synkroniserat |
| Projektuppgift | Överordnad uppgift | Synkroniserad | Ej synkroniserat |
| Projektuppgift | Project | Synkroniserad | Ej synkroniserat |
| Projektuppgift | Projektuppgift | Synkroniserad | Ej synkroniserat |
| Projektuppgift | Projektuppgiftens namn | Synkroniserad | Ej synkroniserat |
| Projektuppgift | Resursenhet (utfasad i version 3.0) | Synkroniserad | Ej synkroniserat |
| Projektuppgift | Schemalagd tid | Synkroniserad | Ej synkroniserat |
| Projektuppgift | Startdatum | Synkroniserad | Ej synkroniserat |
| Projektuppgift | ID för WBS | Synkroniserad | Ej synkroniserat |

### <a name="team-member-entity-table"></a>Entitetsregister för teammedlem
I följande tabell beskrivs hur data för teammedlemmar synkroniseras mellan Project Service Automation och Micros

| **Entitet** | **Fält** | **Microsoft Project till Project Service Automation** | **Project Service Automation till Microsoft Project** |
| --- | --- | --- | --- |
| Teammedlem | Klient-ID för MS Project | Synkroniserad | Ej synkroniserat |
| Teammedlem | Positionens namn | Synkroniserad | Ej synkroniserat |
| Teammedlem | projekt | Synkroniserad | Synkroniserad |
| Teammedlem | Projektteam | Synkroniserad | Synkroniserad |
| Teammedlem | Resursenhet | Ej synkroniserat | Synkroniserad |
| Teammedlem | Roll | Ej synkroniserat | Synkroniserad |
| Teammedlem | Arbetstider | Ej synkroniserat | Ej synkroniserat |

### <a name="resource-assignment-entity-table"></a>Entitetstabell för resurstilldelning
I följande tabell beskrivs hur data för resurstilldelningar synkroniseras mellan Project Service Automation och Micros

| **Entitet** | **Fält** | **Microsoft Project till Project Service Automation** | **Project Service Automation till Microsoft Project** |
| --- | --- | --- | --- |
| Resurstilldelning | Från den | Synkroniserad | Ej synkroniserat |
| Resurstilldelning | timmar | Synkroniserad | Ej synkroniserat |
| Resurstilldelning | Klient-ID för MS Project | Synkroniserad | Ej synkroniserat |
| Resurstilldelning | Planerat arbete | Synkroniserad | Ej synkroniserat |
| Resurstilldelning | Project | Synkroniserad | Ej synkroniserat |
| Resurstilldelning | Projektteam | Synkroniserad | Ej synkroniserat |
| Resurstilldelning | Resurstilldelning | Synkroniserad | Ej synkroniserat |
| Resurstilldelning | Uppgift | Synkroniserad | Ej synkroniserat |
| Resurstilldelning | Hittills | Synkroniserad | Ej synkroniserat |

### <a name="project-task-dependencies-entity-table"></a>Entitetstabell för projektaktivitetsberoenden
I följande tabell beskrivs hur entitetsdata för projektuppgiftsberoenden synkroniseras mellan Project Service Automation och Micros

| **Entitet** | **Fält** | **Microsoft Project till Project Service Automation** | **Project Service Automation till Microsoft Project** |
| --- | --- | --- | --- |
| Beroenden för projektuppgift | Beroende för projektuppgift | Synkroniserad | Ej synkroniserat |
| Beroenden för projektuppgift | Länktyp | Synkroniserad | Ej synkroniserat |
| Beroenden för projektuppgift | Föregående uppgift | Synkroniserad | Ej synkroniserat |
| Beroenden för projektuppgift | Project | Synkroniserad | Ej synkroniserat |
| Beroenden för projektuppgift | Efterföljande uppgift | Synkroniserad | Ej synkroniserat |

### <a name="additional-resources"></a>Ytterligare resurser
 [Guiden för projektledare](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
