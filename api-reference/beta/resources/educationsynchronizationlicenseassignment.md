---
title: tipo de recurso educationSynchronizationLicenseAssignment
description: Representa la información de licencia para asignar a las cuentas de usuario. El recurso se usará para configurar asignaciones de licencias al crear nuevas cuentas de usuario.
ms.openlocfilehash: a324007dc4d6b5557db407c39d27a640f56ceb55
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089023"
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
