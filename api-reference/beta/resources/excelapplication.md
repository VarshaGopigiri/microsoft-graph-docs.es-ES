---
title: Tipo de recurso de aplicación
description: Representa la aplicación de Excel que administra el libro.
localization_priority: Normal
ms.openlocfilehash: a8e2124910301818e753b1f90a3168da3a072862
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27804441"
---
# <a name="application-resource-type"></a>Tipo de recurso de aplicación

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la aplicación de Excel que administra el libro.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener la aplicación](../api/excelapplication-get.md) | [Application](application.md) |Leer las propiedades y las relaciones del objeto application.|
|[Calculate](../api/excelapplication-calculate.md)|Ninguno|Recalcula todos los libros abiertos actualmente en Excel.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|calculationMode|string|Devuelve el modo de cálculo que se usa en el libro. Los valores posibles son: `Automatic`, `AutomaticExceptTables` y `Manual`. Solo lectura.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.application"
}-->

```json
{
  "calculationMode": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Application resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
