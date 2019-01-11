---
title: tipo de recurso passwordCredential
description: Contiene una credencial de contraseña asociada con una aplicación o un servicio de entidad de seguridad. La propiedad **passwordCredentials** de la entidad servicePrincipal y de la entidad de la aplicación es una colección de **passwordCredential**.
localization_priority: Normal
ms.openlocfilehash: 5cb995c00a7dcfcfb4bda331e24dcb4d732f04f9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814444"
---
# <a name="passwordcredential-resource-type"></a>tipo de recurso passwordCredential

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Contiene una credencial de contraseña asociada con una aplicación o un servicio de entidad de seguridad. La propiedad **passwordCredentials** de la entidad [servicePrincipal](serviceprincipal.md) y de la entidad de la [aplicación](application.md) es una colección de **passwordCredential**.


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.passwordCredential"
}-->

```json
{
  "customKeyIdentifier": "binary",
  "endDateTime": "String (timestamp)",
  "keyId": "guid",
  "startDateTime": "String (timestamp)",
  "secretText": "string",
  "hint": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|customKeyIdentifier|Binario|            |
|endDateTime|DateTimeOffset|La fecha y hora de caducidad de la contraseña. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|Id|Guid|            |
|startDateTime|DateTimeOffset|La fecha y la hora en que la contraseña es válida. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|secretText|Cadena| Las contraseñas deben ser 16-64 caracteres de longitud |
|Sugerencia|String|  |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "passwordCredential resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
