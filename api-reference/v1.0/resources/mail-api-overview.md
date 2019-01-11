---
title: Usar la API de REST de correo de Outlook
description: Microsoft Graph permite a la aplicación obtener acceso autorizado a los datos de correo de Outlook de un usuario de una cuenta personal o la organización.
localization_priority: Priority
ms.openlocfilehash: 7085f0316e27aabc54556ddfeb7c9934105b042d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805925"
---
# <a name="use-the-outlook-mail-rest-api"></a>Usar la API de REST de correo de Outlook

Microsoft Graph permite que su aplicación obtenga acceso autorizado a los datos de correo de Outlook de un usuario en una cuenta personal o de organización. Con los [permisos apropiados delegados o de la aplicación](/graph/permissions-reference), su aplicación puede tener acceso a los datos de correo del usuario que ha iniciado sesión o cualquier usuario en un espacio empresarial. Los datos de correo pueden estar en la nube en Exchange Online como parte de Office 365 o en Exchange local en una [implementación híbrida](/graph/hybrid-rest-support).

## <a name="using-the-mail-rest-api"></a>Uso de la API de REST de correo

Se realizan solicitudes de API de correo en nombre de un [usuario](../resources/user.md) que puede identificarse por la propiedad de **id.** de un usuario (un GUID único), la dirección de correo electrónico o el alias de acceso directo `me` para el usuario que ha iniciado sesión.

Los mensajes de correo electrónico están representados por el recurso [message](../resources/message.md) y organizados en una carpeta [mailFolder](../resources/mailfolder.md). Los mensajes y las carpetas de correo se identifican por su propiedad de **id.**, que puede obtenerse de las operaciones `GET`.

>**Nota:** En general, no se debe suponer que los id. **message** y **mailfolder** son únicos e inmutables dentro un buzón. Se podrían cambiar tras determinadas acciones como copiar, mover o enviar.

Los cuerpos del mensaje se pueden mostrar en formato de texto o HTML.

Puede usar los nombres de las carpetas conocidas como `Inbox`, `Drafts`, `SentItems`, o `DeletedItems` para identificar ciertas carpetas de correo que existen de forma predeterminada para todos los usuarios. Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).

Por ejemplo, puede obtener los mensajes en la carpeta **Elementos enviados** de Outlook del usuario ha iniciado sesión, sin obtener primero el identificador de carpeta:

```http
GET /me/mailFolders('SentItems')/messages?$select=sender,subject
```

## <a name="common-use-cases"></a>Casos de uso común

El recurso **message** expone propiedades como **categories**, **conversationId**, **flag** e **importance** que corresponden a las funciones disponibles en la interfaz de usuario, lo que permite a las aplicaciones automatizarse o integrarse con la experiencia de usuario integrada de Outlook.

La API de Microsoft Graph también proporciona métodos y acciones que admiten casos de uso común de mensajes.

| Casos de uso | Recursos de REST | Consulte también |
|:----------|:---------------|:---------|
| **Acciones centradas en el usuario** | | |
| Borrador, leer, responder, reenviar, enviar, actualizar o eliminar los mensajes | [message](../resources/message.md) | [Métodos de message](../resources/message.md#methods) |
| Delegar a otro usuario para enviar mensajes en nombre del propietario del buzón | [message](../resources/message.md) | Configuración de las propiedades **de** y **remitente** en un [mensaje](../resources/message.md) |
| Permitir que el usuario vea primero los mensajes más importantes | [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) | [Bandeja de entrada Prioritarios](../resources/manage-focused-inbox.md) |
| Agregar, obtener o eliminar datos adjuntos de un mensaje | [attachment](../resources/attachment.md), <br> [fileAttachment](../resources/fileattachment.md), <br> [itemAttachment](../resources/itemattachment.md), <br> [referenceAttachment](../resources/referenceattachment.md), <br> [message](../resources/message.md) | [Métodos de attachment](../resources/attachment.md#methods) |
| Obtener o actualizar la configuración regional, la zona horaria, el horario laboral o la respuesta automática de un usuario | [mailboxSettings](../resources/mailboxsettings.md), <br> [automaticRepliesSetting](../resources/automaticrepliessetting.md), <br> [localeInfo](../resources/localeinfo.md), <br> [workingHours](../resources/workinghours.md) | [Obtener la configuración del buzón del usuario](../api/user-get-mailboxsettings.md), <br> [Actualizar la configuración del buzón del usuario](../api/user-update-mailboxsettings.md), |
| Obtener sugerencias de correo electrónico de estado especial del resto de los destinatarios, como fuera de la oficina | [usuario](../resources/user.md), <br> [sugerencias de correo electrónico](../resources/mailtips.md) | [Obtener sugerencias de correo electrónico](../api/user-getmailtips.md) |
| **Administración de carpetas y correo** | | |
| Organizar los mensajes en una jerarquía de carpetas del correo | [mailFolder](../resources/mailfolder.md)  | [Métodos de mailFolder](../resources/mailfolder.md#methods) |
| Buscar y filtrar mensajes | [message](../resources/message.md) | [Parámetros de consulta](/graph/query-parameters)  |
| Obtener notificaciones de los cambios en los mensajes de una carpeta | [subscription](../resources/subscription.md) | [Trabajar con webhooks en Microsoft Graph](../resources/webhooks.md) |
| Sincronizar la jerarquía de carpetas del correo o los mensajes | [message](../resources/message.md) | [Obtener los cambios incrementales en los mensajes de una carpeta](/graph/delta-query-messages) |
| **Desarrollo de aplicaciones** | | |
| Agregar datos de aplicación personalizadas como encabezados de mensaje de Internet de un mensaje | [message](../resources/message.md) | Agregar datos personalizados a la propiedad **internetMessageHeaders** del mensaje. |
| Agregar datos personalizados de la aplicación a un mensaje utilizando extensiones | [openTypeExtension](../resources/opentypeextension.md), <br>[schemaExtension](../resources/schemaextension.md) | [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview) |
| Datos personalizados de acceso para las propiedades de MAPI de Outlook subexpuestas | [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md), <br> [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) | [Información general sobre las propiedades extendidas de Outlook](../resources/extended-properties-overview.md) |

## <a name="next-steps"></a>Siguientes pasos

La API de correo puede abrir nuevas formas de comunicarse con los usuarios:

- [Información general sobre la API de correo de Outlook](/graph/outlook-mail-concept-overview)
- Profundizar en los [métodos](../resources/message.md#methods), las [propiedades](../resources/message.md#properties) y las [relaciones](../resources/message.md#relationships) de los recursos [message](../resources/message.md) y [mailFolder](../resources/mailfolder.md).
- Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).

¿Necesita más ideas? Vea [cómo algunos de nuestros socios utilizan Microsoft Graph](https://developer.microsoft.com/graph/graph/examples#partners).
