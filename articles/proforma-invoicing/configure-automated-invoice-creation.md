---
title: Konfigurera automatiskt fakturaskapande
description: I det här ämnet finns information om hur du konfigurerar systemet för att automatiskt skapa fakturor.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dffa95c163f7f8d5074e02cd56d6f1ed429a7c72
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005363"
---
# <a name="configure-automatic-invoice-creation"></a>Konfigurera automatiskt fakturaskapande

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_


Följ stegen nedan om du vill konfigurera automatisk fakturering i Dynamics 365 Project Operations.

1. Gå till **Inställningar** > **Batchjobb**.
2. Skapa ett batch-jobb och ge det namnet **Project Operations skapa fakturor**. Namnet på batch-jobbet måste innehålla orden "skapa fakturor".
3. I fältet **Jobbtyp**, välj **Ingen**. Som standard är alternativen **Frekvens dagligen** och **Är aktiv** angivna som **Ja**.
4. Välj **Kör arbetsflöde**. I dialogrutan **Sök efter post** visas tre arbetsflöden:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Välj **ProcessRunCaller** och välj **Lägg till**.
6. Klicka på **OK** i nästa dialogrutan. Arbetsflödet **Vila** följs av **Process**.

  > [!NOTE]
  > Du kan också välja **ProcessRunner** i steg 5. När du sedan väljer **OK**, följs arbetsflödet **Process** av arbetsflödet **Vila**.

Arbetsflödena **ProcessRunCaller** och **ProcessRunner** skapar fakturor. **ProcessRunCaller** anropar **ProcessRunner**. **ProcessRunner** är det arbetsflöde som verkligen skapade fakturorna. Det går igenom alla kontraktrader som fakturorna måste skapas för och fakturor för dessa rader skapas. För att fastställa vilka kontraktrader som fakturor ska skapas tittar jobbet på körningsdatum för faktura för kontraktraderna. Om kontraktrader som tillhör ett kontrakt har samma datum för fakturakörning kombineras transaktionerna till en faktura med två fakturarader. Om det inte finns några transaktioner för att skapa fakturor hoppar jobbet över skapandet av fakturan.

När **ProcessRunner** har körts klart anropas **ProcessRunCaller**, anger sluttiden och är stängd. **ProcessRunCaller** startar sedan en timer som körs i 24 timmar från den angivna sluttiden. **ProcessRunCaller** stängs i slutet av timern.

Batchprocessjobbet för att skapa fakturor är ett återkommande jobb. Om batchprocessen körs flera gånger skapas flera instanser av jobbet och det uppstår fel. Därför bör du endast starta batchprocessen en gång och du bör starta om den endast om den slutar att fungera.

> [!NOTE]
> Batchfakturering körs endast för projektkontraktrader som konfigurerats av fakturascheman. En kontraktrad med en fast pris faktureringsmetod måste ha milstolpar konfigurerad. En projekts kontraktrad med en tids- och material faktureringsmetod måste ha en datumbaserad fakturauppställning. Detsamma gäller för en projektrelaterad kontraktrad.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]