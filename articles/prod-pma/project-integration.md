---
title: Integrering för Microsoft Project Client
description: Det kan vara komplicerat att planera och underhålla ett projekt. Det innebär att projektledarna måste använda verktyg som hjälper dem att hantera den här uppgiften. Integrering med Microsoft Project Client tillhandahåller stöd för att öppna och hantera en uppdelad arbetsstruktur för projekt.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: b312ec5b1f4e6a98a2cbf1667b2f55b758b2d613
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269857"
---
# <a name="microsoft-project-client-integration"></a>Integrering för Microsoft Project Client

[!include [banner](../includes/banner.md)]

Det kan vara komplicerat att planera och underhålla ett projekt. Det innebär att projektledarna måste använda verktyg som hjälper dem att hantera den här uppgiften. Integrering med Microsoft Project Client tillhandahåller stöd för att öppna och hantera en uppdelad arbetsstruktur för projekt. Projektledaren kan publicera alla ändringar i Dynamics 365 Finance uppdelad arbetsstruktur för projekt.

> [!NOTE]
> Om du använder uppdateringen från juli (version 10.0.4) måste du installera KB 4054797 och 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Konfigurera tillägget Microsoft Project Client
För att aktivera Microsoft Project Client krävs tillägg Microsoft Dynamics 365 krävs för att installeras i användarens klient Microsoft Project-appar. Det gör du genom att öppna **arbetsytan projektledning**.

•   Klicka på **Konfigurera tillägg för projektklient** från avsnittet **Länkar** > **Konfiguration** på arbetsytan.

•   Klicka på **Öppna** och sedan på **Kör** när du uppmanas till det.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Öppna och redigera ett befintligt utkast av uppdelad arbetsstruktur i Microsoft Project Client
Om ett projekt Dynamics 365 Finance redan har en uppdelad arbetsstruktur kan du öppna arbetsstrukturen i Microsoft Project Client-appar om strukturen för arbete är i utkastform. Om du vill öppna från **Projekt** klickar du på länken **Öppna i Microsoft Project** fliken **Plan**. Du kan även öppna den här sidan från Microsoft Project Client-appar genom att klicka på **Öppna** i fliken **Microsoft Dynamics 365**. Välj **juridisk person** och **projekt** i listan.

> [!NOTE]
> Om du använder Internet Explorer som webbläsare måste du klicka på **Spara** för att manuellt öppna från platsen där filen hämtas till. Du kan också klicka på **Spara och öppna** för att öppna filen i Microsoft Project Client. Byt inte namn på filnamnet när du sparar.

Innan du gör några ändringar i filen med Microsoft Project Client måste du checka ut den. Klicka på **checka ut** på fliken **Microsoft Dynamics 365**. Detta gör att andra användare inte kan redigera uppdelad arbetsstruktur från Finance på samma gång. Om du vill publicera uppdelad arbetsstrukturen när du har slutfört eventuella ändringar klickar du på **checka in** på fliken **Microsoft Dynamics 365**.

Om ett projektteam redan har lagts till i projektet i Finance kommer resurslistan att fyllas i med teammedlemmarna. Om ett projektteam ännu inte har lagts till i projektet kan du välja resurser och bygga teamet i Microsoft Project Client genom att klicka på knappen **Resurser** på fliken **Microsoft Dynamics 365**. 

Följande data kommer att synkroniseras tillbaka till Finance som en del av incheckningsprocessen:

•   Uppgiftsnamn

•   Startdatum

•   Slutdatum

•   Föregångare

•   Resursnamn

•   Kategori

•   Resurskategori

•   Arbetstider

•   Anteckningar

•   Prioritet

> [!NOTE]
> Om du lägger till några andra kolumner i Microsoft Project Client-filen sparas de inte i filen och kommer inte att visas när filen öppnas igen.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Skapa en uppdelad arbetsstruktur för ett befintligt projekt med hjälp av Microsoft Project Client
För att skapa en ny uppdelad arbetsstruktur genom att använda Microsoft Project Client följ dessa steg:


1.  Öppna Microsoft Project Client.

2.  På fliken **Microsoft Dynamics 365** klicka på **Öppna**.

3.  Välj **juridisk person** för projektet.

4.  Välj **projektet**.

5.  Klicka på **Prova** på fliken **Microsoft Dynamics 365**.

6.  När du är klar att publicera till Finance, klickar du på **Checka in** på fliken **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Ersätt befintlig uppdelad arbetsstruktur för ett befintligt projekt med hjälp av Microsoft Project Client
Gör så här om du vill skapa en ny uppdelad arbetsstruktur av Microsoft Project Client och ersätta en befintlig arbetsstruktur för ett befintligt projekt:

1.  Öppna Microsoft Project Client.

2.  Skapa schemat i Microsoft Project Client.

3.  På fliken **Microsoft Dynamics 365** klicka på **Spara ändringar** > **Ersätt befintligt projekt**.

4.  Välj **juridisk person** för projektet.

5.  Välj **projektet**.

6.  Klicka på **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Skapa ett nytt projekt från Microsoft Project Client


1.  Öppna Microsoft Project Client.

2.  Skapa schemat i Microsoft Project Client.

3.  På fliken **Microsoft Dynamics 365** klicka på **Spara ändringar** > **Spara till nytt projekt**.

4.  Välj **juridisk person** för projektet.

5.  Ange **Projekt-ID**, om nödvändigt.

6.  Ange **produktnamnet**.

7.  Välj **Projekttyp**, **Projektgruppen** och **Projektkontrakts-ID**. Du kan också skapa ett nytt projektkontrakt genom att klicka på **nytt**.

8.  Välj den **kalender** som ska användas för resurser.

11. Klicka på **OK**.

> [!NOTE]
> Project Client-tillägget stöder inte följande tecken i projekt-ID-formatet:
> 
>   - Understreck
>   - Punkt
>   - Blanksteg
>   - Snedstreck

[!INCLUDE[footer-include](../includes/footer-banner.md)]
