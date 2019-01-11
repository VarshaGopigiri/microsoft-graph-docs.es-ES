---
title: tipo de recurso connectorGroup
description: Aquí tiene una representación JSON del recurso.
localization_priority: Normal
ms.openlocfilehash: 211efe5d8caae57457a6a5cc4fa95d145cd176f3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823194"
---
# <a name="connectorgroup-resource-type"></a>tipo de recurso connectorGroup

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener connectorGroup](../api/connectorgroup-get.md) | [connectorGroup](connectorgroup.md) |Leer las propiedades y las relaciones del objeto connectorGroup.|
|[Crear la aplicación](../api/connectorgroup-post-applications.md) |[application](application.md)| Asociación de una aplicación con el grupo de conector por la publicación de la colección de aplicaciones.|
|[Aplicaciones de lista](../api/connectorgroup-list-applications.md) |colección de la [aplicación](application.md)| Obtener la colección de objetos de la aplicación asociada.|
|[Creación de conector](../api/connectorgroup-post-members.md) |[conector](connector.md)| Agregar un conector para el conector de grupo de contabilización a la colección members.|
|[Enumerar miembros](../api/connectorgroup-list-members.md) |colección de [conector](connector.md)| Obtener un conector de colección de objetos.|
|[Update](../api/connectorgroup-update.md) | [connectorGroup](connectorgroup.md)    |Actualizar el objeto connectorGroup. |
|[Delete](../api/connectorgroup-delete.md) | Ninguno |Eliminar el objeto connectorGroup. Todos los conectores deben quitar antes de que se puede eliminar un grupo de conector. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|connectorGroupType|string| El tipo de conectores que se utilizará junto con el grupo. Los valores posibles son: `applicationProxy`.|
|id|Cadena| El identificador del objeto de la connectorGroup|
|isDefault|Booleano| Indica si la connectorGroup es el grupo predeterminado de conector. Sólo un conector grupo puede ser el connectorGroup de forma predeterminada y se establece el sistema.|
|name|Cadena| El nombre asociado con el connectorGroup.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Description|
|:---------------|:--------|:----------|
|aplicaciones|colección de la [aplicación](application.md)| Solo lectura. Admite valores NULL.|
|members|colección de [conector](connector.md)| Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.connectorGroup"
}-->

```json
{
  "connectorGroupType": "string",
  "id": "String (identifier)",
  "isDefault": true,
  "name": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "connectorGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
