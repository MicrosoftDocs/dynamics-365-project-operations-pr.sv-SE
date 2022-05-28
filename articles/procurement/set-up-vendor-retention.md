---
title: Ställa kvarhållning av leverantörer
description: Det här avsnittet innehåller information om hur du ställer in kvarhållning av leverantörer.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e0cd7669c7d6b916261e2c85cce0f24ff241a075
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583726"
---
# <a name="set-up-vendor-retention"></a>Ställa kvarhållning av leverantörer

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Detta ämne ger information om hur du ställer in kvarhållning av leverantörer.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Konfigurera ett leverantörslagringskonto i huvudboken

1. I Dynamics 365 Finance går du till **Redovisning** > **Inställningar för bokföring** > **Konton för automatiska överföringar**.
2. Lägg till ny rad.
3. I fältet **Bokföringstyp** väljer du **Kvarhållning av leverantörer**.
4. Välj huvudkontot för bokföring av leverantörslagring.

## <a name="create-vendor-retention-terms"></a>Skapa kvarhållandevillkor för leverantör

Använd sidan **Kvarhållandevillkor för leverantör** att ställa in och behålla lagringsvillkor för leverantörsbetalningar. Du kan ange procentandelen av en leverantörsbetalning för kvarhållande som du vill hålla inne och procentandelen av tidigare innehållna belopp som ska frisläppas. Belopp hålls automatiskt inne på leverantörsfakturor tills kontraktet når det angivna slutsteget. När du har angett lagringsvillkor för en leverantör kan du tillämpa dem på alla projekt som leverantören arbetar i.

1. I Finance, gå till **Projekthantering och redovisning** > **Inställningar** > **Kvarhållande** > **Villkor för innehållen leverantörsbetalning**.
2. Välj **Ny** om du vill lägga till ett nytt villkor för kvarhållande för leverantören. Värdet i fältet **Regel-ID** för det nya villkoret anges i automatiskt. 
3. I fältet **Beskrivning** anger du en beskrivning för det nya villkor.
4. På fliken **Villkor**, välj **Lägg till rad** för att ange ett kvarhållandevillkor för leverantör.
5. I fältet **Levererade enheter i procent** ange en slutförandeprocent för regeln. Belopp hålls inne automatiskt på leverantörsfakturor tills projektslutförandefasen är lika med procentsatsen som du anger. Om du till exempel anger 50,00 kvarhålls beloppen tills projektet har slutförts till 50 procent.
6. Fältet **Procent att hålla inne**, ange en procentandel av leverantörsfakturor som ska hållas inne. Om du till exempel anger 10,00 i det här fältet hålls 10 procent av beloppet på leverantörsfakturorna inne tills projektet når slutförandeprocenten som du väljer i formuläret **Levererade enheter i procent**.
7. I fältet **Procent att frisläppa** för att ange en procentandel av tidigare behållna belopp som ska frisläppas för den valda nivån för projektets slutförande.

> [!NOTE]
> Om du har mer än en milstolpe för olika nivåer för projektslutförande anger du en separat rad för villkor för innehållet belopp för varje regel. Varje rad kan ange en annan kvarhållandeprocentsats och en annan procentsats för frisläppning på varje nivå av projektslutförande.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Skapa ett leverantörsavtal för projektet

Ange de villkor för leverantörslagring som gäller för projektet. Villkoren för leverantörskvarhållande visas även på inköpsorder som du skapar för leverantören.

1. I Finance, gå till **Projekthantering och redovisning** > **Projekt** > **Alla projekt**. 
2. Välj ett projekt och välj i åtgärdsfönstret **Projektgrupp** > **Leverantörsavtal**.
3. Lägg till en ny rad på sidan **Leverantöravtal**.
4. I fältet **Kontokod** väljer du något av följande alternativ:
   - **Tabell**: Villkoren för leverantörskvarhållande gäller för en enskild leverantör.
   - **Grupp**: Villkoren för leverantörskvarhållande gäller för alla leverantörer i en leverantörsgrupp.
   - **Alla**: Villkoren för leverantörskvarhållande gäller för alla leverantörer.
5. I fältet **Leverantör/leverantörsgrupp** väljer du den leverantör eller leverantörsgrupp som villkoren för leverantörskvarhållande gäller för. Om du valde **Alla** i föregående steg är detta fält inte tillgängligt.
6. I fältet **Villkor för leverantörslagring** väljer du regel-ID för de lagringsvillkor som ska gälla för den här leverantören.

