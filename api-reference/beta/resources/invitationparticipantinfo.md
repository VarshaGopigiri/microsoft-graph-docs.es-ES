---
title: tipo de recurso invitationParticipantInfo
description: El **InvitationParticipant** se usa para representar un conjunto de identidades asociado con una invitación a una conversación y proporciona los parámetros de invitación adicionales.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: 7a6fb418b7076b0f0a42dc05b6afe71dcda6a71e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27865005"
---
# <a name="invitationparticipantinfo-resource-type"></a>tipo de recurso invitationParticipantInfo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El **InvitationParticipant** se usa para representar un conjunto de identidades asociado con una invitación a una conversación y proporciona los parámetros de invitación adicionales.

## <a name="properties"></a>Propiedades

| Propiedad                           | Tipo                          | Description                                                                          |
| :--------------------------------- | :---------------------------- | :----------------------------------------------------------------------------------- |
| endpointType                       | String                        | Los valores posibles son: `default` y `voicemail`. |
| identity                           | [identitySet](identityset.md) | El [identitySet](identityset.md) asociado con esta invitación.                   |
| languageId                         | Cadena                        | La cadena de referencia cultural del idioma.                                                                                     |
| región                             | Cadena                        | Región del participante.                                                           |
| replacesCallId                     | Cadena                        | Opcional. La llamada que la idenity destino actualmente es una parte de. Una vez que el participante se agrega, se eliminará esta llamada. |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.invitationParticipantInfo"
}-->
```json
{
  "endpointType": "default | voicemail",
  "identity": {"@odata.type": "#microsoft.graph.identitySet"},
  "languageId": "String",
  "region": "String",
  "replacesCallId": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "invitationParticipantInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
