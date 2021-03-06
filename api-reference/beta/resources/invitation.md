---
title: administrador de invitaciones
description: 'Use el Administrador de invitaciones para crear una invitación para agregar un usuario externo a la organización. '
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 72ff2ca13a0de314697961504da9a4203afdb2b1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981052"
---
# <a name="invitation-manager"></a>administrador de invitaciones

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Use el Administrador de invitaciones para crear una invitación para agregar un usuario externo a la organización. 

El proceso de invitación sigue el flujo siguiente:

* Se crea una invitación
* Se envía una invitación al usuario invitado (que contiene un vínculo de invitación)
* El usuario invitado hace clic en el vínculo de la invitación, inicia sesión, canjea la invitación y finaliza la creación de la entidad de usuario que representa al usuario invitado
* Se redirige al usuario a una página específica después del canje

Al crear una invitación, se devolverá una dirección URL de canje en la respuesta (*inviteRedeemUrl*). La API para crear la invitación puede enviar automáticamente un correo electrónico con la dirección URL de canje al usuario invitado, al establecer *sendInvitationMessage* en true. También puede personalizar el mensaje que se enviará al usuario invitado. En su lugar, si quiere enviar la dirección URL de canje a través de otros medios, puede establecer *sendInvitationMessage* en false y usar la dirección URL de canje de la respuesta para elaborar su propia comunicación. Actualmente, no hay ninguna API para realizar el proceso de canje. El usuario invitado tiene que hacer clic en el vínculo *inviteRedeemUrl* enviado en la comunicación en el paso anterior y pasar por el proceso de canje interactivo en un explorador. Una vez completado, el usuario invitado se convierte en usuario externo de la organización.


## <a name="methods"></a>Métodos
| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Crear invitación](../api/invitation-post.md) | invitation | Escriba las propiedades y relaciones del objeto de invitación.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|invitedUserDisplayName|String|Nombre para mostrar del usuario al que se invita.|
|invitedUserEmailAddress|String|Dirección de correo electrónico del usuario al que se invita. Necesario.|
|invitedUserMessageInfo|[invitedUserMessageInfo](invitedusermessageinfo.md)|Configuración adicional para el mensaje que se envía al usuario invitado, incluidos la personalización del texto del mensaje, el idioma y la lista de destinatarios CC.|
|sendInvitationMessage|Booleano|Indica si se debe enviar un correo electrónico al usuario al que se invita o no. El valor predeterminado es false.|
|inviteRedirectUrl|String|La dirección URL a la que se redirigirá al usuario una vez que se canjee la invitación. Necesario.|
|inviteRedeemUrl|String|La dirección URL que puede usar el usuario para canjear su invitación. Solo lectura|
|invitedUserType|String|userType del usuario al que se invita. El valor predeterminado es Guest. Puede invitar como Member si es administrador de la empresa. |
|status|String|El estado de la invitación. Valores posibles: PendingAcceptance, Completed, InProgress y Error|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|invitedUser|[User](user.md)|El usuario creado como parte de la creación de la invitación. Solo lectura|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.invitations" } -->
```json
{
  "invitedUserDisplayName": "string",
  "invitedUserEmailAddress": "string",
  "invitedUserMessageInfo": {"@odata.type": "microsoft.graph.invitedUserMessageInfo"},
  "sendInvitationMessage": false,
  "inviteRedirectUrl": "string",
  "inviteRedeemUrl": "string",
  "status": "string",

  "invitedUser": [{"@odata.type": "microsoft.graph.user"}]
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2016-22-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "invitation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
