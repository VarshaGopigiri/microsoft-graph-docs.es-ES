---
title: Tipo de recurso Filter
description: Administra el filtrado de la columna de una tabla.
localization_priority: Normal
ms.openlocfilehash: 5bbc4eff85f40e116ea513c27fa2966dd28a5493
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27852790"
---
# <a name="filter-resource-type"></a>Tipo de recurso Filter

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Administra el filtrado de la columna de una tabla.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Apply](../api/filter-apply.md)|None|Aplica los criterios de filtro especificados en la columna especificada.|
|[Clear](../api/filter-clear.md)|None|Borra el filtro de la columna especificada.|

## <a name="properties"></a>Propiedades
Ninguno

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|criterios|[FilterCriteria](filtercriteria.md)|Filtro aplicado actualmente en la columna especificada. Solo lectura.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Filter resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
