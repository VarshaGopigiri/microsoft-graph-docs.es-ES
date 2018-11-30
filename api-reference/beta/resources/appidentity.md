---
title: tipo de recurso appIdentity
description: Indica la identidad de la aplicación que realiza la acción o se ha cambiado. Incluye el identificador de aplicación, el nombre, el identificador de entidad de seguridad de servicio y el nombre. Se llama a este recurso por la API de directoryAudit
ms.openlocfilehash: 6fcbe8dbb1e17139111c5f1fa9e8681cd1b996a7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086964"
---
# <a name="appidentity-resource-type"></a>tipo de recurso appIdentity
Indica la identidad de la aplicación que realiza la acción o se ha cambiado. Incluye el identificador de aplicación, el nombre, el identificador de entidad de seguridad de servicio y el nombre. Se llama a este recurso por la API [directoryAudit](../api/directoryaudit-get.md)


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|appId|cadena|Hace referencia a los GUID único que representa el identificador de aplicación en Azure Active Directory.|
|displayName|String|Hace referencia al nombre de la aplicación que se muestra en el Portal de Azure.|
|servicePrincipalId|String|Hace referencia a los GUID único que indica el identificador de entidad de seguridad de servicio en Azure Active Directory para la aplicación correspondiente.|
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