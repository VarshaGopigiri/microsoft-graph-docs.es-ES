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
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All    |
|Aplicación | Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/root:/{item-path}:/thumbnails
GET /me/drive/items/{item-id}/thumbnails
GET /groups/{group-id}/drive/items/{item-id}/thumbnails
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite el [parámetro de consulta OData](../../../concepts/query_parameters.md) `$select` para personalizar la respuesta.

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [ThumbnailSet](../resources/thumbnailset.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "request",
  "name": "get_thumbnails"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{item-id}/thumbnails
```


##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta.

<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.thumbnailSet",
  "isCollection": true
} -->
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

## <a name="retrieve-a-single-thumbnail"></a>Recuperar una sola miniatura

Recupere los metadatos de una sola miniatura y un tamaño solicitándolo directamente en una solicitud.

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "request", "name": "get-one-thumbnail" } -->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{item-id}/thumbnails/{thumb-id}/{size}
```

## <a name="path-parameters"></a>Parámetros de ruta de acceso

| Nombre         | Tipo   | Descripción                                                                         |
|:-------------|:-------|:------------------------------------------------------------------------------------|
| **item-id**  | string | El identificador único para el elemento al que se hace referencia.                                      |
| **thumb-id** | número | El índice de la miniatura, normalmente de 0-4.                                            |
| **size**     | string | El tamaño de la miniatura solicitada. Debe ser uno de los tamaños estándares enumerados. |

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.thumbnail" } -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "width": 100,
  "height": 100,
  "url": "http://onedrive.com/asd123a/asdjlkasjdkasdjlk.jpg"
}
```

## <a name="retrieve-thumbnail-content"></a>Recuperar el contenido de miniaturas

Puede recuperar directamente el contenido de la miniatura solicitando la propiedad **content** de la miniatura.

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "request", "name":"get-thumbnail-content" } -->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{item-id}/thumbnails/{thumb-id}/{size}/content
```

## <a name="response"></a>Respuesta

El servicio responde con un redireccionamiento a la dirección URL de la miniatura.

<!-- { "blockType": "response" } -->
```http
HTTP/1.1 302 Found
Location: https://b0mpua-by3301.files.1drv.com/y23vmagahszhxzlcvhasdhasghasodfi
```

Las direcciones URL de contenido en miniatura se autentican previamente y no requieren la descarga de un encabezado de autorización. Estas direcciones URL son de corta duración, solo son válidas durante unas horas y las aplicaciones no deben almacenarlas en caché.


## <a name="size-values"></a>Valores de tamaño

Esta tabla define los tamaños posibles de las miniaturas. Puede solicitar cualquier tamaño de miniatura arbitrario, pero es probable que existan valores definidos y que se devuelva un valor rápidamente:

| Nombre           | Resolución  | Relación de aspecto | Descripción                                                          |
|:---------------|:------------|:-------------|:---------------------------------------------------------------------|
| `small`        | borde más largo 96  | Original     | Miniatura pequeña y muy comprimida recortada en una relación de aspecto cuadrada. |
| `medium`       | borde más largo 176 | Original     | Miniatura recortada al tamaño estándar del elemento para la vista web de OneDrive.         |
| `large`        | borde más largo 800 | Original     | Miniatura con el borde más largo cambiado a un tamaño de 800 píxeles.               |

## <a name="remarks"></a>Comentarios

**Nota** En OneDrive para la Empresa y en SharePoint:

* El uso de estas llamadas para expandir la colección de miniaturas no funcionará: `GET /drive/root:/{item-path}?expand=children(expand=thumbnails)`
  `GET /drive/items/{item-id}/children?expand=thumbnails`


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get metadata and content for thumbnails of multiple sizes for OneDrive items.",
  "keywords": "thumbnail,content,download,sizes",
  "section": "documentation",
  "tocPath": "OneDrive/Item/List thumbnails"
} -->
