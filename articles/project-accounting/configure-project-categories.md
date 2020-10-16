---
title: Konfigurera projektkategorier
description: I det här ämnet finns information om inställningar för projektkategorier.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895988"
---
# <a name="configure-project-categories"></a>Konfigurera projektkategorier

_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_

Med Project Operations får du robusta funktioner för att kategorisera intäkter och utgifter i projekt. Med kategorier kan du rapportera och analysera projekttransaktioner samt driva bokföring till huvudboken.

I följande diagram illustreras korrelationen mellan transaktionskategorier, delade kategorier och projektkategorier. 

Transaktionskategorier är den grundläggande grupperingen för projekttransaktioner. Inom gruppen finns det en uppsättning delade kategorier som kan delas mellan program och moduler. Projektkategorierna är de mest detaljerade kategorierna för att få ännu mer specifika steg. Projektkategorier är specifika för juridisk person, modul och program.

![Korrelationen mellan transaktionskategorier, delade kategorier och projektkategorier](media/project-categories.png)

## <a name="transaction-categories"></a>Transaktionskategorier

Transaktionskategorier representerar den grundläggande grupperingen av projekttransaktioner och är inte företags- eller transaktionsspecifika. Contoso Robotics använder t.ex. transaktionskategorierna Design, Resor, Installation och Tjänst för att gruppera projekttransaktioner.

Transaktionskategorier definieras i modulen Project Operations. 
1. Gå till **Inställningar** \> **Transaktionskategorier** för att öppna formuläret. 
2. Skapa en ny transaktionskategori genom att välja **Ny** eller genom att välja **Importera från Excel**.

## <a name="shared-categories"></a>Delade kategorier

Dynamics 365 använder de delade kategorierna för att kategorisera utgifter i olika program, till exempel Dynamics 365 Finance Dynamics 365 Supply Chain och Dynamics 365 Project Operations. För varje transaktionskategori som skapas, skapar Project Operations fyra relaterade delade kategorier automatiskt: Timmar, Utgift, Avgifter och Artikel. Du kan granska och justera de delade kategorierna genom att gå till **Projekthantering och redovisning** \> **Inställningar** \> **Kategorier** \> **Delade kategorier**.

## <a name="project-categories"></a>Produktkategorier

Projektkategorierna representerar den mest detaljerade nivån av kategorikonfiguration och måste konfigureras separat och för varje företag av en projektrevisor.

1. Gå till **Projekthantering och redovisning** \> **Inställningar** \> **Kategorier** \> **Projektkategorier**.
2. Välj **Nytt**.
3. Välj **Kategori-ID** för den delade kategori du skapade i föregående avsnitt. Med Project Operations kan du endast använda de delade kategorierna som är associerade med transaktionskategorier.
4. Välj en kategorigrupp.

## <a name="category-groups"></a>Kategorigrupper

Kategorigrupper används för att dela egenskaper, främst bokföringsprofiler, mellan relaterade projektkategorier. Det måste finnas minst en kategorigrupp för varje transaktionstyp och varje projektkategori tilldelas en grupp.

Bokföringsspecifikationen i Project Operations definieras av reglerna för projektkostnads- och intäktsprofiler, projektkategorierna och kategorigrupperna. Du kan ställa in kategorigrupper genom att gå till **Projekthantering och redovisning** \> **Inställningar** \> **Kategorier** \> **Kategorigrupper**.
