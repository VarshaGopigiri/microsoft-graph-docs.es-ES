---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: ContentTypeInfo
localization_priority: Normal
ms.openlocfilehash: e394d52a5f7ed5e8dce1c61d31d787d62bd36e56
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27892340"
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

| Nombre de la propiedad  | Tipo    | Descripción
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
