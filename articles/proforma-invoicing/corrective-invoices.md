---
title: Det här avsnittet innehåller information om korrigerade fakturor.
description: I det här ämnet finns information om korrigerade fakturor.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122410"
---
# <a name="corrected-invoices"></a><span data-ttu-id="97d1a-103">Korrigerande fakturor</span><span class="sxs-lookup"><span data-stu-id="97d1a-103">Corrected invoices</span></span>

<span data-ttu-id="97d1a-104">_**Gäller:** Project Operations för resursscenarier/icke lagerbaserade scenarier_</span><span class="sxs-lookup"><span data-stu-id="97d1a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="97d1a-105">Bekräftade fakturor kan redigeras.</span><span class="sxs-lookup"><span data-stu-id="97d1a-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="97d1a-106">När du redigerar en bekräftad faktura skapas ett utkast av den korrigerade fakturan.</span><span class="sxs-lookup"><span data-stu-id="97d1a-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="97d1a-107">Eftersom det är en förutsättning att du vill återföra alla transaktioner och kvantiteter från den ursprungliga fakturan, inkluderar den korrigerade fakturan alla transaktioner från den ursprungliga fakturan och alla kvantiteter på den är noll (0).</span><span class="sxs-lookup"><span data-stu-id="97d1a-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="97d1a-108">När transaktioner inte kräver korrigering kan du ta bort dem från utkastfakturan.</span><span class="sxs-lookup"><span data-stu-id="97d1a-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="97d1a-109">Om du vill återföra eller returnera en delkvantitet kan du redigera fältet antal på raddetaljen.</span><span class="sxs-lookup"><span data-stu-id="97d1a-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="97d1a-110">Om du öppnar fakturaradinformationen visas ursprungligt fakturaantal.</span><span class="sxs-lookup"><span data-stu-id="97d1a-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="97d1a-111">Du kan sedan redigera aktuellt fakturerat antal så att det är mindre än eller lika med den ursprungliga fakturan.</span><span class="sxs-lookup"><span data-stu-id="97d1a-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="97d1a-112">När du bekräftar en rättningsfaktura återförs den ursprungliga fakturerade faktiska försäljningen och en ny fakturerad faktisk försäljning skapas.</span><span class="sxs-lookup"><span data-stu-id="97d1a-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="97d1a-113">Om antalet minskas kommer differensen att skapa en ny fakturerad faktiskt försäljning.</span><span class="sxs-lookup"><span data-stu-id="97d1a-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="97d1a-114">Om t.ex. den ursprungliga fakturerade försäljningen var åtta timmar och detaljerna för den korrigerade fakturaraden har en mindre mängd på sex timmar, återförs den ursprungliga faktureringsförsäljningsraden och två nya faktiska värden skapas:</span><span class="sxs-lookup"><span data-stu-id="97d1a-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="97d1a-115">En fakturerad faktisk försäljning som faktiskt innehåller sex timmar.</span><span class="sxs-lookup"><span data-stu-id="97d1a-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="97d1a-116">En ofakturerad faktisk försäljning för de återstående två timmarna.</span><span class="sxs-lookup"><span data-stu-id="97d1a-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="97d1a-117">Denna transaktion kan antingen faktureras senare eller vara markerad som icke debiterbar, beroende på förhandlingarna med kunden.</span><span class="sxs-lookup"><span data-stu-id="97d1a-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
