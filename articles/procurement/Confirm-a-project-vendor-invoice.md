---
title: Bekräfta projektleverantörsfakturor
description: I denna artikel beskrivs hur du bekräftar en projektleverantörsfaktura i Microsoft Dynamics 365 Project Operations och den ekonomiska påverkan av att bekräfta en projektleverantörsfaktura.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475445"
---
# <a name="confirm-project-vendor-invoices"></a>Bekräfta projektleverantörsfakturor

**Gäller:** Project Operations för resursbaserade/icke-lagerbaserade scenarier

När parametern **Manuell bekräftelse av PM krävs** är aktiverad får leverantörsfakturor som skapats i Microsoft Dataverse statusen **Utkast**. Leverantörsfakturor som skapas på det här sättet måste granskas och bekräftas manuellt. När parametern **Manuell bekräftelse av PM krävs** är inaktiverad bekräftas leverantörsfakturor som skapats i Dataverse automatiskt. Inga ytterligare åtgärder krävs. 

När du har kontrollerat alla rader på en leverantörsfaktura i Dynamics 365 Project Operations väljer du **Bekräfta** för att bekräfta leverantörsfakturan.

När du väljer **Bekräfta** på en leverantörsfaktura sker följande:

1. Leverantörsfakturans status uppdateras till **Bekräftad**.
1. Den bekräftade leverantörsfakturan och dess relaterade poster blir skrivskyddade och kan inte redigeras eller tas bort.
1. Om några faktiska kostnader refererar till leverantörens fakturarad som en del av matchningsprocessen kommer alla faktiska kostnader som är kopplade till den refererade leverantörens fakturarad att återställas.
1. Nya faktiska kostnader skapas med hjälp av informationen på leverantörens fakturarad.
1. Du kan inte längre skapa korrigeringsjournaler, behandla återkallning av tidsposter eller avbryta godkännande av den ursprungliga tiden, utgiften eller faktiska material som har återförts.
1. I Dynamics 365 Finance uppdateras värdet **Projektkostnad** med hjälp av integrationskontot Projekt, och integrationskontot Inköp *återförs* efter att projektintegrationsjournalen har publicerats.

> [!NOTE]
> Om någon rad i en leverantörsfaktura har en annan verifikationsstatus än **Slutförd** kan leverantörsfakturan inte bekräftas.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
