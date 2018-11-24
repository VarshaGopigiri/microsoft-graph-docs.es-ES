# <a name="use-the-microsoft-graph-api-to-get-change-notifications"></a><span data-ttu-id="a939e-101">Usar la API de gráfico de Microsoft para obtener las notificaciones de cambios</span><span class="sxs-lookup"><span data-stu-id="a939e-101">Use the Microsoft Graph API to get change notifications</span></span>

<span data-ttu-id="a939e-102">La API de REST de Microsoft Graph usa un mecanismo webhook para entregar notificaciones a los clientes.</span><span class="sxs-lookup"><span data-stu-id="a939e-102">The Microsoft Graph REST API uses a webhook mechanism to deliver notifications to clients.</span></span> <span data-ttu-id="a939e-103">Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="a939e-103">A client is a web service that configures its own URL to receive notifications.</span></span> <span data-ttu-id="a939e-104">Aplicaciones cliente usar notificaciones para actualizar su estado cuando se producen cambios.</span><span class="sxs-lookup"><span data-stu-id="a939e-104">Client apps use notifications to update their state upon changes.</span></span> <span data-ttu-id="a939e-105">Para obtener más detalles, incluido cómo suscribirse a y controlar las notificaciones recibidas, vea [Configurar notificaciones para los cambios en los datos de usuario](../../../concepts/webhooks.md).</span><span class="sxs-lookup"><span data-stu-id="a939e-105">For more details, including how to subscribe to and handle incoming notifications, see [Set up notifications for changes in user data](../../../concepts/webhooks.md).</span></span>

<span data-ttu-id="a939e-106">Mediante la API de Microsoft Graph, una aplicación puede suscribirse a cambios en los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="a939e-106">Using the Microsoft Graph API, an app can subscribe to changes on the following resources:</span></span>

- <span data-ttu-id="a939e-107">Mensajes</span><span class="sxs-lookup"><span data-stu-id="a939e-107">Messages</span></span>
- <span data-ttu-id="a939e-108">Eventos</span><span class="sxs-lookup"><span data-stu-id="a939e-108">Events</span></span>
- <span data-ttu-id="a939e-109">Contacts</span><span class="sxs-lookup"><span data-stu-id="a939e-109">Contacts</span></span>
- <span data-ttu-id="a939e-110">Usuarios</span><span class="sxs-lookup"><span data-stu-id="a939e-110">Users</span></span>
- <span data-ttu-id="a939e-111">Grupos</span><span class="sxs-lookup"><span data-stu-id="a939e-111">Groups</span></span>
- <span data-ttu-id="a939e-112">Conversaciones de grupo</span><span class="sxs-lookup"><span data-stu-id="a939e-112">Group conversations</span></span>
- <span data-ttu-id="a939e-113">Contenido compartido en OneDrive, incluidas las unidades asociadas con los sitios de SharePoint</span><span class="sxs-lookup"><span data-stu-id="a939e-113">Content shared on OneDrive, including drives associated with SharePoint sites</span></span>
- <span data-ttu-id="a939e-114">Carpetas OneDrive personales de los usuarios</span><span class="sxs-lookup"><span data-stu-id="a939e-114">Users' personal OneDrive folders</span></span>
- <span data-ttu-id="a939e-115">Alertas de seguridad</span><span class="sxs-lookup"><span data-stu-id="a939e-115">Security alerts</span></span>

## <a name="permissions"></a><span data-ttu-id="a939e-116">Permisos</span><span class="sxs-lookup"><span data-stu-id="a939e-116">Permissions</span></span>

<span data-ttu-id="a939e-p102">En general, las operaciones de suscripción requieren permiso de lectura en el recurso. Por ejemplo, para obtener notificaciones en mensajes, la aplicación necesita el permiso `Mail.Read`. En el artículo sobre cómo [crear suscripciones](../api/subscription_post_subscriptions.md) se muestran los permisos necesarios para cada tipo de recurso. En la siguiente tabla aparecen los tipos de permisos que la aplicación puede solicitar para usar webhooks con tipos de recurso concretos.</span><span class="sxs-lookup"><span data-stu-id="a939e-p102">In general, subscription operations require read permission to the resource. For example, to get notifications for messages, your app needs the `Mail.Read` permission. The [create subscription](../api/subscription_post_subscriptions.md) article lists permissions needed for each resource type. The following table lists the types of permissions your app can request to use webhooks for specific resource types.</span></span>

| <span data-ttu-id="a939e-121">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a939e-121">Permission type</span></span>                        | <span data-ttu-id="a939e-122">Tipos de recursos admitidos en v1.0</span><span class="sxs-lookup"><span data-stu-id="a939e-122">Supported resource types in v1.0</span></span>                                 |
| :------------------------------------- | :--------------------------------------------------------------- |
| <span data-ttu-id="a939e-123">Delegado: cuenta profesional o educativa</span><span class="sxs-lookup"><span data-stu-id="a939e-123">Delegated - work or school account</span></span>     | <span data-ttu-id="a939e-124">[póngase en contacto con][], [conversación][], [unidad][], [evento][], [mensaje][], [alerta][]</span><span class="sxs-lookup"><span data-stu-id="a939e-124">[contact][], [conversation][], [drive][], [event][], [message][], [alert][]</span></span> |
| <span data-ttu-id="a939e-125">Delegado: cuenta personal de Microsoft</span><span class="sxs-lookup"><span data-stu-id="a939e-125">Delegated - personal Microsoft account</span></span> | <span data-ttu-id="a939e-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a939e-126">None</span></span>                                                             |
| <span data-ttu-id="a939e-127">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a939e-127">Application</span></span>                            | <span data-ttu-id="a939e-128">[póngase en contacto con][], [conversación][], [evento][], [mensaje][], [alerta][]</span><span class="sxs-lookup"><span data-stu-id="a939e-128">[contact][], [conversation][], [event][], [message][], [alert][]</span></span>           |

## <a name="see-also"></a><span data-ttu-id="a939e-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a939e-129">See also</span></span>

- [<span data-ttu-id="a939e-130">Tipo de recurso de suscripción</span><span class="sxs-lookup"><span data-stu-id="a939e-130">Subscription resource type</span></span>](./subscription.md)
- [<span data-ttu-id="a939e-131">Obtener suscripción</span><span class="sxs-lookup"><span data-stu-id="a939e-131">Get subscription</span></span>](../api/subscription_get.md)
- [<span data-ttu-id="a939e-132">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="a939e-132">Create subscription</span></span>](../api/subscription_post_subscriptions.md)
- [<span data-ttu-id="a939e-133">Actualizar suscripción</span><span class="sxs-lookup"><span data-stu-id="a939e-133">Update subscription</span></span>](../api/subscription_update.md)
- [<span data-ttu-id="a939e-134">Eliminar suscripción</span><span class="sxs-lookup"><span data-stu-id="a939e-134">Delete subscription</span></span>](../api/subscription_delete.md)

[contact]: ./contact.md
[conversation]: ./conversation.md
[drive]: ./drive.md
[event]: ./event.md
[message]: ./message.md
[alerta]: ./alert.md
[alert]: ./alert.md