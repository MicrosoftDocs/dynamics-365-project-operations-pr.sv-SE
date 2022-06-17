---
title: Resultat av projektresursschemaläggning
description: Den här artikeln innehåller information om hur du förbättrar prestanda vid resursplanering för ett stort antal projekt.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 072476d43fb3b3d4f96480ec2d3dc5f9db28e501
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921922"
---
# <a name="project-resource-scheduling-performance"></a>Resultat av projektresursschemaläggning

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Prestandaproblem som hänger samman med resursschemaläggning kan inträffa när antalet projekt når tusentals. För att förbättra resursschemaläggningens prestanda finns en funktion som gör att användare kan öppna formulär för resurstillgänglighet snabbare. Detta tar bort synkroniseringsprocessen för sammanslagning av resurskapacitet och använder tabellen **ResProjectResource** för att påskynda resursuppslaget. Observera att tabellen **ResRollup** inte längre används.

> [!IMPORTANT]
> Om det finns ett beroende antingen på den pågående synkroniseringen för sammanslagning av resurskapacitet eller i tabellen **ResProjectResource** ska du inte använda den här funktionen.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Aktivera förbättrad prestanda hos resursschemaläggning
Följ stegen nedan om du vill aktivera prestandaförbättringar för resursschemaläggning.

1. Gå till **Funktionshantering** > **Alla** och i listan med funktioner letar du upp **Aktivera förbättrad prestanda hos schemaläggning av projektresurser**.
2. Välj **Aktivera nu**.

> [!NOTE]
> Om du inte hittar funktionen i listan kan du välja **Sök efter uppdateringar** för att uppdatera listan.

3. Uppdatera webbläsaren och gå sedan till **Projekthantering och redovisning** > **Periodiskt** > **Projektresurser** > **Synkronisera resurskalenderns kapacitet för alla företag**.
4. Ställ in **Ta bort befintliga kapacitetsposter** på **Ja** om du vill ta bort tidigare data. Om du vill generera stegvisa data anger du det till **Nej**.
5. I fältet **Periodkod** väljer du den period då data ska skapas. Om du väljer en periodkod behöver du inte ange start- och slutdatum.
6. Om du lämnar fältet **Periodkod** tomt ska du välja specifika start- och slutdatum för att generera data.
7. Välj **OK**.

 > [!NOTE]
 > Detta innebär att allmänna data distribueras till tabellen **ResCalendarCapacity** i alla företag i din miljö, så att batch-jobbet endast behöver köras i en juridisk person. Data i det här batch-jobbet behövs för att beräkna resurskapacitet via den associerade kalendern.

8. Gå till **Projektledning och redovisning** > **Periodiskt** > **Projektresurser** > **Fylla i projektresurser över alla företag** och välj sedan **OK**. Detta är datauppgraderingsskriptet för allmänna data i tabellerna **ResProjectResource**, **ResCalendarDateTimeRange** och **ResEffectiveDateTimeRange**. Värden för fältet **PSAPRojSchedRole.RootActivity** uppdateras också. Om det inte körs får du en varning när du försöker köra resursplaneringsåtgärder.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Inaktivera förbättrad prestanda hos resursschemaläggning

1. Gå till **Funktionshantering** > **Alla** och sök efter **Aktivera förbättrad prestanda hos schemaläggning av projektresurser**.
2. Markera funktionen och välj sedan knappen **Inaktivera**.
3. Uppdatera webbläsaren.
4. Gå till **Projektledning och redovisning** > **Periodiskt** > **Kapacitetssynkronisering** > **Synkronisera sammanslagning av resurskapacitet**.
5. På sidan **Synkronisering av sammanslagning av kapacitet** ställer du in **Ta bort befintliga kapacitetsposter** på **Ja** för att ta bort tidigare data. Om du vill generera stegvisa data anger du det till **Nej**.
6. I fältet **Periodkod** väljer du den period då data ska skapas. Om du väljer en periodkod behöver du inte ange start- och slutdatum.
7. Om du lämnar fältet **Periodkod** tomt ska du välja specifika start- och slutdatum för att generera data.
8. Välj **OK**.

> [!NOTE]
> Detta innebär att allmänna data distribueras till tabellen **ResRollup** i alla företag i din miljö, så att batch-jobbet endast behöver köras i en juridisk person. Det här batch-jobbet krävs för alla vyer i **Resurstillgänglighet**. Om det här batch-jobbet inte körs kommer **ResRollup**-data att skapas i farten, vilket kan ta tid.


[!INCLUDE[footer-include](../includes/footer-banner.md)]