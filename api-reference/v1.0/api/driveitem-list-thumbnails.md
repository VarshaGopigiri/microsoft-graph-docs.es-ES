---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Recuperar miniaturas de un archivo o una carpeta
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 7543a8177c146779c645d848292b1600a80c3398
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990596"
---
# <a name="list-thumbnails-for-a-driveitem"></a>Enumerar miniaturas de un DriveItem

Recupere una colección de recursos de [ThumbnailSet](../resources/thumbnailset.md) de un recurso de [DriveItem](../resources/driveitem.md).

Un DriveItem puede estar representado por cero o más recursos [ThumbnailSet](../resources/thumbnailset.md). Cada **thumbnailSet** puede tener uno o varios objetos en [**miniatura**](../resources/thumbnail.md), que son imágenes que representan el elemento. Por ejemplo, un **thumbnailSet** puede incluir objetos en **miniatura**, los más comunes son `small`, `medium` o `large`.

Hay muchas maneras de trabajar con miniaturas en OneDrive. Aquí tiene las más comunes:

* Enumerar las miniaturas disponibles para un elemento
* Recuperar una sola miniatura para un elemento
* Recuperar el contenido de miniaturas
* Recuperar miniaturas para varios elementos en una sola solicitud
* Recuperar los tamaños personalizados de miniaturas
* Cargar una miniatura personalizada para un elemento 
* Determinar si existe una miniatura cargada personalizada

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All    |
|Aplicación | Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/thumbnails
GET /groups/{group-id}/drive/items/{item-id}/thumbnails
GET /me/drive/items/{item-id}/thumbnails
GET /sites/{site-id}/drive/items/{item-id}/thumbnails
GET /users/{user-id}/drive/items/{item-id}/thumbnails
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método admite el [parámetro de consulta OData](/graph/query-parameters) `$select` para personalizar la respuesta.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ThumbnailSet](../resources/thumbnailset.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

Aquí tiene un ejemplo de la solicitud que recupera las miniaturas disponibles de un elemento en el OneDrive del usuario actual.

<!-- { "blockType": "request", "name": "enum-item-thumbnails", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/items/{item-id}/thumbnails
```

Esta devuelve una matriz de **thumbnailSets** disponibles para el elemento. Cualquier elemento de una unidad puede tener cero o más miniaturas.

**Nota:** Puede usar el parámetro de cadena de consulta _select_ para controlar qué tamaños de miniatura se devuelven en **ThumbnailSet**.
Por ejemplo, `/thumbnails?select=medium` recupera solo las miniaturas medianas.


### <a name="response"></a>Respuesta

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.thumbnailSet)" } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "0",
      "small": { "height": 64, "width": 96, "url": "https://sn3302files..."},
      "medium": { "height": 117, "width": 176, "url": "https://sn3302files..."},
      "large": { "height": 533, "width": 800, "url": "https://sn3302files..."}
    }
  ]
}
```

## <a name="get-a-single-thumbnail"></a>Obtener una única miniatura

Recupere los metadatos de una sola miniatura y un tamaño solicitándolo directamente en una solicitud.

### <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "request", "name": "get-one-thumbnail", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/items/{item-id}/thumbnails/{thumb-id}/{size}
```

### <a name="path-parameters"></a>Parámetros de ruta de acceso

| Nombre         | Tipo   | Descripción                                                                              |
|:-------------|:-------|:-----------------------------------------------------------------------------------------|
| **item-id**  | string | El identificador único para el elemento al que se hace referencia.                                           |
| **thumb-id** | número | El índice de la miniatura, normalmente de 0 a 4. Si existe una miniatura personalizada, su índice es 0. |
| **size**     | cadena | El tamaño de la miniatura solicitada. Puede ser uno de los tamaños estándares enumerados a continuación o uno personalizado. |

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.thumbnail" } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "width": 100,
  "height": 100,
  "url": "https://onedrive.com/asd123a/asdjlkasjdkasdjlk.jpg"
}
```

## <a name="retrieve-thumbnail-binary-content"></a>Recuperar el contenido binario de miniaturas

Puede recuperar directamente el contenido de la miniatura solicitando la propiedad **content** de la miniatura.

### <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "request", "name":"get-thumbnail-content", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/items/{item-id}/thumbnails/{thumb-id}/{size}/content
```

### <a name="response"></a>Respuesta

El servicio responde con un redireccionamiento a la dirección URL de la miniatura.

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 302 Found
Location: https://b0mpua-by3301.files.1drv.com/y23vmagahszhxzlcvhasdhasghasodfi
```

Las direcciones URL de la miniatura son seguras en caché. La dirección URL cambiará si el elemento cambia de manera que necesite generar una nueva miniatura.


## <a name="getting-thumbnails-while-listing-driveitems"></a>Obtención de miniaturas al enumerar recursos DriveItem

Si está recuperando una lista de recursos DriveItem para mostrar, puede usar el parámetro de cadena de consulta _$expand_ para que también incluya las miniaturas de esos recursos.
Esto permite que su aplicación recupere miniaturas y elementos en una única solicitud, en lugar de emitir varias solicitudes.

### <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "request", "name":"get-thumbnail-while-listing", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/items/{item-id}/children?$expand=thumbnails
```

### <a name="response"></a>Respuesta

Las respuestas del servicio con la lista de recursos DriveItem y sus miniaturas.

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.driveItem)", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "182331E8-2788-4932-B52A-A6550577043F",
      "name": "my photo.jpg",
      "thumbnails": [
        {
          "small": { "width": 96,
                     "height": 96,
                     "url": "https://sn3302files..."
                   }
        }
      ]
    },
    {
      "id": "2D223953-A56B-4D9B-ADF3-13E7820673A2",
      "name": "presentation.pptx",
      "thumbnails": [
        {
          "small": { "width": 96,
                     "height": 96,
                     "url": "https://sn3302files..."
                   }
        }
      ]
    }
  ]
}
```

## <a name="size-options"></a>Opciones de tamaño

Esta tabla define los tamaños posibles de las miniaturas. Puede solicitar cualquier tamaño de miniatura arbitrario, pero es probable que existan valores definidos y que se devuelva un valor rápidamente:

| Nombre           | Resolución  | Relación de aspecto | Descripción                                                          |
|:---------------|:------------|:-------------|:---------------------------------------------------------------------|
| `small`        | borde más largo 96  | Original     | Miniatura pequeña y muy comprimida recortada en una relación de aspecto cuadrada. |
| `medium`       | borde más largo 176 | Original     | Miniatura recortada al tamaño estándar del elemento para la vista web de OneDrive.         |
| `large`        | borde más largo 800 | Original     | Miniatura con el borde más largo cambiado a un tamaño de 800 píxeles.               |
| `smallSquare`  | 96x96       | Recorte cuadrado  | Miniatura de cuadrado pequeño                                               |
| `mediumSquare` | 176x176     | Recorte cuadrado  | Miniatura de cuadrado pequeño                                               |
| `largeSquare`  | 800x800     | Recorte cuadrado  | Miniatura de cuadrado grande                                               |

## <a name="requesting-custom-thumbnail-sizes"></a>Solicitar tamaños personalizados de miniaturas

Además de los tamaños definidos, la aplicación puede solicitar un tamaño de miniatura personalizado especificando las dimensiones de la miniatura prefijada con `c`.
Por ejemplo, si su aplicación necesita miniaturas de tamaño 300x400, puede solicitar ese tamaño de esta forma:

<!-- { "blockType": "request", "name": "get-thumbnail-custom-size", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/items/{item-id}/thumbnails?select=c300x400_Crop
```

Que responde solo con el tamaño de miniatura personalizado seleccionado:

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.thumbnailSet)" } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "0",
      "c300x400_Crop": { "height": 300, "width": 400, "url": "https://sn3302files.onedrive.com/123"},
    }
  ]
}
```

Puede especificar las siguientes opciones después del tamaño de la miniatura solicitado:

### <a name="examples-of-custom-identifiers"></a>Ejemplos de identificadores personalizados

| Identificador de miniatura | Resolución             | Relación de aspecto | Descripción                                                                                                                                         |
|:---------------------|:-----------------------|:-------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| c300x400             | Limitado por un cuadro de 300x400 | Original     | Genera una miniatura que se adapta dentro de un cuadro de 300x400 píxeles, manteniendo la relación de aspecto                                                                 |
| c300x400_Crop        | 300x400                | Recortado      | Genera una miniatura que tiene 300x400 píxeles. Esto funciona cambiando el tamaño de la imagen para rellenar el cuadro de 300x400 y recortando lo que sobresalga de este. |

**Nota:** La miniatura devuelta puede no coincidir exactamente con las dimensiones en píxeles que se solicitaron, pero coincidirá con la relación de aspecto.
En algunos casos, puede devolverse una miniatura más grande que la que se ha solicitado si la miniatura ya existe y se puede escalar fácilmente para ajustarse a la resolución solicitada.

## <a name="remarks"></a>Comentarios

**Nota** En OneDrive para la Empresa y en SharePoint:

El uso de estas llamadas para expandir la colección de miniaturas no funcionará:

* `GET /drive/root:/{item-path}?expand=children(expand=thumbnails)`
* `GET /drive/items/{item-id}/children?expand=thumbnails`

Las miniaturas no se admiten en SharePoint Server 2016.

### <a name="error-responses"></a>Respuestas de error

Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.

[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "Get metadata and content for thumbnails of multiple sizes for OneDrive items.",
  "keywords": "thumbnail,content,download,sizes",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/api/driveitem-list-thumbnails.md:
      Unable to map some markdown elements into schema.
         Unmapped methods:
      enum-item-thumbnails, get-one-thumbnail, get-thumbnail-content, get-thumbnail-while-listing, get-thumbnail-custom-size
         Unmapped tables:
      Permissions - AuthScopes, Path parameters - PathParameters, Size options - Unknown, Examples of custom identifiers - Unknown",
    "Warning: Couldn't serialize request for path /me/drive/items/{var}/thumbnails/{var}/{var}/content into EDMX: System.InvalidOperationException: Uri path requires navigating into unknown object hierarchy: missing property '{var}' on 'thumbnailSet'. Possible issues:
         1) Doc bug where '{var}' isn't defined on the resource.         2) Doc bug where '{var}' is an example key and should instead be replaced with a placeholder like {item-id} or declared in the sampleKeys annotation.       3) Doc bug where 'thumbnailSet' is supposed to be an entity type, but is being treated as a complex because it (and its ancestors) are missing the keyProperty annotation
     at ApiDocs.Publishing.CSDL.CsdlWriter.ParseRequestTargetType(String requestPath, MethodCollection requestMethodCollection, EntityFramework edmx, IssueLogger issues) in D:/src/mds2/ApiDocs.Publishing/CSDL/CsdlWriter.cs:line 1145
     at ApiDocs.Publishing.CSDL.CsdlWriter.ProcessRestRequestPaths(EntityFramework edmx, String[] baseUrlsToRemove, IssueLogger issues) in D:/src/mds2/ApiDocs.Publishing/CSDL/CsdlWriter.cs:line 821"
  ],
  "tocPath": "Items/Thumbnails"
} -->
