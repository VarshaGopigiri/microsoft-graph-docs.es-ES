---
title: 'notebook: getRecentNotebooks'
description: Obtener una lista de instancias de recentNotebook a las que ha accedido el usuario que inició sesión.
ms.openlocfilehash: dd273197ecfc417bd385ff6d769f96efd3972362
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085930"
---
# <a name="notebook-getrecentnotebooks"></a>notebook: getRecentNotebooks

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Obtener una lista de instancias de [recentNotebook](../resources/recentnotebook.md) a las que ha accedido el usuario que inició sesión.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All|
|Delegado (cuenta personal de Microsoft) | Notes.Create, Notes.Read, Notes.ReadWrite |
|Aplicación | Notes.Read.All, Notes.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks/getRecentNotebooks(includePersonalNotebooks=includePersonalNotebooks-value)
GET /users/<id | userPrincipalName>/onenote/notebooks/getRecentNotebooks(includePersonalNotebooks=includePersonalNotebooks-value)
```

El `<id | userPrincipalName>` del usuario debe coincidir con el usuario codificado en el token de autorización que se usa para realizar la solicitud.

## <a name="function-parameters"></a>Parámetros de función

| Parámetro    | Tipo   |Descripción|
|:---------------|:--------|:----------|
|includePersonalNotebooks|Boolean|Incluir los blocs de notas que pertenecen al usuario. Se establece en `true` para incluir los blocs de notas que pertenecen al usuario; en caso contrario, se establece en `false`. Si no incluye el parámetro `includePersonalNotebooks`, la solicitud devolverá una respuesta de error `400`.|

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Descripción|
|:---------------|:----------|
| Autorización  | Portador {código}|

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta
Una respuesta correcta devuelve un valor `200 OK` que contiene una colección JSON de **recentNotebooks**.

## <a name="example"></a>Ejemplo
En el siguiente ejemplo se muestra cómo llamar a esta API.

##### <a name="request"></a>Solicitud
En el ejemplo siguiente se muestra la solicitud.
<!-- { "blockType": "request", "name": "recent_notebooks", "scopes": "notes.read" } -->
```http
GET https://graph.microsoft.com/v1.0/onenote/notebooks/getrecentnotebooks(includePersonalNotebooks=true)
```

##### <a name="response"></a>Respuesta
En el ejemplo siguiente se muestra la respuesta.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.notebook",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-Length: 1110

{
  "value":[
    {
      "name":"Personal Notebook","lastAccessedTime":"timestamp","links":{
        "oneNoteClientUrl":{
          "href":"onenote:href-value"
        },"oneNoteWebUrl":{
          "href":"href-value"
        }
      },"sourceService":"OneDrive"
    },{
      "name":"Team Shared Notebook","lastAccessedTime":"timestamp","links":{
        "oneNoteClientUrl":{
          "href":"onenote:href-value"
        },"oneNoteWebUrl":{
          "href":"href-value"
        }
      },"sourceService":"OneDriveForBusiness"
    }
  ]
}
```
