# <a name="onenoteresource-resource-type"></a>Tipo de recurso OneNoteResource

Imagen u otro recurso de archivo en una página de OneNote. 

Puede obtener los datos binarios de un recurso, pero no puede obtener una representación JSON de un objeto de recurso o una colección de recursos.

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.onenoteEntityBaseModel",
  "optionalProperties": [],
  "isMediaEntity": true,
  "@odata.type": "microsoft.graph.onenoteResource"
}-->

```json
{
  "content": { "@odata.type": "Edm.Stream" },
  "contentUrl": "string (url)"
}
```

Obtenga los datos binarios de un recurso específico enviando una solicitud GET al punto de conexión `content` del recurso:

```
GET ../onenote/resources/{id}/content
```

El URI de recurso del archivo se devuelve al obtener el contenido HTML de una página mediante la siguiente solicitud:

```
GET ../onenote/pages/{id}/content
```

En la página HTML, la etiqueta `img` incluye puntos de conexión del recurso de imagen original en el atributo `data-fullres-src` y de la imagen optimizada en el atributo `src`:
```
<img 
    src="image-resource-url"  
    data-src-type="media-type"
    data-fullres-src="image-resource-url"  
    data-fullres-src-type="media-type" ... />
```

La etiqueta `object` (que representa archivos como PDF, DOCX y PNG) incluye el punto de conexión del recurso de archivo en el atributo `data`:

```
<object
    data="file-resource-url"
    data-attachment="file-name.file-type" 
    type="media-type" ... />
```

## <a name="properties"></a>Propiedades

| Propiedad             | Tipo            | Descripción
|:---------------------|:----------------|:---------------------------------
| content              | Secuencia          | La secuencia de contenido
| contentUrl           | Cadena (url)    | La dirección URL para descargar el contenido

## <a name="relationships"></a>Relaciones
Ninguna.


## <a name="methods"></a>Métodos
| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener datos binarios de recursos](../api/resource_get.md) | Secuencia |Recuperar los datos binarios de un recurso de archivo o imagen.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "resource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->