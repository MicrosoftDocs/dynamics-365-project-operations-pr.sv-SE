---
title: Beställa ej lagerfört material för projekt som använder projektinköpsorder
description: Denna artikel förklarar hur du kan beställa ej lagerfört material för projekt som använder projektinköpsorder.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929834"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Inköpskategorier för beställning eller ej lagerfört material för ett projekt som använder projektinköpsorder

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Anskaffningsavdelningen i organisationen kan använda [inköporder](/dynamics365/supply-chain/procurement/purchase-order-overview) för att spåra varor och tjänsteorder. Inköpsorder för inköpskategorier eller ej lagerfört material kan tillskrivas ett projekt. När dessa köporder faktureras posters kostnaden för projektet.

## <a name="prerequisites"></a>Förutsättningar
Aktivera projektorderfunktionen genom att följa stegen nedan.

1. Gå till arbetsytan **Funktionshantering** i Dynamics 365 Finance.
2. Leta upp och markera funktionen i funktionslistan, **Aktivera projektinköpsorder för Project Operations för resursbaserade/icke-lagerbaserade scenarier**.
3. Välj **Aktivera**.
4. Konfigurera icke-lagermaterial och väntande leverantörsfakturor enligt beskrivningen i [Konfigurera icke-lagermaterial och väntande leverantörsfakturor](configure-materials-nonstocked.md).
5. Konfigurera inköpskategorier enligt [Använd inköpskategorier med projektinköpsorder och väntande leverantörsfakturor](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Skapa en projektorder från projektorderlistan

1. I Finance, gå till **Projekthantering och redovisning** > **Projekt** > **Alla projekt** och välj ett projekt.
2. I åtgärdsfönstret, på **Hantera** i grupp **Ny**, välj **Artikeluppgift** > **Inköpsorder**.
3. På sidan **Skapa köporder** markerar du den leverantör som du vill placera ordern med, anger annan information efter behov och väljer sedan **OK**.
4. På sida **Inköpsorder** i rutnätet **Inköpsorderrader**, välj **Lägg till**.
5. Ange ett artikelnummer eller en inköpskategori, kvantitet, enhet, enhetspris och annan information.

    > [!NOTE]
    > Endast inköpskategorier - inte artiklar som inte är i lager - och tjänster kan användas för projektinköpsorder. Lagerartiklar stöds inte.

6. Fortsätt för att lägga till artiklar eller inköpskategorier efter behov, och bekräfta sedan inköpsordern.

    Varor och tjänster kvitton kan registreras genom att skapa och bokföra ett produktkvitto.

    > [!NOTE]
    > Produktinslag registreras inte i projektets faktiska värden och påverkar Microsoft Dataverse inte projektundersänkaren.

    När en leverantör skickar fakturan för varor och tjänster på inköpsordern kan upphandlingsavdelningen generera en faktura för inköpsordern genom att gå till **Faktura** > **Generera** > **Faktura** i åtgärdsfönstret Mer information om väntande leverantörsfakturor finns i [Köp olagrat material med en väntande leverantörsfaktura](pending-vendor-invoices.md).
