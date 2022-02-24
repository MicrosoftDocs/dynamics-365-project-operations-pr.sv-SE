---
title: Nyheter i november 2020 – Project Operations för resursscenarier/icke lagerbaserade scenarier
description: I det här ämnet finns information om de kvalitetsuppdateringar som är tillgängliga i utgåvan november 2020 för Project Operations för resursscenarier/icke lagerbaserade scenarier.
author: sigitac
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c7ec9360401bf214ae867769b0e48e545a6bad48
ms.sourcegitcommit: 64d0de964a9b66c015ffcf1db62cbb6216cb3187
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367288"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i november 2020 – Project Operations för resursscenarier/icke lagerbaserade scenarier

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Det här ämnet gäller för följande komponenter och versioner i Dynamics 365 Project Operations:

- Project Operations i CDS-miljö version 4.4.0.70
- Projektledning och redovisning i Dynamics 365 Finance-miljö version 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Uppdateringar i Project Operations för resursscenarier/icke lagerbaserade scenarier

### <a name="project-operations-on-cds"></a>Project Operations i CDS

| Funktionsområde                 | Referensnummer | Kvalitetsuppdatering                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Affärsmöjlighetshantering       | 2036993          | Beräkningsrad och resurstilldelnings kontraktrader uppdateras på vinnande offerter när offertradtypen är **alla uppgifter**.                                                 |
| Fakturering och prissättning          | 2070392          | Projektkontraktraderna på fakturan ökar varje gång **uppdatera fakturatransaktioner** väljs.                                                                         |
| Projektplanering             | 2043336          | Det går inte att ta bort en medlemspost i projektgruppen.                                                                                                                                  |
| Projektplanering             | 2046013          | Inkonsekvent beteende för uppskattningar av kolumnerna vid inläsning jämfört med vid ändring av tidsfastyp.                                                                                   |
| Projektplanering             | 2046647          | Start- och sluttider infaller efter en timme när resurskrav genereras från projektets teammedlemmar.                                                                      |
| Projektplanering             | 2053879          | (Enligt kommande CDS-lansering) PublishUnassignedAssignments gör ett försök att spara en aktivitet när felmeddelandet "värdet som skickades för ConditionOperator.In är tomt" visas.                       |
| Projektplanering             | 2055501          | Om du låter **projektets startdatum** vara tomt uppstår ett fel i schemat.                                                                                                      |
| Projektplanering             | 2066817          | Det går inte att skapa en allmän resurs med hjälp av personväljaren på fliken **uppgifter**.                                                                                                   |
| Projektplanering             | 2067034          | Knappen **Visa detaljer** är inte tillgänglig på sidan **information om uppgiften**.                                                                                                       |
| Resurshantering          | 2046667          | Allmänna teammedlemmar tas inte bort även efter att alla resurser har uppfyllts.                                                                                                    |
| Post för tid och snabbutgift | 2047499          | Knappen **Ny** på sidan tidspost öppnar sidan **ny e-postsignatur**.                                                                                               |
| Post för tid och snabbutgift | 2059859          | Oväntat popup-fönster öppnas när en utgiftspost skapas.                                                                                                                         |
| Annat                         | 2044181          | (Avinstallerar inköpsorder) - när du försöker avinstallera msdyn_ProjectServiceCore_Patch och msdyn för Project Service-kärnlösningar visas felmeddelandet "posten är inte tillgänglig".  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektledning och redovisning i Dynamics 365 Finance

| Funktionsområde        | Referensnummer | Kvalitetsuppdatering                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intäktsredovisning | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Procentvärdet för projektuppskattningen är fel när ett kontrakt använder en utländsk valuta och arbetsprocessens procentsats för slutförande metod.                     |
| Intäktsredovisning | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Det går inte att bokföra uppskattningar med den **faktisk kostnad** slutförandemetoden.                                                                                                    |
| Intäktsredovisning | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Eliminering misslyckas på grund av ett obalans i verifikation när företagsvalutan och transaktionsvalutan är olika.                                              |
| Utgiftshantering  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | För användare som inte är administratörer visas inte uppslagsvärden för kolumner för utgiftsrader, till exempel **projekt-ID** och **utgiftskategori** i dataanslutningsramen. |
| Utgiftshantering  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Standard för radegenskap visas inte för utgiftskategorier.                                                                                                         |
| Utgiftshantering  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Utgiftsintegration måste inkludera radegenskapen från utgiftsrapporten.                                                                                             |
| Fakturering           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Det går inte att bokföra projektfakturaförslag på grund av ett felmeddelande om att kombinationen av FD inte har verifierats.                                                    |
| Fakturering           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Det går inte att visa transaktioner från detaljsidan **faktura**.                                                                                                              |
| Fakturering           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Fakturaförslagsrader kan tas bort.                                                                                                                                  |
| Projektredovisning  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Menyalternativet **Prognos** visas inte på listsidan **projekt**.                                                                                                   |
| Projektredovisning  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Det går inte att öppna **projektrapport**   > **transaktioner och prognos**.                                                                                                       |
| Projektredovisning  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Justera redovisning** är inte aktiverat för fakturerade projekttransaktioner.                                                                                                  |
| Projektredovisning  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Redovisningsinformationen visas inte i **ProjCDSActualsImport** tabellen när **Integration** journalen bokförs.                                                  |
| Projektredovisning  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Projektprognostransaktionen dubbleras när du tar bort och sedan läser en resurstilldelning.                                                                            |
| Projektredovisning  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | När du väljer en projekt-ID-länk öppnas inte URL: n djup länk för CDS.                                                                                                         |
| Projektredovisning  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Det går inte att uppdatera startdatum för en aktivitet i CDS.                                                                                                                           |
| Projektredovisning  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Det går inte att aktivera funktionen eftersom flera kontraktrader inte är möjliga utan integrering av CDS.                                                                                   |

### <a name="regulatory-updates"></a>Regleringsuppdateringar
Mer information om regleringsuppdateringar för Finance and Operations-appar finns i [regleringsuppdateringar](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Du kan också logga in på LCS och visa de planerade regeluppdateringarna med hjälp av verktyget för att söka efter problem. Med problemsökning kan du söka efter land, typ av funktion och utgåva.
