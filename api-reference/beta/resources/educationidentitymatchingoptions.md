---
title: tipo de recurso educationIdentityMatchingOptions
description: Proporciona una asignación entre una propiedad de origen y una propiedad de destino para que coincidan con las cuentas de usuario. La propiedad source debe existir en el origen de datos. La propiedad de destino debe ser una propiedad válida en Azure Active Directory (AD Azure).
ms.openlocfilehash: 2cabb255648f4089d437912a97bb7d29ff286779
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088550"
---
# <a name="educationidentitymatchingoptions-resource-type"></a>tipo de recurso educationIdentityMatchingOptions

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Proporciona una asignación entre una propiedad de origen y una propiedad de destino para que coincidan con las cuentas de usuario. La propiedad source debe existir en el origen de datos. La propiedad de destino debe ser una propiedad válida en Azure Active Directory (AD Azure).

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:-|:-|:-|
| **appliesTo** | string |  El tipo de función de usuario para asignar a la licencia. Los valores posibles son: `student` y `teacher`.      |
| **sourcePropertyName** | string |  El nombre de la propiedad source, que debe ser un nombre de campo en el origen de datos. Esta propiedad distingue mayúsculas de minúsculas.        |
| **targetPropertyName** | string |  El nombre de la propiedad de destino, que debe ser una propiedad válida en Azure AD. Esta propiedad distingue mayúsculas de minúsculas.     |
| **targetDomain** | string |  El dominio en sufijo con la propiedad de origen para que coincidan en el destino. Si se proporciona como null, la propiedad source se usará para hacer coincidir con la propiedad de destino.        |

## <a name="json-representation"></a>Representación JSON
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationIdentityMatchingOptions"
}-->

```json
{
    "appliesTo": {"@odata.type": "#microsoft.graph.educationUserRole"},
    "sourcePropertyName": "String",
    "targetPropertyName": "String",
    "targetDomain": "String"
}
```
