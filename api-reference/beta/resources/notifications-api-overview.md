---
title: Usar la API de REST de notificaciones en Microsoft Graph
description: Puede usar las notificaciones de la API de Microsoft Graph para enviar notificaciones de inserción a un usuario. Simplemente una cuenta de usuario para enviar una notificación de destino, y la plataforma le ofrecerá la notificación a todos los extremos de dispositivo. Las solicitudes de la API de notificaciones se realizan en nombre de un usuario a través de permisos delegados y el [permiso de notificación]( /graph/permissions_reference), que se puede usar con puede ser cuentas de Microsoft o las cuentas de trabajo o escuela.
ms.openlocfilehash: 07b59fb7d7eae2e626b58325e82999bbd36c5489
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086527"
---
# <a name="use-the-notifications-rest-api-in-microsoft-graph"></a><span data-ttu-id="697a5-105">Usar la API de REST de notificaciones en Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="697a5-105">Use the notifications REST API in Microsoft Graph</span></span>

> <span data-ttu-id="697a5-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="697a5-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="697a5-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="697a5-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="697a5-108">Puede usar las notificaciones de la API de Microsoft Graph para enviar notificaciones de inserción a un usuario.</span><span class="sxs-lookup"><span data-stu-id="697a5-108">You can use the notifications API in Microsoft Graph to send push notifications to a user.</span></span> <span data-ttu-id="697a5-109">Simplemente una cuenta de usuario para enviar una notificación de destino, y la plataforma le ofrecerá la notificación a todos los extremos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="697a5-109">Simply target a user account to send a notification to, and the platform will deliver the notification to all device endpoints.</span></span> <span data-ttu-id="697a5-110">Las solicitudes de la API de notificaciones se realizan en nombre de un usuario a través de [permisos delegados](/graph/permissions-reference#delegated-permissions-application-permissions-and-effective-permissions) y el [permiso de notificación]( /graph/permissions_reference), que se puede usar con puede ser cuentas de Microsoft o las cuentas de trabajo o escuela.</span><span class="sxs-lookup"><span data-stu-id="697a5-110">Notifications API requests are performed on behalf of a user via [delegated permissions](/graph/permissions-reference#delegated-permissions-application-permissions-and-effective-permissions) and the [notification permission]( /graph/permissions_reference), which can be used with either Microsoft accounts or work or school accounts.</span></span>
<span data-ttu-id="697a5-111">Este tipo de notificación centrado en el usuario está representado por el recurso de [notificación](../resources/projectrome-notification.md) y se almacena en Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="697a5-111">This type of user-centric notification is represented by the [notification](../resources/projectrome-notification.md) resource and is stored in Microsoft Graph.</span></span> <span data-ttu-id="697a5-112">A continuación, se accede a y administrado por la aplicación de publicación a través de las [API de SDK de Project Roma](https://github.com/Microsoft/project-rome).</span><span class="sxs-lookup"><span data-stu-id="697a5-112">It can then be accessed and managed by the publishing app via the [Project Rome SDK APIs](https://github.com/Microsoft/project-rome).</span></span> 

## <a name="next-steps"></a><span data-ttu-id="697a5-113">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="697a5-113">Next steps</span></span>
- <span data-ttu-id="697a5-114">Consulte el [recurso de notificación](../resources/projectrome-notification.md) y crear notificaciones para integrarse con los usuarios.</span><span class="sxs-lookup"><span data-stu-id="697a5-114">See the [notification resource](../resources/projectrome-notification.md) and create notifications to engage with your users.</span></span> 
- <span data-ttu-id="697a5-115">Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).</span><span class="sxs-lookup"><span data-stu-id="697a5-115">Try the API in the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer).</span></span>