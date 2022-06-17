---
title: Sidhuvudinformation för leverantörsfakturor
description: I denna artikel beskrivs funktionerna i leverantörsfakturahuvudet i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929880"
---
# <a name="header-details-for-vendor-invoices"></a>Sidhuvudinformation för leverantörsfakturor

[!include [banner](../../includes/dataverse-preview.md)]

_**Gäller:** Enkel distribution – avtal till proforma-fakturering_

I denna artikel beskrivs funktionerna i leverantörsfakturahuvudet i Microsoft Dynamics 365 Project Operations.

När projektansvariga planerar och genomför projekt kan de komma att använda underleverantörer och köpa produkter och tjänster från leverantörer. Under ett projekts genomförande uppstår kostnader för tjänster, material och utgiftskategorier genom avtal med underleverantörer. Leverantörer fakturerar dessa kostnader till projekt genom att skapa leverantörsfakturor.

Följande tabell innehåller information om sidhuvudfälten i leverantörsfakturor i Project Operations.

| Fält | Description | Funktionellt påverkan |
| --- | --- | --- |
| Name | Namn på leverantörsfakturan. | I alla listrutor för leverantörsfaktura visas namnet på leverantörsfakturan i den första kolumnen så att du kan identifiera leverantörsfakturan. När en leverantörsfaktura skapas från en underleverantör anges värdet för fältet **Namn** på leverantörsfakturan som ett värde som består av namnet på underleverantören plus det aktuella datumet. |
| Description | En kort beskrivning av de tjänster och produkter som faktureras på leverantörsfakturan. | None |
| Leverantör | Namnet på det företag som fakturerar produkterna och tjänsterna. Det här företaget ska vara en kontopost med relationstypen **Leverantör** eller **Källa**. | <p>Standardvärden anges automatiskt i följande fält baserat på den leverantör som valts:</p><ul><li>Valuta</li><li>Prislistor</li><li>Betalningsvillkor</li><li>Betalningsadress</li></ul> |
| Underleverantörskontrakt | En referens till leveranstörsfakturans underleverantör. | <p>Standardvärden anges automatiskt i följande fält baserat på den underleverantör som valts:</p><ul><li>Valuta</li><li>Prislistor</li><li>Betalningsvillkor</li><li>Betalningsadress</li></ul><p>Den underleverantör som väljs i leverantörsfakturahuvudet anges som standard på leverantörsfakturaraderna och kan inte ändras där.</p> |
| Fakturadatum | Datumet för de faktiska kostnaderna som skapas när leverantörsfakturan bekräftas. | Fakturadatum används också för att välja rätt inköpsprislista antingen från de prislistor som är kopplade till den relaterade leverantören eller från projektparametrarna. |
| Statusorsak | Status för leverantörsfaktura. | <p>Statusen avgör var leverantörsfakturan befinner sig i affärsprocessen, samt huruvida den kan redigeras. Här är några av de tillgängliga värdena:</p><ul><li>**Utkast** – Leverantörsfakturan kan redigeras.</li><li>**Bekräftad** – Leverantörsfakturan har verifierats och bekräftats. Det går inte att redigera eller radera leverantörsfakturor med denna status.</li><li>**Pågår –** Leverantörsfakturan granskas. Det går att redigera leverantörsfakturor med denna status, men däremot inte att radera dem.</li><li>**Annullerad** – Leverantörsfakturan annullerades. Det går inte att redigera eller radera leverantörsfakturor med denna status.</li></ul> |
| Valuta | Den valuta som leverantören faktureras i för produkterna och tjänsterna på leverantörsfakturan. | På en leverantörsfaktura som refererar till en underleverantör anges valutan för underleverantören som standard som valutan i leverantörsfakturan. På en leverantörsfaktura som inte refererar till en underleverantör anges standardvärdet från leverantörens kontopost och kan ändras. När en leverantörsfaktura har sparats går det inte längre att redigera valutan. |
| Kontrakteringsenhet | Den avdelning i företaget som ansvarar för att ta emot tjänsterna och/eller produkterna från leverantören. | None |
| Betalningsvillkor | Betalningsvillkor för leverantörsfakturor som utfärdas. Standardvärdet anges automatiskt från leverantörskontot. | Betalningsvillkor från en underleverantör kopieras till alla leverantörsfakturor som är relaterade till underleverantören. Betalningsvillkor kan uppdateras om leverantörsfakturan har statusen **Utkast**. |
| Betalningsadress | Adressen till den leverantör som betalningar måste skickas till. Standardvärdet anges automatiskt från leverantörskontot. | Betalningsadressen från ett underleverantörskontrakt kopieras som betalningsadress till alla leverantörsfakturor som skapas för den underleverantören. Betalningsadressen kan uppdateras om leverantörsfakturan har statusen **Utkast**. |
| Delsumma | Om leverantörsfakturan inte har några rader anger du fakturans delsumma före moms. Om leverantörsfakturan innehåller rader är det här fältet skrivskyddat. I detta fall utgör det belopp som visas delsumman för alla rader i leverantörsfakturan. | None |
| Moms totalt | Om leverantörsfakturan inte har några rader anger du total moms i underkontraktet. Om leverantörsfakturan innehåller rader är det här fältet skrivskyddat. I detta fall utgör det belopp som visas summan av alla momsbelopp från alla rader i leverantörsfakturan. | None |
| Totalbelopp | Det beräknade fältet visar totalbeloppet för leverantörsfakturan efter att moms inkluderats. | None |

> [!NOTE]
> Följande fält i en leverantörsfaktura kan inte ändras när leverantörsfakturan har sparats: **Leverantör**, **Underleverantör**, **Valuta**, **Kontraktenhet** och **Betalningsvillkor**. Om det krävs några ändringar i dessa fält i en leverantörsfaktura måste du ta bort leverantörsfakturan och skapa en ny leverantörsfaktura.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
