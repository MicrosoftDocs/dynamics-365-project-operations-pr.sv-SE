---
title: Översikt över faktureringsprocessen
description: Detta ämne innehåller en processöversikt över faktureringen i Project Operations för resurs- eller icke-lagerbaserade scenarier.
author: sigitac
ms.date: 01/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 804d42f7e8bfd103b9143dc0f5c7ddecdee9e66e6072c3e7bf76b2a8c549cf55
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003793"
---
# <a name="invoicing-process-overview"></a>Översikt över faktureringsprocessen

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Project Operations för resurs-/icke-lagerbaserade scenarier erbjuder omfattande funktioner som är skräddarsydda för både projektansvarig och kundreskontra-/projektrevisor. För faktureringsprocessen hanterar projektledaren eftersläpningen (backlogg) för projektfakturering och kundreskontra-/projektrevisorn skapar ett kompatibelt och korrekt kundriktat fakturadokument.

![Diagram över faktureringsflöde.](./media/invoicing-flow.png)

På projektkontraktraden definieras faktureringsmetoden för associerade projekttransaktioner. När projektledaren godkänner tids- och utgiftstransaktioner registrerar systemet transaktionerna i entiteten **Faktiska projektvärden** och skickar informationen till modulen **Projekthantering och redovisning** i Dynamics 365 Finance. Projektrevisorn granskar och publicerar sedan posterna med hjälp av [integrationsjournalen för Project Operations](../project-accounting/project-operations-integration-journal.md). Denna artikel innehåller viktiga redovisningsuppgifter för projektets faktiska värden, till exempel fakturering, momsgrupp, momsgrupp för faktureringsobjekt och ekonomiska mått.

Projektledaren kan granska icke-fakturerade försäljningstransaktioner med hjälp av faktureringsmetoden för tid och material i [faktureringseftersläpningen för tid och material](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) samt fastprisfakturering i [milstolpar med fast pris](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Med dessa vyer kan du filtrera och välja transaktioner som behöver tas med i nästa faktureringscykel och sedan markera dem som **Redo att fakturera**.

Du kan [skapa en proforma-faktura manuellt](../proforma-invoicing/create-manual-proforma-invoice.md) eller använda en [periodisk process](../proforma-invoicing/configure-automated-invoice-creation.md). Projektledaren kan [justera ett proforma-fakturautkast](../proforma-invoicing/manage-proforma-invoice.md) efter behov och sedan bekräfta det.

Den bekräftade proforma-fakturan skickas till modulen **Projekthantering och redovisning** i Finance. Projektrevisorerna utformar och uppdaterar projektfakturaförslaget och publicerar samt skrider sedan ut dokumentet. Bokförda projektfakturor registreras i huvudboken samt i under-transaktionsregistren för kunder och projekt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]