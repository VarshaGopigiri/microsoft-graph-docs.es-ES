---
title: tipo de recurso educationIdentityDomain
description: 'Representa la asignación entre un tipo de usuario de formación y el dominio al que pertenece la cuenta de usuario. El recurso de dominio forma parte de la configuración de creación de identidad. '
localization_priority: Normal
ms.openlocfilehash: 5675499aca010f90deeb517210065ac4802d66b5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27807752"
---
# <a name="educationidentitydomain-resource-type"></a>tipo de recurso educationIdentityDomain

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la asignación entre un tipo de usuario de formación y el dominio al que pertenece la cuenta de usuario. El recurso de dominio forma parte de la [configuración de creación de identidad](educationidentitycreationconfiguration.md). 

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Description |
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
