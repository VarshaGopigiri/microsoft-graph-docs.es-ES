---
title: Tipo de recurso domainState
description: Representa el estado de las operaciones asincrónicas programadas en un dominio.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: cee5ef9e0d0f4a5ada0d9117f755c407d081461d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27963104"
---
# <a name="domainstate-resource-type"></a>Tipo de recurso domainState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa el estado de las operaciones asincrónicas programadas en un dominio.

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo | Descripción |
|:---------------|:--------|:----------|
| lastActionDateTime | DateTimeOffset | Marca de tiempo de la última actividad. El valor se actualiza cuando se programa una operación, se inicia la tarea asincrónica y cuando termina la operación. |
| operación | Cadena | Tipo de operación asincrónica. Los valores pueden ser *ForceDelete* o *Verification* |
| status | Cadena | Estado actual de la operación. <br> *Programada*: La operación se ha programado, pero no se ha iniciado. <br> *En curso*: La tarea se ha iniciado y está en curso. <br> *Error*: Se ha producido un error en la operación. |

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainState"
}-->

```json
{
  "lastActionDateTime": "String (timestamp)",
  "operation": "String",
  "status": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
