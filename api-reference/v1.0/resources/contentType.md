---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: ContentType
ms.openlocfilehash: 38142299b06313da43637fd0a15ba95f3da362e2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030118"
---
# <a name="contenttype-resource-type"></a>Tipo de recurso ContentType

El recurso **contentType** representa un _tipo de contenido_ en SharePoint.
Los tipos de contenido le permiten definir un conjunto de columnas que debe estar presente en cada objeto [**listItem**][listItem] en un recurso [**list**][list].

[list]: list.md
[listItem]: listitem.md

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON de un recurso **contentType**.
<!-- {
  "blockType": "resource",
 "baseType": "microsoft.graph.entity",
 "@odata.type": "microsoft.graph.contentType" } -->

```json
{
  "description": "string",
  "group": "string",
  "hidden": false,
  "id": "string",
  "inheritedFrom": { "@type": "microsoft.graph.itemReference" },
  "name": "string",
  "order": { "@type": "microsoft.graph.contentTypeOrder" },
  "parentId": "string",
  "readOnly": false,
  "sealed": false,

  "columnLinks": [{ "@type": "microsoft.graph.columnLink" }]
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad     | Tipo                 | Descripción
|:------------------|:---------------------|:----------------------------------
| **description**   | string               | Texto descriptivo del elemento.
| **group**         | string               | El nombre del grupo al que pertenece este tipo de contenido. Ayuda a organizar los tipos de contenido relacionados.
| **hidden**        | boolean              | Indica si el tipo de contenido está oculto en el menú "Nuevo" de la lista.
| **id**            | string               | El identificador único del tipo de contenido.
| **inheritedFrom** | [itemReference][]    | Si este tipo de contenido se hereda de otro ámbito (por ejemplo, un sitio), proporciona una referencia al elemento en que se define el tipo de contenido.
| **name**          | string               | El nombre del tipo de contenido.
| **order**         | [contentTypeOrder][] | Especifica el orden en el que aparece el tipo de contenido en la interfaz de usuario de selección.
| **parentId**      | string               | El identificador único del tipo de contenido.
| **readOnly**      | boolean              | Si es `true`, no se puede modificar el tipo de contenido, a menos que este valor se establezca primero en `false`.
| **sealed**        | boolean              | Si es `true`, los usuarios no pueden modificar el tipo de contenido, ni a través de operaciones de inserción. Solo los administradores de la colección de sitios pueden sellar o quitar el sello de los tipos de contenido.

## <a name="relationships"></a>Relaciones

| Nombre de la propiedad   | Tipo                      | Descripción
|:----------------|:--------------------------|:-------------------------------
| **columnLinks** | Colección [columnLink][] | La colección de columnas que requiere este tipo de contenido

Vea [Introducción a los tipos de contenido y publicación del tipo de contenido][contentTypeIntro] para obtener más información.

[columnLink]: columnlink.md
[contentTypeIntro]: https://support.office.com/en-us/article/Introduction-to-content-types-and-content-type-publishing-e1277a2e-a1e8-4473-9126-91a0647766e5
[itemReference]: itemreference.md
[contentTypeOrder]: contenttypeorder.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ContentType"
} -->
