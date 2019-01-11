---
title: tipo de filtro de recurso
description: Determina qué objetos se deben aprovisionar a la aplicación. Por ejemplo, es posible que desee sólo los usuarios de aprovisionamiento que se encuentran en los Estados Unidos. Cuando un filtro de ámbito está presente, se omitirá los objetos que no cumplen con el filtro durante la sincronización.
localization_priority: Normal
ms.openlocfilehash: 754271e9d33159a14d1abf356280dd619643002f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894414"
---
# <a name="filter-resource-type"></a>tipo de filtro de recurso

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Determina qué objetos se deben aprovisionar a la aplicación. Por ejemplo, es posible que desee sólo los usuarios de aprovisionamiento que se encuentran en los Estados Unidos. Cuando un filtro de ámbito está presente, se omitirá los objetos que no cumplen con el filtro durante la sincronización.

Filtro de forma parte de la [asignación de objetos](synchronization-objectmapping.md). Consta de varios conjuntos de grupos de filtro, y cada grupo de filtro contiene una o más cláusulas. Se considera como un objeto en el ámbito del grupo (el grupo se evalúa a `true`) sólo si todas las cláusulas del grupo se evalúan a `true`.

Se considera como un objeto en el ámbito para el conjunto de grupo (conjunto de grupos se evalúa a `true`) si cualquiera de los grupos en el conjunto se evalúa a `true`.

Para obtener más información, vea [aplicación basada en el atributo de aprovisionamiento con filtros de ámbito](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-saas-scoping-filters)

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|categoryFilterGroups|colección de [filterGroup](synchronization-filtergroup.md)|`*Experimental*`Filtrar conjunto de grupo que se usa para decidir si objeto dado pertenece y se debe procesar como parte de este objeto de asignación. Se considera como un objeto en el ámbito *Si cualquiera de los grupos de la colección se evalúa a `true` *.|
|grupos|colección de [filterGroup](synchronization-filtergroup.md)|Filtrar conjunto de grupo que se usa para decidir si el objeto dado es en el ámbito de aprovisionamiento. **Éste es el filtro que debe usarse en la mayoría de los casos**. Si un objeto que se utiliza para satisfacer este filtro en un momento dado y, a continuación, el objeto o el filtro se ha cambiado por lo que el filtro no satisfecho, ya existe el objeto * obtener aprovisionará desaprovisionamiento ". Se considera como un objeto en el ámbito *Si cualquiera de los grupos de la colección se evalúa a `true` *.|
|inputFilterGroups|colección de [filterGroup](synchronization-filtergroup.md)|`*Experimental*`Filtrar conjunto de grupo que se usa para filtrar objetos en la fase temprana de leerlos desde el directorio. Si un objeto no satisface este filtro no se procesarán aún más. Es importante comprender que, si utiliza un objeto para satisfacer este filtro en un momento dado y, a continuación, el objeto o el filtro se cambió lo ese filtro está ya no se cumple, por ejemplo, objeto *no obtener aprovisionará desaprovisionamiento*. Se considera como un objeto en el ámbito *Si cualquiera de los grupos de la colección se evalúa a `true` *. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.filter"
}-->

```json
{
  "categoryFilterGroups": [{"@odata.type": "microsoft.graph.filterGroup"}],
  "groups": [{"@odata.type": "microsoft.graph.filterGroup"}],
  "inputFilterGroups": [{"@odata.type": "microsoft.graph.filterGroup"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "filter resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
