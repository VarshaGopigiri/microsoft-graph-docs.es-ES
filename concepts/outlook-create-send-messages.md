# <a name="create-and-send-outlook-messages"></a><span data-ttu-id="84087-101">Crear y enviar mensajes de Outlook</span><span class="sxs-lookup"><span data-stu-id="84087-101">Create and send Outlook messages</span></span>

<span data-ttu-id="84087-102">Los correos electrónicos se representan mediante el recurso [message](../api-reference/v1.0/resources/message.md) en Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="84087-102">Emails are represented by the [message](../api-reference/v1.0/resources/message.md) resource in Microsoft Graph.</span></span>

<span data-ttu-id="84087-103">De forma predeterminada, los mensajes se identifican por un identificador de entrada único en la propiedad **id**.</span><span class="sxs-lookup"><span data-stu-id="84087-103">By default, messages are identified by a unique entry ID in the **id** property.</span></span> <span data-ttu-id="84087-104">Un proveedor de almacenamiento asigna a un mensaje un identificador de entidad cuando el mensaje se guarda inicialmente como un borrador o se envía.</span><span class="sxs-lookup"><span data-stu-id="84087-104">A store provider assigns a message an entry ID when the message is initially saved as a draft or sent.</span></span> <span data-ttu-id="84087-105">Ese identificador cambia cuando el mensaje se copia o se mueve a otra carpeta, almacenamiento o archivo .PST.</span><span class="sxs-lookup"><span data-stu-id="84087-105">That ID changes when the message is copied or moved to another folder, store, or .PST file.</span></span>

## <a name="creating-and-sending-mail"></a><span data-ttu-id="84087-106">Crear y enviar correo electrónico</span><span class="sxs-lookup"><span data-stu-id="84087-106">Creating and sending mail</span></span>

<span data-ttu-id="84087-107">En Outlook, puede crear y enviar un correo electrónico en la misma acción [sendMail](../api-reference/v1.0/api/user_sendmail.md), o bien puede [crear](../api-reference/v1.0/api/user_post_messages.md) un borrador, posteriormente [agregar contenido](../api-reference/v1.0/api/message_update.md) y [enviar](../api-reference/v1.0/api/message_send.md) el borrador.</span><span class="sxs-lookup"><span data-stu-id="84087-107">In Outlook, you can create and send an email in the same [sendMail](../api-reference/v1.0/api/user_sendmail.md) action, or you can [create](../api-reference/v1.0/api/user_post_messages.md) a draft, subsequently [add content](../api-reference/v1.0/api/message_update.md) and [send](../api-reference/v1.0/api/message_send.md) the draft.</span></span>

