---
title: Nyheter i juli 2021 – Project Operations för resurs/icke-lagerbaserade scenarier
description: Den ämne innehåller information om kvalitetsuppdateringarna som är tillgängliga i juli 2021-versionen av Project Operations för resurs-/icke-lagerbaserade scenarier.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1c88f3b4747005bee0d68d0e8a4314c01ffdaf34
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600902"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter i juli 2021 – Project Operations för resurs/icke-lagerbaserade scenarier

*Gäller: Project Operations för resurs-/icke-lagerbaserade scenarier*

Detta ämne gäller för följande Dynamics 365 Project Operations-komponenter och -versioner:

   - Project Operations i Microsoft Dataverse miljöversion 4.12.0.148 eller 4.12.0.152.
   - Projekthantering och redovisning i en Dynamics 365 Finance-miljö, version 10.0.20.

## <a name="features-included-in-this-release"></a>Funktioner som ingår i denna version

Följande funktioner ingår i denna version:

- Möjlighet för administratörer att visa PSS-loggar och operationsuppsättningsloggar från inställningsmenyn. Loggarna lagras i 90 dagar.

## <a name="project-operations-dual-write-maps-updates"></a>Uppdateringar av Project Operations mappningar med dubbelriktad skrivning

Det finns inga uppdateringar för mappning för dubbelriktad skrivning för Project Operations i den här versionen.

En aktuell lista och mappningsversioner för dubbelriktad skrivning för Project Operations finns i [Mappningsversioner för dubbelriktad skrivning för Project Operations](../environment/resource-dual-write-maps.md).

