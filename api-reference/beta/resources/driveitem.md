---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: DriveItem
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 98930017f9ca3f70501cd10e4a3029f7a240ce41
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977780"
---
# <a name="driveitem-resource-type"></a>tipo de recurso driveItem

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **driveItem** representa un archivo, una carpeta u otro elemento almacenado en una unidad. Todos los objetos del sistema de archivos en OneDrive y SharePoint se devuelven como recursos de **driveItem**.

Hay dos maneras principales de abordar un recurso **driveItem**:

* Con el identificador único **driveItem** utilizando `drive/items/{item-id}`
* Con la ruta de acceso del sistema de archivos utilizando `/drive/root:/path/to/file`

Los recursos **DriveItem** tienen facetas modeladas como propiedades que proporcionan datos sobre las identidades y las capacidades de driveItem. Por ejemplo:

* Las carpetas tienen una [**faceta folder**][folder].
* Los archivos tienen una [**faceta file**][file].
* Las imágenes tienen una [**faceta image**][image], además de su faceta file.
* Las imágenes tomadas con una cámara (fotos) tienen una [**faceta photo**][photo] que identifica el elemento como una foto. Además, facilita las propiedades que indican cuándo se tomó la foto y con qué dispositivo.

Los elementos con una faceta **folder** actúan como contenedores de elementos y, por lo tanto, tienen una referencia `children` que indica una colección de **driveItems** dentro de la carpeta.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON del recurso **driveItem**.

El recurso **driveItem** deriva de [**baseItem**][baseItem] y hereda las propiedades de ese recurso.

<!-- { "blockType": "resource", "@type": "microsoft.graph.driveItem", "@type.aka": "oneDrive.item",
       "baseType": "microsoft.graph.baseItem",
       "optionalProperties": ["cTag", "children", "folder", "file", "image", "audio", "video",
       "location", "deleted", "specialFolder", "photo", "thumbnails", "searchResult", "remoteItem",
       "shared", "content", "@microsoft.graph.conflictBehavior", "@microsoft.graph.downloadUrl", "@content.sourceUrl",
       "sharepointIds"],
       "keyProperty": "id", "openType": true } -->

```json
{
  "audio": { "@odata.type": "microsoft.graph.audio" },
  "cTag": "string (etag)",
  "deleted": { "@odata.type": "microsoft.graph.deleted"},
  "description": "string",
  "file": { "@odata.type": "microsoft.graph.file" },
  "fileSystemInfo": { "@odata.type": "microsoft.graph.fileSystemInfo" },
  "folder": { "@odata.type": "microsoft.graph.folder" },
  "image": { "@odata.type": "microsoft.graph.image" },
  "location": { "@odata.type": "microsoft.graph.geoCoordinates" },
  "package": { "@odata.type": "microsoft.graph.package" },
  "photo": { "@odata.type": "microsoft.graph.photo" },
  "publication": {"@odata.type": "microsoft.graph.publicationFacet"},
  "remoteItem": { "@odata.type": "microsoft.graph.remoteItem" },
  "root": { "@odata.type": "microsoft.graph.root" },
  "searchResult": { "@odata.type": "microsoft.graph.searchResult" },
  "shared": { "@odata.type": "microsoft.graph.shared" },
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" },
  "size": 1024,
  "specialFolder": { "@odata.type": "microsoft.graph.specialFolder" },
  "video": { "@odata.type": "microsoft.graph.video" },
  "webDavUrl": "string",

  /* relationships */
  "activities": [{"@odata.type": "microsoft.graph.itemActivity"}],
  "content": { "@odata.type": "Edm.Stream" },
  "children": [ { "@odata.type": "microsoft.graph.driveItem" }],
  "permissions": [ {"@odata.type": "microsoft.graph.permission"} ],
  "thumbnails": [ {"@odata.type": "microsoft.graph.thumbnailSet"}],
  "versions": [ {"@odata.type": "Collection(microsoft.graph.driveItemVersion)"}],

  /* inherited from baseItem */
  "id": "string (identifier)",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "eTag": "string",
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "name": "string",
  "parentReference": {"@odata.type": "microsoft.graph.itemReference"},
  "webUrl": "string",

  /* instance annotations */
  "@microsoft.graph.conflictBehavior": "string",
  "@microsoft.graph.downloadUrl": "url",
  "@microsoft.graph.sourceUrl": "url"
}
```

