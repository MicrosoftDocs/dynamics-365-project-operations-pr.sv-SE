---
title: Konfigurera Project Operations-integrering efter juridisk person
description: I det här ämnet finns information om hur du konfigurerar integrering efter juridisk person i Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64606a20a49fd8e9602b6ac3c1ab1880796eb128
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585860"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Konfigurera Project Operations-integrering efter juridisk person 

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Det ämne genom stegen som krävs för att konfigurera Dynamics 365 Project Operations per juridisk entitet.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Aktivera funktionsnycklar i Dynamics 365 Finance

Följ stegen nedan om du vill aktivera de funktioner som krävs.

1. Gå till arbetsytan **Funktionshantering** i Dynamics 365 Finance.
2. I **Funktionslista** letar du upp och aktiverar följande funktioner:
  
    - **Aktivera flera kontraktrader för ett projekt**
    - **Aktivera Project Operations på Dynamics 365 Customer Engagement**

> [!NOTE]
> Om du inte ser **Funktionsnycklar** kontrollerar du att din version av Finance uppfyller minimikraven (programversion 10.0.13 med alla kvalitetsuppdateringar eller senare). Välj **Sök efter uppdateringar** för att uppdatera funktionslistan.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definiera ett scenario för distribution av Project Operations för en juridisk person

Du kan aktivera Project Operations på Dynamics 365 Customer Engagement på en juridisk entitetsnivå. Du kan ha en juridisk entitet med Project Operations i Dynamics 365 Customer Engagement för resurs-/icke-lagerbaserade scenarier. I samma miljö kan du ha en annan juridisk person med Project Operations för lagerbaserade/produktionsorderbaserade scenarier.

1. I Dynamics 365 Finance går du till **Projekthantering och redovisning** > **Inställningar** > **Globala Projekthanterings- och redovisningsparametrar**.
2. I listan över tillgängliga juridiska entiteter väljer du entiteter där flera kontraktrader och Project Operations-funktioner för Dynamics 365 Customer Engagement aktiveras. Lämna juridiska personer som ska använda Project Operations för lagerbaserade/produktionsorderbaserade scenarier omarkerade.

> [!NOTE]
> En juridisk person kan endast väljas om den inte har några befintliga projekt.

## <a name="configure-project-management-and-accounting-parameters"></a>Konfigurera parametrar för projektledning och redovisning

Varje juridisk entitet som använder Project Operations på Dynamics 365 Customer Engagement måste ha en uppsättning standardparametrar. Dessa parametrar konfigureras under fliken **Project Operations** på sidan **Projektledning och redovisningsparametrar**. Parametrarna är:

  - **Standard för faktureringstyp**: Project Operations använder en fast uppsättning standardfaktureringstyper som måste mappas till egenskaper i Finance. Skapa en post för varje faktureringstyp: **Inte angiven**, **Debiterbar**, **Inte debiterbar**, **Kostnadsfri** och **Ej tillgänglig**.
  - **Standardprojektkategori**: Välj de projektkategorier som ska användas som standard för varje transaktionstyp. De här standardvärdena används i **Project Operations integreringsjournal** och i uppskattningar där ingen transaktionskategori har angetts för projektets faktiska värden.
  - **Prognoser**: Välj vilken prognosmodell som ska användas för uppskattning av tid och utgifter.


[!INCLUDE[footer-include](../includes/footer-banner.md)]