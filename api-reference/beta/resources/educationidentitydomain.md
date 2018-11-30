---
title: tipo de recurso educationIdentityDomain
description: 'Representa la asignación entre un tipo de usuario de formación y el dominio al que pertenece la cuenta de usuario. El recurso de dominio forma parte de la configuración de creación de identidad. '
ms.openlocfilehash: 8298e1eb38ae70f982719ee3a7d6588cd181bdd8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088351"
---
# <a name="educationidentitydomain-resource-type"></a>tipo de recurso educationIdentityDomain

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la asignación entre un tipo de usuario de formación y el dominio al que pertenece la cuenta de usuario. El recurso de dominio forma parte de la [configuración de creación de identidad](educationidentitycreationconfiguration.md). 

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:-|:-|:-|
| **appliesTo** | string |  El tipo de función de usuario para asignar a la licencia. Los valores posibles son: `student` y `teacher`.      |
| **name** | string |  Representa el dominio para la cuenta de usuario.         |

## <a name="json-representation"></a>Representación JSON
<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "#microsoft.graph.educationIdentityDomain"
}-->

```json
{
    "appliesTo": {"@odata.type": "#microsoft.graph.educationUserRole"},
    "name": "String"
}
```
