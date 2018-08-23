# <a name="use-the-microsoft-graph-api-to-get-change-notifications"></a><span data-ttu-id="47f56-101">Usar la API de Microsoft Graph para obtener notificaciones de cambios</span><span class="sxs-lookup"><span data-stu-id="47f56-101">Use the Microsoft Graph API to get change notifications</span></span>

<span data-ttu-id="47f56-102">La API de REST de Microsoft Graph usa un mecanismo webhook para entregar notificaciones a los clientes.</span><span class="sxs-lookup"><span data-stu-id="47f56-102">The Microsoft Graph REST API uses a webhook mechanism to deliver notifications to clients.</span></span> <span data-ttu-id="47f56-103">Un cliente es un servicio web que configura su dirección URL para recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="47f56-103">A client is a web service that configures its own URL to receive notifications.</span></span> <span data-ttu-id="47f56-104">Las aplicaciones cliente usan notificaciones para actualizar su estado cuando se producen cambios.</span><span class="sxs-lookup"><span data-stu-id="47f56-104">Client apps use notifications to update their state upon changes.</span></span> <span data-ttu-id="47f56-105">Para obtener más detalles, incluido cómo suscribirse y gestionar las notificaciones recibidas, vea [Configurar notificaciones para los cambios en los datos de usuario](../../../concepts/webhooks.md).</span><span class="sxs-lookup"><span data-stu-id="47f56-105">For more details, including how to subscribe to and handle incoming notifications, see [Set up notifications for changes in user data](../../../concepts/webhooks.md).</span></span>

<span data-ttu-id="47f56-106">Mediante la API de Microsoft Graph, una aplicación puede suscribirse a cambios en los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="47f56-106">Using the Microsoft Graph API, an app can subscribe to changes on the following resources:</span></span>

- <span data-ttu-id="47f56-107">Mensajes</span><span class="sxs-lookup"><span data-stu-id="47f56-107">Messages</span></span>
- <span data-ttu-id="47f56-108">Eventos</span><span class="sxs-lookup"><span data-stu-id="47f56-108">Events</span></span>
- <span data-ttu-id="47f56-109">Contactos</span><span class="sxs-lookup"><span data-stu-id="47f56-109">Contacts</span></span>
- <span data-ttu-id="47f56-110">Usuarios</span><span class="sxs-lookup"><span data-stu-id="47f56-110">Users</span></span>
- <span data-ttu-id="47f56-111">Grupos</span><span class="sxs-lookup"><span data-stu-id="47f56-111">Groups</span></span>
- <span data-ttu-id="47f56-112">Conversaciones de grupo</span><span class="sxs-lookup"><span data-stu-id="47f56-112">Group conversations</span></span>
- <span data-ttu-id="47f56-113">Contenido compartido en OneDrive, incluidas las unidades de disco asociadas a sitios de SharePoint</span><span class="sxs-lookup"><span data-stu-id="47f56-113">Content shared on OneDrive including drives associated with SharePoint sites</span></span>
- <span data-ttu-id="47f56-114">Carpetas de OneDrive personales de los usuarios</span><span class="sxs-lookup"><span data-stu-id="47f56-114">User's personal OneDrive folders</span></span>

## <a name="permissions"></a><span data-ttu-id="47f56-115">Permisos</span><span class="sxs-lookup"><span data-stu-id="47f56-115">Permissions</span></span>

<span data-ttu-id="47f56-p102">En general, las operaciones de suscripción requieren permiso de lectura en el recurso. Por ejemplo, para obtener notificaciones en mensajes, la aplicación necesita el permiso `Mail.Read`. En el artículo sobre cómo [crear suscripciones](../api/subscription_post_subscriptions.md) se muestran los permisos necesarios para cada tipo de recurso. En la siguiente tabla aparecen los tipos de permisos que la aplicación puede solicitar para usar webhooks con tipos de recurso concretos.</span><span class="sxs-lookup"><span data-stu-id="47f56-p102">In general, subscription operations require read permission to the resource. For example, to get notifications for messages, your app needs the `Mail.Read` permission. The [create subscription](../api/subscription_post_subscriptions.md) article lists permissions needed for each resource type. The following table lists the types of permissions your app can request to use webhooks for specific resource types.</span></span>

| <span data-ttu-id="47f56-120">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="47f56-120">Permission type</span></span>                        | <span data-ttu-id="47f56-121">Tipos de recursos admitidos en v1.0</span><span class="sxs-lookup"><span data-stu-id="47f56-121">Supported resource types in v1.0</span></span>                                 |
| :------------------------------------- | :--------------------------------------------------------------- |
| <span data-ttu-id="47f56-122">Delegado: cuenta profesional o educativa</span><span class="sxs-lookup"><span data-stu-id="47f56-122">Delegated - work or school account</span></span>     | <span data-ttu-id="47f56-123">[contacto][], [conversación][], [unidad de disco][], [evento][], [mensaje][]</span><span class="sxs-lookup"><span data-stu-id="47f56-123">[contact][], [conversation][], [drive][], [event][], [message][]</span></span> |
| <span data-ttu-id="47f56-124">Delegado: cuenta personal de Microsoft</span><span class="sxs-lookup"><span data-stu-id="47f56-124">Delegated - personal Microsoft account</span></span> | <span data-ttu-id="47f56-125">Ninguno</span><span class="sxs-lookup"><span data-stu-id="47f56-125">None</span></span>                                                             |
| <span data-ttu-id="47f56-126">Aplicación</span><span class="sxs-lookup"><span data-stu-id="47f56-126">Application</span></span>                            | <span data-ttu-id="47f56-127">[contacto][], [conversación][], [evento][], [mensaje][]</span><span class="sxs-lookup"><span data-stu-id="47f56-127">[contact][], [conversation][], [event][], [message][]</span></span>            |

## <a name="see-also"></a><span data-ttu-id="47f56-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="47f56-128">See also</span></span>

- [<span data-ttu-id="47f56-129">Tipo de recurso de suscripción</span><span class="sxs-lookup"><span data-stu-id="47f56-129">Subscription resource type</span></span>](./subscription.md)
- [<span data-ttu-id="47f56-130">Obtener suscripción</span><span class="sxs-lookup"><span data-stu-id="47f56-130">Get subscription</span></span>](../api/subscription_get.md)
- [<span data-ttu-id="47f56-131">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="47f56-131">Create subscription</span></span>](../api/subscription_post_subscriptions.md)
- [<span data-ttu-id="47f56-132">Actualizar suscripción</span><span class="sxs-lookup"><span data-stu-id="47f56-132">Update subscription</span></span>](../api/subscription_update.md)
- [<span data-ttu-id="47f56-133">Eliminar suscripción</span><span class="sxs-lookup"><span data-stu-id="47f56-133">Delete subscription</span></span>](../api/subscription_delete.md)

[contacto]: ./contact.md
[contact]: ./contact.md
[conversación]: ./conversation.md
[conversation]: ./conversation.md
[unidad de disco]: ./drive.md
[drive]: ./drive.md
[evento]: ./event.md
[event]: ./event.md
[mensaje]: ./message.md
[message]: ./message.md
