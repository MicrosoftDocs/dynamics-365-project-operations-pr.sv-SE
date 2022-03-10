---
title: Vad är nytt i juli 2021 – Project Operations lite-distribution
description: Den ämne innehåller information om kvalitetsuppdateringarna som är tillgängliga i julio 2021-versionen av Project Operations Lite-distribution.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8cff4c37e1c2df29041ef86cdcf05afa6093f890565a855024202e87fd533ea5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009238"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Vad är nytt i juli 2021 – Project Operations lite-distribution

_Gäller: Lite-distribution - avtal till proforma-fakturering_

Detta ämne gäller för följande Dynamics 365 Project Operations-komponenter och -versioner:

  - Project Operations i Dataverse miljöversion 4.12.0.148 eller 4.12.0.152.

## <a name="quality-updates"></a>Kvalitetsuppdateringar
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
