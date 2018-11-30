---
author: psampath
ms.author: psampath
ms.date: 06/20/2018
title: StoragePlanInformation
ms.openlocfilehash: 07552f405ec8c5d6ae8345a8238cd8aec3763b11
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088151"
---
# <a name="storageplaninformation-resource-type"></a>tipo de recurso storagePlanInformation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **storagePlanInformation** proporciona información acerca de los planes de cuota de almacenamiento de información de la unidad.

### <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
   "@odata.type": "microsoft.graph.storagePlanInformation",
} -->

```json
{
  "upgradeAvailable": true
}

```
## <a name="properties"></a>Propiedades

| Nombre de propiedad     | Tipo      | Descripción                                                             |
|:------------------|:----------|:----------------------------------------------------------------------- |
| upgradeAvailable  | Booleano   | Indica si hay planes de cuota de almacenamiento superiores. Solo lectura. |


<!-- {
  "type": "#page.annotation",
  "description": "storagePlanInformation resource contains information about storage quota plans that make up the drive's storage space quota.",
  "keywords": "quota,plans,upgradeAvailable",
  "section": "documentation",
  "tocPath": "Resources/StoragePlanInformation"
} -->

