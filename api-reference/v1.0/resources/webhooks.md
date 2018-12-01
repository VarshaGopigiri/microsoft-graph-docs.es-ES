---
title: Usar la API de gráfico de Microsoft para obtener las notificaciones de cambios
description: La API de REST de Microsoft Graph usa un mecanismo webhook para entregar notificaciones a los clientes. Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones. Aplicaciones cliente usar notificaciones para actualizar su estado cuando se producen cambios. Para obtener más detalles, incluido cómo suscribirse a y controlar las notificaciones recibidas, vea el conjunto de seguridad de las notificaciones de los cambios en los datos de usuario.
ms.openlocfilehash: c7d468b7c5064911d27d3a93bc3160d03c2a4dc3
ms.sourcegitcommit: 02ead22efd4f10cd50f89c9f5aa3b6dfda96aeec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/01/2018
ms.locfileid: "27123948"
---
# <a name="use-the-microsoft-graph-api-to-get-change-notifications"></a><span data-ttu-id="90e28-106">Usar la API de gráfico de Microsoft para obtener las notificaciones de cambios</span><span class="sxs-lookup"><span data-stu-id="90e28-106">Use the Microsoft Graph API to get change notifications</span></span>

<span data-ttu-id="90e28-107">La API de REST de Microsoft Graph usa un mecanismo webhook para entregar notificaciones a los clientes.</span><span class="sxs-lookup"><span data-stu-id="90e28-107">The Microsoft Graph REST API uses a webhook mechanism to deliver notifications to clients.</span></span> <span data-ttu-id="90e28-108">Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="90e28-108">A client is a web service that configures its own URL to receive notifications.</span></span> <span data-ttu-id="90e28-109">Aplicaciones cliente usar notificaciones para actualizar su estado cuando se producen cambios.</span><span class="sxs-lookup"><span data-stu-id="90e28-109">Client apps use notifications to update their state upon changes.</span></span> <span data-ttu-id="90e28-110">Para obtener más detalles, incluido cómo suscribirse a y controlar las notificaciones recibidas, vea [Configurar notificaciones para los cambios en los datos de usuario](/graph/webhooks).</span><span class="sxs-lookup"><span data-stu-id="90e28-110">For more details, including how to subscribe to and handle incoming notifications, see [Set up notifications for changes in user data](/graph/webhooks).</span></span>

<span data-ttu-id="90e28-111">Mediante la API de Microsoft Graph, una aplicación puede suscribirse a cambios en los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="90e28-111">Using the Microsoft Graph API, an app can subscribe to changes on the following resources:</span></span>

- <span data-ttu-id="90e28-112">Mensajes</span><span class="sxs-lookup"><span data-stu-id="90e28-112">Messages</span></span>
- <span data-ttu-id="90e28-113">Eventos</span><span class="sxs-lookup"><span data-stu-id="90e28-113">Events</span></span>
- <span data-ttu-id="90e28-114">Contacts</span><span class="sxs-lookup"><span data-stu-id="90e28-114">Contacts</span></span>
- <span data-ttu-id="90e28-115">Usuarios</span><span class="sxs-lookup"><span data-stu-id="90e28-115">Users</span></span>
- <span data-ttu-id="90e28-116">Grupos</span><span class="sxs-lookup"><span data-stu-id="90e28-116">Groups</span></span>
- <span data-ttu-id="90e28-117">Conversaciones de grupo</span><span class="sxs-lookup"><span data-stu-id="90e28-117">Group conversations</span></span>
- <span data-ttu-id="90e28-118">Contenido compartido en OneDrive, incluidas las unidades asociadas con los sitios de SharePoint</span><span class="sxs-lookup"><span data-stu-id="90e28-118">Content shared on OneDrive, including drives associated with SharePoint sites</span></span>
- <span data-ttu-id="90e28-119">Carpetas OneDrive personales de los usuarios</span><span class="sxs-lookup"><span data-stu-id="90e28-119">Users' personal OneDrive folders</span></span>
- <span data-ttu-id="90e28-120">Alertas de seguridad</span><span class="sxs-lookup"><span data-stu-id="90e28-120">Security alerts</span></span>

## <a name="permissions"></a><span data-ttu-id="90e28-121">Permissions</span><span class="sxs-lookup"><span data-stu-id="90e28-121">Permissions</span></span>

