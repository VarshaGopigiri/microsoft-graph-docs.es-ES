---
title: Crear y enviar mensajes de Outlook
description: Los correos electrónicos se representan mediante el recurso message en Microsoft Graph.
ms.openlocfilehash: 49670df0d5d735e412a0fd97e3404fab044f6f50
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092882"
---
# <a name="create-and-send-outlook-messages"></a>Crear y enviar mensajes de Outlook

Los correos electrónicos se representan mediante el recurso [message](/graph/api/resources/message?view=graph-rest-1.0) en Microsoft Graph.

De forma predeterminada, los mensajes se identifican por un identificador de entrada único en la propiedad **id**. Un proveedor de almacenamiento asigna a un mensaje un identificador de entidad cuando el mensaje se guarda inicialmente como un borrador o se envía. Ese identificador cambia cuando el mensaje se copia o se mueve a otra carpeta, almacenamiento o archivo .PST.

## <a name="creating-and-sending-mail"></a>Crear y enviar correo electrónico

En Outlook, puede crear y enviar un correo electrónico en la misma acción [sendMail](/graph/api/user-sendmail?view=graph-rest-1.0), o bien puede [crear](/graph/api/user-post-messages?view=graph-rest-1.0) un borrador, posteriormente [agregar contenido](/graph/api/message-update?view=graph-rest-1.0) y [enviar](/graph/api/message-send?view=graph-rest-1.0) el borrador.

De forma similar, cuando responde a un correo electrónico, puede crear y enviar la respuesta en la misma acción ([reply](/graph/api/message-reply?view=graph-rest-1.0), [reply-all](/graph/api/message-replyall?view=graph-rest-1.0) o [forward](/graph/api/message-forward?view=graph-rest-1.0)). O bien, puede crear un borrador de la respuesta ([reply](/graph/api/message-createreply?view=graph-rest-1.0), [reply-all](/graph/api/message-createreplyall?view=graph-rest-1.0) or [forward](/graph/api/message-createforward?view=graph-rest-1.0)), [agregar contenido](/graph/api/message-update?view=graph-rest-1.0) y [enviar](/graph/api/message-send?view=graph-rest-1.0) el borrador más tarde.

Para distinguir un borrador de un mensaje enviado mediante programación, consulte la propiedad **isDraft**.

De forma predeterminada, los borradores se guardan en la carpeta `Drafts` y los mensajes enviados en la carpeta `Sent Items`. Para mayor comodidad, puede identificar las carpetas Drafts y SentItems por sus [nombres de carpeta correspondientes conocidos](/graph/api/resources/mailfolder?view=graph-rest-1.0). Por ejemplo, puede hacer lo siguiente para [obtener los mensajes](/graph/api/user-list-messages?view=graph-rest-1.0) en la carpeta Drafts:

```http
GET /me/mailfolders('Drafts')
```

### <a name="body-format-and-malicious-script"></a>Formato de cuerpo y script malintencionado

<!-- Remove the following 2 sections from the message.md topics
-->

El cuerpo del mensaje puede ser HTML o texto, con HTML como el tipo de cuerpo del mensaje predeterminado que se devuelve en una respuesta GET.

Cuando [obtenga un mensaje](/graph/api/message-get?view=graph-rest-1.0), puede especificar el siguiente encabezado de solicitud para devolver las propiedades **body** y **uniqueBody** en el formato del texto:

```http
Prefer: outlook.body-content-type="text"
```

Puede especificar el siguiente encabezado o, simplemente omita el encabezado, para obtener el cuerpo del mensaje en formato HTML:

```http
Prefer: outlook.body-content-type="html"
```

Al especificar cualquier encabezado, una respuesta correcta incluirá el encabezado `Preference-Applied` correspondiente:

- Para las solicitudes de formato de texto: `Preference-Applied: outlook.body-content-type="text"`
- Para las solicitudes de formato HTML: `Preference-Applied: outlook.body-content-type="html"`

Si el cuerpo se muestra en HTML, de forma predeterminada, Outlook quita cualquier código HTML potencialmente peligroso (por ejemplo, JavaScript) insertado en la propiedad **body** antes de devolver el contenido del cuerpo en una respuesta REST.

Para obtener todo el contenido HTML original, incluya el siguiente encabezado de solicitud HTTP:

