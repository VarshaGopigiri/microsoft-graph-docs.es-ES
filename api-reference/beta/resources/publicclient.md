---
title: tipo de recurso publicClient
description: Especifica la configuración para que no sean Web App o la Api de Web. (por ejemplo, Mobile u otro pública cliente como una aplicación instalada que se ejecutan en un dispositivo de escritorio)
localization_priority: Normal
ms.openlocfilehash: c466c91f90ac8adc2bf3806fa212e0b01e6d2507
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27864200"
---
# <a name="publicclient-resource-type"></a>tipo de recurso publicClient

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Especifica la configuración para que no sean Web App o la Api de Web. (por ejemplo, Mobile u otro pública cliente como una aplicación instalada que se ejecutan en un dispositivo de escritorio)

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Description |
|:---------------|:--------|:----------|
|redirectUris|Colección String| Especifica las direcciones URL que los tokens de usuario se envían a para el inicio de sesión o el redireccionamiento de los códigos de autorización de los URI que OAuth 2.0 y tokens de acceso se envían a. |

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.installedClient"
}-->

```json
{
  "redirectUris": ["String"]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "installedClient resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
