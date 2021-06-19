---
title: Koncernintern fakturering – Översikt
description: Detta ämne innehåller information och exempel om konfigurering av koncernintern fakturering av projekt.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42af89105f8325f1c94df6d2133d2c329facf2b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002663"
---
# <a name="intercompany-invoicing-overview"></a>Koncernintern fakturering – Översikt

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Organisationen kan ha flera avdelningar, dotterbolag och andra juridiska enheter som överför produkter och tjänster till varandra för projekt. Den juridiska person som tillhandahåller tjänsten eller produkten kallas den *långivande juridiska personen*. Den juridiska person som erhåller tjänsten eller produkten kallas den *låntagande juridiska personen*.

Följande illustration visar ett typiskt scenario där två juridiska entiteter, Contoso Robotics USA (den lånande juridiska entiteten) och Contoso Robotics UK (den utlånande juridiska entiteten), delar resurser för att leverera ett projekt till kunden, Adventure works. För detta scenario har Contoso Robotics USA ingått ett avtal om att leverera arbetet till Adventure Works.

![Koncernintern fakturering](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations använder följande flöde för att bearbeta koncerninterna transaktioner:

1. Resurser från den utlånande juridiska personen registrerar koncerninterna tids- eller utgiftstransaktioner efter bokningstid och kostnad mot projekt i den låntagande juridiska personen.
2. Tids- och utgiftskostnader bokförs i det långivande företaget genom att använda det låntagande företagets enhetskostnadslista.
3. Koncerninterna, icke-fakturerade säljtransaktioner bokförs i det långivande företaget genom att använda det låntagande företagets enhetskostnadslista.
4. Ej fakturerade intäkter bokförs i det låntagande företaget med hjälp av projektkontraktets försäljningsprislista. Kunden kan faktureras när ej fakturerade intäkter registreras. Kunden behöver inte vänta tills den koncerninterna fakturahanteringen är klar.
5. Koncerninterna kundfakturor skapas på periodisk basis i det långivande företaget. Fakturorna skapas manuellt eller genom att använda en periodisk automatiserad process. En enskild faktura kan skapas för varje låntagande juridisk person, eller också kan separata fakturor kapas efter projekt.
6. När den koncerninterna kundfakturan bokförs i den utlånande juridiska personen skapas motsvarande, väntande leverantörsfaktura i låntagande juridisk person. Kostnaderna i den väntande leverantörsfakturan kommer att registreras i projektredovisningen när fakturan bokförs.

Följande diagram illustrerar koncernintern fakturering eftersom denna avser redovisningshändelser och förväntade bokföringar i redovisningen.

![Koncerninternt flöde](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Ytterligare resurser

- [Konfigurera koncernintern fakturering](configure-intercompany-invoicing.md)
- [Registrera koncerninterna transaktioner](create-intercompany-transactions.md)
- [Skapa koncerninterna kund- och leverantörsfakturor](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]