<span data-ttu-id="84087-108">De forma similar, cuando responde a un correo electrónico, puede crear y enviar la respuesta en la misma acción ([reply](../api-reference/v1.0/api/message_reply.md), [reply-all](../api-reference/v1.0/api//message_replyall.md) o [forward](../api-reference/v1.0/api/message_forward.md)).</span><span class="sxs-lookup"><span data-stu-id="84087-108">Similarly, when responding to an email, you can create and send the response in the same action ([reply](../api-reference/v1.0/api/message_reply.md), [reply-all](../api-reference/v1.0/api//message_replyall.md), or [forward](../api-reference/v1.0/api/message_forward.md)).</span></span> <span data-ttu-id="84087-109">O bien, puede crear un borrador de la respuesta ([reply](../api-reference/v1.0/api/message_createreply.md), [reply-all](../api-reference/v1.0/api//message_createreplyall.md) or [forward](../api-reference/v1.0/api/message_createforward.md)), [agregar contenido](../api-reference/v1.0/api/message_update.md) y [enviar](../api-reference/v1.0/api/message_send.md) el borrador más tarde.</span><span class="sxs-lookup"><span data-stu-id="84087-109">Or, you can create a draft for the response ([reply](../api-reference/v1.0/api/message_createreply.md), [reply-all](../api-reference/v1.0/api//message_createreplyall.md), or [forward](../api-reference/v1.0/api/message_createforward.md)), [add content](../api-reference/v1.0/api/message_update.md), and then [send](../api-reference/v1.0/api/message_send.md) the draft at a later time.</span></span>

<span data-ttu-id="84087-110">Para distinguir un borrador de un mensaje enviado mediante programación, consulte la propiedad **isDraft**.</span><span class="sxs-lookup"><span data-stu-id="84087-110">To distinguish between a draft and a sent message programmatically, check the **isDraft** property.</span></span>

<span data-ttu-id="84087-111">De forma predeterminada, los borradores se guardan en la carpeta `Drafts` y los mensajes enviados en la carpeta `Sent Items`.</span><span class="sxs-lookup"><span data-stu-id="84087-111">By default, draft messages are saved in the `Drafts` folder, sent messages are saved in the `Sent Items` folder.</span></span> <span data-ttu-id="84087-112">Para mayor comodidad, puede identificar las carpetas Drafts y SentItems por sus [nombres de carpeta correspondientes conocidos](../api-reference/v1.0/resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="84087-112">For convenience, you can identify the Drafts folder and SentItems folder by their corresponding [well-known folder names](../api-reference/v1.0/resources/mailfolder.md).</span></span> <span data-ttu-id="84087-113">Por ejemplo, puede hacer lo siguiente para [obtener los mensajes](../api-reference/v1.0/api/user_list_messages.md) en la carpeta Drafts:</span><span class="sxs-lookup"><span data-stu-id="84087-113">For example, you can do the following to [get the messages](../api-reference/v1.0/api/user_list_messages.md) in the Drafts folder:</span></span>

```http
GET /me/mailfolders('Drafts')
```

### <a name="body-format-and-malicious-script"></a><span data-ttu-id="84087-114">Formato de cuerpo y script malintencionado</span><span class="sxs-lookup"><span data-stu-id="84087-114">Body format and malicious script</span></span>

<!-- Remove the following 2 sections from the message.md topics
-->

<span data-ttu-id="84087-115">El cuerpo del mensaje puede ser HTML o texto, con HTML como el tipo de cuerpo del mensaje predeterminado que se devuelve en una respuesta GET.</span><span class="sxs-lookup"><span data-stu-id="84087-115">The message body can be either HTML or text, with HTML as the default message body type returned in a GET response.</span></span>

<span data-ttu-id="84087-116">Cuando [obtenga un mensaje](../api-reference/v1.0/api/message_get.md), puede especificar el siguiente encabezado de solicitud para devolver las propiedades **body** y **uniqueBody** en el formato del texto:</span><span class="sxs-lookup"><span data-stu-id="84087-116">When [getting a message](../api-reference/v1.0/api/message_get.md), you can specify the following request header to return the **body** and **uniqueBody** properties in text format:</span></span>

```http
Prefer: outlook.body-content-type="text"
```

<span data-ttu-id="84087-117">Puede especificar el siguiente encabezado o, simplemente omita el encabezado, para obtener el cuerpo del mensaje en formato HTML:</span><span class="sxs-lookup"><span data-stu-id="84087-117">You can specify the following header, or, just skip the header, to get the message body in HTML format:</span></span>

```http
Prefer: outlook.body-content-type="html"
```

<span data-ttu-id="84087-118">Al especificar cualquier encabezado, una respuesta correcta incluirá el encabezado `Preference-Applied` correspondiente:</span><span class="sxs-lookup"><span data-stu-id="84087-118">When you specify either header, a successful response would include the corresponding `Preference-Applied` header:</span></span>

- <span data-ttu-id="84087-119">Para las solicitudes de formato de texto: `Preference-Applied: outlook.body-content-type="text"`</span><span class="sxs-lookup"><span data-stu-id="84087-119">For text format requests: `Preference-Applied: outlook.body-content-type="text"`</span></span>
- <span data-ttu-id="84087-120">Para las solicitudes de formato HTML: `Preference-Applied: outlook.body-content-type="html"`</span><span class="sxs-lookup"><span data-stu-id="84087-120">For HTML format requests: `Preference-Applied: outlook.body-content-type="html"`</span></span>

<span data-ttu-id="84087-121">Si el cuerpo se muestra en HTML, de forma predeterminada, Outlook quita cualquier código HTML potencialmente peligroso (por ejemplo, JavaScript) insertado en la propiedad **body** antes de devolver el contenido del cuerpo en una respuesta REST.</span><span class="sxs-lookup"><span data-stu-id="84087-121">If the body is HTML, by default, Outlook removes any potentially unsafe HTML (for example, JavaScript) embedded in the **body** property before returning the body content in a REST response.</span></span>

<span data-ttu-id="84087-122">Para obtener todo el contenido HTML original, incluya el siguiente encabezado de solicitud HTTP:</span><span class="sxs-lookup"><span data-stu-id="84087-122">To get the entire, original HTML content, include the following HTTP request header:</span></span>

```http
Prefer: outlook.allow-unsafe-html
```

### <a name="differentiating-the-from-and-sender-properties"></a><span data-ttu-id="84087-123">Diferenciar de las propiedades from y sender</span><span class="sxs-lookup"><span data-stu-id="84087-123">Differentiating the from and sender properties</span></span>

<span data-ttu-id="84087-124">Cuando se redacta un mensaje, en la mayoría de los casos, Outlook establece las propiedades **from** y **sender** para el mismo usuario que haya iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="84087-124">When a message is being composed, in most cases, Outlook sets the **from** and **sender** properties to the same signed-in user.</span></span> <span data-ttu-id="84087-125">Puede actualizar estas propiedades en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="84087-125">You can update these properties in the following scenarios:</span></span>

- <span data-ttu-id="84087-p105">La propiedad **from** se puede cambiar si el administrador de Exchange ha asignado los derechos **sendAs** del buzón a otros usuarios. El administrador puede realizar esta acción si selecciona **Permisos del buzón** del propietario del buzón en Azure Portal, o si usa el Centro de administración de Exchange o un cmdlet Add-ADPermission de Windows PowerShell. Después, puede configurar mediante programación la propiedad **from** para uno de los usuarios que tiene derechos **sendAs** de ese buzón.</span><span class="sxs-lookup"><span data-stu-id="84087-p105">The **from** property can be changed if the Exchange administrator has assigned **sendAs** rights of the mailbox to some other users. The administrator can do this by selecting **Mailbox Permissions** of the mailbox owner in the Azure portal, or by using the Exchange Admin Center or a Windows PowerShell Add-ADPermission cmdlet. Then, you can programmatically set the **from** property to one of these users who have **sendAs** rights for that mailbox.</span></span>
- <span data-ttu-id="84087-129">La propiedad **sender** se puede cambiar si el propietario del buzón ha delegado uno o más usuarios para que puedan enviar mensajes desde ese buzón.</span><span class="sxs-lookup"><span data-stu-id="84087-129">The **sender** property can be changed if the mailbox owner has delegated one or more users to be able to send messages from that mailbox.</span></span> <span data-ttu-id="84087-130">El propietario del buzón puede delegar en Outlook.</span><span class="sxs-lookup"><span data-stu-id="84087-130">The mailbox owner can delegate in Outlook.</span></span> <span data-ttu-id="84087-131">Cuando un delegado envía un mensaje en nombre del propietario del buzón, Outlook establece la propiedad **sender** en la cuenta del delegado y la propiedad **from** sigue siendo el propietario del buzón.</span><span class="sxs-lookup"><span data-stu-id="84087-131">When a delegate sends a message on behalf of the mailbox owner, Outlook sets the **sender** property to the delegate’s account, and the **from** property remains as the mailbox owner.</span></span> <span data-ttu-id="84087-132">Mediante programación, puede configurar la propiedad **sender** para un usuario que tiene permisos de delegado en ese buzón.</span><span class="sxs-lookup"><span data-stu-id="84087-132">Programmatically, you can set the **sender** property to a user who has got delegate permissions for that mailbox.</span></span>

## <a name="using-mailtips-to-check-recipient-status-and-save-time-preview"></a><span data-ttu-id="84087-133">Usar Sugerencias de correo electrónico para comprobar el estado del destinatario y ahorrar tiempo (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="84087-133">Using MailTips to check recipient status and save time (preview)</span></span>

<span data-ttu-id="84087-134">Use [Sugerencias de correo electrónico](../api-reference/beta/resources/mailtips.md) para tomar decisiones inteligentes antes de enviar un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="84087-134">Use [MailTips](../api-reference/beta/resources/mailtips.md) to make smart decisions before sending an email.</span></span>
<span data-ttu-id="84087-135">Las sugerencias de correo electrónico pueden proporcionarle información, como que el buzón del destinatario está limitado a determinados remitentes o si se necesita aprobación para enviar un correo electrónico al destinatario.</span><span class="sxs-lookup"><span data-stu-id="84087-135">MailTips can tell you information such as the recipient's mailbox is restricted to specific senders, or approval is required for emailing the recipient.</span></span>

## <a name="integrating-with--social-gesture-preview"></a><span data-ttu-id="84087-136">Integración con gesto de redes sociales "@" (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="84087-136">Integrating with '@' social gesture (preview)</span></span>

<span data-ttu-id="84087-137">Las @menciones son notificaciones para avisar a los usuarios si se les menciona en los mensajes.</span><span class="sxs-lookup"><span data-stu-id="84087-137">@-mentions are notifications to alert users if they are mentioned in messages.</span></span> <span data-ttu-id="84087-138">El recurso [mention](../api-reference/beta/resources/mention.md) permite a las aplicaciones configurar y obtener el gesto de redes sociales en línea común, el prefijo "@", en los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="84087-138">The [mention](../api-reference/beta/resources/mention.md) resource enables apps to set and get the common online social gesture, the '@' prefix, in emails.</span></span>
<span data-ttu-id="84087-139">Puede:</span><span class="sxs-lookup"><span data-stu-id="84087-139">You can:</span></span>

- <span data-ttu-id="84087-140">Crear @menciones al [crear un mensaje](../api-reference/beta/api/user_post_messages.md#request-2)</span><span class="sxs-lookup"><span data-stu-id="84087-140">Create @-mentions when [creating a message](../api-reference/beta/api/user_post_messages.md#request-2)</span></span>
- [<span data-ttu-id="84087-141">Obtener todos los mensajes del buzón de un usuario que contiene una @mención al usuario</span><span class="sxs-lookup"><span data-stu-id="84087-141">Get all the messages in a user's mailbox that contain an @-mention of the user</span></span>](../api-reference/beta/api/user_list_messages.md#request-2)
- [<span data-ttu-id="84087-142">Obtener todas las @menciones en un mensaje</span><span class="sxs-lookup"><span data-stu-id="84087-142">Get all the @-mention is a message</span></span>](../api-reference/beta/api/message_get.md#request-2)

## <a name="other-shared-capabilities"></a><span data-ttu-id="84087-143">Otras funcionalidades compartidas</span><span class="sxs-lookup"><span data-stu-id="84087-143">Other shared capabilities</span></span>

<span data-ttu-id="84087-144">Aproveche las ventajas de las siguientes funciones comunes que se comparten entre las entidades de Microsoft Graph:</span><span class="sxs-lookup"><span data-stu-id="84087-144">Take advantage of the following common capabilities that are shared among Microsoft Graph entities:</span></span>

- <span data-ttu-id="84087-145">Suscríbase a las [notificaciones de cambios](../api-reference/v1.0/resources/webhooks.md) en los mensajes cuando se produce uno o varios tipos de cambios, como la creación o actualización del mensaje.</span><span class="sxs-lookup"><span data-stu-id="84087-145">Subscribe to [change notifications](../api-reference/v1.0/resources/webhooks.md) on messages when one or more types of changes occur, such as message creation or update.</span></span>
- <span data-ttu-id="84087-146">[Realice un seguimiento de los cambios incrementales en los mensajes de una carpeta](delta_query_messages.md).</span><span class="sxs-lookup"><span data-stu-id="84087-146">[Track these incremental changes to messages in a folder](delta_query_messages.md).</span></span>
- <span data-ttu-id="84087-147">Cree [extensiones abiertas](extensibility_overview.md#open-extensions) o [extensiones de esquema](extensibility_overview.md#schema-extensions) para agregar datos personalizados a una instancia de mensaje.</span><span class="sxs-lookup"><span data-stu-id="84087-147">Create [open extensions](extensibility_overview.md#open-extensions) or [schema extensions](extensibility_overview.md#schema-extensions) to add custom data to a message instance.</span></span>
- <span data-ttu-id="84087-148">Cree [propiedades extendidas](../api-reference/v1.0/resources/extended-properties-overview.md) en una instancia de mensaje para almacenar datos personalizados de las propiedades MAPI de Outlook cuando estas propiedades aún no están expuestas en los metadatos de la API de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="84087-148">Create [extended properties](../api-reference/v1.0/resources/extended-properties-overview.md) in a message instance to store custom data for Outlook MAPI properties, when these properties are not already exposed in the Microsoft Graph API metadata.</span></span>

## <a name="next-steps"></a><span data-ttu-id="84087-149">Siguientes pasos</span><span class="sxs-lookup"><span data-stu-id="84087-149">Next steps</span></span>

<span data-ttu-id="84087-150">Obtenga más información sobre:</span><span class="sxs-lookup"><span data-stu-id="84087-150">Find out more about:</span></span>

- [<span data-ttu-id="84087-151">¿Por qué debería realizar la integración con Correo de Outlook?</span><span class="sxs-lookup"><span data-stu-id="84087-151">Why integrate with Outlook mail</span></span>](outlook-mail-concept-overview.md)
- <span data-ttu-id="84087-152">[Usar la API de correo](../api-reference/v1.0/resources/mail_api_overview.md) y sus [casos de uso](../api-reference/v1.0/resources/mail_api_overview.md#common-use-cases) en la versión 1.0 de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="84087-152">[Using the mail API](../api-reference/v1.0/resources/mail_api_overview.md) and its [use cases](../api-reference/v1.0/resources/mail_api_overview.md#common-use-cases) in Microsoft Graph v1.0.</span></span>


<!-- {
  "type": "#page.annotation",
  "suppressions": [
    "Error: /concepts/outlook-create-send-messages.md:
        BookmarkSkippedDocFileNotFound: Link '[creating a message](../api-reference/beta/api/user_post_messages.md#request-2)'.",
    "Error: /concepts/outlook-create-send-messages.md:
      BookmarkSkippedDocFileNotFound: Link '[Get all the messages in a user's mailbox that contain an @-mention of the user](../api-reference/beta/api/user_list_messages.md#request-2)'.",
    "Error: /concepts/outlook-create-send-messages.md:
      BookmarkSkippedDocFileNotFound: Link '[Get all the @-mention is a message](../api-reference/beta/api/message_get.md#request-2)'."
  ]
}-->
