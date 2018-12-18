---
title: 'mensaje: cancelar su suscripción'
description: Envía una solicitud de correo electrónico en nombre del usuario que ha iniciado sesión para cancelar la suscripción a una lista de distribución de correo electrónico. Utiliza la información de la `List-Unsubscribe` encabezado.
author: angelgolfer-ms
ms.openlocfilehash: e516a8aa68bde02f056e503da9c85d4e7a6f62fc
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27357228"
---
# <a name="message-unsubscribe"></a>mensaje: cancelar su suscripción

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Envía una solicitud de correo electrónico en nombre del usuario que ha iniciado sesión para cancelar la suscripción a una lista de distribución de correo electrónico. Utiliza la información de la `List-Unsubscribe` encabezado.

Remitentes de mensajes pueden usar listas de correo de una manera fácil de usar mediante la inclusión de una opción para los destinatarios para excluir. Puede hacerlo mediante la especificación de la `List-Unsubscribe` encabezado en cada mensaje que sigue a [RFC 2369](https://www.faqs.org/rfcs/rfc2369.html).

**Nota** En concreto, para que la acción **Cancelar su suscripción** para que funcione, debe especificar el remitente `mailto:` y no basados en la dirección URL de información de cancelación de suscripción.

Configuración de ese encabezado también establecería la propiedad **unsubscribeEnabled** de la instancia de [mensaje](../resources/message.md) a `true`y la propiedad **unsubscribeData** para los datos del encabezado.

Si la propiedad **unsubscribeEnabled** de un mensaje es `true`, puede usar la acción de **cancelación de suscripción** para cancelar la suscripción al usuario de mensajes futuros similar como administrada por el remitente del mensaje.

Una acción correcta **Cancelar su suscripción** , mueve el mensaje a la carpeta **Elementos eliminados** . La exclusión real del usuario de la distribución de correo futuras se administra por el remitente.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Mail.Send    |
|Delegado (cuenta personal de Microsoft) | Mail.Send    |
|Aplicación | Mail.Send |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/messages/{id}/unsubscribe
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Type | Descripción|
|:---------------|:--------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
Aquí tiene un ejemplo de cómo llamar a esta API.
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "message_unsubscribe"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages/{id}/unsubscribe
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: unsubscribe",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
