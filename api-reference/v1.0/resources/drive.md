---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Unidad de disco
ms.openlocfilehash: 0b178967f7eb8da8bdf8584bb13a7d4f9950392b
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="drive-resource-type"></a>Tipo de recurso Drive

El recurso de unidad es el objeto de nivel superior que representa el OneDrive de un usuario o una biblioteca de documentos de SharePoint.

Los usuarios de OneDrive siempre tendrán al menos una unidad disponible, la unidad predeterminada. Es posible que los usuarios sin licencia de OneDrive no tengan una unidad predeterminada disponible.

## <a name="json-representation"></a>Representación JSON

A continuación se muestra una representación JSON de un recurso Drive.

El recurso **drive** deriva de [**baseItem**](baseitem.md) y hereda las propiedades de ese recurso.

<!-- { "blockType": "resource", 
       "@odata.type": "microsoft.graph.drive",
       "keyProperty": "id", 
       "optionalProperties": [ "activities", "createdBy", "createdDateTime", "description", "lastModifiedBy", "lastModifiedDateTime", "name", "webUrl", "items", "root", "special", "system"] } -->

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
| description          | String                        | Proporciona una descripción de la unidad visible para el usuario. Lectura y escritura.
| driveType            | String                        | Describe el tipo de unidad que representa este recurso. Las unidades personales de OneDrive devolverán `personal`. OneDrive para la Empresa devolverá `business`. Las bibliotecas de documentos de SharePoint devolverán `documentLibrary`. Solo lectura. |
| id                   | String                        | El identificador único de la unidad. Solo lectura.                                                                                                                                                                                   |
| lastModifiedBy       | [identitySet][]               | Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.                                                                                                                                           |
| lastModifiedDateTime | dateTimeOffset                | Fecha y hora de la última modificación del elemento. Solo lectura.                                                                                                                                                                             |
| name                 | string                        | Nombre del elemento. Lectura y escritura.                                                                                                                                                                                                |
| owner                | [identitySet](identityset.md) | Opcional. La cuenta de usuario propietaria de la unidad. Solo lectura.                                                                                                                                                                       |
| quota                | [quota](quota.md)             | Opcional. Información sobre la cuota de espacio de almacenamiento de la unidad. Solo lectura.                                                                                                                                                          |
| sharepointIds        | [sharepointIds][]             | Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.                                                                                                                                                         |
| sistema               | [systemFacet][]               | Si está presente, indica que se trata de una unidad administrada por el sistema. Solo lectura.
| webUrl               | string (url)                  | Dirección URL que muestra el recurso en el explorador. Solo lectura.                                                                                                                                                                        |

[identitySet]: identityset.md
[sharepointIds]: sharepointids.md
[systemFacet]: systemfacet.md

## <a name="relationships"></a>Relaciones

| Relación | Tipo                                 | Descripción
|:-------------|:-------------------------------------|:-----------------------
| items        | Colección [driveitem](driveitem.md) | Todos los elementos contenidos en la unidad. Solo lectura. Admite valores NULL.
| root         | [driveitem](driveitem.md)            | La carpeta raíz de la unidad. Solo lectura.
| special      | Colección [driveitem](driveitem.md) | Colección de carpetas comunes disponibles en OneDrive. Solo lectura. Admite valores NULL.

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
  "tocPath": "Drives",
  "tocBookmarks": { "Resources/Drive": "#" }
} -->
