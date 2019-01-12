---
title: 'mensaje: cancelar su suscripción'
description: Envía una solicitud de correo electrónico en nombre del usuario que ha iniciado sesión para cancelar la suscripción a una lista de distribución de correo electrónico. Utiliza la información de la `List-Unsubscribe` encabezado.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 772c01c0522becc737d07d6e842c610a5abecc0d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968165"
---
# <a name="message-unsubscribe"></a><span data-ttu-id="f5413-104">mensaje: cancelar su suscripción</span><span class="sxs-lookup"><span data-stu-id="f5413-104">message: unsubscribe</span></span>

> <span data-ttu-id="f5413-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f5413-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f5413-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f5413-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f5413-107">Envía una solicitud de correo electrónico en nombre del usuario que ha iniciado sesión para cancelar la suscripción a una lista de distribución de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f5413-107">Submits a email request on behalf of the signed-in user to unsubscribe from an email distribution list.</span></span> <span data-ttu-id="f5413-108">Utiliza la información de la `List-Unsubscribe` encabezado.</span><span class="sxs-lookup"><span data-stu-id="f5413-108">Uses the information in the `List-Unsubscribe` header.</span></span>

<span data-ttu-id="f5413-109">Remitentes de mensajes pueden usar listas de correo de una manera fácil de usar mediante la inclusión de una opción para los destinatarios para excluir. Puede hacerlo mediante la especificación de la `List-Unsubscribe` encabezado en cada mensaje que sigue a [RFC 2369](https://www.faqs.org/rfcs/rfc2369.html).</span><span class="sxs-lookup"><span data-stu-id="f5413-109">Message senders can use mailing lists in a user-friendly way by including an option for recipients to opt out. They can do so by specifying the `List-Unsubscribe` header in each message following [RFC-2369](https://www.faqs.org/rfcs/rfc2369.html).</span></span>

<span data-ttu-id="f5413-110">**Nota** En concreto, para que la acción **Cancelar su suscripción** para que funcione, debe especificar el remitente `mailto:` y no basados en la dirección URL de información de cancelación de suscripción.</span><span class="sxs-lookup"><span data-stu-id="f5413-110">**Note** In particular, for the **unsubscribe** action to work, the sender must specify `mailto:` and not URL-based unsubscribe information.</span></span>

<span data-ttu-id="f5413-111">Configuración de ese encabezado también establecería la propiedad **unsubscribeEnabled** de la instancia de [mensaje](../resources/message.md) a `true`y la propiedad **unsubscribeData** para los datos del encabezado.</span><span class="sxs-lookup"><span data-stu-id="f5413-111">Setting that header would also set the **unsubscribeEnabled** property of the [message](../resources/message.md) instance to `true`, and the **unsubscribeData** property to the header data.</span></span>

<span data-ttu-id="f5413-112">Si la propiedad **unsubscribeEnabled** de un mensaje es `true`, puede usar la acción de **cancelación de suscripción** para cancelar la suscripción al usuario de mensajes futuros similar como administrada por el remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f5413-112">If the **unsubscribeEnabled** property of a message is `true`, you can use the **unsubscribe** action to unsubscribe the user from similar future messages as managed by the message sender.</span></span>

<span data-ttu-id="f5413-113">Una acción correcta **Cancelar su suscripción** , mueve el mensaje a la carpeta **Elementos eliminados** .</span><span class="sxs-lookup"><span data-stu-id="f5413-113">A successful **unsubscribe** action moves the message to the **Deleted Items** folder.</span></span> <span data-ttu-id="f5413-114">La exclusión real del usuario de la distribución de correo futuras se administra por el remitente.</span><span class="sxs-lookup"><span data-stu-id="f5413-114">The actual exclusion of the user from future mail distribution is managed by the sender.</span></span>

## <a name="permissions"></a><span data-ttu-id="f5413-115">Permisos</span><span class="sxs-lookup"><span data-stu-id="f5413-115">Permissions</span></span>
<span data-ttu-id="f5413-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f5413-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f5413-118">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f5413-118">Permission type</span></span>      | <span data-ttu-id="f5413-119">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f5413-119">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f5413-120">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f5413-120">Delegated (work or school account)</span></span> | <span data-ttu-id="f5413-121">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="f5413-121">Mail.Send</span></span>    |
|<span data-ttu-id="f5413-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f5413-122">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f5413-123">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="f5413-123">Mail.Send</span></span>    |
|<span data-ttu-id="f5413-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f5413-124">Application</span></span> | <span data-ttu-id="f5413-125">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="f5413-125">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="f5413-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f5413-126">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/messages/{id}/unsubscribe
```
## <a name="request-headers"></a><span data-ttu-id="f5413-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f5413-127">Request headers</span></span>
| <span data-ttu-id="f5413-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="f5413-128">Name</span></span>       | <span data-ttu-id="f5413-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5413-129">Type</span></span> | <span data-ttu-id="f5413-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5413-130">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="f5413-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="f5413-131">Authorization</span></span>  | <span data-ttu-id="f5413-132">string</span><span class="sxs-lookup"><span data-stu-id="f5413-132">string</span></span>  | <span data-ttu-id="f5413-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f5413-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f5413-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f5413-135">Request body</span></span>
<span data-ttu-id="f5413-136">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f5413-136">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f5413-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5413-137">Response</span></span>

<span data-ttu-id="f5413-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5413-p107">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f5413-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f5413-140">Example</span></span>
<span data-ttu-id="f5413-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f5413-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f5413-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f5413-142">Request</span></span>
<span data-ttu-id="f5413-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f5413-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_unsubscribe"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages/{id}/unsubscribe
```

##### <a name="response"></a><span data-ttu-id="f5413-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5413-144">Response</span></span>
<span data-ttu-id="f5413-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5413-145">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: unsubscribe",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
