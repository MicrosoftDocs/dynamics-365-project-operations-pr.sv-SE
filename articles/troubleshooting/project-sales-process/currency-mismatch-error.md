---
title: Valutamatchningsfel
description: Det här ämnet innehåller felsökningsinformation om ett valutamatchningsfel som uppstår när du sparar vissa posttyper.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903547"
---
# <a name="currency-mismatch-error"></a>Valutamatchningsfel 

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

När du sparar ett projekt, ett kontrakt, en offert eller en bokningsbar resurs kan det hända att du får felmeddelandet **Det ägande företagets valuta motsvarar inte den upphandlande enhetens valuta. Välj ett annat ägande företag eller en annan upphandlande enhet för att fortsätta**. Det beror på att det finns ett valutamatchningsfel mellan den upphandlande enhetens valutan för posten och det ägande företagets valuta.


## <a name="resolution"></a>Upplösning

Kringgå problemet genom att göra följande:
- Kontrollera valutan för den här postens upphandlande enhet. Du kan visa valutan genom att öppna organisationsenhetsposten och kontrollera värdet under fliken **Allmänt** i fältet **Valuta**.
- Kontrollera valutan för det ägande företaget. Du kan visa valutan genom att gå till **Relaterat** > **Redovisningar** i företagsposten. Dubbelklicka på den redovisningspost som är associerad med företaget och kontrollera värdet under fliken **Allmänt** i fältet **Redovisningsvaluta**.

Om valutan i den upphandlande enheten och redovisningsposten inte stämmer överens, ändrar du konfigurationen eller väljer andra värden när du sparar posten. Systemet kräver att dessa poster stämmer överens för att säkerställa rätt faktureringsflöden inom koncernen. Mer information om de koncerninterna konfigurationerna finns i [Skapa koncerninterna transaktioner](../../project-accounting/create-intercompany-transactions.md).

Om företagsposten inte har någon associerad redovisningspost tyder detta på att det saknas en konfiguration när du ställer in miljön. Konfigurationen måste åtgärdas av systemadministratören. Systemadministratören måste gå till **Konfigurationer för dubbelriktad skrivning** och stoppa och starta om **Redovisningsmappning för dubbelriktad skrivning** med den första synkroniseringen av mappningen och dess förutsättningar. Mer information finns i [Project Operations-versioner med dubbelriktad skrivning](../../environment/resource-dual-write-maps.md).
