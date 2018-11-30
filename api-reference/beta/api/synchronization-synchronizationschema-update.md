---
title: Actualizar synchronizationSchema
description: Actualizar el esquema de sincronización para un determinado trabajo o una plantilla. Este método reemplaza totalmente el esquema actual con el proporcionado en la solicitud. Para actualizar el esquema de una plantilla, realizar la llamada en el objeto application. Debe ser el propietario de la aplicación.
ms.openlocfilehash: 18ad164f0f1860ce954a9d4e1170f71e47f513b5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088678"
---
# <a name="update-synchronizationschema"></a>Actualizar synchronizationSchema

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Actualizar el esquema de sincronización para un determinado trabajo o una plantilla. Este método reemplaza totalmente el esquema actual con el proporcionado en la solicitud. Para actualizar el esquema de una plantilla, realizar la llamada en el objeto application. Debe ser el propietario de la aplicación.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso                        | Permisos (de menos a más privilegiados)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     |Directory.ReadWrite.All  |
|Delegado (cuenta personal de Microsoft) |No admitida.|
|Aplicación                            |No admitida.| 

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PUT /servicePrincipals/{id}/synchronization/jobs/{jobId}/schema
PUT /applications/{id}/synchronization/templates/{templateId}/schema
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre           | Tipo    | Descripción|
|:---------------|:--------|:-----------|
| Authorization  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione el objeto [synchronizationSchema](../resources/synchronization-synchronizationschema.md) que va a reemplazar el esquema existente con.

## <a name="response"></a>Respuesta

Si se realiza correctamente, devuelve un `204 No Content` código de respuesta. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud
El siguiente es un ejemplo de una solicitud.

>**Nota:** El objeto de solicitud que se muestra aquí es más cortos para mejorar la legibilidad. Proporcionar todas las propiedades en una llamada real.
<!-- {
  "blockType": "request",
  "name": "update_synchronizationschema"
}-->
```http
PUT https://graph.microsoft.com/beta/servicePrincipals/{id}/synchronization/jobs/{jobId}/schema

{
    "directories": [
        {
            "name": "Azure Active Directory",
            "objects": [
                {
                    "name": "User",
                    "attributes": [
                        {
                            "name": "userPrincipalName",
                            "type": "string"
                        }
                    ]
                },
            ]
        },
        {
            "name": "Salesforce",
        }
    ],
    "synchronizationRules":[
        {
            "name": "USER_TO_USER",
            "sourceDirectoryName": "Azure Active Directory",
            "targetDirectoryName": "Salesforce",
            "objectMappings": [
                {
                    "sourceObjectName": "User",
                    "targetObjectName": "User",
                    "attributeMappings": [
                        {
                            "source": {},
                            "targetAttributeName": "userName"
                        },
                    ]
                },
            ]
        },
    ]
}

```

##### <a name="response"></a>Respuesta
El siguiente es un ejemplo de una respuesta.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.synchronizationSchema"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update synchronizationschema",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->