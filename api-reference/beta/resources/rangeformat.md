---
title: Tipo de recurso RangeFormat
description: Objeto de formato que encapsula la fuente, el relleno, los bordes, la alineación y otras propiedades del rango.
ms.openlocfilehash: dc1eb1fd06370dff554e1245245ec24cdf5a6658
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086465"
---
# <a name="rangeformat-resource-type"></a>Tipo de recurso RangeFormat

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Objeto de formato que encapsula la fuente, el relleno, los bordes, la alineación y otras propiedades del rango.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get RangeFormat](../api/rangeformat-get.md) | [RangeFormat](rangeformat.md) |Lee las propiedades y relaciones del objeto rangeFormat.|
|[Create RangeBorder](../api/rangeformat-post-borders.md) |[RangeBorder](rangeborder.md)| Crea un RangeBorder publicándolo en la colección borders.|
|[List borders](../api/rangeformat-list-borders.md) |Colección [RangeBorder](rangeborder.md)| Obtiene una colección de objetos RangeBorder.|
|[Update](../api/rangeformat-update.md) | [RangeFormat](rangeformat.md) |Actualiza el objeto RangeFormat. |
|[Autofitcolumns](../api/rangeformat-autofitcolumns.md)|None|Cambia el ancho de las columnas del rango actual para obtener el ajuste perfecto (según los datos actuales de las columnas).|
|[Autofitrows](../api/rangeformat-autofitrows.md)|None|Cambia el alto de las filas del rango actual para obtener el ajuste perfecto (según los datos actuales de las columnas).|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|columnWidth|double|Obtiene o establece el ancho de todas las columnas del rango. Si los anchos de columna no son uniformes, se devolverá null.|
|horizontalAlignment|string|Representa la alineación horizontal del objeto especificado. Valores posibles: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`.|
|rowHeight|double|Obtiene o establece el alto de todas las filas del rango. Si los altos de fila no son uniformes, se devolverá null.|
|verticalAlignment|string|Representa la alineación vertical del objeto especificado. Valores posibles: `Top`, `Center`, `Bottom`, `Justify`, `Distributed`.|
|wrapText|boolean|Indica si Excel ajusta el texto del objeto. Un valor null indica que el intervalo no tiene una configuración de ajuste uniforme.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|borders|Colección [RangeBorder](rangeborder.md)|Colección de objetos border que se aplican al rango global seleccionado. Solo lectura.|
|fill|[RangeFill](rangefill.md)|Devuelve el objeto de relleno definido en el rango global. Solo lectura.|
|font|[RangeFont](rangefont.md)|Devuelve el objeto de fuente definido en el intervalo global seleccionado. Solo lectura.|
|protection|[FormatProtection](formatprotection.md)|Devuelve el objeto de protección de formato de un rango. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.rangeFormat"
}-->

```json
{
  "columnWidth": 1024,
  "horizontalAlignment": "string",
  "rowHeight": 1024,
  "verticalAlignment": "string",
  "wrapText": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->