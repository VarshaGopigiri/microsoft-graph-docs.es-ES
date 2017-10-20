---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: ItemReference
ms.openlocfilehash: abd8b438e6c4e364a7a4b010d0808255425fa4df
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="itemreference-resource-type"></a>Tipo de recurso ItemReference

El recurso **ItemReference** proporciona información necesaria para dirigir un [DriveItem](driveitem.md) a través de la API.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "path", "shareId", "sharepointIds" ],
  "@odata.type": "microsoft.graph.itemReference"
}-->

```json
{
  "driveId": "string",
  "driveType": "personal | business | documentLibrary",
  "id": "string",
  "name": "string",
  "path": "string",
  "shareId": "string",
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" }
}
```

## <a name="properties"></a>Propiedades

| Propiedad      | Tipo              | Descripción
|:--------------|:------------------|:-----------------------------------------
| driveId       | Cadena            | Identificador único de la instancia de la unidad que contiene el elemento. Solo lectura.
| driveType     | String            | Identifica el tipo de unidad. Consulte el recurso [drive][] para ver los valores.
| id            | String            | Identificador único del elemento en la unidad. Solo lectura.
| name          | String            | El nombre del elemento al que se hace referencia. Solo lectura.
| path          | String            | Ruta de acceso que se puede usar para navegar hasta el elemento. Solo lectura.
| shareId       | Cadena            | Un identificador único para un recurso compartido al que se puede tener acceso a través de la API [Shares][].
| sharepointIds | [sharepointIds][] | Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.

[drive]: ../resources/drive.md
[sharepointIds]: ../resources/sharepointids.md
[Shares]: ../api/shares_get.md

## <a name="remarks"></a>Comentarios

Para resolver un **driveItem** de un recurso **itemReference**, cree una dirección URL con el formato:

```http
GET https://graph.microsoft.com/v1.0/drives/{driveId}/items/{id}
```

El valor **path** es una ruta de acceso de API relativa a la unidad de destino, por ejemplo: `/drive/root:/Documents/myfile.docx`.

Para recuperar la ruta de acceso legible de una ruta de navegación, puede ignorar todo hasta la primera `:` en la cadena de ruta de acceso.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ItemReference returns a pointer to another item.",
  "section": "documentation",
  "tocPath": "Resources/ItemReference"
} -->
