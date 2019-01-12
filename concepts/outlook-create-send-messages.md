---
title: Automatizar la creación, el envío y el procesamiento de mensajes
description: Los correos electrónicos se representan mediante el recurso message en Microsoft Graph.
author: angelgolfer-ms
localization_priority: Priority
ms.prod: outlook
ms.openlocfilehash: 160db6aae079d90f1ce20640429181cdbe6a4da5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27927614"
---
# <a name="automate-creating-sending-and-processing-messages"></a><span data-ttu-id="4263d-103">Automatizar la creación, el envío y el procesamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="4263d-103">Automate creating, sending, and processing messages</span></span>

<span data-ttu-id="4263d-104">Los correos electrónicos se representan mediante el recurso [message](/graph/api/resources/message?view=graph-rest-1.0) en Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="4263d-104">Emails are represented by the [message](/graph/api/resources/message?view=graph-rest-1.0) resource in Microsoft Graph.</span></span>

<span data-ttu-id="4263d-105">De forma predeterminada, los mensajes se identifican por un identificador de entrada único en la propiedad **id**.</span><span class="sxs-lookup"><span data-stu-id="4263d-105">By default, messages are identified by a unique entry ID in the **id** property.</span></span> <span data-ttu-id="4263d-106">Cuando se crea y se guarda inicialmente como borrador un mensaje o se envía, el proveedor de almacén asigna al mensaje un id. de entrada.</span><span class="sxs-lookup"><span data-stu-id="4263d-106">When a message is initially created and saved as a draft or sent, the store provider assigns the message an entry ID.</span></span> <span data-ttu-id="4263d-107">De manera predeterminada, ese id. cambia cuando el mensaje se copia o se mueve a otra carpeta, almacén o archivo .PST.</span><span class="sxs-lookup"><span data-stu-id="4263d-107">By default, that ID changes when the message is copied or moved to another folder, store, or .PST file.</span></span> <span data-ttu-id="4263d-108">Se hace referencia el mensaje con su Id. actual para un procesamiento adicional.</span><span class="sxs-lookup"><span data-stu-id="4263d-108">You reference the message by its current ID for further processing.</span></span>

## <a name="creating-and-sending-mail"></a><span data-ttu-id="4263d-109">Crear y enviar correo electrónico</span><span class="sxs-lookup"><span data-stu-id="4263d-109">Creating and sending mail</span></span>

<span data-ttu-id="4263d-110">En Outlook, puede crear y enviar un correo electrónico en la misma acción [sendMail](/graph/api/user-sendmail?view=graph-rest-1.0), o bien puede [crear](/graph/api/user-post-messages?view=graph-rest-1.0) un borrador, posteriormente [agregar contenido](/graph/api/message-update?view=graph-rest-1.0) y [enviar](/graph/api/message-send?view=graph-rest-1.0) el borrador.</span><span class="sxs-lookup"><span data-stu-id="4263d-110">In Outlook, you can create and send an email in the same [sendMail](/graph/api/user-sendmail?view=graph-rest-1.0) action, or you can [create](/graph/api/user-post-messages?view=graph-rest-1.0) a draft, subsequently [add content](/graph/api/message-update?view=graph-rest-1.0) and [send](/graph/api/message-send?view=graph-rest-1.0) the draft.</span></span>

