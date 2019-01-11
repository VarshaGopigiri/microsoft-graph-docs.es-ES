---
title: tipo de recurso educationSynchronizationLicenseAssignment
description: Representa la información de licencia para asignar a las cuentas de usuario. El recurso se usará para configurar asignaciones de licencias al crear nuevas cuentas de usuario.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: 9100ba799c8981d5defdd74d6346a66859b2d53e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27804911"
---
# <a name="educationsynchronizationlicenseassignment-resource-type"></a>tipo de recurso educationSynchronizationLicenseAssignment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la información de licencia para asignar a las cuentas de usuario. El recurso se usará para configurar asignaciones de licencias al crear nuevas cuentas de usuario.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Description |
|:-|:-|:-|
| **appliesTo** | string | El tipo de función de usuario para asignar a la licencia. Los valores posibles son: `student` y `teacher`.         |
| **skuIds** | colección de cadenas |  Representa los identificadores SKU de las licencias para asignar.        |

## <a name="json-representation"></a>Representación JSON
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationSynchronizationLicenseAssignment"
}-->

```json
{
    "appliesTo": {"@odata.type": "#microsoft.graph.educationUserRole"},
    "skuIds": ["String"]
}
```
