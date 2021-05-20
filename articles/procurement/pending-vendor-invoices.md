---
title: Inköp av icke-lagerbaserade material med väntande leverantörsfaktura
description: I ämnet beskrivs hur du registrerar väntande leverantörsfakturor.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880690"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Inköp av icke-lagerbaserade material med väntande leverantörsfaktura

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

När ett företag köper in icke-lagerbaserade material till ett projekt, kan kostnaderna registreras direkt på projektet. 

Exempelvis utför Contoso Robotics US ett projekt för utrustningsförnyelse och behöver programvarulicenser. Licenserna köps in från en tredjepartsleverantör.  Med Dynamics 365 Finance registrerar den ansvariga för leverantörsreskontra ett väntande leverantörsfakturadokument och registrerar licenskostnaderna direkt på utrustningsförnyelseprojektet. 

> [!IMPORTANT]
> Innan du använder funktionerna som beskrivs i ämnet måste du granska och tillämpa de konfigurationer som krävs. Mer information finns i [Aktivera icke-lagerbaserade material och väntande leverantörsfakturor](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Registrera en projektrelaterad väntande leverantörsfaktura 

Väntande leverantörsfakturor kan registreras på sidan **Väntande leverantörsfakturor** (**Leverantörsreskontra** > **Fakturor** > **Väntande leverantörsfakturor**). Slutför följande steg för att registrera en projektrelaterad väntande leverantörsfaktura:

1. Gå till **Leverantörsreskontra** > **Fakturor** och välj **Ny**. 
2. I fältet **Fakturakonto** väljer du leverantör och i fältet **Nummer** fyller du i identifiering för leverantörsfakturan.
3. Lägg till en rad i leverantörsfakturan och i fältet **Artikelnummer** väljer du den icke-lagerbaserade artikeln som köpts in från leverantören. 

    > [!NOTE]
    > Det går inte att registrera leverantörsfakturarader som är baserade på en inköpskategori på projektet. 
    
5. Lägg till kvantiteten som köpts in. Systemet fyller i enhetspriset baserat på priskonfiguration för den icke-lagerbaserade artikeln. 
6. Kontrollera totalbeloppet och annan obligatorisk information på raden.
7. På fliken **Projekt**, i radinformationen, väljer du projekt-ID som denna artikel ska registreras på.
8. Alternativt kan du välja aktivitetsnumret och uppdatera projektkategorin och radegenskapen.
9. Efter väntande leverantörsfaktura. När fakturan har registrerats bokför systemet:
    
    - Leverantörens saldobelopp.
    - Momsbeloppet.
    - Kostnaden på projektet registreras på inköpsintegrationskontot.
    - Den faktiska projekttransaktionen i Dataverse. Transaktionen bearbetas vidare med [Project Operations-integrationsjournal](../project-accounting/project-operations-integration-journal.md). Om du registrerar journalen flyttas beloppet från inköpsintegrationskontot till projektkostnadskontot.
