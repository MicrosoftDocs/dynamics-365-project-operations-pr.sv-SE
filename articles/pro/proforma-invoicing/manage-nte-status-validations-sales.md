---
title: Hantera undre status och valideringar
description: I det här ämnet finns information om kontroller av undre gränser som har utförts i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 09dea414e91a365f33bd23089c427b5f63f55c8e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130015"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Hantera undre status och valideringar 

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

## <a name="not-to-exceed-on-approvals"></a>Undre gräns vid godkännanden

När en tid eller utgiftspost skickas skapas en godkännandepost. Om godkännandet är debiterbart och mappar till en kontrraktrad för tid och material, slutför systemet en undre gräns för valideringskontroll på följande nivåer:

  - Kontrollera mot den gräns som har ställts in för kunden på projektkontraktraden
  - Kontrollera mot den gräns på kontraktraden
  - Kontrollera mot den gräns för kunden
  - Kontrollera mot den gräns på kontraktet

Kontrollerna på varje nivå innebär att se till att beloppet för försäljningsvärdet för detta godkännande inte kommer att strida mot det belopp som inte överstiger överskridandet på den nivån efter det att den bokförda faktureringstiden har bokförts och det belopp som fakturerats till den nivån.

Om kontrollen lyckas får godkännandet en valideringsstatus som **lyckats**.

Om kontrollen misslyckas får godkännandet en valideringsstatus som **misslyckats**. Den undre gränsen för verifieringsinformationen meddelar användaren vid vilken nivå verifieringen misslyckades.

När den inskickade tiden eller utgiftsposten inte betraktas som debiterbar är undre gränsen för valideringsstatusen inställd på **inte tillämpligt** med valideringsinformationen lika med **inte tillämpligt**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Undre gräns på ej fakturerade försäljningsvärden

När en tids- eller utgiftspost godkänns skapas endast verkliga och utgående försäljningsposter. Om ofakturerade faktiska försäljningen som skapats är debiterbar och mappar till en kontraktrad för tid och material utför appen en undre gräns för valideringskontroll på följande nivåer:

  - Kontrollera mot den gräns som har ställts in för kunden på projektkontraktraden
  - Kontrollera mot den gräns på kontraktraden
  - Kontrollera mot den gräns för kunden
  - Kontrollera mot den gräns på kontraktet

Kontrollerna på varje nivå innebär att se till att beloppet för försäljningsvärdet för det faktiska värdet inte kommer att strida mot det belopp som inte överstiger överskridandet på den nivån efter det att den bokförda faktureringstiden har bokförts och det belopp som fakturerats till den nivån.

Om kontrollen godkänns får den ofakturerade faktiska försäljningen en status som inte är högre än det **bekräftade**.

Om kontrollen misslyckas får den ofakturerade faktiska försäljningen en status som inte är högre än det **misslyckad**. Verifieringsinformationen meddelar användaren vid vilken nivå verifieringen misslyckades.

När det ej fakturerade försäljningsvärdet beaktas som debiterbar eller ingår finns det ingen inställning för undre gräns på någon av de fyra nivåerna, eller om den faktiska skapas är kostnad, kvarhållare, resursenhet eller försäljning mellan företag måste fälten **Undre status** och **Valideringsinformation om undre gräns** måste ställas in på **Gäller inte**.

## <a name="reset-the-not-to-exceed-status"></a>Återställ till status Överskrid inte

Du kan göra en massåterställning av statusen Överskrid inte. Detta gör det möjligt för projektledarna att justera Överskrid inte-validering för att prioritera fakturering av en viss del av arbetet, tiden eller kostnaderna över andra som redan har beställts från det tillgängliga beloppet för Överskrid inte.

När statusen för Överskrid inte-status har återställts för faktiska fakturerade försäljningsvärden minskas utfäst belopp. Projektledaren kan välja en annan del av arbetet, tid eller utgifter som tidigare inte kunde överskrida valideringen och utvärdera dem på nytt. Med minskningen av det utfästa beloppet godkänns de här värdena i automatiskt valideringen. Detta hjälper projektledaren att utöva större inflytande och styra de fakturerade transaktionerna för perioden.

Om du vill återställa statusen till Överskrid inte väljer du en eller flera värden från någon av vyerna **Eftersläpad fakturering av tid och material** eller **Faktiska värden** och väljer sedan **Återställ till status Överskrid inte**.

Överskrid inte-status återställs till **inte utvärderad** på alla relevanta valda faktiska värden. Verkliga värden som har statusåterställning för överskrid inte är ej fakturerade försäljningsvärden som inte redan har fakturerats, inte på fakturautkast och är markerade som debiterbara. Alla andra valda faktiska värden ignoreras.

## <a name="reevaluate-not-to-exceed-status"></a>Omvärdera status för Överskrid inte

Du kan göra en en ny utvärdering i bulk av statusen Överskrid inte. Ny utvärdering av statusen Överskrid inte är användbar när:

  - En omförhandling av undre gränsen med kunden och de faktiska värdena behöver utvärderas på igen.
  - Projektledaren vill finjustera faktureringen av ej fakturerade försäljningsvärden genom att prioritera en del av arbetet över en annan.

Om du vill omvärdera statusen till Överskrid inte väljer du en eller flera värden från någon av vyerna **Eftersläpad fakturering av tid och material** eller **Faktiska värden** och väljer sedan **Omvärdera status Överskrid inte**.

Alla relevanta valda faktiska värden med en undre gräns utvärderas mot den begränsningsinställning för undre gräns. Verkliga värden som är relevanta för omvärdering för överskrid inte-status är ej fakturerade försäljningsvärden som inte redan har fakturerats, inte på fakturautkast och är markerade som debiterbara. Alla andra valda faktiska värden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]