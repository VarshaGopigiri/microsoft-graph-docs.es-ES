---
title: Actualizar mensaje
description: Actualice las propiedades del objeto de mensaje.
author: angelgolfer-ms
localization_priority: Priority
ms.openlocfilehash: 24705fbf986f9ecf1142e66d189ae2071e1be223
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884787"
---
# <a name="update-message"></a>Actualizar mensaje

Actualizar las propiedades de un objeto de mensaje.
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Mail.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | Mail.ReadWrite    |
|Aplicación | Mail.ReadWrite |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/messages/{id}
PATCH /users/{id | userPrincipalName}/messages/{id}
PATCH /me/mailFolders/{id}/messages/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio. |
| Content-Type | string  | Naturaleza de los datos en el cuerpo de una entidad. Obligatorio. |
## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado. Las siguientes propiedades se pueden actualizar.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|bccRecipients|Recipient|Los destinatarios de CCO del mensaje. |
|body|ItemBody|El cuerpo del mensaje. Actualizable sólo si isDraft = true.|
|categories|Colección String|Las categorías asociadas al mensaje.|
|ccRecipients|Colección Recipient|Los destinatarios de Cc del mensaje. |
|from|Recipient|El propietario del buzón y el remitente del mensaje. Debe corresponder con el buzón real que se usa.|
|importance|Cadena|La importancia del mensaje. Los valores posibles son: `Low`, `Normal`, `High`.|
|inferenceClassification | Cadena | La clasificación del mensaje para el usuario, basándose en la relevancia inferida o importancia, o en un reemplazo explícito. Los valores posibles son: `focused` o `other`. |
|internetMessageId |String |El identificador del mensaje en el formato especificado por [RFC2822](https://www.ietf.org/rfc/rfc2822.txt). Actualizable sólo si isDraft = true.|
|isDeliveryReceiptRequested|Booleano|Indica si se solicita confirmación de lectura para el mensaje.|
|isRead|Booleano|Indica si se ha leído el mensaje.|
|isReadReceiptRequested|Booleano|Indica si se solicita confirmación de lectura para el mensaje.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md)| La colección de propiedades extendidas de varios valores definidos para el mensaje. Admite valores NULL.|
|replyTo|Colección Recipient|Las direcciones de correo electrónico que se utilizan al responder. Actualizable sólo si isDraft = true.|
|sender|Recipient|La cuenta que se utiliza realmente para generar el mensaje. Actualizable cuando se envía un mensaje desde un [buzón compartido](https://docs.microsoft.com/en-us/exchange/collaboration/shared-mailboxes/shared-mailboxes)o enviar un mensaje como un [delegado](https://support.office.com/en-us/article/allow-someone-else-to-manage-your-mail-and-calendar-41c40c04-3bd1-4d22-963a-28eafec25926). En cualquier caso, el valor debe corresponder al buzón real que se usa.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md)| La colección de propiedades extendidas de valor único definido para el mensaje. Admite valores NULL.|
|subject|Cadena|El asunto del mensaje. Actualizable sólo si isDraft = true.|
|toRecipients|Colección Recipient|Los destinatarios para el mensaje.|

Dado que el recurso **message** admite [extensiones](/graph/extensibility-overview), puede utilizar la operación `PATCH` para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia **message** existente.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [message](../resources/message.md) actualizado en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "update_message"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/messages/{id}
Content-type: application/json
Content-length: 248

{
  "subject": "subject-value",
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "inferenceClassification": "other"
}
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value",
  "inferenceClassification": "other"
}
```

## <a name="see-also"></a>Vea también

- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)](/graph/extensibility-open-users)
<!--
- [Add custom data to groups using schema extensions (preview)](/graph/extensibility-schema-groups)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update message",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
