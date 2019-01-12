---
title: 'message: forward'
description: 'Reenviar un mensaje, agregar un comentario o modificar las propiedades actualizables  '
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 18394c29d57c090811bca9a70371c451b090fb26
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27971490"
---
# <a name="message-forward"></a>message: forward

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Reenviar un mensaje, agregar un comentario o modificar las propiedades actualizables  
todo en uno **desviar** llamadas. El mensaje se guarda en la carpeta Elementos enviados.

Como alternativa, puede [crear un borrador de mensaje hacia delante](../api/message-createforward.md) para incluir un comentario o actualizar las propiedades del mensaje y, a continuación, [Enviar](../api/message-send.md) el mensaje de borrador.

**Nota**

- Puede especificar un comentario o la propiedad **body** de la `message` parámetro. Si se especifica tanto devolverá un error HTTP 400 Solicitud incorrecta.
- Debe especificar el `toRecipients` parámetro o la propiedad **toRecipients** de la `message` parámetro. Si se especifica tanto o especificar ninguno devolverá un error HTTP 400 Solicitud incorrecta.

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
POST /me/messages/{id}/forward
POST /users/{id | userPrincipalName}/messages/{id}/forward
POST /me/mailFolders/{id}/messages/{id}/forward
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/forward
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio. |
| Content-Type | string  | Naturaleza de los datos en el cuerpo de una entidad. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro    | Tipo   |Descripción|
|:---------------|:--------|:----------|
|comment|String|Comentario que se va a incluir. Puede ser una cadena vacía.|
|toRecipients|Colección [recipient](../resources/recipient.md)|La lista de destinatarios.|
|mensaje|[message](../resources/message.md)|Cualquier propiedad grabable para actualizar en el mensaje de respuesta.|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
En el ejemplo siguiente se establece la propiedad **isDeliveryReceiptRequested** en true, se agrega un comentario y reenvía el mensaje.
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "message_forward"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages/AAMkADA1MTAAAH5JaLAAA=/forward
Content-Type: application/json

{
  "message":{  
    "isDeliveryReceiptRequested": true,
    "toRecipients":[
      {
        "emailAddress": {
          "address":"danas@contoso.onmicrosoft.com",
          "name":"Dana Swope"
        }
      }
     ]
  },
  "comment": "Dana, just want to make sure you get this." 
}
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
  "description": "message: forward",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