Kör alltid den senaste versionen av kartan i miljön och aktivera alla relaterade tabellmappningar när du uppdaterar Project Operations Dataverse-lösningen och ekonomilösningen. Vissa funktioner kanske inte fungerar korrekt om den senaste versionen av mappningen inte har aktiverats. Den aktiva versionen av kartan visas på sidan **Dubbelriktad skrivning** i kolumnen **Version**. Aktivera en ny version av kartan genom att välja **tabellmappningsversioner**, välja den senaste versionen och sedan spara den valda versionen. Om du har anpassat en "out-of-the-box"-tabellmappning ska du tillämpa ändringarna på nytt. Mer information finns i [Program för livscykelhantering](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Om du stöter på ett problem som startar kartan, följ instruktionerna i avsnittet [Saknade tabellkolumner saknas på kartor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i felsökningsguiden för dubbla skrivningar.

## <a name="quality-updates"></a>Kvalitetsuppdateringar

### <a name="project-operations-on-dataverse"></a>Project Operations i Dataverse

| **Funktionsområde**              | **Referensnummer** | **Kvalitetsuppdatering**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fakturering och prissättning           | 2224046              | Fältet **Transaktionsklass** kan redigeras på fliken **Information om offertrad** men är låst om du arbetar från sidan **Information om offertrad**.                                                                     |
| Fakturering och prissättning           | 2224400              | Åtgärden **Stäng offerten som vunnen** misslyckas om en offert inte har några datummilstolpar.                                                                                                                                    |
| Fakturering och prissättning           | 2234089              | När du anger en produktbeskrivning manuellt rensas den efter att du har ange en kvantitet för en materialberäkning.                                                                                                                         |
| Fakturering och prissättning           | 2234100              | Rutnätet **Faktureringsinställningar för uppgift** inkluderar inte kolumnen **Material** och dess värde på fliken **Uppgiftsfakturering** för projektet.                                                                                                       |
| Fakturering och prissättning           | 2277409              | Produkt-ID är inte tillgängligt på kontraktradsdetaljen för en materialtypsrad.                                                                                                                                        |
| Fakturering och prissättning           | 2281728              | Att skapa en kontraktsruta omvärderar onödigt faktiskt och orsakar betydande ökningar i datavolym, vilket påverkar prestandan.                                                                                |
| Fakturering och prissättning           | 2298668              | Rader som hör till en förterad och borttagna utgifter tas inte bort.                                                                                                                                     |
| Fakturering och prissättning           | 2300192              | När flera användare redigerar en faktura går det att skapa en ny fakturaradsdetalj på en bekräftad faktura.                                                                                   |
| Fakturering och prissättning           | 2301569              | Det går inte att korrigera fakturor om \$0 belopp har använts.                                                                                                                                        |
| Fakturering och prissättning           | 2307965              | Ett fel visas om ett kategoripris skapas med värden som saknas.                                                                                                                           |
| Fakturering och prissättning           | 2326870              | Ett fel uppstår i **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** om **producttypecode** är null.                                                                            |
| Fakturering och prissättning           | 2332732              | Ett fel visas om en kontraktradsmilstolpar skapas utan en orderrad.                                                                                                                |
| Projektplanering och spårning | 2181094              | API för projektschemaläggning stöder nu PSS-loggar och användningsuppsättningsloggar som lagras i 90 dagar.                                                                                                                  |
| Projektplanering och spårning | 2254201              | Etiketten **Schemaläggningsläge** uppdateras med information som beskriver standardlogiken.                                                                                                                                      |
| Projektplanering och spårning | 2300252              | Svarscachen **openProject** uppdateras och inkluderar tokenägaren i cachenyckeln, **bas-URL** och **Segment-URL** så att **Begäran-URL** alltid kan återskapas om **bas-URL** ändras. |
| Projektplanering och spårning | 2301312              | **msdyn_membershipstatus** har tagits bort från vyn **Medlemmar i projektteamet**.                                                                                                                                        |
| Projektplanering och spårning | 2302759              | Produkter hämtas i onödan på flikarna **Resurstilldelningar**, **Uppskattningar** och **Utgiftsberäkningar**.                                                                                                        |
| Projektplanering och spårning | 2308050              | **CopyProject** misslyckas med felmeddelandet "Det gick inte att hämta token för att tala med fjärrtjänst".                                                                                                                           |
| Projektplanering och spårning | 2322650              | Vyn **Projektuppgiftslista** har uppdaterats så att datumet för uppgiften visas som standard.                                                                                                            |
| Projektplanering och spårning | 2327266              | **CopyProject** genereras felmeddelandet "Nyckeln finns inte i ordlistan" vid kopiering.                                                                                                      |
| Projektplanering och spårning | 2328123              | **CopyProject** genererar felet "Det gick inte att hämta token för att tala med fjärrtjänst".                                                                                                                          |
| Projektplanering och spårning | 2336258              | **CopyProject** kopierar felaktigt platsnamnen för resurser.                                                                                                                                                 |
| Fakturering och prissättning           | 2224476              | Fältet **Bokningsbar resurs** är inte korrekt standard för den inloggade användaren på sidan **Materialanvändning**.                                                                                                            |
| Resurshantering           | 2277249              | Ett fel uppstår när ett resurskrav som inte är baserat på projekt uppdateras.                                                                                                            |
| Resurshantering           | 2323869              | Filtrerade resurser känns inte igen korrekt i resursutnyttjandet.                                                                                                                                             |
| Tid och utgift              | 2176538              | Felaktiga filteroperatörer används på kontrollen **Tidsinmatning**.                                                                                                                                                   |
| Tid och utgift              | 2177462              | Om du tar bort en tidsinmatning i rutnätet uppdateras inte knappstatus **Skicka**, **Återkalla**, **Ta bort** och **Redigera post** som förväntat.                                                                                        |
| Tid och utgift              | 2299985              | **TimeEntriesImportFromResourceAssignment** upprätthåller inte start-/sluttiden från tilldelningens konturer.                                                                                                  |
| Tid och utgift              | 2318426              | När en tidspost har skickats in kan låsta fält fortfarande redigeras.                                                                                                                                   |
| Tid och utgift              | 2323749              | Ett fel uppstår när en kostnad skapas från fliken **Relaterad** för en bokningsbar resurs.                                                                                                      |
| Tid och utgift              | 2327678              | När du skapar en tidspost från fliken **Relaterad** för en bokningsbar resurs skickas inte den överordnade resursen till tidsinmatningskontrollen.                                                                            |
| Allmänt                       | 2296857              | Förloppsspårning för jobb som körs länge.                                                                                                                                                                        |
| Allmänt                       | 2253682              | Project Operations-lösningen med dubbelriktade skrivningar bör inte installeras när dubbelriktade skrivning installeras i en miljö utan lösningen med dubbelriktade skrivningar.                                                |
| Allmänt                       | 2316420              | Det går inte att tillhandahålla kärnetablering för Project Service om programanvändarens affärsenhet ändras.                                                                                                                     |
| Allmänt                       | 2376405              | Åtgärdat publicerarbaserat uppdateringsproblem (kvalitetsuppdatering är tillgänglig i version 4.12.0.152)                                                                                                                     |
### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektledning och redovisning i Dynamics 365 Finance

| Funktionsområde                      | Referensnummer | Kvalitetsuppdatering                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektledning och redovisning | 4620267          | Det går inte att anpassa formulär för att lägga till fältet **Syfte** till sidorna **Projektposterad transaktion**, **Skapa fakturaförslag** och **Fakturaförslag**.                                                                                                                                                                                         |
| Projektledning och redovisning | 4613449          | När du väljer ett Projektkontrakt-ID i Finance öppnas sidan Project Operations för att skapa en ny post, i stället för sidan för projektkontrakt som redan skapats.                                                                                                                                           |
| Projektledning och redovisning | 4614445          | I Project Operations i en integrerad scenariodistribution kan du inte redigera fältet **Momsgrupp för artikelförsäljning** i fakturaförslaget som har importerats från testerna. Artikelförsäljningsgruppen ska vara redigerbar för ett öppet fakturaförslag av alla transaktionstyper, inklusive för konto, timmar, utgifter, avgifter och objekt. |
| Projektledning och redovisning |                  | Det går inte att publicera ett fakturaförslag på grund av en korrigering av en negativ tidstransaktion.                                                                                                                                                                                                                                              |
| Projektledning och redovisning |                  | Fakturaförslagsrader dupliceras på grund av flera periodiska processer för **importera från mellanlagring** som körs samtidigt.                                                                                                                                                                                                                |

