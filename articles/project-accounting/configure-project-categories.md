---
title: Konfigurera projektkategorier
description: I den här artikeln finns information om att ställa in projektkategorier.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 440fc712750c07e8426d54e3a1f994f506879e3c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933606"
---
# <a name="configure-project-categories"></a>Konfigurera projektkategorier

_**Gäller:** Project Operations för resurs-/icke-lagerbaserade scenarier_

Med Project Operations får du robusta funktioner för att kategorisera intäkter och utgifter i projekt. Med kategorier kan du rapportera och analysera projekttransaktioner samt driva bokföring till huvudboken.

I följande diagram illustreras korrelationen mellan transaktionskategorier, delade kategorier och projektkategorier. 

Transaktionskategorier är den grundläggande grupperingen för projekttransaktioner. Inom gruppen finns det en uppsättning delade kategorier som kan delas mellan program och moduler. Projektkategorierna är de mest detaljerade kategorierna för att få ännu mer specifika steg. Projektkategorier är specifika för juridisk person, modul och program.

![Korrelationen mellan transaktionskategorier, delade kategorier och projektkategorier.](media/project-categories.png)

## <a name="transaction-categories"></a>Transaktionskategorier

Transaktionskategorier representerar den grundläggande grupperingen av projekttransaktioner och är inte företags- eller transaktionsspecifika. Contoso Robotics använder t.ex. transaktionskategorierna Design, Resor, Installation och Tjänst för att gruppera projekttransaktioner.

Transaktionskategorier definieras i modulen Project Operations. 
1. Gå till **Inställningar** \> **Transaktionskategorier** för att öppna formuläret. 
2. Skapa en ny transaktionskategori genom att välja **Ny** eller genom att välja **Importera från Excel**.

## <a name="shared-categories"></a>Delade kategorier

Dynamics 365 använder konceptet Delade kategorier för att kategorisera utgifter i olika program, till exempel Dynamics 365 Finance, Dynamics 365 Supply Chain och Dynamics 365 Project Operations. För varje transaktionskategori som skapas, skapar Project Operations fyra relaterade delade kategorier automatiskt: Timmar, Utgift, Avgifter och Artikel. Du kan granska och justera de delade kategorierna genom att gå till **Projekthantering och redovisning** \> **Inställningar** \> **Kategorier** \> **Delade kategorier**.

## <a name="project-categories"></a>Produktkategorier

Projektkategorierna representerar den mest detaljerade nivån av kategorikonfiguration och måste konfigureras separat och för varje företag av en projektrevisor.

1. Gå till **Projekthantering och redovisning** \> **Inställningar** \> **Kategorier** \> **Projektkategorier**.
2. Välj **Nytt**.
3. Välj **Kategori-ID** för den delade kategori du skapade i föregående avsnitt. Med Project Operations kan du endast använda de delade kategorierna som är associerade med transaktionskategorier.
4. Välj en kategorigrupp.

## <a name="category-groups"></a>Kategorigrupper

Kategorigrupper används för att dela egenskaper, främst bokföringsprofiler, mellan relaterade projektkategorier. Det måste finnas minst en kategorigrupp för varje transaktionstyp och varje projektkategori tilldelas en grupp.

Bokföringsspecifikationen i Project Operations definieras av reglerna för projektkostnads- och intäktsprofiler, projektkategorierna och kategorigrupperna. Du kan ställa in kategorigrupper genom att gå till **Projekthantering och redovisning** \> **Inställningar** \> **Kategorier** \> **Kategorigrupper**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]