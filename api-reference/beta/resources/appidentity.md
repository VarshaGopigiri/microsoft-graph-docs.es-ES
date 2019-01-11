---
title: tipo de recurso appIdentity
description: Indica la identidad de la aplicación que realiza la acción o se ha cambiado. Incluye el identificador de aplicación, el nombre, el identificador de entidad de seguridad de servicio y el nombre. Se llama a este recurso por la API de directoryAudit
localization_priority: Normal
ms.openlocfilehash: ec61782fca0ab4004fab5a55bd4774c0d64afb3a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855786"
---
# <a name="appidentity-resource-type"></a>tipo de recurso appIdentity
Indica la identidad de la aplicación que realiza la acción o se ha cambiado. Incluye el identificador de aplicación, el nombre, el identificador de entidad de seguridad de servicio y el nombre. Se llama a este recurso por la API [directoryAudit](../api/directoryaudit-get.md)


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|appId|cadena|Hace referencia a los GUID único que representa el identificador de aplicación en Azure Active Directory.|
|displayName|Cadena|Hace referencia al nombre de la aplicación que se muestra en el Portal de Azure.|
|servicePrincipalId|Cadena|Hace referencia a los GUID único que indica el identificador de entidad de seguridad de servicio en Azure Active Directory para la aplicación correspondiente.|
|servicePrincipalName|cadena|Hace referencia al nombre Principal de servicio es el nombre de la aplicación en el inquilino. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.appIdentity"
}-->

```json
{
  "appId": "String",
  "displayName": "String",
  "servicePrincipalId": "String",
  "servicePrincipalName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "appIdentity resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
