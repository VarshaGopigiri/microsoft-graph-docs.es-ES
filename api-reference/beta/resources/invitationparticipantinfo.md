---
title: tipo de recurso invitationParticipantInfo
description: El **InvitationParticipant** se usa para representar un conjunto de identidades asociado con una invitación a una conversación y proporciona los parámetros de invitación adicionales.
author: VinodRavichandran
ms.openlocfilehash: f833fcd0c555dfcc88da4027313ed7f40da81428
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380488"
---
# <a name="invitationparticipantinfo-resource-type"></a>tipo de recurso invitationParticipantInfo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El **InvitationParticipant** se usa para representar un conjunto de identidades asociado con una invitación a una conversación y proporciona los parámetros de invitación adicionales.

## <a name="properties"></a>Propiedades

| Propiedad                           | Tipo                          | Descripción                                                                          |
| :--------------------------------- | :---------------------------- | :----------------------------------------------------------------------------------- |
| endpointType                       | String                        | Los valores posibles son: `default` y `voicemail`. |
| identity                           | [identitySet](identityset.md) | El [identitySet](identityset.md) asociado con esta invitación.                   |
| languageId                         | String                        | La cadena de referencia cultural del idioma.                                                                                     |
| región                             | String                        | Región del participante.                                                           |
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
