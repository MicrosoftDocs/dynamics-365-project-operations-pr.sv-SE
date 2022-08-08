---
title: Mobilapp för projekt tidsrapport
description: Denna artikel innehåller information om mobilappen Microsoft Dynamics 365 Project Timesheet. Mobilappen tidsrapport låter användarna skicka och godkänna tidsrapporter för projekt på deras mobila enhet.
author: abruer
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110997"
---
# <a name="project-timesheet-mobile-application"></a>Mobilapp för projekt tidsrapport

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Översikt

Mobilappen Microsoft Dynamics 365 Project Timesheet låter användarna skicka och godkänna tidsrapporter för projekt på deras mobila enhet (iPhone eller Android). Denna mobilapp hämtar funktionerna för tidrapport och projekthantering och redovisningsområde för Dynamics 365 Finance. Den hjälper till att förbättra användarnas produktivitet och effektivitet, och hjälper dig att snabbt och effektivt inträda och godkänna projekt tidrapporter.

## <a name="download-and-install-the-mobile-app"></a>Ladda ned och installera en mobilapp

Hämta och installera Microsoft Dynamics 365 Project Timesheet mobilappen för Android eller iPhone från enhetens appbutik.

## <a name="enable-the-app"></a>Aktivera appen 

I Finance måste mobilappen för projekt tidrapport vara aktiverad. För att aktivera funktionaliteten, gå till **Projektledning och redovisningsparametrar \> Tidsrapport** och välj **Aktivera Microsoft Dynamics 365 Project Timesheet**-parameter.

### <a name="resolve-sign-in-issues"></a>Lösa inloggningsproblem

**Problem:** Under inloggningen till mobilappen för projekt tidrapport får användarna ett felmeddelande om att de "inte kan komma åt programmet '2bc50526-cdc3-4e36-a970-c284c34cbd6e' i klientorganisationen."

**Problem:** Under inloggningen till mobilappen för projekt tidrapport får användarna ett felmeddelande som ser ut som ett av följande exempel:

- "AADSTS50020: Användarkonto '[användarnamn]' från identitetsleverantören 'https://sts.windows.net/[app id]' finns inte i klientorganisationens [klientorganisations-ID] och kan inte komma åt programmet [app-id] i den klientorganisationen."
- "Valt användarkonto finns inte i klientorganisationen [klientorganisations-id] och kan inte få åtkomst till programmet [app id] i den klientorganisationen".

**Förklaring:** Dessa problem beror på en ändring som gjordes i Azure Active Directory (Azure AD) i maj 2022 och som är relaterad till externa användare. Eftersom den här ändringen inte har gjorts för att apparna för ekonomi och drift kan den påverka kunderna på alla versioner av plattformen eller programmet.

**Korrigering:** Alla externa användare måste bjudas in till klientorganisationen via Azure AD. Mer information finns i [Bjuda in användare med hjälp av Azure Active Directory B2B-samarbete](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration).

## <a name="sign-in-to-the-app"></a>Logga in på appen

1.  Starta appen på din mobila enhet.

2.  Fyll i Finance URL.

3.  Första gången du loggar in ombeds du ange ditt användarnamn och lösenord. Ange dina autentiseringsuppgifter.

4. Du kommer att vara inloggad på standardföretaget.

## <a name="submit-a-project-timesheet"></a>Skicka ett projekttidrapport

Du kan skapa och skicka en projekttidrapport i appen. Du kan basera en ny tidrapport på information från en tidigare tidrapport, sparade rader eller projekttilldelningar. Om du är utsedd till ombud kan du även ange en tidrapport för en annan arbetare. Om du vill skapa en tidrapport som ombud väljer du **meny**-knappen och väljer sedan ett resursnamn.

På tidrapport sidan skapas en ny tidrapport för tidrapport perioden utifrån det aktuella datumet. Arbetsveckan är det namn som visas. Om tidrapport perioden omfattar flera veckor kan du välja en annan arbetsvecka från flikarna arbetsvecka.
Om det finns en tidrapport för det innevarande datumet visas den. Om du behöver skapa en ny tidrapport i en annan tidrapport period markerar du **meny**-knappen och väljer sedan **ny tidrapport**.

Du kan ange projektinformation genom att klicka på åtgärden **Lägg till tid** eller **Kopiera tid från**. Med åtgärden **Kopiera tid från** kopieras projektrad information men inte från timmarna. Menyn **Kopiera tid** innehåller följande alternativ:

- **Kopiera från befintlig tid rapport** – Kopiera tidrapport rader från en befintlig tidrapport.

- **Kopiera från favorit** – skapa nya tidrapport rader genom att använda tidrapport inställningarna som du valde som favoriter.

- **Kopiera från tilldelning** – skapa nya tidrapport rader från tilldelade projekt.

Projektinformationen som visas beror på de parametrar för mobilparametrar som du angav på sidan **Projektledning och redovisningsparametrar**.

I fältet **juridiska personen** som du utförde projektarbetet för i fältet juridisk person. Fältet **Juridisk person** är endast tillgängligt om stöd för koncernintern tidrapport har aktiverats för den juridiska personen.

Markera den kund som är associerad med projektet för tidrapporten. För den första frisläppningen i Android stöds inte inmatning efter kund eftersom du först måste välja projektet. Om du först markerade projektet fältet **Kund** fylls kund fältet i automatiskt.

I fältet **Projekt** välj det projekt som du anger tid för. Fältet **Kund** fylls i automatiskt.

Med sökningarna för kund och projekt kan du aktivera sökning i både kunder och projekt.

Välj information i fältet **kategori**, **aktivitet**, **radegenskap**, **momsgrupp** och **artikelmomsgrupp** efter behov. Fälten kan åsidosättas.

Värdet **Radegenskap** kommer att ställas in till ett standardvärde baserat på projektledning och redovisningsparametrar. När parametrarna projekt/kategori och kategori/resurs har aktiveras ändras värdet **radegenskap** till det standardvärde som du har angett för valideringen. När projekt/kategori och kategori/resursparametrar inte är aktiverade värdet **Radegenskap** egenskapen radegenskap i fält **Aktivera standardradegenskap** sidan **Projektledning och redovisningsparametrar**. Värdet **Line egenskapen** kan åsidosättas.

Välj en dag om du vill lägga till tid. Ange antalet timmar som du har arbetat varje dag.

Om du vill lägga till kommentarer om de timmar du skriver in klickar du på **lägg till kommentarer** och anger kommentarer för en intern publik, kundpublik eller båda.
Interna kommentarer kan visas av projektledare. Kundkommentarer ingår i fakturor.

Om du vill spara raden som en favorit markerar du kryssrutan och klickar på **Spara som favorit**.

Stöd för ekonomisk dimension och bifogade filer tillhandahålls inte i mobilapp.

Fortsätt att lägga till de rader som behövs för att slutföra tidrapporten.

Klicka på **Skicka** för att skicka tid rapporten till godkännande arbetsflödet.

## <a name="review-timesheets"></a>Granska tidrapporter

En lista över de tidrapporter som måste granskas visas på menyn. Det här alternativet är bara tillgängligt om du har angetts som godkännande för arbetsflödet. Både rubrik och rad godkännande stöds. Med godkännande av radnivå kan du markera en eller flera rader för godkännande. När du har granskat tid rapport informationen klickar du på **godkänn**, **delegera** eller **återgå** för att fortsätta arbetsflödet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
