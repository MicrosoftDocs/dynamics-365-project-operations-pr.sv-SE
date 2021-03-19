---
title: Intäktsredovisning – Översikt
description: I det här ämnet finns information om vyn intäktsredovisning i Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278890"
---
# <a name="revenue-recognition-overview"></a>Intäktsredovisning – Översikt

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

I Dynamics 365 Project Operations varierar principerna för intäktsredovisning baserat på den valda faktureringsmetoden för ett projekt eller en del av projektet. I det här ämnet finns information om vyn intäktsredovisning i Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Transaktionerna redovisas med hjälp av metoden för fakturering av tid och material

- Kostnads- och intäktsredovisning är anslutna. Transaktionskostnad och ej fakturerad försäljning bokförs med hjälp av [integrationsjournal för Project Operations](../project-accounting/project-operations-integration-journal.md).
- Projektkostnads- och intäktsprofil avgör om ej fakturerade försäljningstransaktioner bokförs i redovisningen. Om **Periodisera intäkter** väljs kommer systemet att använda kontona **Försäljningsvärde för PIA** och **Försäljningsvärde för periodiserade intäkter**. Följande är ett exempel på denna metod.  

  | Transaktionstyp | Debet/kredit | Belopp |
  | --- | --- | --- |
  | Försäljningsvärde för PIA | Debet | 100 |
  | Försäljningsvärde för periodiserade intäkter | Kredit | 100 |

- Intäkter redovisas i samband med fakturering. Systemet använder kontot **Fakturerad intäkt** i samband med bokföring. Följande är ett exempel på denna metod.  

  | Transaktionstyp | Debet/kredit | Belopp |
  | --- | --- | --- |
  | Kundsaldo | Debet | 120 |
  | Omsättningsskatt | Kredit | 20 |
  | Fakturerad intäkt | Kredit | 100 |

- Om intäkter periodiseras när den ej fakturerade försäljningen bokförs kommer systemet att återföra den periodiserade intäkten vid fakturering.

  | Transaktionstyp | Debet/kredit | Belopp |
  | --- | --- | --- |
  | Försäljningsvärde för PIA | Kredit | 100 |
  | Försäljningsvärde för periodiserade intäkter | Debet | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Transaktionerna redovisas med hjälp av faktureringsmetoden för fast pris

- Kostnads- och intäktsredovisning är separata. Transaktionskostnaden bokförs med hjälp av [integrationsjournalen för Project Operations](../project-accounting/project-operations-integration-journal.md). Ej fakturerade försäljningstransaktioner skapas inte.
- Intäkter kan redovisas under faktureringen om projektets kostnad och intäktsprofil har **Princip som används för beräkningar av projektslutförande** anges som **Ingen PIA**. Använd bara denna metod för enklare, mer kortsiktiga projekt.
- Intäkter kan redovisasmed hjälp av uppskattningar av fastprisintäkter, med antingen metoden **Slutfört kontrakt** eller **Slutförd intäktsredovisning i procent**.

## <a name="additional-resources"></a>Ytterligare resurser
[Konfigurera redovisning för fakturerbar projektartikel](../project-accounting/configure-accounting-billable-projects.md)

[Intäktsberäkningar för fastprisprojekt](rev-rec-percentage-completion-method.md)

[Hantera intäktsberäkningar](rev-rec-completed-contract-method.md)

[Kostnad för slutförandemetoder](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]