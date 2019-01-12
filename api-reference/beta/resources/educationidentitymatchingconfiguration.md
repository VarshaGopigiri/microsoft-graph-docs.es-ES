---
title: tipo de recurso educationIdentityMatchingConfiguration
description: Define la configuración para que coincidan con las identidades de perfil de datos de school. Estas identidades incluyen estudiantes y profesores. En función de esta configuración, los usuarios se actualizará en el directorio.
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: 9ee9f58c2f69882361ee105a1d7531bb5756e165
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977552"
---
## <a name="educationidentitymatchingconfiguration-resource-type"></a>tipo de recurso educationIdentityMatchingConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Define la configuración para que coincidan con las identidades de perfil de datos de school. Estas identidades incluyen estudiantes y profesores. En función de esta configuración, los usuarios se actualizará en el directorio.

> **Nota:** Ningún usuario se crea cuando se selecciona este recurso.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:-|:-|:-|
| **matchingOptions** | colección de [educationIdentityMatchingOptions](educationidentitymatchingoptions.md) | Asignación entre la cuenta de usuario y las opciones para usar para identificar de forma única al usuario que actualice. |

## <a name="json-representation"></a>Representación JSON
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationIdentityMatchingConfiguration"
}-->

```json
{
    "@odata.type": "#microsoft.graph.educationIdentityMatchingConfiguration",
    "matchingOptions": [
        {
            "appliesTo": {"@odata.type": "#microsoft.graph.educationUserRole"},
            "sourcePropertyName": "String",
            "targetPropertyName": "String",
            "targetDomain": "String"
        }
    ]
}
```
