---
title: Konfigurera koncernintern projektfakturering
description: I det här ämne visas hur du konfigurerar projektfakturering mellan två företag i organisationen.
author: Yowelle
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab0d1eb2806d2e1650faccf3fbb63c63c0fa9e05
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683297"
---
# <a name="configure-intercompany-project-invoicing"></a>Konfigurera koncernintern projektfakturering

[!include [banner](../../includes/banner.md)]

I det här ämne visas hur du konfigurerar projektfakturering mellan två företag i organisationen. I den här uppgiften används USSI-datauppsättningen.

1. I navigeringsfönstret går du till **moduler > leverantörsreskontra > leverantörer > alla leverantörer**.
2. I listan **Alla leverantörer** leta upp och markera önskad post.
3. Välj plan i åtgärdsrutan **Allmänt**.
4. Välj **Koncerninternt**.
5. Ställ in **aktiv** till **Ja** för att aktivera koncernintern handel.
6. I fältet **Kundens företag** ange eller välja ett värde.
7. I fältet **Mitt konto** ange eller välj ett värde.
8. Välj **Spara**.
9. Stäng sidorna för att återgå till startsidan.
10. I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > pris > projektledning och redovisningsparametrar**.
11. Välj fliken **Koncerninternt**.
12. Flytta skjutreglaget till **Ja** för att aktivera koncernintern resursplanering och tidrapporter.
13. Markera den markerade raden i listan.
14. Välj **Nytt**.
15. I fältet **låntagande juridisk person** ange eller välj ett värde.
16. Markera kryssrutan för **periodiserad intäkt**.
17. I fältet **Standardkategori för tidsrapport** ange eller välj ett värde.
18. I fältet **Standardkategori för utgift** ange eller välj ett värde.
19. Välj **Spara**.
20. Stäng sidan.
21. I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > bokföring > inställning av bokföring**.
22. I fältet **Typer av redovisningskonton** välj ett alternativ.
23. Välj **Nytt**.
24. I fältet **huvudkonto** för den nya raden, ange önskade värden.
25. Välj **Spara**.
26. Stäng sidan.
27. I navigeringsfönstret går du till **moduler > projektledning och redovisning > inställning > pris > överföringspris**.
28. Välj **Nytt**.
29. I fältet **Effektivt datum** anger du ett datum.
30. I fältet **låntagande juridisk person** ange eller välj ett värde.
31. I fält **Överföringsprismodell** välj alternativ,
32. I fältet **Prissättning** anger du ett nummer.
33. Välj **Spara**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]