---
title: Usar la API de gráfico de Microsoft para obtener las notificaciones de cambios
description: La API de REST de Microsoft Graph usa un mecanismo webhook para entregar notificaciones a los clientes. Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones. Aplicaciones cliente usar notificaciones para actualizar su estado cuando se producen cambios. Para obtener más detalles, incluido cómo suscribirse a y controlar las notificaciones recibidas, vea el conjunto de seguridad de las notificaciones de los cambios en los datos de usuario.
localization_priority: Normal
author: piotrci
ms.openlocfilehash: fe571fe0a9a7c982ee7ce93b08457586134d7d91
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27986141"
---
# <a name="use-the-microsoft-graph-api-to-get-change-notifications"></a><span data-ttu-id="8358e-106">Usar la API de gráfico de Microsoft para obtener las notificaciones de cambios</span><span class="sxs-lookup"><span data-stu-id="8358e-106">Use the Microsoft Graph API to get change notifications</span></span>

> <span data-ttu-id="8358e-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8358e-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8358e-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8358e-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8358e-109">La API de REST de Microsoft Graph usa un mecanismo webhook para entregar notificaciones a los clientes.</span><span class="sxs-lookup"><span data-stu-id="8358e-109">The Microsoft Graph REST API uses a webhook mechanism to deliver notifications to clients.</span></span> <span data-ttu-id="8358e-110">Un cliente es un servicio web que configura su propia dirección URL para recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="8358e-110">A client is a web service that configures its own URL to receive notifications.</span></span> <span data-ttu-id="8358e-111">Aplicaciones cliente usar notificaciones para actualizar su estado cuando se producen cambios.</span><span class="sxs-lookup"><span data-stu-id="8358e-111">Client apps use notifications to update their state upon changes.</span></span> <span data-ttu-id="8358e-112">Para obtener más detalles, incluido cómo suscribirse a y controlar las notificaciones recibidas, vea [Configurar notificaciones para los cambios en los datos de usuario](/graph/webhooks).</span><span class="sxs-lookup"><span data-stu-id="8358e-112">For more details, including how to subscribe to and handle incoming notifications, see [Set up notifications for changes in user data](/graph/webhooks).</span></span>

<span data-ttu-id="8358e-113">Mediante la API de Microsoft Graph, una aplicación puede suscribirse a cambios en los siguientes recursos:</span><span class="sxs-lookup"><span data-stu-id="8358e-113">Using the Microsoft Graph API, an app can subscribe to changes on the following resources:</span></span>

- <span data-ttu-id="8358e-114">Mensajes</span><span class="sxs-lookup"><span data-stu-id="8358e-114">Messages</span></span>
- <span data-ttu-id="8358e-115">Eventos</span><span class="sxs-lookup"><span data-stu-id="8358e-115">Events</span></span>
- <span data-ttu-id="8358e-116">Contacts</span><span class="sxs-lookup"><span data-stu-id="8358e-116">Contacts</span></span>
- <span data-ttu-id="8358e-117">Usuarios</span><span class="sxs-lookup"><span data-stu-id="8358e-117">Users</span></span>
- <span data-ttu-id="8358e-118">Grupos</span><span class="sxs-lookup"><span data-stu-id="8358e-118">Groups</span></span>
- <span data-ttu-id="8358e-119">Conversaciones de grupo</span><span class="sxs-lookup"><span data-stu-id="8358e-119">Group conversations</span></span>
- <span data-ttu-id="8358e-120">Contenido compartido en OneDrive, incluidas las unidades asociadas con los sitios de SharePoint</span><span class="sxs-lookup"><span data-stu-id="8358e-120">Content shared on OneDrive, including drives associated with SharePoint sites</span></span>
- <span data-ttu-id="8358e-121">Carpetas OneDrive personales de los usuarios</span><span class="sxs-lookup"><span data-stu-id="8358e-121">Users' personal OneDrive folders</span></span>
- <span data-ttu-id="8358e-122">Alertas de seguridad</span><span class="sxs-lookup"><span data-stu-id="8358e-122">Security alerts</span></span>

## <a name="permissions"></a><span data-ttu-id="8358e-123">Permisos</span><span class="sxs-lookup"><span data-stu-id="8358e-123">Permissions</span></span>

