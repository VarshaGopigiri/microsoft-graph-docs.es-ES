---
title: tipo de recurso educationSynchronizationLicenseAssignment
description: Representa la información de licencia para asignar a las cuentas de usuario. El recurso se usará para configurar asignaciones de licencias al crear nuevas cuentas de usuario.
author: mmast-msft
ms.openlocfilehash: 478d939c8f4c6a0bc1971d66afc4ecc7ae640e39
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344397"
---
# <a name="educationsynchronizationlicenseassignment-resource-type"></a>tipo de recurso educationSynchronizationLicenseAssignment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la información de licencia para asignar a las cuentas de usuario. El recurso se usará para configurar asignaciones de licencias al crear nuevas cuentas de usuario.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
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
