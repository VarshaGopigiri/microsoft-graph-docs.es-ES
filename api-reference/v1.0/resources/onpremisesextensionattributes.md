---
title: tipo de recurso onPremisesExtensionAttributes
description: La propiedad **onPremisesExtensionAttributes** de la entidad de usuario contiene quince las propiedades de atributo de extensión personalizada. Para un usuario **onPremisesSyncEnabled** , este conjunto de propiedades se han usado en Active Directory local y sincronizado con Azure AD y es de sólo lectura. Para un usuario solo en la nube (donde **onPremisesSyncEnabled** es false), estas propiedades se pueden establecer durante la creación o actualizar.
ms.openlocfilehash: e5a56b5a846cf48cfc819b6d884689be10d6992e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030834"
---
# <a name="onpremisesextensionattributes-resource-type"></a>tipo de recurso onPremisesExtensionAttributes

La propiedad **onPremisesExtensionAttributes** de la entidad de [usuario](user.md) contiene quince las propiedades de atributo de extensión personalizada. Para un usuario **onPremisesSyncEnabled** , este conjunto de propiedades se han usado en Active Directory local y sincronizado con Azure AD y es de sólo lectura. Para un usuario solo en la nube (donde **onPremisesSyncEnabled** es false), estas propiedades se pueden establecer durante la creación o actualizar.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|extensionAttribute1|String| Primer atributo de extensión personalizable. |
|extensionAttribute2|String| Segundo atributo de extensión personalizable. |
|extensionAttribute3|String| Tercer atributo de extensión personalizable. |
|extensionAttribute4|String| Cuarto atributo de extensión personalizable. |
|extensionAttribute5|String| Atributo de extensión personalizable quinto. |
|extensionAttribute6|String| Atributo de extensión personalizable sexto. |
|extensionAttribute7|String| Séptimo atributo de extensión personalizable. |
|extensionAttribute8|String| Atributo de extensión personalizable octavo. |
|extensionAttribute9|String| Noveno atributo de extensión personalizable. |
|extensionAttribute10|String| Décimo atributo de extensión personalizable. |
|extensionAttribute11|String| Atributo de extensión undécima personalizable. |
|extensionAttribute12|String| Atributo de extensión duodécima personalizable. |
|extensionAttribute13|String| Atributo de extensión Decimotercera personalizable. |
|extensionAttribute14|String| Atributo de extensión decimocuarta personalizable. |
|extensionAttribute15|String| Atributo de extensión decimoquinta personalizable. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onPremisesExtensionAttributes"
}-->


```json
{
      "extensionAttribute1": "string",
      "extensionAttribute2": "string",
      "extensionAttribute3": "string",
      "extensionAttribute4": "string",
      "extensionAttribute5": "string",
      "extensionAttribute6": "string",
      "extensionAttribute7": "string",
      "extensionAttribute8": "string",
      "extensionAttribute9": "string",
      "extensionAttribute10": "string",
      "extensionAttribute11": "string",
      "extensionAttribute12": "string",
      "extensionAttribute13": "string",
      "extensionAttribute14": "string",
      "extensionAttribute15": "string"
  }

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onPremisesExtensionAttributes resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->