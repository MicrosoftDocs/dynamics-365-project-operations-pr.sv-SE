---
title: Använda API:er för projektscheman med Power Automate
description: Detta ämne tillhandahåller ett exempelflöde som använder API:er ("Project schedule application programming interfaces").
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9708226b0955cfa6c405b9616c14765f9ebc21f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597728"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Använda API:er för projektscheman med Power Automate

_**Gäller:** Project Operations för resurs- och icke-lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Detta ämne beskriver ett exempelflöde som visar hur du skapar en komplett projektplan med hjälp av Microsoft Power Automate, hur du skapar en åtgärdsuppsättning och uppdaterar en entitet. Exemplet visar hur du skapar ett projekt, en projektteammedlem, åtgärdsgrupper, projektuppgifter samt resurstilldelningar. Detta ämne förklarar även hur du uppdaterar en entitet och kör en åtgärdsuppsättning.

Följande utgör en fullständig lista över de steg som dokumenteras i exempelflödet i detta ämne:

1. [Skapa en PowerApps-utlösare](#1)
2. [Skapa ett projekt](#2)
3. [Initiera en variabel för teammedlemmen](#3)
4. [Skapa en generisk teammedlem](#4)
5. [Skapa en åtgärdsuppsättning](#5)
6. [Skapa en projektbucket](#6)
7. [Initiera en variabel för länkstatusen](#7)
8. [Initiera en variabel för antalet uppgifter](#8)
9. [Initiera en variabel för projektets uppgifts-ID](#9)
10. [Gör till](#10)
11. [Ange en projektuppgift](#11)
12. [Skapa en projektuppgift](#12)
13. [Skapa en resurstilldelning](#13)
14. [Minska en variabel](#14)
15. [Byt namn på en projektuppgift](#15)
16. [Kör en åtgärdsuppsättning](#16)

## <a name="assumptions"></a>Antaganden

Detta ämne förutsätter att du har grundläggande kunskaper om Dataverse-plattformen, molnflöden och API (Project Schedule Application Programming Interface). Mer information finns i avsnittet [Referenser](#references) senare i det här avsnittet.

## <a name="create-a-flow"></a>Skapa ett flöde

### <a name="select-an-environment"></a>Välj en miljö

Du kan inte skapa Power Automate-flödet i din miljö.

1. Gå till <https://flow.microsoft.com> och logga in med dina autentiseringsuppgifter som global administratör.
2. Välj **Miljöer** i det övre högra hörnet.
3. I listan väljer du den miljö där Dynamics 365 Project Operations finns installerat.

### <a name="create-a-solution"></a>Skapa en lösning

Följ dessa steg om du vill skapa ett [lösningsmedvetet flöde](/power-automate/overview-solution-flows). Genom att skapa ett lösningsmedvetet flöde kan du enklare exportera flödet och använda det senare.

1. I den navigeringsrutan väljer du **Lösningar**.
2. På sidan **Lösningar** väljer du **Ny lösning**.
3. I dialogrutan **Ny lösning** anger du erforderliga fält och väljer sedan **Skapa**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Steg 1: Skapa en PowerApps-utlösare

1. På sidan **Lösningar** väljer du den lösning du skapat och sedan **Nytt**.
2. I det vänstra fönstret väljer du **Molnflöden** \> **Automation** \> **Molnflöde** \> **Direkt**.
3. I fältet **Flödesnamn** anger du **Schemalägg API-demonstrationsflöde**.
4. I listan **Välj hur du vill utlösa detta flöde** väljer du **Power Apps**. När du skapar en Power Apps-utlösare är logiken upp till dig som författare. I detta ämne lämnar du indataparametrarna tomma för testningssyften.
5. Välj **Skapa**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Steg 2: Skapa ett projekt

Skapa ett exempelprojekt genom att följa stegen nedan.

1. I flödet som du skapat väljer du **Nytt steg**.

    ![Lägga till ett nytt steg.](media/newstep.png)

2. I dialogrutan **Välj en åtgärd** anger du **utför utgående åtgärd** i sökfältet. På fliken **Åtgärder** markerar du åtgärden i resultatlistan.

    ![Välja en åtgärd.](media/chooseactiontab.png)

3. I det nya steget markerar du ellipsen (**...**) och sedan **Byt namn**.

![Byta namn på ett steg.](media/renamestep.png)

4. Byt namn på steget **Skapa projekt**.
5. I fältet **Åtgärdsnamn** väljer du **msdyn\_CreateProjectV1**.
6. Under fältet **msdyn\_subject** väljer du **Lägg till dynamiskt innehåll**.
7. I fliken **Uttryck** anger du **Projektnamn - utcNow()** i funktionsfältet.
8. Välj **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Steg 3: Initiera en variabel för teammedlemmen

1. I flödet väljer du **Nytt steg**.
2. I dialogrutan **Välj en åtgärd** anger du **initiera variabel** i sökfältet. På fliken **Åtgärder** markerar du åtgärden i resultatlistan.
3. I det nya steget markerar du ellipsen (**...**) och sedan **Byt namn**.
4. Byt namn på steget **Init-teammedlem**.
5. I fältet **Namn** anger du **TeamMemberAction**.
6. I fältet **Typ** väljer du **Sträng**.
7. I fältet **Värde** anger du **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Steg 4: Skapa en generisk teammedlem

1. I flödet väljer du **Nytt steg**.
2. I dialogrutan **Välj en åtgärd** anger du **utför utgående åtgärd** i sökfältet. På fliken **Åtgärder** markerar du åtgärden i resultatlistan.
3. I det nya steget markerar du ellipsen (**...**) och sedan **Byt namn**.
4. Byt namn på steget **Skapa teammedlem**.
5. För fältet **Åtgärdsnamn** väljer du **TeamMemberAction** i dialogrutan **Dynamiskt innehåll**.
6. Ange följande parameterinformation i fältet **Åtgärdsparametrar**.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Här följer en förklaring av parametrarna:

    - **\@\@odata.type** – Entitetens namn. Skriv till exempel **"Microsoft.Dynamics.CRM.msdynprojectteam\_"**.
    - **msdyn\_projectteamid** – Den primära nyckeln för projektteamets ID. Värdet är ett GUID-uttryck (globalt unik identifierare).   ID:t skapas från uttrycksfliken.

    - **msdyn\_project\@odata.bind** – Projekt-ID för ägande projekt. Värdet blir dynamiskt innehåll som kommer från svaret i steget Skapa projekt. Kontrollera att du anger den fullständiga sökvägen och lägger till dynamiskt innehåll mellan parenteserna. Citattecken krävs. Skriv till exempel **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_name** – Namnet på teammedlemmen. Skriv till exempel **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Steg 5: Skapa en åtgärdsuppsättning

1. I flödet väljer du **Nytt steg**.
2. I dialogrutan **Välj en åtgärd** anger du **utför utgående åtgärd** i sökfältet. På fliken **Åtgärder** markerar du åtgärden i resultatlistan.
3. I det nya steget markerar du ellipsen (**...**) och sedan **Byt namn**.
4. Byt namn på steget **Skapa åtgärdsuppsättning**.
5. I fältet **Åtgärdsnamn** väljer du den anpassade Dataverse-åtgärden **msdyn\_CreateOperationSetV1**.
6. I fältet **Beskrivning** anger du **ScheduleAPIDemoOperationSet**.
7. I fältet **Projekt** anger du **/msdyn\_projects(**.
8. I dialogrutan **Dynamiskt innehåll** väljer du **msdyn\_CreateProjectV1Response ProjectId**.
9. I fältet **Projekt** anger du **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Steg 6: Skapa en projektbucket

1. I flödet väljer du **Nytt steg**.
2. I dialogrutan **Välj en åtgärd** anger du **lägg till ny rad** i sökfältet. På fliken **Åtgärder** markerar du åtgärden i resultatlistan.
3. I det nya steget markerar du ellipsen (**...**) och sedan **Byt namn**.
4. Byt namn på steget **Skapa bucket**.
5. I fältet **Tabellnamn** väljer du **Projekt-buckets**.
6. I fältet **Namn** anger du **ScheduleAPIDemoBucket1**.
7. För fältet **Projekt** väljer du **msdyn\_CreateProjectV1Response ProjectId** i dialogrutan **Dynamiskt innehåll**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Steg 7: Initiera en variabel för länkstatusen

1. I flödet väljer du **Nytt steg**.
2. I dialogrutan **Välj en åtgärd** anger du **initiera variabel** i sökfältet. På fliken **Åtgärder** markerar du åtgärden i resultatlistan.
3. I det nya steget markerar du ellipsen (**...**) och sedan **Byt namn**.
4. Byt namn på steget **Init länkstatus**.
5. I fältet **Namn** anger du **länkstatus**.
6. I fältet **Typ** väljer du **Heltal**.
7. I fältet **Värde** anger du **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Steg 8: Initiera en variabel för antalet uppgifter

1. I flödet väljer du **Nytt steg**.
2. I dialogrutan **Välj en åtgärd** anger du **initiera variabel** i sökfältet. På fliken **Åtgärder** markerar du åtgärden i resultatlistan.
3. I det nya steget markerar du ellipsen (**...**) och sedan **Byt namn**.
4. Byt namn på steget **Init antalet uppgifter**.
5. I fältet **Namn** anger du **antalet uppgifter**.
6. I fältet **Typ** väljer du **Heltal**.
7. I fältet **Värde** anger du **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Steg 9: Initiera en variabel för projektets uppgifts-ID

1. I flödet väljer du **Nytt steg**.
2. I dialogrutan **Välj en åtgärd** anger du **initiera variabel** i sökfältet. På fliken **Åtgärder** markerar du åtgärden i resultatlistan.
3. I det nya steget markerar du ellipsen (**...**) och sedan **Byt namn**.
4. Byt namn på steget **Init ProjectTaskID**.
5. I fältet **Namn** anger du **antalet uppgifter**.
6. I fältet **Typ** väljer du **Sträng**.
7. För fältet **Värde** anger du **guid()** i uttrycksverktyget.

## <a name="step-10-do-until"></a><a id="10"></a>Steg 10: Gör till

1. I flödet väljer du **Nytt steg**.
2. I dialogrutan **Välj en åtgärd** anger du **Gör till** i sökfältet. På fliken **Åtgärder** markerar du åtgärden i resultatlistan.
3. Ange det första värdet i den villkorliga instruktionen till variabeln **antal uppgifter** från dialogrutan **Dynamiskt innehåll**.
4. Ange villkoret som **mindre än lika med**.
5. Ange det andra värdet i den villkorliga instruktionen som **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Steg 11: Ange en projektuppgift

1. I flödet väljer du **Nytt steg**.
2. I dialogrutan **Välj en åtgärd** anger du **ange variabel** i sökfältet. På fliken **Åtgärder** markerar du åtgärden i resultatlistan.
3. I det nya steget markerar du ellipsen (**...**) och sedan **Byt namn**.
4. Byt namn på steget **Ange projektuppgift**.
5. I fältet **Namn** väljer du **msdyn\_projecttaskid**.
6. För fältet **Värde** anger du **guid()** i uttrycksverktyget.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Steg 12: Skapa en projektuppgift

Följ instruktionerna nedan om du vill skapa en projektuppgift med ett unikt ID som hör till det aktuella projektet och den projektbucket du skapat.

1. I flödet väljer du **Nytt steg**.
2. I dialogrutan **Välj en åtgärd** anger du **utför utgående åtgärd** i sökfältet. På fliken **Åtgärder** markerar du åtgärden i resultatlistan.
3. I det nya steget markerar du ellipsen (**...**) och sedan **Byt namn**.
4. Byt namn på steget till **Skapa projektuppgift**.
5. I fältet **Åtgärdsnamn** väljer du **msdyn\_PssCreateV1**.
6. Ange följande parameterinformation i fältet **Entitet**.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Här följer en förklaring av parametrarna:

    - **\@\@odata.type** – Entitetens namn. Skriv till exempel **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – Uppgiftens unika ID. Värdet ska anges till en dynamisk variabel från **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – Projekt-ID för ägande projekt. Värdet blir dynamiskt innehåll som kommer från svaret i steget Skapa projekt. Kontrollera att du anger den fullständiga sökvägen och lägger till dynamiskt innehåll mellan parenteserna. Citattecken krävs. Skriv till exempel **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_subject** – Valfritt uppgiftsnamn.
    - **msdyn\_projectbucket\@odata.bind** – Den projektbucket som innehåller uppgifterna. Värdet blir dynamiskt innehåll som kommer från svaret i steget "Skapa bucket". Kontrollera att du anger den fullständiga sökvägen och lägger till dynamiskt innehåll mellan parenteserna. Citattecken krävs. Skriv till exempel **"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_start** – Dynamiskt innehåll för startdatum. Morgondagen representeras till exempel som **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – Det tidsplanerade startdatumet. Morgondagen representeras till exempel som **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – Det schemalagda slutdatumet. Välj ett datum i framtiden. Ange till exempel **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – Länkstatusen. Ange till exempel **"192350000"**.

7. För fältet **OperationSetId** väljer du **msdyn\_CreateOperationSetV1Response** i dialogrutan **Dynamiskt innehåll**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Steg 13: Skapa en resurtilldelning

1. I flödet väljer du **Nytt steg**.
2. I dialogrutan **Välj en åtgärd** anger du **utför utgående åtgärd** i sökfältet. På fliken **Åtgärder** markerar du åtgärden i resultatlistan.
3. I det nya steget markerar du ellipsen (**...**) och sedan **Byt namn**.
4. Byt namn på steget **Skapa tilldelning**.
5. I fältet **Åtgärdsnamn** väljer du **msdyn\_PssCreateV1**.
6. Ange följande parameterinformation i fältet **Entitet**.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. För fältet **OperationSetId** väljer du **msdyn\_CreateOperationSetV1Response** i dialogrutan **Dynamiskt innehåll**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Steg 14: Minska en variabel

1. I flödet väljer du **Nytt steg**.
2. I dialogrutan **Välj en åtgärd** anger du **minska variabel** i sökfältet. På fliken **Åtgärder** markerar du åtgärden i resultatlistan.
3. I fältet **Namn** välje du **antal uppgifter**.
4. I fältet **Värde** anger du **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Steg 15: Byt namn på en projektuppgift

1. I flödet väljer du **Nytt steg**.
2. I dialogrutan **Välj en åtgärd** anger du **utför utgående åtgärd** i sökfältet. På fliken **Åtgärder** markerar du åtgärden i resultatlistan.
3. I det nya steget markerar du ellipsen (**...**) och sedan **Byt namn**.
4. Byt namn på steget till **Byt namn på projektuppgift**.
5. I fältet **Åtgärdsnamn** väljer du **msdyn\_PssUpdateV1**.
6. Ange följande parameterinformation i fältet **Entitet**.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. För fältet **OperationSetId** väljer du **msdyn\_CreateOperationSetV1Response** i dialogrutan **Dynamiskt innehåll**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Steg 16: Kör en åtgärdsuppsättning

1. I flödet väljer du **Nytt steg**.
2. I dialogrutan **Välj en åtgärd** anger du **utför utgående åtgärd** i sökfältet. På fliken **Åtgärder** markerar du åtgärden i resultatlistan.
3. I det nya steget markerar du ellipsen (**...**) och sedan **Byt namn**.
4. Byt namn på steget **Kör åtgärdsuppsättning**.
5. I fältet **Åtgärdsnamn** väljer du **msdyn\_ExecuteOperationSetV1**.
6. För fältet **OperationSetId** väljer du **msdyn\_CreateOperationSetV1ResponseOperationSetId** i dialogrutan **Dynamiskt innehåll**.

## <a name="references"></a>Referenser

- [Översikt över hur du integrerar flöden med Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Använda API:er för projektscheman för att utföra åtgärder med schemaläggningsentiteter](schedule-api-preview.md)
- [Översikt av molnflödena - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Översikt över lösningsmedvetna flöden - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