<span data-ttu-id="8358e-p104">En general, las operaciones de suscripción requieren permiso de lectura en el recurso. Por ejemplo, para obtener notificaciones en mensajes, la aplicación necesita el permiso `Mail.Read`. En el artículo sobre cómo [crear suscripciones](../api/subscription-post-subscriptions.md) se muestran los permisos necesarios para cada tipo de recurso. En la siguiente tabla aparecen los tipos de permisos que la aplicación puede solicitar para usar webhooks con tipos de recurso concretos.</span><span class="sxs-lookup"><span data-stu-id="8358e-p104">In general, subscription operations require read permission to the resource. For example, to get notifications for messages, your app needs the `Mail.Read` permission. The [create subscription](../api/subscription-post-subscriptions.md) article lists permissions needed for each resource type. The following table lists the types of permissions your app can request to use webhooks for specific resource types.</span></span>

| <span data-ttu-id="8358e-128">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8358e-128">Permission type</span></span>                        | <span data-ttu-id="8358e-129">Tipos de recursos admitidos</span><span class="sxs-lookup"><span data-stu-id="8358e-129">Supported resource types</span></span>                                                      |
| :------------------------------------- | :------------------------------------------------------------------------------------ |
| <span data-ttu-id="8358e-130">Delegado: cuenta profesional o educativa</span><span class="sxs-lookup"><span data-stu-id="8358e-130">Delegated - work or school account</span></span>     | <span data-ttu-id="8358e-131">[póngase en contacto con][], [conversación][], [unidad][], [evento][], [grupo][], [mensaje][], [usuario][], [alerta][]</span><span class="sxs-lookup"><span data-stu-id="8358e-131">[contact][], [conversation][], [drive][], [event][], [group][], [message][], [user][], [alert][]</span></span> |
| <span data-ttu-id="8358e-132">Delegado: cuenta personal de Microsoft</span><span class="sxs-lookup"><span data-stu-id="8358e-132">Delegated - personal Microsoft account</span></span> | <span data-ttu-id="8358e-133">[póngase en contacto con][], [unidad][], [evento][], [mensaje][]</span><span class="sxs-lookup"><span data-stu-id="8358e-133">[contact][], [drive][], [event][], [message][]</span></span>                                        |
| <span data-ttu-id="8358e-134">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8358e-134">Application</span></span>                            | <span data-ttu-id="8358e-135">[póngase en contacto con][], [conversación][], [unidad][], [evento][], [grupo][], [mensaje][], [usuario][], [alerta][]</span><span class="sxs-lookup"><span data-stu-id="8358e-135">[contact][], [conversation][], [drive][], [event][], [group][], [message][], [user][], [alert][]</span></span> |

## <a name="see-also"></a><span data-ttu-id="8358e-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8358e-136">See also</span></span>

- [<span data-ttu-id="8358e-137">Tipo de recurso de suscripción</span><span class="sxs-lookup"><span data-stu-id="8358e-137">Subscription resource type</span></span>](subscription.md)
- [<span data-ttu-id="8358e-138">Suscripciones de lista</span><span class="sxs-lookup"><span data-stu-id="8358e-138">List subscriptions</span></span>](../api/subscription-list.md)
- [<span data-ttu-id="8358e-139">Obtener suscripción</span><span class="sxs-lookup"><span data-stu-id="8358e-139">Get subscription</span></span>](../api/subscription-get.md)
- [<span data-ttu-id="8358e-140">Crear suscripción</span><span class="sxs-lookup"><span data-stu-id="8358e-140">Create subscription</span></span>](../api/subscription-post-subscriptions.md)
- [<span data-ttu-id="8358e-141">Actualizar suscripción</span><span class="sxs-lookup"><span data-stu-id="8358e-141">Update subscription</span></span>](../api/subscription-update.md)
- [<span data-ttu-id="8358e-142">Eliminar suscripción</span><span class="sxs-lookup"><span data-stu-id="8358e-142">Delete subscription</span></span>](../api/subscription-delete.md)

[contact]: ./contact.md
[conversation]: ./conversation.md
[drive]: ./drive.md
[event]: ./event.md
[group]: ./group.md
[message]: ./message.md
[user]: ./user.md
[alerta]: ./alert.md
[alert]: ./alert.md