## <a name="properties"></a>Propiedades

| Propiedad             | Tipo               | Descripción
|:---------------------|:-------------------|:---------------------------------
| audio                | [audio][]          | Metadatos de audio, si el elemento es un archivo de audio. Solo lectura.
| createdBy            | [identitySet][]    | Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.
| createdDateTime      | DateTimeOffset     | Fecha y hora de creación del elemento. Solo lectura.
| cTag                 | String             | Un eTag del contenido del elemento. No se cambia este eTag si solo se modifican los metadatos. **Nota** Esta propiedad no se devuelve si el elemento es una carpeta. Solo lectura.
| deleted              | [deleted][]        | Información sobre el estado del elemento eliminado. Solo lectura.
| description          | Cadena             | Proporciona una descripción del elemento visible para el usuario. Lectura y escritura. Solo en OneDrive Personal
| eTag                 | Cadena             | ETag de todo el elemento (metadatos + contenido). Solo lectura.
| file                 | [file][]           | Metadatos de archivo, si el elemento es un archivo. Solo lectura.
| fileSystemInfo       | [fileSystemInfo][] | Información del sistema de archivos del cliente. Lectura y escritura.
| folder               | [folder][]         | Metadatos de carpeta, si el elemento es una carpeta. Solo lectura.
| id                   | Cadena             | El identificador único del elemento dentro del Drive. Solo lectura.
| image                | [image][]          | Metadatos de imagen, si el elemento es una imagen. Solo lectura.
| lastModifiedBy       | [identitySet][]    | Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.
| lastModifiedDateTime | DateTimeOffset     | Fecha y hora de la última modificación del elemento. Solo lectura.
| location             | [geoCoordinates][] | Metadatos de ubicación, si el elemento tiene datos de ubicación. Solo lectura.
| name                 | Cadena             | El nombre del elemento (nombre de archivo y extensión). Lectura y escritura.
| paquete              | [package][]        | Si está presente, indica que este elemento es un paquete en lugar de una carpeta o archivo. Los paquetes se tratan como archivos en algunos contextos y como carpetas en otros. Solo lectura.
| parentReference      | [itemReference][]  | Información primaria, si el elemento tiene un elemento primario. Lectura y escritura.
| photo                | [photo][]          | Metadatos de foto, si el elemento es una foto. Solo lectura.
| publication          | [publicationFacet][] | Proporciona información sobre el estado publicado o extraído de un elemento, en ubicaciones que admiten esas acciones. Esta propiedad no se devuelve de forma predeterminada. Solo lectura. |
| remoteItem           | [remoteItem][]     | Datos de elemento remoto, si el elemento se comparte desde una unidad distinta a la de acceso. Solo lectura.
| root                 | [root][]           | Si esta propiedad no es NULL, indica que el driveItem es el driveItem de nivel superior de la unidad.
| searchResult         | [searchResult][]   | Metadatos de búsqueda, si el elemento es un resultado de búsqueda. Solo lectura.
| compartido               | [shared][]         | Indica que el elemento se ha compartido con otros usuarios y proporciona información sobre el estado del elemento compartido. Solo lectura.
| sharepointIds        | [sharepointIds][]  | Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.
| size                 | Int64              | Tamaño del elemento en bytes. Solo lectura.
| specialFolder        | [specialFolder][]  | Si el elemento actual también está disponible como una carpeta especial, se devuelve esta faceta. Solo lectura.
| video                | [video][]          | Metadatos de vídeo, si el elemento es un vídeo. Solo lectura.
| webDavUrl            | Cadena             | Dirección URL compatible con WebDAV del elemento.
| webUrl               | Cadena             | Dirección URL que muestra el recurso en el explorador. Solo lectura.

