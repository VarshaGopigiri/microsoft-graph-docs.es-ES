---
title: ProgramControls de lista de un programa
description: En la característica de revisiones de access Azure AD, enumera todos los objetos de programControl, vinculados a un programa en particular.
localization_priority: Normal
ms.openlocfilehash: 8895634b098474cdbeab695cbe730a1e2fd02e2c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809341"
---
# <a name="list-programcontrols-of-a-program"></a>ProgramControls de lista de un programa

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, enumera todos los objetos de [programControl](../resources/programcontrol.md) , vinculados a un programa en particular.
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
GET /programs('{programId}')/controls
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre         | Tipo        | Descripción |
|:-------------|:------------|:------------|
| Autorización | string | Bearer \{token\}. Necesario. |

## <a name="request-body"></a>Cuerpo de la solicitud
No se debe suministrar ningún cuerpo de la solicitud.

## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200, OK` código de respuesta y una matriz de objetos de [programControl](../resources/programcontrol.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "get_programControl_from_program"
}-->
```http
GET https://graph.microsoft.com/beta/programs('673a7379-9c38-4f01-bd9d-4fda7260b807')/controls
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
            "id": "bd68f301-e44b-4ad1-ba6d-a07314ed2e79",
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


<!-- {
  "type": "#page.annotation",
  "description": "List programControls of a program",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
