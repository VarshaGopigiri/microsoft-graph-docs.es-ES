---
title: tipo de recurso teamsTemplate
description: Describe la entidad teamsTemplate.
author: nkramer
ms.openlocfilehash: b4e32448f864048fdcb54dc001b21b262df2bba3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27327716"
---
# <a name="teamstemplate-resource-type"></a>tipo de recurso teamsTemplate

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una plantilla de equipo es un blueprint para la creación de un [equipo](../resources/team.md) en Microsoft Teams. Una plantilla especifica la estructura, configuración y, incluso un contenido que se debe aprovisionar en un nuevo equipo creado mediante la plantilla. Microsoft proporciona un conjunto de plantillas de bases y los clientes pueden guardar sus propias plantillas personalizadas.

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo     | Descripción |
|:------------------- |:-------- |:----------- |
| id                  | String   | Identificador único de la plantilla. No puede ser null. |

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsTemplate",
  "baseType": "microsoft.graph.entity"
}-->

```json
{
  "id": "string"
}
```

# <a name="see-also"></a>Vea también

- [equipo](team.md)

