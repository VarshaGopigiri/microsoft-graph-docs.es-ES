---
title: Tipo de recurso localeInfo
description: Información sobre la configuración regional, como el idioma preferido y el país o región del usuario que inició sesión.
ms.openlocfilehash: 5dae464a4931fb094ae47cce600a95d55c6c3f93
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089467"
---
# <a name="localeinfo-resource-type"></a>Tipo de recurso localeInfo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Información sobre la configuración regional, como el idioma preferido y el país o región del usuario que inició sesión.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|configuración regional|string|Representación de la configuración regional del usuario, que incluye el idioma preferido y el país o región del usuario. Por ejemplo, "es-es". El componente de idioma sigue códigos de dos letras, tal y como se define en [ISO 639-1](https://www.iso.org/iso/home/standards/language_codes.htm), y el componente de país sigue códigos de dos letras, tal y como se define en [ISO 3166-1 alpha-2](https://www.iso.org/iso/country_codes.htm).|
|displayName|string|Nombre que representa la configuración regional del usuario en lenguaje natural, por ejemplo, "Inglés (Estados Unidos)".|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.localeInfo"
}-->

```json
{
  "locale": "string",
  "displayName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "localeInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->