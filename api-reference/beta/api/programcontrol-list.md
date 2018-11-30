---
title: Lista programControls
description: En la característica de revisiones de access Azure AD, incluya todos los objetos de programControl, a través de todos los programas en el inquilino.
ms.openlocfilehash: 7e1dcb197a546e3aa823b731a9e7954803b36c2a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084136"
---
# <a name="list-programcontrols"></a>Lista programControls

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, incluya todos los objetos de [programControl](../resources/programcontrol.md) , a través de todos los programas en el inquilino.
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso                        | Permisos (de menos a más privilegiados)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     | `ProgramControl.Read.All`, `ProgramControl.ReadWrite.All`.  También debe ser el usuario iniciado en un rol de Active directory que le permita leer un programa. |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación                            | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /programControls
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre         | Tipo        | Descripción |
|:-------------|:------------|:------------|
| Authorization | string | Bearer \{token\}. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
No se debe suministrar ningún cuerpo de la solicitud.

## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200, OK` código de respuesta y una matriz de objetos de [programControl](../resources/programcontrol.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "get_programControl"
}-->
```http
GET https://graph.microsoft.com/beta/programControls
```

##### <a name="response"></a>Respuesta
>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.programControl",
    "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{

    "value": [
        {
            "id": "f6abf8ef-a05e-4788-adc9-5af909c400af",
            "controlId": "bc81d51d-be53-4606-a8c2-f90a2beb5f40",
            "programId": "673a7379-9c38-4f01-bd9d-4fda7260b807",
            "controlTypeId": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
            "displayName": "guest user review",
            "status": "Completed",
            "createdDateTime": "2017-09-20T20:18:05.1318394Z"
        }
    ]
}

```

## <a name="see-also"></a>Vea también

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[ProgramControls de lista de un programa](program-listcontrols.md) |     colección de [programControl](../resources/programcontrol.md)|    Obtener una colección de los controles de un programa.|


<!-- {
  "type": "#page.annotation",
  "description": "List programControls",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
