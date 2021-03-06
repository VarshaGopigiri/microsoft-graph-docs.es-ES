---
title: Tipo de recurso resource
description: 'Imagen u otro recurso de archivo en una página de OneNote. '
localization_priority: Normal
ms.openlocfilehash: a8ba7b2afb5b083e4fe5250ef499043029a1195b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879523"
---
# <a name="resource-resource-type"></a>Tipo de recurso resource

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Imagen u otro recurso de archivo en una página de OneNote. 

Puede obtener los datos binarios de un recurso, pero no puede obtener una representación JSON de un objeto de recurso o una colección de recursos.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onenoteResource"
}-->

Obtenga los datos binarios de un recurso específico enviando una solicitud GET al punto de conexión `content` del recurso:

```
GET ../onenote/resources/{id}/content
```

El URI de recurso del archivo se devuelve al obtener el contenido HTML de una página mediante la siguiente solicitud:

```
GET ../onenote/pages/{id}/content
```

En la página HTML, la etiqueta `img` incluye puntos de conexión del recurso de imagen original en el atributo `data-fullres-src` y de la imagen optimizada en el atributo `src`:
```
<img 
    src="image-resource-url"  
    data-src-type="media-type"
    data-fullres-src="image-resource-url"  
    data-fullres-src-type="media-type" ... />
```

La etiqueta `object` (que representa archivos como PDF, DOCX y PNG) incluye el punto de conexión del recurso de archivo en el atributo `data`:

```
<object
    data="file-resource-url"
    data-attachment="file-name.file-type" 
    type="media-type" ... />
```

## <a name="properties"></a>Propiedades
Ninguna.

## <a name="relationships"></a>Relaciones
Ninguno.


## <a name="methods"></a>Métodos
| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener datos binarios de recursos](../api/resource-get.md) | Secuencia |Recuperar los datos binarios de un recurso de archivo o imagen.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "resource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
