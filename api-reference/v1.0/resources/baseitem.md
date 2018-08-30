---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: BaseItem
ms.openlocfilehash: eaf73cf54671393b61cc37b5a5d1922060640882
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23268917"
---
# <a name="baseitem-resource-type"></a>Tipo de recurso BaseItem

El recurso **baseItem** es un recurso abstracto que contiene un conjunto común de propiedades compartidas entre varios tipos de recursos. Recursos derivados de **baseItem**:

* [drive](drive.md)
* [driveItem](driveitem.md)
* [site](site.md)
* [sharedDriveItem](shareddriveitem.md)

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON del recurso **baseItem**.

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "createdBy", "lastModifiedBy", "description", "parentReference", "webUrl" ],
  "keyProperty": "id",
  "abstract": true,
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.baseItem"
}-->

```json
{
  "id": "string (identifier)",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "datetime",
  "description": "string",
  "eTag": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "datetime",
  "name": "string",
  "parentReference": { "@odata.type": "microsoft.graph.itemReference" },
  "webUrl": "url"
}
```

## <a name="properties"></a>Propiedades

| Propiedad             | Tipo              | Descripción                                                                            |
| :------------------- | :---------------- | :------------------------------------------------------------------------------------- |
| id                   | cadena            | El identificador único de la unidad. Solo lectura.                                         |
| createdBy            | [identitySet][]   | Identidad del usuario, del dispositivo o de la aplicación que ha creado el elemento. Solo lectura.        |
| createdDateTime      | dateTimeOffset    | Fecha y hora de creación del elemento. Solo lectura.                                             |
| description          | Cadena            | Proporciona una descripción del elemento visible para el usuario. Opcional.                             |
| eTag                 | cadena            | ETag para el elemento. Solo lectura.                                                          |
| lastModifiedBy       | [identitySet][]   | Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura. |
| lastModifiedDateTime | dateTimeOffset    | Fecha y hora de la última modificación del elemento. Solo lectura.                                   |
| name                 | cadena            | Nombre del elemento. Lectura y escritura.                                                      |
| parentReference      | [itemReference][] | Información primaria, si el elemento tiene un elemento primario. Lectura y escritura.                              |
| webUrl               | cadena (url)      | Dirección URL que muestra el recurso en el explorador. Solo lectura.                              |

## <a name="relationships"></a>Relaciones

| Relación       | Tipo     | Descripción
|:-------------------|:---------|:---------------------------------------------
| createdByUser      | [user][] | Identidad del usuario que ha creado el elemento. Solo lectura.
| lastModifiedByUser | [user][] | Identidad del usuario que ha modificado por última vez el elemento. Solo lectura.

[identitySet]: identityset.md
[itemReference]: itemreference.md
[user]: user.md

## <a name="remarks"></a>Comentarios

El tipo `baseItem` no debe utilizarse directamente.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/BaseItem"
} -->