<span data-ttu-id="90e28-p103">En general, las operaciones de suscripción requieren permiso de lectura en el recurso. Por ejemplo, para obtener notificaciones en mensajes, la aplicación necesita el permiso `Mail.Read`. En el artículo sobre cómo [crear suscripciones](../api/subscription-post-subscriptions.md) se muestran los permisos necesarios para cada tipo de recurso. En la siguiente tabla aparecen los tipos de permisos que la aplicación puede solicitar para usar webhooks con tipos de recurso concretos.</span><span class="sxs-lookup"><span data-stu-id="90e28-p103">In general, subscription operations require read permission to the resource. For example, to get notifications for messages, your app needs the `Mail.Read` permission. The [create subscription](../api/subscription-post-subscriptions.md) article lists permissions needed for each resource type. The following table lists the types of permissions your app can request to use webhooks for specific resource types.</span></span>

| <span data-ttu-id="90e28-126">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="90e28-126">Permission type</span></span>                        | <span data-ttu-id="90e28-127">Tipos de recursos admitidos</span><span class="sxs-lookup"><span data-stu-id="90e28-127">Supported resource types</span></span>                                                      |
| :------------------------------------- | :------------------------------------------------------------------------------------ |
| <span data-ttu-id="90e28-128">Delegado: cuenta profesional o educativa</span><span class="sxs-lookup"><span data-stu-id="90e28-128">Delegated - work or school account</span></span>     | <span data-ttu-id="90e28-129">[póngase en contacto con][], [conversación][], [unidad][], [evento][], [grupo][], [mensaje][], [usuario][], [alerta][]</span><span class="sxs-lookup"><span data-stu-id="90e28-129">[contact][], [conversation][], [drive][], [event][], [group][], [message][], [user][], [alert][]</span></span> |
| <span data-ttu-id="90e28-130">Delegado: cuenta personal de Microsoft</span><span class="sxs-lookup"><span data-stu-id="90e28-130">Delegated - personal Microsoft account</span></span> | <span data-ttu-id="90e28-131">[póngase en contacto con][], [unidad][], [evento][], [mensaje][]</span><span class="sxs-lookup"><span data-stu-id="90e28-131">[contact][], [drive][], [event][], [message][]</span></span>                                        |
| <span data-ttu-id="90e28-132">Aplicación</span><span class="sxs-lookup"><span data-stu-id="90e28-132">Application</span></span>                            | <span data-ttu-id="90e28-133">[póngase en contacto con][], [conversación][], [unidad][], [evento][], [grupo][], [mensaje][], [usuario][], [alerta][]</span><span class="sxs-lookup"><span data-stu-id="90e28-133">[contact][], [conversation][], [drive][], [event][], [group][], [message][], [user][], [alert][]</span></span> |

## <a name="see-also"></a><span data-ttu-id="90e28-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="90e28-134">See also</span></span>

- [<span data-ttu-id="90e28-135">Tipo de recurso de suscripción</span><span class="sxs-lookup"><span data-stu-id="90e28-135">Subscription resource type</span></span>](./subscription.md)
- [<span data-ttu-id="90e28-136">Suscripciones de lista</span><span class="sxs-lookup"><span data-stu-id="90e28-136">List subscriptions</span></span>](../api/subscription-list.md)
- [<span data-ttu-id="90e28-137">Obtener suscripción</span><span class="sxs-lookup"><span data-stu-id="90e28-137">Get subscription</span></span>](../api/subscription-get.md)
- [<span data-ttu-id="90e28-138">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="90e28-138">Create subscription</span></span>](../api/subscription-post-subscriptions.md)
- [<span data-ttu-id="90e28-139">Actualizar suscripción</span><span class="sxs-lookup"><span data-stu-id="90e28-139">Update subscription</span></span>](../api/subscription-update.md)
- [<span data-ttu-id="90e28-140">Eliminar suscripción</span><span class="sxs-lookup"><span data-stu-id="90e28-140">Delete subscription</span></span>](../api/subscription-delete.md)

[contact]: ./contact.md
[conversation]: ./conversation.md
[drive]: ./drive.md
[event]: ./event.md
[group]: ./group.md
[message]: ./message.md
[user]: ./user.md
[alerta]: ./alert.md
[alert]: ./alert.md