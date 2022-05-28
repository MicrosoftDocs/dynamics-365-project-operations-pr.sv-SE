---
title: Distribuera appen Project Operations Dataverse manuellt med stöd för dubbelriktad skrivning
description: I ämne beskrivs hur du manuellt distribuerar appen Project Operations Dataverse så att den har stöd för dubbelriktad skrivning.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: b82eef7b5f64705f37f224172c14f6734612329e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591242"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Distribuera appen Project Operations Dataverse manuellt med stöd för dubbelriktad skrivning

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

I ämne beskrivs hur du manuellt distribuerar appen Microsoft Dynamics 365 Project Operations i Microsoft Dataverse så att den har stöd för dubbelriktad skrivning. Project Operations identifierar miljöns konfiguration och lägger till ytterligare stöd för dubbelriktad skrivning om kraven uppfylls.

Under distributionen via Microsoft Dynamics Lifecycle Services (LCS), om du har följt instruktionerna i det här ämnet kan du hoppa över distributionen av Microsoft Power Platform-integrering (kallades tidigare Common Data Service-miljö).

Processen av att distribuera Project Operations i Dataverse så att den stöder dubbelriktad skrivning har fyra huvudsteg:

1. [Skapa en ny miljö i Dataverse som ger stöd för dubbelriktad skrivning](#create).
2. [Lägg till krav för dubbelriktad skrivning i miljön](#prerequisites).
3. [Lägg till Project Operations Dataverse-app](#dataverse).
4. [Länka dina miljöer](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Skapa en ny miljö i Dataverse som ger stöd för dubbelriktad skrivning

Du måste logga in som en administratör.

1. Öppna [Power Platform administrationscenter](https://admin.powerplatform.com) och logga in som en administratör.
2. Skapa en ny miljö och namnge den.
3. Välj miljötypen. Välj om du har registrerat dig för erbjudande om utvärderingsversion **utvärderingsversion (prenumerationsbaserad)**.
4. Bekräfta distributionsområdet.
5. Aktivera alternativet **Skapa en databas för miljön**. 
6. Bekräfta språket och kontrollera sedan att valutan matchar valutan för apparna för ekonomi och drift.
7. Aktivera alternativet **Dynamics 365-appar** och bekräfta att fältet **Automatiskt distribuera dessa appar** har angetts till **Inget**.
8. Lägg till en säkerhetsgrupp om en säkerhetsgrupp krävs.
9. Välj **Spara** för att skapa miljön.
10. Vänta tills distributionen har slutförts och miljön har nått tillståndet **Klar**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Lägg till krav för dubbelriktad skrivning i miljön.

Stöd för dubbelriktad skrivning omfattar ytterligare fält som läggs till i nyckelentiteter, till exempel entiteten **Företag**. Om du lägger till stöd för dubbelriktad skrivning i en befintlig miljö kan du behöva uppdatera informationen för att aktivera supporten. Information om hur du startar data finns i [Bootstrap företagsdata](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Mer information om dubbelriktad skrivning finns i [Systemkrav för dubbelriktad skrivning](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Slutför proceduren om du vill lägga till krav med dubbelriktad skrivningar i miljön.

1. Öppna den miljö du just skapat och gå sedan till **Resurs** \> **Dynamics 365-appar**.
2. Välj **lösning för dubbelriktad skrivning** i applistan och installera den.
3. Vänta tills installationen har slutförts. Välj sedan **Orkestreringslösning för dubbelriktad skrivning** i applistan och installera den.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Lägg till Project Operations Dataverse-app

Du kan endast utföra den här proceduren om du har slutfört de föregående procedurerna innan du installerade Project Operations. Under installationen analyseras miljökonfigurationen och stöd för dubbelriktning skrivning läggs till om det behövs.

1. Öppna den miljö du just skapat och gå sedan till **Resurs** \> **Dynamics 365-appar**.
2. Välj **Microsoft Dynamics 365 Project Operations** i applistan och installera det.

## <a name="link-your-environments"></a><a name="link"></a>Länka dina miljöer.

När Dataverse-miljön har distribuerats kan du konfigurera länken i dina appar för ekonomi och drift. Följ anvisningarna i [Använd guiden för dubbelriktade skrivningar för att länka dina miljöer](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
