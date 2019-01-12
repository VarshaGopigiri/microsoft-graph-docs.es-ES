---
title: tipo de recurso educationIdentityDomain
description: 'Representa la asignación entre un tipo de usuario de formación y el dominio al que pertenece la cuenta de usuario. El recurso de dominio forma parte de la configuración de creación de identidad. '
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: 280ae1a65e0c14e7960d316cc21154e405f2ee0d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982032"
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
