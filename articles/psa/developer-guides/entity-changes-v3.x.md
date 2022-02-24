---
title: Ändringar av entitet, kontroll och användargränssnitt (Project Service Automation 3.x)
description: I det här ämnet beskrivs lösningsändringar för Microsoft Dynamics Project Service Automation 3.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 48062eda1f524dd3ca0d5feccf11fd5577521275
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148755"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Ändringar av entitet, kontroll och användargränssnitt (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


I och med lanseringen av Microsoft Dynamics Project Service Automation (PSA) 3.x, har många ändringar gjorts i entiteter, kontroller, vyer och användargränssnitt. Det här ämnet innehåller information om dessa viktiga ändringar.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Överordnade-underordnade relationer för entiteter för försäljningsdokument, försäljningsdokumentrad, raddetaljer i försäljningsdokument
I versioner av Dynamics 365 Project Service Automation (PSA) som har getts ut före version 3.0 implementeras en del av relationer mellan entiteter för försäljningsdokument, försäljningsdokumentrad, raddetaljer i försäljningsdokument via strängfält som skulle innehålla en strängrepresentation av en GUID för den relaterade entiteten. Detta beror på plattformsbegränsningarna som kräver en viktig anpassad kod på server- och klientsidorna i lösningen för att göra att dessa relationer fungerar liknande Dynamics CRM entitetsrelationer och för att skapa strängfält fungerar som uppslagsfält.

PSA 3.0 har uppdaterats för att påverka den nya entiteten relationer mellan entiteterna försäljningsdokument och försäljningsdokumentrad.

Eftersom uppslagsfält nu kan användas för att indikera referenser till entiteter behövs inte längre de fält som har strängvärdet för GUID för den relaterade entiteten i tidigare versioner. Den anpassade klient- och serversidkoden som hanterar relationer som definieras av äldre strängfält har också föråldrats.

### <a name="entity-schema-changes"></a>Enhetsschemaändringar
Följande tabell innehåller en en-mot-en-lista med de inaktuella strängfälten och de nya uppslagsfälten för entiteterna. 

 Entitet |   Inaktuellt fält (sträng) | Nytt fält (uppslag)
--- | --- | ---
invoicedetail (fakturarad) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (faktisk) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (projektkontraktradens faktureringstidsplan) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (milstolpen för en projektkontraktrad) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (fakta) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (fakturaraddetalj) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (Journalrad) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (resurskategori för projektkontraktrad) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Information om projektkontraktrad) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Transaktionskategori för projektkontraktrad) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Transaktionsklassificering för projektkontraktrad) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Faktureringsschema för offertrad) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Resurskategori för offertrad) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Milstolpe för offertrad) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Information om offertrad) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Transaktionskategori för offertrad) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Transaktionsklassificering för offertrad) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Orderrad) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Inaktuella anpassade vyer och kontroller
Följande anpassade vyer och kontroller och relaterade artefakter, är inaktuella.

- Debiterbar vy.
- Anpassade rutnätskontroller för att visa offertradinformation på sidan **projektinformation** för offertraden.
- Anpassade rutnätskontroller för att visa information om projektets kontraktrader på sidan **projektinformation** för försäljningsorderraden.

> [!NOTE]
> En fullständig lista över inaktuella resurser finns i [Inaktuella webbresurser i Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).

## <a name="unified-client-interface-app-module"></a>Unified Client Interface appmodul
När du introducerar en Unified Client Interface (UCI) appmodul har PSA poster för webbplatsöversikt tagits bort från systemet.  
Funktioner som är relaterade till formulärväxling för affärsmöjlighet, offert, order, faktura är inaktuell eftersom de inte längre behövs eftersom app-modulen för icke-appar endast innehåller PSA-versioner av formulären.  

Följande webbresurser är inaktuella:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> En fullständig lista över inaktuella resurser finns i [Inaktuella webbresurser i Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).


