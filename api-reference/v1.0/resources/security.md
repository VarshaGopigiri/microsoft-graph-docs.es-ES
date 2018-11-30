---
title: tipo de recurso de seguridad
description: El recurso de seguridad es el punto de entrada para el modelo de objetos de seguridad. Devuelve un recurso de seguridad singleton. No contiene todas las propiedades utilizables.
ms.openlocfilehash: ddf00e46135733ef18c18918c0c365134138671f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029528"
---
# <a name="security-resource-type"></a>tipo de recurso de seguridad

El recurso de seguridad es el punto de entrada para el modelo de objetos de seguridad. Devuelve un recurso de seguridad singleton. No contiene todas las propiedades utilizables.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto | Descripción |
|:-------------|:------------|:------------|
| [List alerts](../api/alert-list.md) | colección de [alerta](alert.md) | Obtener una colección de objetos de alerta. |
| [obtener alertas](../api/alert-get.md) | colección de [alerta](alert.md) | Obtener un objeto de alerta. |
| [Actualización de alertas](../api/alert-update.md) | colección de [alerta](alert.md) | Obtener un objeto de alerta. |

## <a name="properties"></a>Propiedades
Ninguno

## <a name="relationships"></a>Relaciones
| Relación | Tipo        | Descripción |
|:-------------|:------------|:------------|
|alerts|colección de [alerta](alert.md)| Solo lectura. Admite valores NULL.|


## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.security"
}-->

```json
{
}
```

## <a name="example"></a>Ejemplo

El recurso de **seguridad** está disponible en la raíz del gráfico.

<!--{
  "blockType": "request"
}-->
```http
GET https://graph.microsoft.com/v1.0/security
```

<!--{
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.security"
}-->
```json
HTTP/1.1 200 OK
Content-type: application/json

{
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "security resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->