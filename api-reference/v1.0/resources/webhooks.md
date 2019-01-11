---
title: Usar la API de gráfico de Microsoft para obtener las notificaciones de cambios
description: La API de REST de Microsoft Graph usa un mecanismo webhook para entregar notificaciones a los clientes. Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones. Aplicaciones cliente usar notificaciones para actualizar su estado cuando se producen cambios. Para obtener más detalles, incluido cómo suscribirse a y controlar las notificaciones recibidas, vea el conjunto de seguridad de las notificaciones de los cambios en los datos de usuario.
localization_priority: Priority
ms.openlocfilehash: e846e31870e2d14a1e7822cbb9f42682c8b2ac1c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860868"
---
# <a name="use-the-microsoft-graph-api-to-get-change-notifications"></a><span data-ttu-id="ccaae-106">Usar la API de gráfico de Microsoft para obtener las notificaciones de cambios</span><span class="sxs-lookup"><span data-stu-id="ccaae-106">Use the Microsoft Graph API to get change notifications</span></span>

<span data-ttu-id="ccaae-107">La API de REST de Microsoft Graph usa un mecanismo webhook para entregar notificaciones a los clientes.</span><span class="sxs-lookup"><span data-stu-id="ccaae-107">The Microsoft Graph REST API uses a webhook mechanism to deliver notifications to clients.</span></span> <span data-ttu-id="ccaae-108">Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="ccaae-108">A client is a web service that configures its own URL to receive notifications.</span></span> <span data-ttu-id="ccaae-109">Aplicaciones cliente usar notificaciones para actualizar su estado cuando se producen cambios.</span><span class="sxs-lookup"><span data-stu-id="ccaae-109">Client apps use notifications to update their state upon changes.</span></span> <span data-ttu-id="ccaae-110">Para obtener más detalles, incluido cómo suscribirse a y controlar las notificaciones recibidas, vea [Configurar notificaciones para los cambios en los datos de usuario](/graph/webhooks).</span><span class="sxs-lookup"><span data-stu-id="ccaae-110">For more details, including how to subscribe to and handle incoming notifications, see [Set up notifications for changes in user data](/graph/webhooks).</span></span>

<span data-ttu-id="ccaae-111">Mediante la API de Microsoft Graph, una aplicación puede suscribirse a cambios en los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="ccaae-111">Using the Microsoft Graph API, an app can subscribe to changes on the following resources:</span></span>

- <span data-ttu-id="ccaae-112">Mensajes</span><span class="sxs-lookup"><span data-stu-id="ccaae-112">Messages</span></span>
- <span data-ttu-id="ccaae-113">Eventos</span><span class="sxs-lookup"><span data-stu-id="ccaae-113">Events</span></span>
- <span data-ttu-id="ccaae-114">Contacts</span><span class="sxs-lookup"><span data-stu-id="ccaae-114">Contacts</span></span>
- <span data-ttu-id="ccaae-115">Usuarios</span><span class="sxs-lookup"><span data-stu-id="ccaae-115">Users</span></span>
- <span data-ttu-id="ccaae-116">Grupos</span><span class="sxs-lookup"><span data-stu-id="ccaae-116">Groups</span></span>
- <span data-ttu-id="ccaae-117">Conversaciones de grupo</span><span class="sxs-lookup"><span data-stu-id="ccaae-117">Group conversations</span></span>
- <span data-ttu-id="ccaae-118">Contenido compartido en OneDrive, incluidas las unidades asociadas con los sitios de SharePoint</span><span class="sxs-lookup"><span data-stu-id="ccaae-118">Content shared on OneDrive, including drives associated with SharePoint sites</span></span>
- <span data-ttu-id="ccaae-119">Carpetas OneDrive personales de los usuarios</span><span class="sxs-lookup"><span data-stu-id="ccaae-119">Users' personal OneDrive folders</span></span>
- <span data-ttu-id="ccaae-120">Alertas de seguridad</span><span class="sxs-lookup"><span data-stu-id="ccaae-120">Security alerts</span></span>

## <a name="permissions"></a><span data-ttu-id="ccaae-121">Permisos</span><span class="sxs-lookup"><span data-stu-id="ccaae-121">Permissions</span></span>

