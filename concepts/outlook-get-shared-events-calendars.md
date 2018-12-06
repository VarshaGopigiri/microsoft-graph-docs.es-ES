---
title: Obtener eventos de Outlook en un calendario compartido o delegado
description: En Outlook, los clientes pueden compartir un calendario con otros usuarios y permitirles ver o modificar los eventos de ese calendario. Los clientes también pueden nominar un delegado que actúe en su nombre, para recibir o responder a convocatorias de reunión y crear o cambiar elementos en el calendario.
ms.openlocfilehash: e05352e164b127adca1305dded5cbb00840eed52
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092841"
---
# <a name="get-outlook-events-in-a-shared-or-delegated-calendar"></a><span data-ttu-id="3b6f3-104">Obtener eventos de Outlook en un calendario compartido o delegado</span><span class="sxs-lookup"><span data-stu-id="3b6f3-104">Get Outlook events in a shared or delegated calendar</span></span>

<span data-ttu-id="3b6f3-105">En Outlook, los clientes pueden compartir un calendario con otros usuarios y permitirles ver o modificar los eventos de ese calendario.</span><span class="sxs-lookup"><span data-stu-id="3b6f3-105">In Outlook, customers can share a calendar with other users and let them view or modify events in that calendar.</span></span> <span data-ttu-id="3b6f3-106">Los clientes también pueden nominar un delegado que actúe en su nombre, para recibir o responder a convocatorias de reunión y crear o cambiar elementos en el calendario.
</span><span class="sxs-lookup"><span data-stu-id="3b6f3-106">Customers can also grant a delegate to act on their  behalf, to receive or respond to meeting requests, or create or change items in the calendar.</span></span>

<span data-ttu-id="3b6f3-107">Mediante programación, Microsoft Graph admite obtener eventos en calendarios que se han compartido con otros usuarios, así como obtener calendarios compartidos.</span><span class="sxs-lookup"><span data-stu-id="3b6f3-107">Programmatically, Microsoft Graph supports getting messages in mail folders that have been shared by other users, as well as getting the shared folders themselves.</span></span> <span data-ttu-id="3b6f3-108">El soporte también se aplica a los calendarios que se han delegado.</span><span class="sxs-lookup"><span data-stu-id="3b6f3-108">The support also applies to calendars that have been delegated.</span></span>

<span data-ttu-id="3b6f3-109">Por ejemplo, Garth ha compartido con John su calendario predeterminado y le ha concedido el acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="3b6f3-109">As an example, Garth has shared with John his default calendar and given John read access.</span></span> <span data-ttu-id="3b6f3-110">Si John ha iniciado sesión en la aplicación y ha proporcionado permisos delegados (Calendars.Read.Shared o Calendars.ReadWrite.Shared), la aplicación podrá acceder al calendario predeterminado de Garth y a los eventos en dicho calendario, tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="3b6f3-110">If John has signed in your app and provided delegated permissions (Mail.Read.Shared or Mail.ReadWrite.Shared), your app will be able to access Garth's mail and Garth's Inbox as described below.</span></span>

## <a name="get-an-event-in-the-shared-calendar"></a><span data-ttu-id="3b6f3-111">Obtener un evento en el calendario compartido</span><span class="sxs-lookup"><span data-stu-id="3b6f3-111">Get an event in the shared calendar</span></span>

<span data-ttu-id="3b6f3-112">Puede obtener un evento específico en el calendario compartido predeterminado de Garth:</span><span class="sxs-lookup"><span data-stu-id="3b6f3-112">You can get a specific event in Garth's shared default calendar:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/calendar/events/{id}
```

<span data-ttu-id="3b6f3-113">Cuando se complete correctamente, verá HTTP 200 OK y la instancia de [event](/graph/api/resources/event?view=graph-rest-1.0) identificada por `{id}` desde el calendario predeterminado de Garth.</span><span class="sxs-lookup"><span data-stu-id="3b6f3-113">On successful completion, you'll get HTTP 200 OK and the [message](/graph/api/resources/event?view=graph-rest-1.0) instance identified by `{id}` from Garth's Inbox.</span></span>

## <a name="get-all-the-events-in-the-shared-calendar"></a><span data-ttu-id="3b6f3-114">Obtener todos los eventos del calendario compartido</span><span class="sxs-lookup"><span data-stu-id="3b6f3-114">Get all the events in the shared calendar</span></span>

<span data-ttu-id="3b6f3-115">Obtenga todos los eventos en el calendario predeterminado que Garth ha compartido con John:</span><span class="sxs-lookup"><span data-stu-id="3b6f3-115">Get all the events in the default calendar that Garth has shared with John:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/calendar/events
```

<span data-ttu-id="3b6f3-116">Cuando se complete correctamente, verá HTTP 200 OK y una colección de instancias [event](/graph/api/resources/event?view=graph-rest-1.0) en el calendario predeterminado de Garth.</span><span class="sxs-lookup"><span data-stu-id="3b6f3-116">On successful completion, you'll get HTTP 200 OK and a collection of [message](/graph/api/resources/event?view=graph-rest-1.0) instances in Garth's Inbox.</span></span>

## <a name="get-the-shared-calendar"></a><span data-ttu-id="3b6f3-117">Obtener el calendario compartido</span><span class="sxs-lookup"><span data-stu-id="3b6f3-117">Get the shared folder</span></span>

<span data-ttu-id="3b6f3-118">Obtenga el calendario predeterminado que Garth ha compartido con John:</span><span class="sxs-lookup"><span data-stu-id="3b6f3-118">Get the folder (Inbox) that Garth has shared with John.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/calendar
```

<span data-ttu-id="3b6f3-119">Cuando se complete correctamente, verá HTTP 200 OK y la instancia [calendar](/graph/api/resources/calendar?view=graph-rest-1.0) que representa la carpeta predeterminada de Garth.</span><span class="sxs-lookup"><span data-stu-id="3b6f3-119">On successful completion, you'll get HTTP 200 OK and a [mailFolder](/graph/api/resources/calendar?view=graph-rest-1.0) instance that represents Garth's Inbox folder.</span></span>

<span data-ttu-id="3b6f3-120">Se aplican las mismas capacidades de GET si Garth ha delegado a John más acceso a su calendario predeterminado o si ha delegado a John todo su buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="3b6f3-120">The same GET capabilities apply if Garth had delegated John further access to Garth's Inbox, or if Garth had delegated John his entire mailbox.</span></span>

<span data-ttu-id="3b6f3-121">Si Garth no ha compartido su calendario predeterminado con John, ni ha delegado su buzón de correo a John, especificar el identificador de usuario de Garth o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="3b6f3-121">If Garth has not shared his calendar with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> 


## <a name="next-steps"></a><span data-ttu-id="3b6f3-122">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="3b6f3-122">Next steps</span></span>

<span data-ttu-id="3b6f3-123">Obtenga más información sobre:</span><span class="sxs-lookup"><span data-stu-id="3b6f3-123">Find out more about:</span></span>

- [<span data-ttu-id="3b6f3-124">¿Por qué debería realizar la integración con el calendario de Outlook?</span><span class="sxs-lookup"><span data-stu-id="3b6f3-124">Why integrate with Outlook calendar?</span></span>](outlook-calendar-concept-overview.md)
- <span data-ttu-id="3b6f3-125">La [API de calendario](/graph/api/resources/calendar?view=graph-rest-1.0) en la versión 1.0 de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="3b6f3-125">The [calendar API](/graph/api/resources/calendar?view=graph-rest-1.0) in Microsoft Graph v1.0.</span></span>