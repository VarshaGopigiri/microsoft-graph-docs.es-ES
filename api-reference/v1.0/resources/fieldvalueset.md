---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: FieldValueSet
localization_priority: Normal
ms.openlocfilehash: 1f8c842f107b5090eb80bba9e614666f10d4dc0b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889694"
---
# <a name="fieldvalueset-resource"></a>Recurso FieldValueSet

Representa los valores de columna en un recurso [listItem](listitem.md).

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON del recurso **fieldValueSet**.
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.fieldValueSet",
      "optionalProperties": ["Author", "AuthorLookupId", "Name", "Color", "Quantity" ],
       "baseType": "microsoft.graph.entity", "openType": true } -->

```json
{
    "Author": "Brad Cleaver",
    "AuthorLookupId": "13",
    "Name": "Kangaroos and Wallabies: A Deep Dive",
    "Color": "Red",
    "Quantity": 350,
}
```

## <a name="properties"></a>Propiedades

Cada campo visible para el usuario en el recurso **listItem** se devuelve como un par nombre-valor en el recurso **fieldValueSet**.
El ejemplo anterior es de una lista que contiene cuatro columnas: **Author** (Autor), **Name** (Nombre), **Color** y **Quantity** (Cantidad).

Los campos de búsqueda (como `Author`) no se devuelven de forma predeterminada.
En su lugar, el servidor devuelve un campo "LookupId" (como `AuthorLookupId`) que hace referencia al recurso listItem que se buscaba.
El nombre del campo "LookupId" es el nombre de campo original seguido de `LookupId`.

Se pueden solicitar hasta 12 campos de búsqueda en una única consulta.
El servidor devolverá valores de búsqueda si la solicitud incluye una instrucción `select` con los campos que necesita.
Ejemplo:

```http
GET https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items?expand=fields(select=Author,BookTitle,PageCount)
```

Puede solicitar hasta 12 campos de búsqueda en una única consulta, además de cualquier número de campos normales.

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/FieldValueSet"
} -->