<span data-ttu-id="ccaae-p103">En general, las operaciones de suscripción requieren permiso de lectura en el recurso. Por ejemplo, para obtener notificaciones en mensajes, la aplicación necesita el permiso `Mail.Read`. En el artículo sobre cómo [crear suscripciones](../api/subscription-post-subscriptions.md) se muestran los permisos necesarios para cada tipo de recurso. En la siguiente tabla aparecen los tipos de permisos que la aplicación puede solicitar para usar webhooks con tipos de recurso concretos.</span><span class="sxs-lookup"><span data-stu-id="ccaae-p103">In general, subscription operations require read permission to the resource. For example, to get notifications for messages, your app needs the `Mail.Read` permission. The [create subscription](../api/subscription-post-subscriptions.md) article lists permissions needed for each resource type. The following table lists the types of permissions your app can request to use webhooks for specific resource types.</span></span>

| <span data-ttu-id="ccaae-126">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ccaae-126">Permission type</span></span>                        | <span data-ttu-id="ccaae-127">Tipos de recursos admitidos</span><span class="sxs-lookup"><span data-stu-id="ccaae-127">Supported resource types</span></span>                                                      |
| :------------------------------------- | :------------------------------------------------------------------------------------ |
| <span data-ttu-id="ccaae-128">Delegado: cuenta profesional o educativa</span><span class="sxs-lookup"><span data-stu-id="ccaae-128">Delegated - work or school account</span></span>     | <span data-ttu-id="ccaae-129">[póngase en contacto con][], [conversación][], [unidad][], [evento][], [grupo][], [mensaje][], [usuario][], [alerta][]</span><span class="sxs-lookup"><span data-stu-id="ccaae-129">[contact][], [conversation][], [drive][], [event][], [group][], [message][], [user][], [alert][]</span></span> |
| <span data-ttu-id="ccaae-130">Delegado: cuenta personal de Microsoft</span><span class="sxs-lookup"><span data-stu-id="ccaae-130">Delegated - personal Microsoft account</span></span> | <span data-ttu-id="ccaae-131">[póngase en contacto con][], [unidad][], [evento][], [mensaje][]</span><span class="sxs-lookup"><span data-stu-id="ccaae-131">[contact][], [drive][], [event][], [message][]</span></span>                                        |
| <span data-ttu-id="ccaae-132">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ccaae-132">Application</span></span>                            | <span data-ttu-id="ccaae-133">[póngase en contacto con][], [conversación][], [unidad][], [evento][], [grupo][], [mensaje][], [usuario][], [alerta][]</span><span class="sxs-lookup"><span data-stu-id="ccaae-133">[contact][], [conversation][], [drive][], [event][], [group][], [message][], [user][], [alert][]</span></span> |

## <a name="see-also"></a><span data-ttu-id="ccaae-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ccaae-134">See also</span></span>

- [<span data-ttu-id="ccaae-135">Tipo de recurso de suscripción</span><span class="sxs-lookup"><span data-stu-id="ccaae-135">Subscription resource type</span></span>](./subscription.md)
- [<span data-ttu-id="ccaae-136">Suscripciones de lista</span><span class="sxs-lookup"><span data-stu-id="ccaae-136">List subscriptions</span></span>](../api/subscription-list.md)
- [<span data-ttu-id="ccaae-137">Obtener suscripción</span><span class="sxs-lookup"><span data-stu-id="ccaae-137">Get subscription</span></span>](../api/subscription-get.md)
- [<span data-ttu-id="ccaae-138">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="ccaae-138">Create subscription</span></span>](../api/subscription-post-subscriptions.md)
- [<span data-ttu-id="ccaae-139">Actualizar suscripción</span><span class="sxs-lookup"><span data-stu-id="ccaae-139">Update subscription</span></span>](../api/subscription-update.md)
- [<span data-ttu-id="ccaae-140">Eliminar suscripción</span><span class="sxs-lookup"><span data-stu-id="ccaae-140">Delete subscription</span></span>](../api/subscription-delete.md)

[contact]: ./contact.md
[conversation]: ./conversation.md
[drive]: ./drive.md
[event]: ./event.md
[group]: ./group.md
[message]: ./message.md
[user]: ./user.md
[alerta]: ./alert.md
[alert]: ./alert.md
