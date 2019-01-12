---
title: Actualizar el grupo de enrutamiento de audio
description: Modificar orígenes y receptores de un audioRoutingGroup.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: ca6e77e71abb7d7a934944ce7fd4de10d79e1a94
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956909"
---
# <a name="update-audio-routing-group"></a>Actualizar el grupo de enrutamiento de audio

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Modificar orígenes y receptores de un [audioRoutingGroup](../resources/audioroutinggroup.md).

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

| Tipo de permiso | Permisos (de menos a más privilegiados)                |
| :-------------- | :--------------------------------------------------------- |
| Delegado (cuenta profesional o educativa)     | No se admite                       |
| Delegado (cuenta personal de Microsoft) | No se admite                       |
| Aplicación     | Calls.JoinGroupCalls.All, Calls.InitiateGroupCalls.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /app/calls/{id}/audioRoutingGroups/{id}
PATCH /applications/{id}/calls/{id}/audioRoutingGroups/{id}
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre          | Descripción               |
|:--------------|:--------------------------|
| Authorization | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.

| Propiedad       | Tipo    |Descripción|
|:---------------|:--------|:----------|
| receptores de | Colección String | Los participantes de destino en la audioRoutingGroup. |
| routingMode | String | Los valores posibles son: `oneToOne` y `multicast`. |
| orígenes | Colección String | El participante de origen en el audioRoutingGroup. |

## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [audioRoutingGroup](../resources/audioroutinggroup.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud
En el ejemplo siguiente se muestra la solicitud.

<!-- {
  "blockType": "request",
  "name": "update-audioRoutingGroup"
}-->
```http
PATCH https://graph.microsoft.com/beta/app/calls/{id}/audioRoutingGroups/{id}
Content-Type: application/json
Content-Length: 233

{
  "id": "oneToOne",
  "routingMode": "oneToOne",
  "sources": [
    "632899f8-2ea1-4604-8413-27bd2892079f"
  ],
  "receivers": [
    "550fae72-d251-43ec-868c-373732c2704f",
    "72f988bf-86f1-41af-91ab-2d7cd011db47"
  ]
}
```
##### <a name="response"></a>Respuesta

> **Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.audioRoutingGroup"
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 233

{
  "id": "oneToOne",
  "routingMode": "oneToOne",
  "sources": [
    "632899f8-2ea1-4604-8413-27bd2892079f"
  ],
  "receivers": [
    "550fae72-d251-43ec-868c-373732c2704f",
    "72f988bf-86f1-41af-91ab-2d7cd011db47"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update audioRoutingGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
