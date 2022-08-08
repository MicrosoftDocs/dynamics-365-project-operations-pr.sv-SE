---
title: Borttagna eller inaktuella funktioner i Dynamics 365 Project Operations
description: I den här artikeln beskrivs funktioner som har tagits bort, eller har planerats för borttagning från Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028351"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Borttagna eller inaktuella funktioner i Dynamics 365 Project Operations

_**Gäller till:** Project Operations för resurs-/icke-lagerbaserade scenarier, Lite-distribution – avtal till proforma-fakturering och Project Operations för lagerbaserade/produktionsbaserade scenarier_

I den här artikeln beskrivs funktioner som har tagits bort, eller har planerats för borttagning från Dynamics 365 Project Operations.

- En *borttagen* funktion är inte längre tillgänglig i produkten.
- En *inaktuell* funktion är inte i aktiv utveckling och kan tas bort i en kommande uppdatering.

Den här listan är avsedd att hjälpa dig att ta hänsyn till dessa borttagningar och avfasningar i din egen planering.

> [!NOTE]
> Detaljerad information om objekt i appar för ekonomi och drift finns i de [**tekniska referensrapporterna**](/dynamics/s-e/global/axtechrefrep_61). Du kan jämföra olika versioner av rapporterna för mer information om objekt som har ändrats eller tagits bort i respektive version av appar för ekonomi och drift.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Borttagna eller inaktuella funktioner i Project Operations-versionen för mars 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Projekthanterings- och redovisningsparametern "Skapa alltid justeringstransaktion"

| &nbsp; | &nbsp; |
|--------|--------|
| **Orsak till avfasning/borttagning** | Justeringstransaktioner krävs för granskningssyften. När parametern har inaktiverats döljs den. Systemet skapar alltid justeringstransaktioner, precis som det gör för tillfället när parametern har inställningen **Ja**. |
| **Ersatt med en annan funktion?** | No |
| **Produktområden som påverkas** | App |
| **Distributionsalternativ** | Project Operations för produktionsbaserade/lagerbaserade scenarier |
| **Status** | Inaktuell: Från den 1 mars 2023 kommer parametern att döljas och systembeteendet ändras så att justeringstransaktioner alltid skapas. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Projekthantering och redovisning: parametern "Använd justeringsdatum som nytt projektdatum"

| &nbsp; | &nbsp; |
|--------|--------|
| **Orsak till avfasning/borttagning** | Parametern användes ursprungligen för att tillåta justeringar när en räkenskapsperiod stängdes. Detta är dock inte längre obligatoriskt eftersom det går att ändra redovisningsdatumet för transaktionen till det första datumet för den öppna perioden, om denna är konfigurerad. Projektdatumet får inte ändras eftersom det motsvarar det datum då transaktionen inträffade. |
| **Ersatt med en annan funktion?** | No |
| **Produktområden som påverkas** | App |
| **Distributionsalternativ** | Project Operations för produktionsbaserade/lagerbaserade scenarier |
| **Status** | Inaktuell: Från den 1 mars 2023 kommer parametern att döljas och systembeteendet ändras så att projektdatumet aldrig ändras i samband med justering. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Arbetsflöde för resursförfrågan i Project Operations för lagerbaserade/produktionsbaserade scenarier

| &nbsp; | &nbsp; |
|--------|--------|
| **Orsak till avfasning/borttagning** | Inaktuellt på grund av begränsningar för låg användning och transaktionsvolym. |
| **Ersatt med en annan funktion?** | No |
| **Produktområden som påverkas** | App |
| **Distributionsalternativ** | Project Operations för produktionsbaserade/lagerbaserade scenarier |
| **Status** | Inaktuell: Från den 1 mars 2023 inaktiverar vi alternativet att begära resurser för projektet med hjälp av arbetsflödet. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Sidan Projektfakturaförslag utan vyer för sidhuvud och rader

| &nbsp; | &nbsp; |
|--------|--------|
| **Orsak till avfasning/borttagning** | Inaktuellt på grund av förbättringar av sidan som introducerades tillsammans med funktionsnyckeln **Använd förslags- och fakturaformulären för projektfaktura med vyerna Sudhuvud och Rader**. |
| **Ersatt med en annan funktion?** | Ja |
| **Produktområden som påverkas** | App |
| **Distributionsalternativ** | Project Operations för produktions-/lagerscenarier; Project Operations för resursbaserade/ej lagerförda scenarier |
| **Status** | Inaktuellt: Från den 1 mars 2023 stänger vi av den tidigare (gamla) sidan och aktiverar funktionsnyckeln **Använd förslags- och fakturaformulären för projektfaktura med vyerna Sudhuvud och Rader** som standard. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Borttagna eller inaktuella funktioner i Project Operations version december 2021

### <a name="collaboration-workspaces"></a>Samarbetesarbetsytor

[Skapa eller länka till en samarbetsyta (Projekt)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Orsak till avfasning/borttagning** | Inaktuell på grund av låg användning. Kunder som använder Project Operations för resurs-/icke-lagerbaserade scenarier kan använda [Samarbete med Office Groups](../project-management/collaboration-groups.md). |
| **Ersatt med en annan funktion?** | No |
| **Produktområden som påverkas** | App  |
| **Distributionsalternativ** | Project Operations för produktionsbaserade/lagerbaserade scenarier |
| **Status** | Inaktuell: Den 1 december 2022 planerar vi att inte längre ha stöd för samarbetsarbetsytor. |
