---
title: Beställa ej lagerfört material för projekt som använder projektinköpsorder
description: Detta ämne förklarar hur du kan beställa ej lagerfört material för projekt som använder projektinköpsorder.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563044"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Beställa ej lagerfört material för projekt som använder projektinköpsorder

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Anskaffningsavdelningen i organisationen kan använda [inköporder](/dynamics365/supply-chain/procurement/purchase-order-overview) för att spåra varor och tjänsteorder. Inköpsorder för icke-lagermaterial kan hänföras till ett projekt. När dessa köporder faktureras posters kostnaden för projektet.

## <a name="prerequisites"></a>Förutsättningar
Aktivera projektorderfunktionen genom att följa stegen nedan.

1. I Dynamics 365 Finance går du till arbetsytan **Funktionshantering**.
2. Leta upp och markera funktionen i funktionslistan, **Aktivera projektinköpsorder för Project Operations för resursbaserade/icke-lagerbaserade scenarier**.
3. Välj **Aktivera**.
4. Konfigurera icke-lagermaterial och väntande leverantörsfakturor enligt beskrivningen i [Konfigurera icke-lagermaterial och väntande leverantörsfakturor](configure-materials-nonstocked.md). 

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Skapa en projektorder från projektorderlistan

1. I Finance, gå till **Projekthantering och redovisning** > **Projekt** > **Alla projekt** och välj ett projekt.
2. I åtgärdsfönstret, på **Hantera** i grupp **Ny**, välj **Artikeluppgift** > **Inköpsorder**.
3. På sidan **Skapa köporder** markerar du den leverantör som du vill placera ordern med, anger annan information efter behov och väljer sedan **OK**.
4. På sida **Inköpsorder** i rutnätet **Inköpsorderrader**, välj **Lägg till**.
5. Ange ett artikelnummer, en kvantitet, en enhet, ett enhetspris och annan information.

    > [!NOTE]
    > Endast objekt och tjänster som inte är i lager kan användas vid projektinköpsorder. Lagerföremål och upphandlingskategorier stöds inte.

6. Fortsätt att lägga till objekt efter behov och bekräfta inköpordern.

    Varor och tjänster kvitton kan registreras genom att skapa och bokföra ett produktkvitto.

    > [!NOTE]
    > Produktinslag registreras inte i projektets faktiska värden och påverkar Microsoft Dataverse inte projektundersänkaren.

    När en leverantör skickar fakturan för varor och tjänster på inköpsordern kan upphandlingsavdelningen generera en faktura för inköpsordern genom att gå till **Faktura** > **Generera** > **Faktura** i åtgärdsfönstret Mer information om väntande leverantörsfakturor finns i [Köp olagrat material med en väntande leverantörsfaktura](pending-vendor-invoices.md).
