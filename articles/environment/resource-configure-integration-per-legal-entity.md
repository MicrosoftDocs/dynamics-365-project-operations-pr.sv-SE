---
title: Konfigurera Project Operations-integrering efter juridisk person
description: I det här ämnet finns information om hur du konfigurerar integrering efter juridisk person i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5d2bb415362a088e01253fbe54f9f06569b4a921
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122905"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfigurera Project Operations-integrering efter juridisk person 

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

I det här ämnet får du stegvisa anvisningar om hur du konfigurerar Dynamics 365 Project Operations per juridisk person.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Aktivera funktionsnycklar i Dynamics 365 Finance

Följ stegen nedan om du vill aktivera de funktioner som krävs.

1. I Dynamics 365 Finance går du till arbetsytan **Funktionshantering**.
2. I **Funktionslista** letar du upp och aktiverar följande funktioner:
  
    - **Aktivera flera kontraktrader för ett projekt**
    - **Aktivera Project Operations på Dynamics 365 Customer Engagement**

> [!NOTE]
> Om du inte ser **Funktionsnycklar** kontrollerar du att din version av Finance uppfyller minimikraven (programversion 10.0.13 med alla kvalitetsuppdateringar eller senare). Välj **Sök efter uppdateringar** för att uppdatera funktionslistan.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definiera ett scenario för distribution av Project Operations för en juridisk person

Du kan aktivera Project Operations på Dynamics 365 Customer Engagement på en nivå för juridisk person. Du kan ha en juridisk person med Project Operations i Dynamics 365 Customer Engagement för resursbaserade/icke lagerbaserade scenarier. I samma miljö kan du ha en annan juridisk person med Project Operations för lagerbaserade/produktionsorderbaserade scenarier.

1. I Dynamics 365 Finance går du till **Projektledning och redovisning** > **Konfiguration** > **Global projektledning och redovisningsparametrar**.
2. I listan över tillgängliga juridiska personer väljer du entiteter där flera kontraktrader och Project Operations i Dynamics 365 Customer Engagement-funktioner aktiveras. Lämna juridiska personer som ska använda Project Operations för lagerbaserade/produktionsorderbaserade scenarier omarkerade.

> [!NOTE]
> En juridisk person kan endast väljas om den inte har några befintliga projekt.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfigurera parametrar för projektledning och redovisning

Varje juridisk person som använder Project Operations i Dynamics 365 Customer Engagement behöver en uppsättning standardparametrar. Dessa parametrar konfigureras under fliken **Project Operations** på sidan **Projektledning och redovisningsparametrar**. Parametrarna är:

  - **Standard för faktureringstyp**: Project Operations använder en fast uppsättning standardfaktureringstyper som måste mappas till egenskaper i Finance. Skapa en post för varje faktureringstyp: **Inte angiven**, **Debiterbar**, **Inte debiterbar**, **Kostnadsfri** och **Ej tillgänglig**.
  - **Standardprojektkategori**: Välj de projektkategorier som ska användas som standard för varje transaktionstyp. De här standardvärdena används i **Project Operations integreringsjournal** och i uppskattningar där ingen transaktionskategori har angetts för projektets faktiska värden.
  - **Prognoser**: Välj vilken prognosmodell som ska användas för uppskattning av tid och utgifter.