---
title: Ta fram projektmallar med Kopiera projekt
description: I det här ämnet finns information om hur du skapar projektmallar med den anpassade åtgärden Kopiera projekt.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085480"
---
# <a name="develop-project-templates-with-copy-project"></a>Ta fram projektmallar med Kopiera projekt

_**Gäller:** Project Operations för resurs- och icke lagerbaserade scenarier, lite distribution – handlar för att proforma-fakturering_

Med Dynamics 365 Project Operations kan du kopiera ett projekt och återställa alla tilldelningar till de allmänna resurser som representerar rollen. Kunderna kan använda den här funktionen för att skapa grundläggande projektmallar.

När du väljer **Kopiera projekt** uppdateras statusen för målprojektet. Använd **Statusorsak** för att bestämma när kopieringsåtgärden är klar. Om du väljer **Kopiera projekt** uppdateras även projektets startdatum till det aktuella startdatumet om inget måldatum hittas i entiteten för målprojektet.

## <a name="copy-project-custom-action"></a>Den anpassade åtgärden Kopiera projekt 

### <a name="name"></a>Namn 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Indataparametrar
Det finns tre indataparametrar:

| Parameter          | Type   | Värden                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** eller **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Entitetsreferens | Källprojekt |
| Mål             | Entitetsreferens | Målprojekt |


- **{"clearTeamsAndAssignments":true}** : Tre standardbeteenden för Project for the Web och tar bort alla tilldelningar och teammedlemmar.
- **{"removeNamedResources":true}** Standardbeteendet för Project Operations och återför tilldelningar till generiska resurser.

Mer standarder vad gäller åtgärder finns i [Använd webb-API-åtgärder](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Specificera vilka fält som ska kopieras 
När en åtgärd anropas tittar **Kopiera projekt** på projektvyn **Kopiera projektkolumner** och avgör vilka fält som ska kopieras när projektet kopieras.
