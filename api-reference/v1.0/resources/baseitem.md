---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: BaseItem
ms.openlocfilehash: bbfebd734407259c391cdb1ce74beb96dc74d8bf
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
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
| eTag                 | string            | ETag para el elemento. Solo lectura.                                                          |
| lastModifiedBy       | [identitySet][]   | Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura. |
| lastModifiedDateTime | dateTimeOffset    | Fecha y hora de la última modificación del elemento. Solo lectura.                                   |
| name                 | string            | Nombre del elemento. Lectura y escritura.                                                      |
| parentReference      | [itemReference][] | Información primaria, si el elemento tiene un elemento primario. Lectura y escritura.                              |
| webUrl               | string (url)      | Dirección URL que muestra el recurso en el explorador. Solo lectura.                              |

[identitySet]: identityset.md
[itemReference]: itemreference.md

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
