---
title: Lista usada
description: Insight calculado que devuelve la lista de archivos que se utiliza con un usuario.
author: simonhult
ms.openlocfilehash: 17f47e4e82d5cb038438b5d164c76371221de11a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27342500"
---
# <a name="list-used"></a>Lista usada

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Insight calculado que devuelve la lista de archivos que se utiliza con un usuario.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Sites.Read.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Sites.Read.All, Sites.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
```http
GET /me/insights/used
```
Solicitar devuelve resultados de otro usuario documentos utilizados ordenados por 'lastModifiedDateTime' y 'lastAccessedDateTime' está establecida en 'lastModifiedDateTime'.
```http
GET /users/<id | userPrincipalName>/insights/used
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.

Puede usar el `$filter` parámetro a los elementos de filtro usado de consulta. Por ejemplo, se basa en el tipo de:

`https://graph.microsoft.com/beta/me/insights/used?$filter=ResourceVisualization/Type eq 'PowerPoint'`

O en función de tipo de contenedor:

`https://graph.microsoft.com/beta/me/insights/used?$filter=ResourceVisualization/containerType eq 'OneDriveBusiness'`

Vea los tipos de contenedor y disponibles que puede filtrar los datos en [resourceVisualization](../resources/insights-resourcevisualization.md).


## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       |  Valor|
|:-------------|:------|
| Authorization  | {token} de portador. Obligatorio.|
| Aceptar  | application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una lista de elementos [utilizados](../resources/insights-used.md) en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.
```http
GET https://graph.microsoft.com/beta/me/insights/used
```

##### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real. 
```http
{
    "value": [
        {   
            "id": "id-value",
            "lastused" : { 
                "lastAccessedDateTime" : "lastAccessedDateTime-value", 
                "lastModifiedDateTime": "lastModifiedDateTime-value" 
            },
            "resourceVisualization": { 
                "title" : "title-value, 
                "type"  : "type-value",
                "mediaType" : "mediaType-value",
                "previewImageUrl" : previewImageUrl-value, 
                "previewText" : "previewText-value", 
                "containerWebUrl" : "containerWebUrl-value", 
                "containerDisplayName" : "containerDisplayName-value", 
                "containerType" : "containerType-value" 
            }, 
            "resourceReference" : { 
                "webUrl" : "webUrl-value", 
                "id": "id-value", 
                "type: "type-value" 
            }
        }
    ]
}
```

### <a name="expanding-resource"></a>Expansión de recursos
Se puede expandir el recurso al que hace referencia un entendimiento usado.
```http
GET https://graph.microsoft.com/beta/me/insights/used/{id}/resource
```
