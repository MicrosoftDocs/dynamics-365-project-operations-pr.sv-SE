---
title: Köpa icke-lagerförda material eller inköpskategorier med hjälp av väntande leverantörsfaktura
description: Den här artikeln innehåller information om hur du registrerar väntande leverantörsfakturor.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922014"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Köpa icke-lagerförda material eller inköpskategorier med hjälp av väntande leverantörsfaktura

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

När ett företag köper in icke-lagerfört material eller inköpskategorier för ett projekt, kan kostnaderna för projektet registreras direkt. 

Contoso Robotics US utför till exempel ett projekt för utrustningsförnyelse och behöver programvarulicenser. Licenserna köps in från en tredjepartsleverantör.  Den aom administrerar leverantörsreskontra använder Dynamics 365 Finance för att registrera ett väntande leverantörsfakturadokument och tillskriver licenskostnaderna direkt till utrustningsförnyelseprojektet. 

> [!IMPORTANT]
> Innan du använder funktionerna som beskrivs i den här artikeln bör du granska och tillämpa de konfigurationer som krävs. Mer information finns i [Aktivera icke-lagermaterial och väntande leverantörsfakturor](configure-materials-nonstocked.md) och [Använd inköpskategorier med projektinköpsorder och väntande leverantörsfakturor](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Registrera en projektrelaterad väntande leverantörsfaktura 

Väntande leverantörsfakturor kan registreras på sidan **Väntande leverantörsfakturor** (**Leverantörsreskontra** > **Fakturor** > **Väntande leverantörsfakturor**). Slutför följande steg för att registrera en projektrelaterad väntande leverantörsfaktura:

1. Gå till **Leverantörsreskontra** > **Fakturor** och välj **Ny**. 
1. Välj en leverantör i fältet **Fakturabelopp** innan du i fältet **Nummer** anger ID för leverantörsfakturan.
1. Lägg till en rad i leverantörsfakturan innan du i fältet **Artikelnummer** väljer det icke-lagerbaserade objekt som köpts från leverantören. I fältet **Inköpskategori** kan du även välja den inköpskategori som köpts från leverantören.   
1. Lägg till den inköpta kvantiteten. I systemet fylls enhetspriset i utifrån priskonfigurationen för artiklar som inte finns i lager. 
1. Kontrollera totalbeloppet och annan obligatorisk information på raden.
1. I radinformationen på fliken **Projekt** väljer du ID för det projekt som denna artikel ska registreras på.
1. Valfritt: Välj aktivitetsnummer och uppdatera projektkategorin och radegenskapen.
1. Bokför väntande leverantörsfaktura. När fakturan har lagts upp registrerar systemet följande information:
    
    - Leverantörens saldobelopp.
    - Momsbeloppet.
    - Kostnaden på projektet registreras på inköpsintegrationskontot.
    - Den faktiska projektkostnadstransaktionen i Dataverse.  Transaktionen bearbetas vidare med [Project Operations-integrationsjournal](../project-accounting/project-operations-integration-journal.md). Om du registrerar journalen flyttas beloppet från inköpsintegrationskontot till projektkostnadskontot. 
    - Inköp som faktureras till projektkunden med hjälp av faktureringsmetoden för tid och material. Dessutom skapas ofakturerade försäljningstransaktioner för inköpen i Dataverse. Produktprislistan i används Dataverse för försäljningspriser och belopp för icke-fakturerad försäljningstransaktion.
