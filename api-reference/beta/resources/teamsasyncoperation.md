---
title: tipo de recurso teamsAsyncOperation
description: 'Una operación asincrónica de Microsoft Teams es una operación que va más allá de la duración de una única solicitud de API. '
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 240e195d01c8fca2b0e92d67d28dcc4b41876e44
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27974521"
---
# <a name="teamsasyncoperation-resource-type"></a>tipo de recurso teamsAsyncOperation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una operación asincrónica de Microsoft Teams es una operación que va más allá de la duración de una única solicitud de API. Estas operaciones son prolongados o demasiado caro para llevar a cabo en el plazo de su solicitud de origen.

Cuando se inicia una operación asincrónica, el método devuelve un código de respuesta aceptados 202. La respuesta contendrá también un encabezado de ubicación, que contiene la ubicación de la teamsAsyncOperation. Compruebe periódicamente el estado de la operación mediante la realización de una solicitud GET en esta ubicación; esperar > 30 segundos entre las comprobaciones.
Cuando la solicitud se completa correctamente, el estado se "correcto" y el targetResourceLocation señalará a los recursos creados o modificados.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo   | Descripción |
|:---------------|:--------|:----------|
|id|string |Identificador único de operación.|
|tipo de operación|[teamsAsyncOperationType](teamsasyncoperationtype.md) |Indica qué tipo de operación que se describen.|
|createdDateTime|DateTimeOffset |Hora de creación de la operación.|
|status|[teamsAsyncOperationStatus](teamsasyncoperationstatus.md)| Estado de la operación.|
|lastActionDateTime|DateTimeOffset |Tiempo de cuándo se actualizó por última vez la operación asincrónica.|
|attemptsCount|Int32|Número de veces que se ha intentado establecer la operación antes de marcarlo correctamente o con errores.|
|targetResourceId|GUID |El identificador del objeto que ha creado o modificado como resultado de esta operación asincrónica, normalmente un [equipo](../resources/team.md).|
|targetResourceLocation|string|La ubicación del objeto que ha creado o modificado como resultado de esta operación asincrónica. Esta dirección URL debe ser se trata como un valor opaco y no se analiza en sus rutas de acceso de componente.|
|error|[operationError](operationerror.md)|Cualquier error que hace que la operación asincrónica se lleve a cabo.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.teamsasyncoperation"
}-->

```json
{
    "id": "string",
    "operationType": "archiveTeam",
    "createdDateTime": "2018-01-01T00:00:00.0000000Z",
    "status": "succeeded",
    "lastActionDateTime": "2018-01-01T00:00:00.0000000Z",
    "attemptsCount": 1,
    "targetResourceId": "fa4aa5a2-a75b-4769-86f4-9e2742a18fda",
    "targetResourceLocation": "/groups('fa4aa5a2-a75b-4769-86f4-9e2742a18fda')/team",
    "error": null
}
```

<!-- uuid: 20fd7863-9545-40d4-ae8f-fee2d115a690
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teams async operation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