<span data-ttu-id="4263d-111">De forma similar, cuando responde a un correo electrónico, puede crear y enviar la respuesta en la misma acción ([reply](/graph/api/message-reply?view=graph-rest-1.0), [reply-all](/graph/api/message-replyall?view=graph-rest-1.0) o [forward](/graph/api/message-forward?view=graph-rest-1.0)).</span><span class="sxs-lookup"><span data-stu-id="4263d-111">Similarly, when responding to an email, you can create and send the response in the same action ([reply](/graph/api/message-reply?view=graph-rest-1.0), [reply-all](/graph/api/message-replyall?view=graph-rest-1.0), or [forward](/graph/api/message-forward?view=graph-rest-1.0)).</span></span> <span data-ttu-id="4263d-112">O bien, puede crear un borrador de la respuesta ([reply](/graph/api/message-createreply?view=graph-rest-1.0), [reply-all](/graph/api/message-createreplyall?view=graph-rest-1.0) or [forward](/graph/api/message-createforward?view=graph-rest-1.0)), [agregar contenido](/graph/api/message-update?view=graph-rest-1.0) y [enviar](/graph/api/message-send?view=graph-rest-1.0) el borrador más tarde.</span><span class="sxs-lookup"><span data-stu-id="4263d-112">Or, you can create a draft for the response ([reply](/graph/api/message-createreply?view=graph-rest-1.0), [reply-all](/graph/api/message-createreplyall?view=graph-rest-1.0), or [forward](/graph/api/message-createforward?view=graph-rest-1.0)), [add content](/graph/api/message-update?view=graph-rest-1.0), and then [send](/graph/api/message-send?view=graph-rest-1.0) the draft at a later time.</span></span>

<span data-ttu-id="4263d-113">Para distinguir un borrador de un mensaje enviado mediante programación, consulte la propiedad **isDraft**.</span><span class="sxs-lookup"><span data-stu-id="4263d-113">To distinguish between a draft and a sent message programmatically, check the **isDraft** property.</span></span>

<span data-ttu-id="4263d-114">De forma predeterminada, los borradores se guardan en la carpeta `Drafts` y los mensajes enviados en la carpeta `Sent Items`.</span><span class="sxs-lookup"><span data-stu-id="4263d-114">By default, draft messages are saved in the `Drafts` folder, sent messages are saved in the `Sent Items` folder.</span></span> <span data-ttu-id="4263d-115">Para mayor comodidad, puede identificar las carpetas Borradores y Elementos enviados por sus [nombres de carpeta conocidos](/graph/api/resources/mailfolder?view=graph-rest-1.0) correspondientes.</span><span class="sxs-lookup"><span data-stu-id="4263d-115">For convenience, you can identify the Drafts folder and SentItems folder by their corresponding [well-known folder names](/graph/api/resources/mailfolder?view=graph-rest-1.0).</span></span> 

### <a name="setting-the-from-and-sender-properties"></a><span data-ttu-id="4263d-116">Configuración de las propiedades from y sender</span><span class="sxs-lookup"><span data-stu-id="4263d-116">Setting the from and sender properties</span></span>

<span data-ttu-id="4263d-117">Cuando se redacta un mensaje, en la mayoría de los casos, Outlook establece las propiedades **from** y **sender** para el mismo usuario que haya iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="4263d-117">When a message is being composed, in most cases, Outlook sets the **from** and **sender** properties to the same signed-in user.</span></span> <span data-ttu-id="4263d-118">Puede actualizar estas propiedades en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="4263d-118">You can update these properties in the following scenarios:</span></span>

- <span data-ttu-id="4263d-p105">La propiedad **from** se puede cambiar si el administrador de Exchange ha asignado los derechos **sendAs** del buzón a otros usuarios. El administrador puede realizar esta acción si selecciona **Permisos del buzón** del propietario del buzón en Azure Portal, o si usa el Centro de administración de Exchange o un cmdlet Add-ADPermission de Windows PowerShell. Después, puede configurar mediante programación la propiedad **from** para uno de los usuarios que tiene derechos **sendAs** de ese buzón.</span><span class="sxs-lookup"><span data-stu-id="4263d-p105">The **from** property can be changed if the Exchange administrator has assigned **sendAs** rights of the mailbox to some other users. The administrator can do this by selecting **Mailbox Permissions** of the mailbox owner in the Azure portal, or by using the Exchange Admin Center or a Windows PowerShell Add-ADPermission cmdlet. Then, you can programmatically set the **from** property to one of these users who have **sendAs** rights for that mailbox.</span></span>
- <span data-ttu-id="4263d-122">La propiedad **sender** se puede cambiar si el propietario del buzón ha delegado uno o más usuarios para que puedan enviar mensajes desde ese buzón.</span><span class="sxs-lookup"><span data-stu-id="4263d-122">The **sender** property can be changed if the mailbox owner has delegated one or more users to be able to send messages from that mailbox.</span></span> <span data-ttu-id="4263d-123">El propietario del buzón puede delegar en Outlook.</span><span class="sxs-lookup"><span data-stu-id="4263d-123">The mailbox owner can delegate in Outlook.</span></span> <span data-ttu-id="4263d-124">Cuando un delegado envía un mensaje en nombre del propietario del buzón, Outlook establece la propiedad **sender** en la cuenta del delegado y la propiedad **from** sigue siendo el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="4263d-124">When a delegate sends a message on behalf of the mailbox owner, Outlook sets the **sender** property to the delegate’s account, and the **from** property remains as the mailbox owner.</span></span> <span data-ttu-id="4263d-125">Mediante programación, puede configurar la propiedad **sender** para un usuario que tiene permisos de delegado en ese buzón.</span><span class="sxs-lookup"><span data-stu-id="4263d-125">Programmatically, you can set the **sender** property to a user who has got delegate permissions for that mailbox.</span></span>

