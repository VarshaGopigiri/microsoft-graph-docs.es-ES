---
title: 'groupLifecyclePolicy: removeGroup'
description: Quita un grupo de una directiva de ciclo de vida.
author: dkershaw10
ms.openlocfilehash: f1fcd8aedc74353d2224b7a670c40b43deb4cd16
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27362660"
---
# <a name="grouplifecyclepolicy-removegroup"></a>groupLifecyclePolicy: removeGroup

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Quita un grupo de una directiva de ciclo de vida.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitido |
|Aplicación |  Directory.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /groupLifecyclePolicies/{id}/removeGroup
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre | Descripción |
|:---------------|:----------|
| Authorization | {token} de portador. Obligatorio. |
| Content-Type  | application/json |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro | Type | Descripción |
|:---------------|:--------|:----------|
|groupId|Guid| El id. del grupo para quitar de la directiva.|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. Si el grupo se quita de la directiva, se devuelve un valor **true** en el cuerpo de la respuesta. En caso contrario, se devuelve un valor **false** en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "ignored",
  "name": "grouplifecyclepolicy_removegroup"
} -->
```http
POST https://graph.microsoft.com/beta/groupLifecyclePolicies/{id}/removeGroup
Content-type: application/json
Content-length: 57

{
  "groupId": "ffffffff-ffff-ffff-ffff-ffffffffffff"
}
```

##### <a name="response"></a>Respuesta
<!-- { "blockType": "ignored" } -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 21

{
  "value": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "groupLifecyclePolicy: removegroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->