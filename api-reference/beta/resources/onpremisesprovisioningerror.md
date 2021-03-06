---
title: tipo de recurso onPremisesProvisioningError
description: Representa los errores de sincronización de Active directory para el usuario, grupo o entidades organizativas de contacto cuando sincronización local de directorios en Azure Active Directory.
localization_priority: Normal
ms.openlocfilehash: 1ea9efcd4d9db5cf7cc5b8f0a18b35345d06c3fe
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27817741"
---
# <a name="onpremisesprovisioningerror-resource-type"></a>tipo de recurso onPremisesProvisioningError

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa los errores de sincronización de Active directory para las entidades de [usuario](user.md), [grupo](group.md)o [contacto organizativa](orgcontact.md) cuando sincronización local de directorios en Azure Active Directory.

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|categoría|String| Categoría del error de aprovisionamiento. Nota: Actualmente, hay un único valor posible. Valor posible: *PropertyConflict* - indica un valor de propiedad no es único. Otros objetos contienen el mismo valor para la propiedad. |
|occurredDateTime|DateTimeOffset| La fecha y la hora a la que se produjo el error. |
|propertyCausingError|Cadena| Nombre de la propiedad de Active directory que provoca el error. Los valores posibles actuales: *UserPrincipalName* o *ProxyAddress* |
|valor|String| Valor de la propiedad que provoca el error. |

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onPremisesProvisioningError"
}-->

```json
{
  "category": "String",
  "occurredDateTime": "String (timestamp)",
  "propertyCausingError": "String",
  "value": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onPremisesProvisioningError resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
