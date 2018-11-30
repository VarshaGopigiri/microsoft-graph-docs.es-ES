---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: ContentTypeInfo
ms.openlocfilehash: 922f87c77280627efb956e4558e1ff269daa9311
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087459"
---
# <a name="contenttypeinfo-resource-type"></a>Tipo de recurso ContentTypeInfo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **contentTypeInfo** indica el tipo de contenido de SharePoint de un elemento.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON de un recurso **ContentTypeInfo**.
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.contentTypeInfo", "@type.aka": "oneDrive.contentTypeFacet" } -->

```json
{
  "id": "string",
  "name": "string"
}
```

## <a name="properties"></a>Propiedades

| Nombre de propiedad  | Tipo    | Descripción
|:---------------|:--------|:--------------------------------------------------
| **id**         | string  | El identificador del tipo de contenido.
| **name**       | string  | El nombre del tipo de contenido.

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ContentTypeInfo"
} -->
