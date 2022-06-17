---
title: Koncernintern fakturering – Översikt
description: Den här artikeln innehåller information och exempel på koncernintern fakturering för projekt.
author: sigitac
ms.date: 11/19/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd17f6542558bae9d4b97d0a92aefae52571cfa8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913596"
---
# <a name="intercompany-invoicing-overview"></a>Koncernintern fakturering – Översikt

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Organisationen kan ha flera avdelningar, dotterbolag och andra juridiska enheter som överför produkter och tjänster till varandra för projekt. Den juridiska person som tillhandahåller tjänsten eller produkten kallas den *långivande juridiska personen*. Den juridiska person som erhåller tjänsten eller produkten kallas den *låntagande juridiska personen*.

Följande bild visar ett typiskt scenario där två juridiska personer, Contoso Robotics USA (den låntagande juridiska personen) och Contoso Robotics UK (den utlånande juridiska personen) delar resurser för att leverera ett projekt åt kunden, Adventure Works. För detta scenario är Contoso Robotics USA kontrakterat att leverera arbetet till Adventure Works.

![Koncernintern fakturering.](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations använder följande flöde för att bearbeta koncerninterna transaktioner:

1. Resurser från den utlånande juridiska personen registrerar koncerninterna tids- eller utgiftstransaktioner efter bokningstid och kostnad mot projekt i den låntagande juridiska personen.
2. Tids- och utgiftskostnader bokförs i det långivande företaget genom att använda det låntagande företagets enhetskostnadslista.
3. Koncerninterna, icke-fakturerade säljtransaktioner bokförs i det långivande företaget genom att använda det låntagande företagets enhetskostnadslista.
4. Ej fakturerade intäkter bokförs i det låntagande företaget med hjälp av projektkontraktets försäljningsprislista. Kunden kan faktureras när ej fakturerade intäkter registreras. Kunden behöver inte vänta tills den koncerninterna fakturahanteringen är klar.
5. Koncerninterna kundfakturor skapas på periodisk basis i det långivande företaget. Fakturorna skapas manuellt eller genom att använda en periodisk automatiserad process. En enskild faktura kan skapas för varje låntagande juridisk person, eller också kan separata fakturor kapas efter projekt.
6. När den koncerninterna kundfakturan bokförs i den utlånande juridiska personen skapas motsvarande, väntande leverantörsfaktura i låntagande juridisk person. Kostnaderna i den väntande leverantörsfakturan kommer att registreras i projektredovisningen när fakturan bokförs.

Följande diagram illustrerar koncernintern fakturering eftersom denna avser redovisningshändelser och förväntade bokföringar i redovisningen.

![Koncerninternt flöde.](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Ytterligare resurser

- [Konfigurera koncernintern fakturering](configure-intercompany-invoicing.md)
- [Registrera koncerninterna transaktioner](create-intercompany-transactions.md)
- [Skapa koncerninterna kund- och leverantörsfakturor](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]