**Nota:** Las propiedades eTag y cTag funcionan de forma diferente en los contenedores (carpetas). El valor de cTag se modifica cuando se cambia el contenido o los metadatos de cualquier descendiente de la carpeta. El valor de eTag solo se modifica cuando se cambian las propiedades de la carpeta, excepto las propiedades que derivan de descendientes (como **childCount** o **lastModifiedDateTime**).

## <a name="relationships"></a>Relaciones

| Relación       | Tipo                            | Descripción
|:-------------------|:--------------------------------|:--------------------------
| activities         | Colección [itemActivity][]     | Lista de actividades recientes que tuvieron lugar en este elemento.
| análisis          | recursos de [itemAnalytics][]      | Análisis acerca de las actividades de vista que tuvieron lugar en este elemento.
| content            | Secuencia                          | La secuencia de contenido, si el elemento representa un archivo.
| children           | Colección driveItem            | Colección que contiene objetos Item de los elementos secundarios inmediatos del elemento. Solo los elementos que representan carpetas tienen elementos secundarios. Solo lectura. Admite valores NULL.
| listItem           | [listItem][]                    | Para las unidades en SharePoint, el elemento de lista de biblioteca de documentos asociada. Solo lectura. Admite valores NULL.
| permissions        | Colección [permission][]       | El conjunto de permisos del elemento. Solo lectura. Admite valores NULL.
| miniaturas         | Colección [thumbnailSet][]     | Colección que contiene objetos [ThumbnailSet][] asociados al elemento. Para obtener más información, consulte [obtener miniaturas][]. Solo lectura. Admite valores NULL.
| versiones           | colección de [driveItemVersion][] | La lista de las versiones anteriores del elemento. Para obtener más información, vea [Introducción a las versiones anteriores][]. Solo lectura. Admite valores NULL.

## <a name="instance-attributes"></a>Atributos de instancia

Los atributos de instancia son propiedades con comportamientos especiales. Estas propiedades son temporales y o bien a) definen el comportamiento que debería tener el servicio o b) proporcionan valores de propiedad a corto plazo, como una dirección URL de descarga de un elemento que expira.

| Nombre de la propiedad                     | Tipo   | Descripción
|:----------------------------------|:-------|:--------------------------------
| @microsoft.graph.conflictBehavior | string | El comportamiento de resolución de conflictos para las acciones que crean un nuevo elemento. Puede utilizar los valores de *fail*, *replace*, o *rename*. El valor predeterminado de PUT es *replace*. Nunca se devuelve un elemento con esta anotación. Solo escritura.
| @microsoft.graph.downloadUrl      | string | Una dirección URL que puede utilizarse para descargar el contenido de este archivo. No es necesaria la autenticación con esta dirección URL. Solo lectura.
| @microsoft.graph.sourceUrl        | string | Al emitir una solicitud PUT, esta anotación de instancia puede utilizarse para indicar al servicio que descargue el contenido de la dirección URL y lo guarde como el archivo. Solo escritura.

**Nota:** El valor de @microsoft.graph.downloadUrl es una dirección URL de corta duración y no se puede almacenar en caché.
La dirección URL sólo estará disponible durante un breve período de tiempo (1 hora) antes de se haya invalidado. Quitar permisos de archivo para un usuario no puede invalidar inmediatamente la dirección URL.

## <a name="methods"></a>Métodos

