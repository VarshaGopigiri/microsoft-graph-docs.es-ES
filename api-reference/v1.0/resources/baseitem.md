---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: BaseItem
localization_priority: Normal
ms.openlocfilehash: daee18357e3f19f646a816070ca41a660f7b7ed3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810951"
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
| id                   | string            | El identificador único de la unidad. Solo lectura.                                         |
| createdBy            | [identitySet][]   | Identidad del usuario, del dispositivo o de la aplicación que ha creado el elemento. Solo lectura.        |
| createdDateTime      | dateTimeOffset    | Fecha y hora de creación del elemento. Solo lectura.                                             |
| description          | Cadena            | Proporciona una descripción del elemento visible para el usuario. Opcional.                             |
| eTag                 | string            | ETag para el elemento. Solo lectura.                                                          |
| lastModifiedBy       | [identitySet][]   | Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura. |
| lastModifiedDateTime | dateTimeOffset    | Fecha y hora de la última modificación del elemento. Solo lectura.                                   |
| name                 | string            | Nombre del elemento. Lectura y escritura.                                                      |
| parentReference      | [itemReference][] | Información primaria, si el elemento tiene un elemento primario. Lectura y escritura.                              |
| webUrl               | string (url)      | Dirección URL que muestra el recurso en el explorador. Solo lectura.                              |

## <a name="relationships"></a>Relaciones

| Relación       | Tipo     | Description
|:-------------------|:---------|:---------------------------------------------
| createdByUser      | [user][] | Identidad del usuario que ha creado el elemento. Solo lectura.
| lastModifiedByUser | [user][] | Identidad del usuario que ha modificado por última vez el elemento. Solo lectura.

[identitySet]: identityset.md
[itemReference]: itemreference.md
[user]: user.md

## <a name="remarks"></a>Observaciones

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
