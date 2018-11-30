---
title: tipo de recurso informationalUrl
description: Información de perfil básico de la aplicación.
ms.openlocfilehash: c8a13f4f686fe3b6ffd460ab05342b7da9b4a808
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088200"
---
# <a name="informationalurl-resource-type"></a>tipo de recurso informationalUrl

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Información de perfil básico de la aplicación.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|de marketing|String| Vínculo a la aplicación de la página de marketing. Por ejemplo: https://www.contoso.com/app/marketing |
|privacidad|String| Vínculo a la declaración de privacidad de la aplicación. Por ejemplo: https://www.contoso.com/app/privacy |
|soporte técnico|String| Vínculo a la página de soporte técnico de la aplicación. Por ejemplo: https://www.contoso.com/app/support |
|termsOfService|String| Vínculo a los términos de la aplicación de instrucción de servicio. Por ejemplo: https://www.contoso.com/app/termsofservice |

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