| Método                                                   | Ruta de acceso a REST
|:---------------------------------------------------------|:------------------
| [Obtener elemento](../api/driveitem-get.md)                      | `GET /drive/items/{item-id}`
| [Enumerar actividades](../api/activities-list.md)             | `GET /drive/items/{item-id}/activities`
| [Obtener análisis][]                                        | `GET /drive/items/{item-id}/analytics`
| [Obtener las actividades por intervalo][]                           | `GET /drive/items/{item-id}/getActivitiesByInterval`
| [Enumerar elementos secundarios](../api/driveitem-list-children.md)       | `GET /drive/items/{item-id}/children`
| [Enumerar versiones](../api/driveitem-list-versions.md)       | `GET /drive/items/{item-id}/versions`
| [Crear elemento](../api/driveitem-post-children.md)         | `POST /drive/items/{item-id}/children`
| [Actualizar elemento](../api/driveitem-update.md)                | `PATCH /drive/items/{item-id}`
| [Cargar contenido](../api/driveitem-put-content.md)        | `PUT /drive/items/{item-id}/content`
| [Descargar contenido](../api/driveitem-get-content.md)      | `GET /drive/items/{item-id}/content`
| [Descargar el formato de archivo específico][download-format]         | `GET /drive/items/{item-id}/content?format={format}`
| [Eliminar elemento](../api/driveitem-delete.md)                | `DELETE /drive/items/{item-id}`
| [Mover elemento](../api/driveitem-move.md)                    | `PATCH /drive/items/{item-id}`
| [Copiar elemento](../api/driveitem-copy.md)                    | `POST /drive/items/{item-id}/copy`
| [Buscar elementos](../api/driveitem-search.md)               | `GET /drive/items/{item-id}/search(q='text')`
| [Enumerar cambios en una unidad](../api/driveitem-delta.md)     | `GET /drive/root/delta`
| [Enumerar miniaturas](../api/driveitem-list-thumbnails.md)   | `GET /drive/items/{item-id}/thumbnails`
| [Crear vínculo para compartir](../api/driveitem-createlink.md)    | `POST /drive/items/{item-id}/createLink`
| [Agregar permisos](../api/driveitem-invite.md)            | `POST /drive/items/{item-id}/invite`
| [Enumerar permisos](../api/driveitem-list-permissions.md) | `GET /drive/items/{item-id}/permissions`
| [Eliminar permiso](../api/permission-delete.md)         | `DELETE /drive/items/{item-id}/permissions/{perm-id}`
| [Obtener WebSocket canal][getWebSocket]                    | `GET /drive/root/subscriptions/socketIo`
| [Vista previa del artículo][item-preview]                             | `POST /drive/items/{item-id}/preview`

[item-preview]: ../api/driveitem-preview.md
[Obtener análisis]: ../api/itemanalytics-get.md
[Obtener las actividades por intervalo]: ../api/itemactivity-getbyinterval.md

## <a name="remarks"></a>Observaciones

En las bibliotecas de documentos de OneDrive para la Empresa o SharePoint, no se devuelve la propiedad **cTag** si **driveItem** tiene una faceta [folder][].

[audio]: audio.md
[baseItem]: baseitem.md
[deleted]: deleted.md
[download-format]: ../api/driveitem-get-content-format.md
[driveItemVersion]: driveitemversion.md
[file]: file.md
[fileSystemInfo]: filesysteminfo.md
[folder]: folder.md
[Introducción a las versiones anteriores]: ../api/driveitem-list-versions.md
[obtener miniaturas]: ../api/driveitem-list-thumbnails.md
[getWebSocket]: ../api/driveitem-subscriptions-socketio.md
[identitySet]: identityset.md
[image]: image.md
[itemActivity]: itemactivity.md
[itemAnalytics]: itemanalytics.md
[itemReference]: itemreference.md
[geoCoordinates]: geocoordinates.md
[List activities]: ../api/activities-list.md
[listItem]: listitem.md
[package]: package.md
[permission]: permission.md
[photo]: photo.md
[remoteItem]: remoteitem.md
[root]: root.md
[searchResult]: searchresult.md
[shared]: shared.md
[sharepointIds]: sharepointids.md
[specialFolder]: specialfolder.md
[thumbnailSet]: thumbnailset.md
[video]: video.md
[user]: https://developer.microsoft.com/graph/docs/api-reference/v1.0/resources/users
[publicationFacet]: publicationfacet.md

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Item is the main data model in the OneDrive API. Everything is an item.",
  "keywords": "item,facet,resource",
  "section": "documentation",
  "tocPath": "Items",
  "tocBookmarks": { "Resources/Item": "#" }
} -->
