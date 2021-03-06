---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Unidad de disco
localization_priority: Priority
ms.prod: sharepoint
ms.openlocfilehash: 3b9744d8b652f0374c71f5304c326ba862c288a4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27929133"
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
| driveType            | String                        | Describe el tipo de unidad que representa este recurso. Las unidades personales de OneDrive devolverán `personal`. OneDrive para la Empresa devolverá `business`. Las bibliotecas de documentos de SharePoint devolverán `documentLibrary`. Solo lectura. |
| id                   | String                        | El identificador único de la unidad. Solo lectura.                                                                                                                                                                                   |
| lastModifiedBy       | [identitySet][]               | Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.                                                                                                                                           |
| lastModifiedDateTime | dateTimeOffset                | Fecha y hora de la última modificación del elemento. Solo lectura.                                                                                                                                                                             |
| name                 | string                        | Nombre del elemento. Lectura y escritura.                                                                                                                                                                                                |
| owner                | [identitySet](identityset.md) | Opcional. La cuenta de usuario propietaria de la unidad. Solo lectura.                                                                                                                                                                       |
| quota                | [quota](quota.md)             | Opcional. Información sobre la cuota de espacio de almacenamiento de la unidad. Solo lectura.                                                                                                                                                          |
| sharepointIds        | [sharepointIds][]             | Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.                                                                                                                                                         |
| system               | [systemFacet][]               | Si está presente, indica que se trata de una unidad administrada por el sistema. Solo lectura.
| webUrl               | string (url)                  | Dirección URL que muestra el recurso en el explorador. Solo lectura.                                                                                                                                                                        |

[identitySet]: identityset.md
[sharepointIds]: sharepointids.md
[systemFacet]: systemfacet.md

## <a name="relationships"></a>Relaciones

| Relación | Tipo                                 | Descripción
|:-------------|:-------------------------------------|:-----------------------
| items        | Colección de [DriveItem](driveitem.md) | Todos los elementos contenidos en la unidad. Solo lectura. Admite valores NULL.
| root         | [DriveItem](driveitem.md)            | La carpeta raíz de la unidad. Solo lectura.
| special      | Colección de [DriveItem](driveitem.md) | Colección de carpetas comunes disponibles en OneDrive. Solo lectura. Admite valores NULL.
| lista         | [List](list.md)                      | Para las unidades en SharePoint, la lista subyacente de biblioteca de documentos. Solo lectura. Admite valores NULL.

## <a name="methods"></a>Métodos

|                        Tarea común                         |         Método HTTP         |
| :--------------------------------------------------------- | :-------------------------- |
| [Obtener los metadatos de la unidad de otra unidad][drive-get]           | `GET /drives/{drive-id}`    |
| [Obtener la carpeta raíz de la unidad predeterminada del usuario][item-get]       | `GET /drive/root`           |
| [Mostrar los elementos secundarios en la unidad][item-children]             | `GET /drive/root/children`  |
| [Mostrar los cambios para todos los elementos de la unidad][item-changes]    | `GET /drive/root/delta`     |
| [Buscar los elementos en la unidad][item-search]               | `GET /drive/root/search`    |
| [Acceso a la carpeta especial](../api/drive-get-specialfolder.md) | `GET /drive/special/{name}` |

En la tabla anterior, los ejemplos usan `/drive` pero también son válidas otras rutas.

[item-resource]: driveitem.md
[identity-set]: identityset.md
[quota-facet]: quota.md
[drive-resource]: drive.md
[drive-get]: ../api/drive-get.md
[item-get]: ../api/driveitem-get.md
[item-changes]: ../api/driveitem-delta.md
[item-search]: ../api/driveitem-search.md
[item-children]: ../api/driveitem-list-children.md


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
