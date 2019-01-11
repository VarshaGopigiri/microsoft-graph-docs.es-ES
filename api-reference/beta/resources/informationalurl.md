---
title: tipo de recurso informationalUrl
description: Información de perfil básico de la aplicación.
localization_priority: Normal
ms.openlocfilehash: 78fd03a2673b342d1a0c904f521fe5a0f8cba205
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816985"
---
# <a name="informationalurl-resource-type"></a>tipo de recurso informationalUrl

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Información de perfil básico de la aplicación.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Description |
|:---------------|:--------|:----------|
|de marketing|Cadena| Vínculo a la aplicación de la página de marketing. Por ejemplo: https://www.contoso.com/app/marketing |
|privacidad|Cadena| Vínculo a la declaración de privacidad de la aplicación. Por ejemplo: https://www.contoso.com/app/privacy |
|soporte técnico|Cadena| Vínculo a la página de soporte técnico de la aplicación. Por ejemplo: https://www.contoso.com/app/support |
|termsOfService|Cadena| Vínculo a los términos de la aplicación de instrucción de servicio. Por ejemplo: https://www.contoso.com/app/termsofservice |

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.informationalUrl"
}-->

```json
{
  "marketing": "String",
  "privacy": "String",
  "support": "String",
  "termsOfService": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "informationalUrl resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