```http
Prefer: outlook.allow-unsafe-html
```

### <a name="differentiating-the-from-and-sender-properties"></a>Diferenciar de las propiedades from y sender

Cuando se redacta un mensaje, en la mayoría de los casos, Outlook establece las propiedades **from** y **sender** para el mismo usuario que haya iniciado sesión. Puede actualizar estas propiedades en las siguientes situaciones:

- La propiedad **from** se puede cambiar si el administrador de Exchange ha asignado los derechos **sendAs** del buzón a otros usuarios. El administrador puede realizar esta acción si selecciona **Permisos del buzón** del propietario del buzón en Azure Portal, o si usa el Centro de administración de Exchange o un cmdlet Add-ADPermission de Windows PowerShell. Después, puede configurar mediante programación la propiedad **from** para uno de los usuarios que tiene derechos **sendAs** de ese buzón.
- La propiedad **sender** se puede cambiar si el propietario del buzón ha delegado uno o más usuarios para que puedan enviar mensajes desde ese buzón. El propietario del buzón puede delegar en Outlook. Cuando un delegado envía un mensaje en nombre del propietario del buzón, Outlook establece la propiedad **sender** en la cuenta del delegado y la propiedad **from** sigue siendo el propietario del buzón. Mediante programación, puede configurar la propiedad **sender** para un usuario que tiene permisos de delegado en ese buzón.

## <a name="using-mailtips-to-check-recipient-status-and-save-time-preview"></a>Usar Sugerencias de correo electrónico para comprobar el estado del destinatario y ahorrar tiempo (versión preliminar)

Use [Sugerencias de correo electrónico](/graph/api/resources/mailtips?view=graph-rest-beta) para tomar decisiones inteligentes antes de enviar un correo electrónico.
Las sugerencias de correo electrónico pueden proporcionarle información, como que el buzón del destinatario está limitado a determinados remitentes o si se necesita aprobación para enviar un correo electrónico al destinatario.

## <a name="integrating-with--social-gesture-preview"></a>Integración con gesto de redes sociales "@" (versión preliminar)

Las @menciones son notificaciones para avisar a los usuarios si se les menciona en los mensajes. El recurso [mention](/graph/api/resources/mention?view=graph-rest-beta) permite a las aplicaciones configurar y obtener el gesto de redes sociales en línea común, el prefijo "@", en los mensajes de correo electrónico.
Puede:

- Crear @menciones al [crear un mensaje](/graph/api/user-post-messages?view=graph-rest-beta#request-2)
- [Obtener todos los mensajes del buzón de un usuario que contiene una @mención al usuario](/graph/api/user-list-messages?view=graph-rest-beta#request-2)
- [Obtener todas las @menciones en un mensaje](/graph/api/message-get?view=graph-rest-beta#request-2)

## <a name="other-shared-capabilities"></a>Otras funcionalidades compartidas

Aproveche las ventajas de las siguientes funciones comunes que se comparten entre las entidades de Microsoft Graph:

- Suscríbase a las [notificaciones de cambios](/graph/api/resources/webhooks?view=graph-rest-1.0) en los mensajes cuando se produce uno o varios tipos de cambios, como la creación o actualización del mensaje.
- [Realice un seguimiento de los cambios incrementales en los mensajes de una carpeta](delta-query-messages.md).
- Cree [extensiones abiertas](extensibility-overview.md#open-extensions) o [extensiones de esquema](extensibility-overview.md#schema-extensions) para agregar datos personalizados a una instancia de mensaje.
- Cree [propiedades extendidas](/graph/api/resources/extended-properties-overview?view=graph-rest-1.0) en una instancia de mensaje para almacenar datos personalizados de las propiedades MAPI de Outlook cuando estas propiedades aún no están expuestas en los metadatos de la API de Microsoft Graph.

## <a name="next-steps"></a>Siguientes pasos

Obtenga más información sobre:

- [¿Por qué integrar con el correo de Outlook?](outlook-mail-concept-overview.md)
- [Usar la API de correo](/graph/api/resources/mail-api-overview?view=graph-rest-1.0) y sus [casos de uso](/graph/api/resources/mail-api-overview?view=graph-rest-1.0#common-use-cases) en Microsoft Graph v1.0.