## <a name="using-mailtips-to-check-recipient-status-and-save-time-preview"></a><span data-ttu-id="4263d-126">Usar Sugerencias de correo electrónico para comprobar el estado del destinatario y ahorrar tiempo (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="4263d-126">Using MailTips to check recipient status and save time (preview)</span></span>

<span data-ttu-id="4263d-127">Use [Sugerencias de correo electrónico](/graph/api/resources/mailtips?view=graph-rest-beta) para tomar decisiones inteligentes antes de enviar un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4263d-127">Use [MailTips](/graph/api/resources/mailtips?view=graph-rest-beta) to make smart decisions before sending an email.</span></span>
<span data-ttu-id="4263d-128">Las Sugerencias de correo electrónico pueden proporcionarle información, como que el buzón del destinatario está limitado a determinados remitentes o si se necesita aprobación para enviar un correo electrónico al destinatario.</span><span class="sxs-lookup"><span data-stu-id="4263d-128">MailTips can tell you information such as the recipient's mailbox is restricted to specific senders, or approval is required for emailing the recipient.</span></span>


## <a name="reading-messages-with-control-over-the-body-format-returned"></a><span data-ttu-id="4263d-129">Se devolvió la lectura de mensajes con control del formato de cuerpo. </span><span class="sxs-lookup"><span data-stu-id="4263d-129">Reading messages with control over the body format returned</span></span>

<span data-ttu-id="4263d-130">También puede [leer un mensaje](/graph/api/message-get?view=graph-rest-1.0) en un buzón haciendo referencia a su Id.:</span><span class="sxs-lookup"><span data-stu-id="4263d-130">You can [read a message](/graph/api/message-get?view=graph-rest-1.0) in a mailbox by referencing its ID:</span></span>

<!-- {
  "blockType": "ignored",
  "sampleKeys": ["AAMkADhMGAAA="]
}-->
```http
GET /me/messages/AAMkADhMGAAA=
```

