---
title: tipo de recurso agreementAcceptance
description: Representa el estado actual de un usuario dentro de ámbito de condiciones personalizable de una compañía de uso con tecnología de Azure Active Directory (AD Azure).
localization_priority: Normal
ms.openlocfilehash: b1c8a5e40fe6a12daf23566ae902ddf61f3ee4df
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828288"
---
# <a name="agreementacceptance-resource-type"></a>tipo de recurso agreementAcceptance

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa el estado actual de un usuario dentro de ámbito de condiciones personalizable de una compañía de uso con tecnología de Azure Active Directory (AD Azure).

<!--
## Methods

| Method       | Return Type | Description |
|:-------------|:------------|:------------|
| [Get agreementAcceptance](../api/agreementacceptance-get.md) | [agreementAcceptance](agreementacceptance.md) | Read properties and relationships of agreementAcceptance object. |
| [Update](../api/agreementacceptance-update.md) | [agreementAcceptance](agreementacceptance.md) | Update an **agreementAcceptance** object. |
| [Delete](../api/agreementacceptance-delete.md) | None | Delete an **agreementAcceptance** object. |
-->

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo        | Description |
|:-------------|:------------|:------------|
|agreementFileId|Cadena|Identificador del archivo de contrato aceptado por el usuario.|
|agreementId|Cadena|Identificador del contrato.|
|id|Cadena| Solo lectura.|
|recordedDateTime|DateTimeOffset|El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|state|string| Los valores posibles son: `accepted` y `declined`.|
|userDisplayName|Cadena|Nombre para mostrar del usuario cuando se registró la aceptación.|
|userEmail|Cadena|Correo electrónico del usuario cuando se registró la aceptación.|
|userId|Cadena|Identificador del usuario que ha aceptado el contrato.|
|userPrincipalName|Cadena|UPN del usuario cuando se registró la aceptación.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.agreementAcceptance"
}-->

```json
{
  "agreementFileId": "String",
  "agreementId": "String",
  "id": "String (identifier)",
  "recordedDateTime": "String (timestamp)",
  "state": "string",
  "userDisplayName": "String",
  "userEmail": "String",
  "userId": "String",
  "userPrincipalName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "agreementAcceptance resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
