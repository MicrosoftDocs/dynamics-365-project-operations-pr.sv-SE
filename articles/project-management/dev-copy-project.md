---
title: Ta fram projektmallar med Kopiera projekt
description: I det här ämnet finns information om hur du skapar projektmallar med den anpassade åtgärden Kopiera projekt.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642430"
---
# <a name="develop-project-templates-with-copy-project"></a>Ta fram projektmallar med Kopiera projekt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations stöder möjligheten att kopiera ett projekt och återställa eventuella tilldelningar till de generiska resurser som representerar rollen. Kunderna kan använda den här funktionen för att skapa grundläggande projektmallar.

När du väljer **Kopiera projekt** uppdateras statusen för målprojektet. Använd **Statusorsak** för att bestämma när kopieringsåtgärden är klar. Om du väljer **Kopiera projekt** uppdateras även projektets startdatum till det aktuella startdatumet om inget måldatum hittas i entiteten för målprojektet.

## <a name="copy-project-custom-action"></a>Den anpassade åtgärden Kopiera projekt 

### <a name="name"></a>Namn 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Indataparametrar
Det finns tre indataparametrar:

| Parameter          | Typ   | Värden                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | Sträng | **{"removeNamedResources":true}** eller **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Entitetsreferens | Källprojekt |
| Mål             | Entitetsreferens | Målprojekt |


- **{"clearTeamsAndAssignments":true}**: Tre standardbeteenden för Project for the Web och tar bort alla tilldelningar och gruppmedlemmar.
- **{"removeNamedResources":true}** Standardbeteendet för Project Operations och återställer tilldelningar till generiska resurser.

Mer standarder vad gäller åtgärder finns i [Använd webb-API-åtgärder](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Specificera vilka fält som ska kopieras 
När en åtgärd anropas tittar **Kopiera projekt** på projektvyn **Kopiera projektkolumner** och avgör vilka fält som ska kopieras när projektet kopieras.
