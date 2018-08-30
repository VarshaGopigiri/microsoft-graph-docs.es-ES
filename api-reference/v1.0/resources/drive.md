---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Unidad de disco
ms.openlocfilehash: c1abdfefa30dc2f510f3207adaf1d61a4d6a5edd
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23270100"
---
# <a name="drive-resource-type"></a>Tipo de recurso Drive

El recurso de unidad es el objeto de nivel superior que representa el OneDrive de un usuario o una biblioteca de documentos de SharePoint.

Los usuarios de OneDrive siempre tendrán al menos una unidad disponible, la unidad predeterminada. Es posible que los usuarios sin licencia de OneDrive no tengan una unidad predeterminada disponible.

## <a name="json-representation"></a>Representación JSON

A continuación se muestra una representación JSON de un recurso Drive.

El recurso **drive** deriva de [**baseItem**](baseitem.md) y hereda las propiedades de ese recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "activities",
    "createdBy",
    "createdDateTime",
    "description",
    "lastModifiedBy",
    "lastModifiedDateTime",
    "name",
    "webUrl",
    "items",
    "root",
    "sharepointIds",
    "special",
    "system"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.baseItem",
  "@odata.type": "microsoft.graph.drive"
}-->

```json
{
  "id": "string",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "string (timestamp)",
  "description": "string",
  "driveType": "personal | business | documentLibrary",
  "items": [ { "@odata.type": "microsoft.graph.driveItem" } ],
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "string (timestamp)",
  "name": "string",
  "owner": { "@odata.type": "microsoft.graph.identitySet" },
  "quota": { "@odata.type": "microsoft.graph.quota" },
  "root": { "@odata.type": "microsoft.graph.driveItem" },
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" },
  "special": [ { "@odata.type": "microsoft.graph.driveItem" }],
  "system": { "@odata.type": "microsoft.graph.systemFacet" },
  "webUrl": "url"
}
```

## <a name="properties"></a>Propiedades

| Propiedad             | Tipo                          | Descripción                                                                                                                                                                                                                      |
| :------------------- | :---------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| createdBy            | [identitySet][]               | Identidad del usuario, del dispositivo o de la aplicación que ha creado el elemento. Solo lectura.                                                                                                                                                  |
| createdDateTime      | dateTimeOffset                | Fecha y hora de creación del elemento. Solo lectura.                                                                                                                                                                                       |
| description          | Cadena                        | Proporciona una descripción de la unidad visible para el usuario. Lectura y escritura.
| driveType            | Cadena                        | Describe el tipo de unidad que representa este recurso. Las unidades personales de OneDrive devolverán `personal`. OneDrive para la Empresa devolverá `business`. Las bibliotecas de documentos de SharePoint devolverán `documentLibrary`. Solo lectura. |
| id                   | Cadena                        | El identificador único de la unidad. Solo lectura.                                                                                                                                                                                   |
| lastModifiedBy       | [identitySet][]               | Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.                                                                                                                                           |
| lastModifiedDateTime | dateTimeOffset                | Fecha y hora de la última modificación del elemento. Solo lectura.                                                                                                                                                                             |
| name                 | cadena                        | Nombre del elemento. Lectura y escritura.                                                                                                                                                                                                |
| owner                | [identitySet](identityset.md) | Opcional. La cuenta de usuario propietaria de la unidad. Solo lectura.                                                                                                                                                                       |
| quota                | [quota](quota.md)             | Opcional. Información sobre la cuota de espacio de almacenamiento de la unidad. Solo lectura.                                                                                                                                                          |
| sharepointIds        | [sharepointIds][]             | Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.                                                                                                                                                         |
| system               | [systemFacet][]               | Si está presente, indica que se trata de una unidad administrada por el sistema. Solo lectura.
| webUrl               | cadena (url)                  | Dirección URL que muestra el recurso en el explorador. Solo lectura.                                                                                                                                                                        |

[identitySet]: identityset.md
[sharepointIds]: sharepointids.md
[systemFacet]: systemfacet.md

## <a name="relationships"></a>Relaciones

| Relación | Tipo                                 | Descripción
|:-------------|:-------------------------------------|:-----------------------
| items        | Colección [DriveItem](driveitem.md) | Todos los elementos contenidos en la unidad de disco. Solo lectura. Admite un valor NULL.
| root         | [DriveItem](driveitem.md)            | La carpeta raíz de la unidad de disco. Solo lectura.
| special      | Colección [DriveItem](driveitem.md) | Colección de carpetas comunes disponibles en OneDrive. Solo lectura. Admite un valor NULL.
| list         | [Lista](list.md)                      | Para unidades de disco en SharePoint, la lista subyacente de la biblioteca de documentos. Solo lectura. Admite un valor NULL.

## <a name="methods"></a>Métodos

|                        Tarea común                         |         Método HTTP         |
| :--------------------------------------------------------- | :-------------------------- |
| [Obtener los metadatos de la unidad de otra unidad][drive-get]           | `GET /drives/{drive-id}`    |
| [Obtener la carpeta raíz de la unidad predeterminada del usuario][item-get]       | `GET /drive/root`           |
| [Mostrar los elementos secundarios en la unidad][item-children]             | `GET /drive/root/children`  |
| [Mostrar los cambios para todos los elementos de la unidad][item-changes]    | `GET /drive/root/delta`     |
| [Buscar los elementos en la unidad][item-search]               | `GET /drive/root/search`    |
| [Acceso a la carpeta especial](../api/drive_get_specialfolder.md) | `GET /drive/special/{name}` |

En la tabla anterior, los ejemplos usan `/drive` pero también son válidas otras rutas.

[item-resource]: driveitem.md
[identity-set]: identityset.md
[quota-facet]: quota.md
[drive-resource]: drive.md
[drive-get]: ../api/drive_get.md
[item-get]: ../api/driveitem_get.md
[item-changes]: ../api/driveitem_delta.md
[item-search]: ../api/driveitem_search.md
[item-children]: ../api/driveitem_list_children.md


<!-- {
  "type": "#page.annotation",
  "description": "Drive is a top level object for OneDrive API that provides access to the contents of a drive. ",
  "keywords": "drive,objects,resources",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/drive.md:
      Found potential enums in resource example that weren't defined in a table:(personal,business,documentLibrary) are in resource, but () are in table"
  ],
  "tocPath": "Drives",
  "tocBookmarks": { "Resources/Drive": "#" }
} -->
