---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: DefaultColumnValue
ms.openlocfilehash: 3a486b6cc90dffb75343390102ecb3b17576e6fb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087461"
---
# <a name="defaultcolumnvalue-resource-type"></a>Tipo de recurso DefaultColumnValue

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **defaultColumnValue** en un recurso [columnDefinition](columndefinition.md) especifica el valor predeterminado de esta columna.
El valor predeterminado puede especificarse directamente o como una fórmula.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON del recurso **defaultColumnValue**.
<!-- { "blockType": "resource", "@type": "microsoft.graph.defaultColumnValue" } -->

```json
{
  "formula": "=[Column1]+[Column2]+[Column3]",
  "value": "defaultValueString"
}
```

## <a name="properties"></a>Propiedades

| Nombre de propiedad | Tipo   | Descripción
|:--------------|:-------|:----------------------------------------------------
| **formula**   | string | La fórmula usada para calcular el valor predeterminado de esta columna.
| **value**     | string | El valor directo que se usará como el valor predeterminado de esta columna.

Solo se puede especificar **formula** o **value** de cada vez.

Las fórmulas de SharePoint usan una sintaxis similar a las fórmulas de Excel.
Vea [Ejemplos de fórmulas comunes en listas de SharePoint][SPFormulas] para obtener más información.

[SPFormulas]: https://support.office.com/en-us/article/Examples-of-common-formulas-in-SharePoint-Lists-d81f5f21-2b4e-45ce-b170-bf7ebf6988b3


<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/DefaultColumnValue"
} -->
