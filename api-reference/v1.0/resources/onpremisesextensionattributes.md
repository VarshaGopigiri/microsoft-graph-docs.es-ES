---
title: tipo de recurso onPremisesExtensionAttributes
description: La propiedad **onPremisesExtensionAttributes** de la entidad de usuario contiene quince las propiedades de atributo de extensión personalizada. Para un usuario **onPremisesSyncEnabled** , este conjunto de propiedades se han usado en Active Directory local y sincronizado con Azure AD y es de sólo lectura. Para un usuario solo en la nube (donde **onPremisesSyncEnabled** es false), estas propiedades se pueden establecer durante la creación o actualizar.
localization_priority: Normal
ms.openlocfilehash: c0cb765efe9e94c8254e45eaa9d55bc16382f6d2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824748"
---
# <a name="onpremisesextensionattributes-resource-type"></a>tipo de recurso onPremisesExtensionAttributes

La propiedad **onPremisesExtensionAttributes** de la entidad de [usuario](user.md) contiene quince las propiedades de atributo de extensión personalizada. Para un usuario **onPremisesSyncEnabled** , este conjunto de propiedades se han usado en Active Directory local y sincronizado con Azure AD y es de sólo lectura. Para un usuario solo en la nube (donde **onPremisesSyncEnabled** es false), estas propiedades se pueden establecer durante la creación o actualizar.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|extensionAttribute1|Cadena| Primer atributo de extensión personalizable. |
|extensionAttribute2|Cadena| Segundo atributo de extensión personalizable. |
|extensionAttribute3|Cadena| Tercer atributo de extensión personalizable. |
|extensionAttribute4|Cadena| Cuarto atributo de extensión personalizable. |
|extensionAttribute5|Cadena| Atributo de extensión personalizable quinto. |
|extensionAttribute6|Cadena| Atributo de extensión personalizable sexto. |
|extensionAttribute7|Cadena| Séptimo atributo de extensión personalizable. |
|extensionAttribute8|Cadena| Atributo de extensión personalizable octavo. |
|extensionAttribute9|Cadena| Noveno atributo de extensión personalizable. |
|extensionAttribute10|Cadena| Décimo atributo de extensión personalizable. |
|extensionAttribute11|Cadena| Atributo de extensión undécima personalizable. |
|extensionAttribute12|Cadena| Atributo de extensión duodécima personalizable. |
|extensionAttribute13|Cadena| Atributo de extensión Decimotercera personalizable. |
|extensionAttribute14|Cadena| Atributo de extensión decimocuarta personalizable. |
|extensionAttribute15|Cadena| Atributo de extensión decimoquinta personalizable. |

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