Puede [recibir mensajes](/graph/api/user-list-messages?view=graph-rest-1.0) en una carpeta específica. <span data-ttu-id="4263d-132">Por ejemplo, para leer mensajes en la carpeta de borradores del usuario que haya iniciado sesión:</span><span class="sxs-lookup"><span data-stu-id="4263d-132">For example, to read messages in the signed-in user's Drafts folder:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/mailfolders('Drafts')
```

<span data-ttu-id="4263d-133">El cuerpo del mensaje de Outlook puede ser un HTML o un texto, con HTML como el tipo de cuerpo del mensaje predeterminado que se devuelve en una respuesta GET.</span><span class="sxs-lookup"><span data-stu-id="4263d-133">The body of an Outlook message can be either HTML or text, with HTML as the default message body type returned in a GET response.</span></span>

<span data-ttu-id="4263d-134">Al recibir un mensaje, puede especificar el siguiente encabezado de solicitud para devolver las propiedades **body** y **uniqueBody** en el formato del texto:</span><span class="sxs-lookup"><span data-stu-id="4263d-134">When getting a message, you can specify the following request header to return the **body** and **uniqueBody** properties in text format:</span></span>

```http
Prefer: outlook.body-content-type="text"
```

<span data-ttu-id="4263d-135">Puede especificar el siguiente encabezado o, simplemente, omitir el encabezado, para obtener el cuerpo del mensaje en formato HTML:</span><span class="sxs-lookup"><span data-stu-id="4263d-135">You can specify the following header, or, just skip the header, to get the message body in HTML format:</span></span>

```http
Prefer: outlook.body-content-type="html"
```

<span data-ttu-id="4263d-136">Al especificar cualquier encabezado, una respuesta correcta incluirá el encabezado `Preference-Applied` correspondiente:</span><span class="sxs-lookup"><span data-stu-id="4263d-136">When you specify either header, a successful response would include the corresponding `Preference-Applied` header:</span></span>

- <span data-ttu-id="4263d-137">Para las solicitudes de formato de texto: `Preference-Applied: outlook.body-content-type="text"`</span><span class="sxs-lookup"><span data-stu-id="4263d-137">For text format requests: `Preference-Applied: outlook.body-content-type="text"`</span></span>
- <span data-ttu-id="4263d-138">Para las solicitudes de formato HTML: `Preference-Applied: outlook.body-content-type="html"`</span><span class="sxs-lookup"><span data-stu-id="4263d-138">For HTML format requests: `Preference-Applied: outlook.body-content-type="html"`</span></span>

<span data-ttu-id="4263d-139">Si el cuerpo se muestra en HTML, de forma predeterminada, Outlook quita cualquier código HTML potencialmente peligroso (por ejemplo, JavaScript) insertado en la propiedad **body** antes de devolver el contenido del cuerpo en una respuesta REST.</span><span class="sxs-lookup"><span data-stu-id="4263d-139">If the body is HTML, by default, Outlook removes any potentially unsafe HTML (for example, JavaScript) embedded in the **body** property before returning the body content in a REST response.</span></span>

<span data-ttu-id="4263d-140">Para obtener todo el contenido HTML original, incluya el siguiente encabezado de solicitud HTTP:</span><span class="sxs-lookup"><span data-stu-id="4263d-140">To get the entire, original HTML content, include the following HTTP request header:</span></span>

```http
Prefer: outlook.allow-unsafe-html
```

## <a name="integrating-with--social-gesture-preview"></a><span data-ttu-id="4263d-141">Integración con gesto de redes sociales "@" (vista previa)</span><span class="sxs-lookup"><span data-stu-id="4263d-141">Integrating with '@' social gesture (preview)</span></span>

<span data-ttu-id="4263d-142">Las @menciones son notificaciones para avisar a los usuarios si se les menciona en los mensajes.</span><span class="sxs-lookup"><span data-stu-id="4263d-142">@-mentions are notifications to alert users if they are mentioned in messages.</span></span> <span data-ttu-id="4263d-143">El recurso [mention](/graph/api/resources/mention?view=graph-rest-beta) permite a las aplicaciones configurar y obtener el gesto de redes sociales en línea común, el prefijo "@", en los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4263d-143">The [mention](/graph/api/resources/mention?view=graph-rest-beta) resource enables apps to set and get the common online social gesture, the '@' prefix, in emails.</span></span>
<span data-ttu-id="4263d-144">Puede:</span><span class="sxs-lookup"><span data-stu-id="4263d-144">You can:</span></span>

- <span data-ttu-id="4263d-145">Crear @menciones al [crear un mensaje](/graph/api/user-post-messages?view=graph-rest-beta#request-2)</span><span class="sxs-lookup"><span data-stu-id="4263d-145">Create @-mentions when [creating a message](/graph/api/user-post-messages?view=graph-rest-beta#request-2)</span></span>
- [<span data-ttu-id="4263d-146">Obtener todos los mensajes del buzón de un usuario que contiene una @mención al usuario</span><span class="sxs-lookup"><span data-stu-id="4263d-146">Get all the messages in a user's mailbox that contain an @-mention of the user</span></span>](/graph/api/user-list-messages?view=graph-rest-beta#request-2)
- [<span data-ttu-id="4263d-147">Obtener todas las @menciones en un mensaje</span><span class="sxs-lookup"><span data-stu-id="4263d-147">Get all the @-mention is a message</span></span>](/graph/api/message-get?view=graph-rest-beta#request-2)

## <a name="other-shared-capabilities"></a><span data-ttu-id="4263d-148">Otras funcionalidades compartidas</span><span class="sxs-lookup"><span data-stu-id="4263d-148">Other shared capabilities</span></span>

<span data-ttu-id="4263d-149">Aproveche las ventajas de las siguientes funciones comunes que se comparten entre las entidades de Microsoft Graph:</span><span class="sxs-lookup"><span data-stu-id="4263d-149">Take advantage of the following common capabilities that are shared among Microsoft Graph entities:</span></span>

- <span data-ttu-id="4263d-150">Suscríbase a las [notificaciones de cambios](/graph/api/resources/webhooks?view=graph-rest-1.0) en los mensajes cuando se produce uno o varios tipos de cambios, como la creación o actualización del mensaje.</span><span class="sxs-lookup"><span data-stu-id="4263d-150">Subscribe to [change notifications](/graph/api/resources/webhooks?view=graph-rest-1.0) on messages when one or more types of changes occur, such as message creation or update.</span></span>
- <span data-ttu-id="4263d-151">[Realice un seguimiento de los cambios incrementales en los mensajes de una carpeta](delta-query-messages.md).</span><span class="sxs-lookup"><span data-stu-id="4263d-151">[Track these incremental changes to messages in a folder](delta-query-messages.md).</span></span>
- <span data-ttu-id="4263d-152">Cree [extensiones abiertas](extensibility-overview.md#open-extensions) o [extensiones de esquema](extensibility-overview.md#schema-extensions) para agregar datos personalizados a una instancia de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4263d-152">Create [open extensions](extensibility-overview.md#open-extensions) or [schema extensions](extensibility-overview.md#schema-extensions) to add custom data to a message instance.</span></span>
- <span data-ttu-id="4263d-153">Cree [propiedades extendidas](/graph/api/resources/extended-properties-overview?view=graph-rest-1.0) en una instancia de mensaje para almacenar datos personalizados de las propiedades MAPI de Outlook cuando estas propiedades aún no están expuestas en los metadatos de la API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="4263d-153">Create [extended properties](/graph/api/resources/extended-properties-overview?view=graph-rest-1.0) in a message instance to store custom data for Outlook MAPI properties, when these properties are not already exposed in the Microsoft Graph API metadata.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4263d-154">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="4263d-154">Next steps</span></span>

<span data-ttu-id="4263d-155">Obtenga más información sobre:</span><span class="sxs-lookup"><span data-stu-id="4263d-155">Find out more about:</span></span>

- [<span data-ttu-id="4263d-156">¿Por qué integrar con el correo de Outlook?</span><span class="sxs-lookup"><span data-stu-id="4263d-156">Why integrate with Outlook mail</span></span>](outlook-mail-concept-overview.md)
- [<span data-ttu-id="4263d-157">Obtener identificadores inmutables para recursos de Outlook (vista previa)</span><span class="sxs-lookup"><span data-stu-id="4263d-157">Get immutable identifiers for Outlook resources (preview)</span></span>](outlook-immutable-id.md)
- <span data-ttu-id="4263d-158">[Usar la API de correo](/graph/api/resources/mail-api-overview?view=graph-rest-1.0) y sus [casos de uso](/graph/api/resources/mail-api-overview?view=graph-rest-1.0#common-use-cases) en Microsoft Graph v1.0.</span><span class="sxs-lookup"><span data-stu-id="4263d-158">[Using the mail API](/graph/api/resources/mail-api-overview?view=graph-rest-1.0) and its [use cases](/graph/api/resources/mail-api-overview?view=graph-rest-1.0#common-use-cases) in Microsoft Graph v1.0.</span></span>
