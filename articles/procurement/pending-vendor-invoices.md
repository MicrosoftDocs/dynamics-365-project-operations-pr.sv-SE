---
title: Inköp av icke-lagerbaserade material med väntande leverantörsfaktura
description: I ämnet beskrivs hur du registrerar väntande leverantörsfakturor.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e95f7dabe597968707fdd2dead40bfb93d7f1f95
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547311"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Inköp av icke-lagerbaserade material med väntande leverantörsfaktura

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

När ett företag köper in icke-lagerbaserade material till ett projekt, kan kostnaderna registreras direkt på projektet. 

Contoso Robotics US utför till exempel ett projekt för utrustningsförnyelse och behöver programvarulicenser. Licenserna köps in från en tredjepartsleverantör.  Med Dynamics 365 Finance registrerar den ansvariga för leverantörsreskontra ett väntande leverantörsfakturadokument och registrerar licenskostnaderna direkt på utrustningsförnyelseprojektet. 

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
    - Den faktiska projektkostnadstransaktionen i Dataverse.  Transaktionen bearbetas vidare med [Project Operations-integrationsjournal](../project-accounting/project-operations-integration-journal.md). Om du registrerar journalen flyttas beloppet från inköpsintegrationskontot till projektkostnadskontot. 
    - Inköp som faktureras till projektkunden med hjälp av faktureringsmetoden för tid och material. Dessutom skapas ofakturerade försäljningstransaktioner för inköpen i Dataverse. Produktprislistan i används Dataverse för försäljningspriser och belopp för icke-fakturerad försäljningstransaktion.
