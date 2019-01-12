---
title: 'educationAssignment: getResourcesFolderUrl'
description: 'Esta función devuelve la dirección URL de OneDrive donde se deben cargar todos los recursos basados en archivos (Word, Excel y así sucesivamente).  '
localization_priority: Normal
author: dipakboyed
ms.prod: education
ms.openlocfilehash: f46bbf9c47ca9cd4396883d106599f94374aad4a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984461"
---
# <a name="educationassignment-getresourcesfolderurl"></a>educationAssignment: getResourcesFolderUrl

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Esta función devuelve la dirección URL de OneDrive donde se deben cargar todos los recursos basados en archivos (Word, Excel y así sucesivamente).  
Tenga en cuenta que los archivos deben estar ubicados en esta carpeta con el fin de agregarse como recursos. Sólo un profesor en la clase puede determinar qué archivos para cargar. 

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) |  EduAssignments.ReadBasic, EduAssignments.Read  |
|Delegado (cuenta personal de Microsoft) |  No admitida.  |
|Aplicación | No admitida. | 

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes/{id}/assignments/{id}/getResourcesFolderUrl

```
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.
## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 Ok`. El cuerpo contiene la dirección URL de OneDrive de una carpeta en la que se va a colocar todos los recursos basados en el archivo.

## <a name="example"></a>Ejemplo
En el siguiente ejemplo se muestra cómo llamar a esta API.
##### <a name="request"></a>Solicitud
El siguiente es un ejemplo de una solicitud.
<!-- {
  "blockType": "request",
  "name": "educationassignment_publish"
}-->
```http
POST https://graph.microsoft.com/beta/education/classes/11012/assignments/19002/getResourcesFolderUrl
```

##### <a name="response"></a>Respuesta
El siguiente es un ejemplo de una respuesta. 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationAssignment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 279

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Edm.String",
    "value": "https://graph.microsoft.com/v1.0/drives/b!8-QjN2tsv0WyGnTv7vOvnQkmGHbbeMNLqYKONmHLVnvCVmBYIGpeT456457AdW9f/items/017NJZI25NOB5XZNLABF7646XAMDZTQQ6T"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationAssignment: publish",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
