---
title: tipo de recurso keyCredential
description: Contiene una credencial de clave asociada con una aplicación o una entidad de seguridad de servicio. La propiedad **keyCredentials** de las entidades de la aplicación y servicePrincipal es una colección de **keyCredential**.
ms.openlocfilehash: d4509360c0425c255566b9f77b9ecd96cf349dec
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083462"
---
# <a name="keycredential-resource-type"></a>tipo de recurso keyCredential

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Contiene una credencial de clave asociada con una aplicación o una entidad de seguridad de servicio. La propiedad **keyCredentials** de las entidades de la [aplicación](application.md) y [servicePrincipal](serviceprincipal.md) es una colección de **keyCredential**.


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.keyCredential"
}-->

```json
{
  "customKeyIdentifier": "binary",
  "endDateTime": "String (timestamp)",
  "keyId": "guid",
  "startDateTime": "String (timestamp)",
  "type": "string",
  "usage": "string",
  "key": "binary"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|customKeyIdentifier|Binario| Identificador de clave personalizado |
|endDateTime|DateTimeOffset|La fecha y hora de caducidad de la credencial. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|Id|Guid|Identificador único (GUID) de la clave.|
|startDateTime|DateTimeOffset|La fecha y la hora en que la credencial es válida. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|type|String|El tipo de credencial clave; Por ejemplo, "Simétrico".|
|uso|String|Una cadena que describa el objetivo para el que se puede usar la clave; Por ejemplo, "comprobar".|
|key|Binary|            |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "keyCredential resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->