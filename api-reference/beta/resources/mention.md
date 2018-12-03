---
title: Mencione el tipo de recurso
description: 'Representa una notificación a una persona en función de la dirección de correo electrónico de la persona. Este tipo de notificación es también conocida como '
ms.openlocfilehash: 7e70c6a84665b474ea4d8421f60e78687ebb49b6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083891"
---
# <a name="mention-resource-type"></a><span data-ttu-id="b899f-104">Mencione el tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="b899f-104">mention resource type</span></span>

> <span data-ttu-id="b899f-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b899f-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b899f-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b899f-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b899f-107">Representa una notificación a una persona en función de la dirección de correo electrónico de la persona.</span><span class="sxs-lookup"><span data-stu-id="b899f-107">Represents a notification to a person based on the person's email address.</span></span> <span data-ttu-id="b899f-108">Este tipo de notificación es también conocida como @ menciones.</span><span class="sxs-lookup"><span data-stu-id="b899f-108">This type of notification is also known as @-mentions.</span></span>

<span data-ttu-id="b899f-109">El recurso de [mensaje](../resources/message.md) admite **mencione**.</span><span class="sxs-lookup"><span data-stu-id="b899f-109">The [message](../resources/message.md) resource supports **mention**.</span></span> <span data-ttu-id="b899f-110">Incluye una propiedad **mentionsPreview** que indica si el usuario ha iniciado sesión se menciona en esa instancia de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b899f-110">It includes a **mentionsPreview** property that indicates whether the signed-in user is mentioned in that message instance.</span></span> <span data-ttu-id="b899f-111">También incluye la propiedad de navegación **menciones** , que admite obtener detalles de una mención o eliminación de una mención en esa instancia.</span><span class="sxs-lookup"><span data-stu-id="b899f-111">It also includes the **mentions** navigation property, which supports getting details of a mention, or deleting a mention in that instance.</span></span>

<span data-ttu-id="b899f-112">Al crear un mensaje, una aplicación puede crear una mención en la misma `POST` solicitud mediante la inclusión de la mención en la propiedad **menciones** .</span><span class="sxs-lookup"><span data-stu-id="b899f-112">When creating a message, an app can create a mention in the same `POST` request by including the mention in the **mentions** property.</span></span> <span data-ttu-id="b899f-113">Uso de un `GET` solicitar con la `$filter` parámetro de consulta, una aplicación puede devolver todos los mensajes en el buzón del usuario que ha iniciado sesión que indiquen el usuario.</span><span class="sxs-lookup"><span data-stu-id="b899f-113">Using a `GET` request with the `$filter` query parameter, an app can return all the messages in the signed-in user's mailbox that mention the user.</span></span> <span data-ttu-id="b899f-114">A `GET` solicitar con la `$expand` consulta parámetro permite que la aplicación expanda todas las menciones en un mensaje específico.</span><span class="sxs-lookup"><span data-stu-id="b899f-114">A `GET` request with the `$expand` query parameter lets the app expand all mentions in a specific message.</span></span>

<span data-ttu-id="b899f-115">Este mecanismo de permitir a una aplicación establecer y obtener menciones en los mensajes permite notificaciones ligero, donde el usuario que realiza la mención puede permanecer en el contexto existente (por ejemplo, para redactar el cuerpo de un mensaje) mientras la aplicación establece la propiedad **menciones** subyacente .</span><span class="sxs-lookup"><span data-stu-id="b899f-115">This mechanism of letting an app set and get mentions in messages enables lightweight notifications, where the user making the mention can remain in the existing context (such as composing a message body) while the app sets the underlying **mentions** property.</span></span> <span data-ttu-id="b899f-116">Mencionado personas pueden descubrir fácilmente si y donde se mencionan a través de `GET` las solicitudes con la `$filter` o `$expand` parámetro de consulta.</span><span class="sxs-lookup"><span data-stu-id="b899f-116">Mentioned persons can easily find out if and where they are mentioned through `GET` requests with the `$filter` or `$expand` query parameter.</span></span>  

<span data-ttu-id="b899f-117">Por ejemplo, en el cliente de correo de Outlook, cuando un usuario escribe `@` al escribir un mensaje, Outlook permite al usuario seleccionar o escribir un nombre para llevar a cabo la mención @.</span><span class="sxs-lookup"><span data-stu-id="b899f-117">For example, in the Outlook mail client, when a user types `@` while writing a message, Outlook lets the user select or enter a name to complete the @-mention.</span></span> <span data-ttu-id="b899f-118">Outlook establece la propiedad **menciones** antes de que se crea y se envía el mensaje o el evento.</span><span class="sxs-lookup"><span data-stu-id="b899f-118">Outlook sets the **mentions** property before it creates and sends the message or event.</span></span> <span data-ttu-id="b899f-119">Outlook también usa `GET` operaciones con `$filter` y `$expand` para permitir que el usuario ha iniciado sesión buscar mensajes que indiquen el usuario, alertar al usuario a elementos de acción o discusiones, lo que permite una respuesta más rápida.</span><span class="sxs-lookup"><span data-stu-id="b899f-119">Outlook also uses `GET` operations with `$filter` and `$expand` to let the signed-in user look up messages that mention the user, alerting the user to action items or discussions, which allows for a faster response.</span></span>


## <a name="json-representation"></a><span data-ttu-id="b899f-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b899f-120">JSON representation</span></span>

<span data-ttu-id="b899f-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b899f-121">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mention"
}-->

```json
{
  "application": "string",
  "clientReference": "string",
  "createdBy": {"@odata.type": "microsoft.graph.emailAddress"},
  "createdDateTime": "DateTimeOffset",
  "deepLink": "string",
  "id": "string (identifier)",
  "mentioned": {"@odata.type": "microsoft.graph.emailAddress"},
  "mentionText": "string",
  "serverCreatedDateTime": "DateTimeOffset"
}

```
## <a name="properties"></a><span data-ttu-id="b899f-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b899f-122">Properties</span></span>
| <span data-ttu-id="b899f-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b899f-123">Property</span></span>     | <span data-ttu-id="b899f-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="b899f-124">Type</span></span>   |<span data-ttu-id="b899f-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="b899f-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b899f-126">aplicación</span><span class="sxs-lookup"><span data-stu-id="b899f-126">application</span></span> | <span data-ttu-id="b899f-127">String</span><span class="sxs-lookup"><span data-stu-id="b899f-127">String</span></span> | <span data-ttu-id="b899f-128">El nombre de la aplicación donde se creó la mención.</span><span class="sxs-lookup"><span data-stu-id="b899f-128">The name of the application where the mention is created.</span></span> <span data-ttu-id="b899f-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b899f-129">Optional.</span></span> <span data-ttu-id="b899f-130">No utilizado y el valor predeterminado como null para el **mensaje**.</span><span class="sxs-lookup"><span data-stu-id="b899f-130">Not used and defaulted as null for **message**.</span></span> |
|<span data-ttu-id="b899f-131">clientReference</span><span class="sxs-lookup"><span data-stu-id="b899f-131">clientReference</span></span> | <span data-ttu-id="b899f-132">String</span><span class="sxs-lookup"><span data-stu-id="b899f-132">String</span></span> | <span data-ttu-id="b899f-133">Un identificador único que representa a un elemento primario de la instancia de recurso.</span><span class="sxs-lookup"><span data-stu-id="b899f-133">A unique identifier that represents a parent of the resource instance.</span></span> <span data-ttu-id="b899f-134">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b899f-134">Optional.</span></span> <span data-ttu-id="b899f-135">No utilizado y el valor predeterminado como null para el **mensaje**.</span><span class="sxs-lookup"><span data-stu-id="b899f-135">Not used and defaulted as null for **message**.</span></span> |
|<span data-ttu-id="b899f-136">createdBy</span><span class="sxs-lookup"><span data-stu-id="b899f-136">createdBy</span></span>  | [<span data-ttu-id="b899f-137">emailAddress</span><span class="sxs-lookup"><span data-stu-id="b899f-137">emailAddress</span></span>](../resources/emailaddress.md) | <span data-ttu-id="b899f-138">La información de correo electrónico del usuario que realizó la mención.</span><span class="sxs-lookup"><span data-stu-id="b899f-138">The email information of the user who made the mention.</span></span> |
|<span data-ttu-id="b899f-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b899f-139">createdDateTime</span></span>  |<span data-ttu-id="b899f-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b899f-140">DateTimeOffset</span></span> |<span data-ttu-id="b899f-141">La fecha y hora en que se creó la mención en el cliente.</span><span class="sxs-lookup"><span data-stu-id="b899f-141">The date and time that the mention is created on the client.</span></span> |
|<span data-ttu-id="b899f-142">deepLink</span><span class="sxs-lookup"><span data-stu-id="b899f-142">deepLink</span></span> | <span data-ttu-id="b899f-143">String</span><span class="sxs-lookup"><span data-stu-id="b899f-143">String</span></span> | <span data-ttu-id="b899f-144">Un vínculo web profundo para el contexto de la mención en la instancia de recurso.</span><span class="sxs-lookup"><span data-stu-id="b899f-144">A deep web link to the context of the mention in the resource instance.</span></span> <span data-ttu-id="b899f-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b899f-145">Optional.</span></span> <span data-ttu-id="b899f-146">No utilizado y el valor predeterminado como null para el **mensaje**.</span><span class="sxs-lookup"><span data-stu-id="b899f-146">Not used and defaulted as null for **message**.</span></span> |
|<span data-ttu-id="b899f-147">id</span><span class="sxs-lookup"><span data-stu-id="b899f-147">id</span></span> | <span data-ttu-id="b899f-148">String</span><span class="sxs-lookup"><span data-stu-id="b899f-148">String</span></span>| <span data-ttu-id="b899f-149">El identificador único de una mención en una instancia de recursos.</span><span class="sxs-lookup"><span data-stu-id="b899f-149">The unique identifier of a mention in a resource instance.</span></span>|
|<span data-ttu-id="b899f-150">mencionado</span><span class="sxs-lookup"><span data-stu-id="b899f-150">mentioned</span></span> | [<span data-ttu-id="b899f-151">emailAddress</span><span class="sxs-lookup"><span data-stu-id="b899f-151">emailAddress</span></span>](../resources/emailaddress.md) | <span data-ttu-id="b899f-152">La información de correo electrónico de la persona se ha mencionado.</span><span class="sxs-lookup"><span data-stu-id="b899f-152">The email information of the mentioned person.</span></span> <span data-ttu-id="b899f-153">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b899f-153">Required.</span></span> |
|<span data-ttu-id="b899f-154">mentionText</span><span class="sxs-lookup"><span data-stu-id="b899f-154">mentionText</span></span> | <span data-ttu-id="b899f-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="b899f-155">String</span></span> | <span data-ttu-id="b899f-156">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b899f-156">Optional.</span></span> <span data-ttu-id="b899f-157">No utilizado y el valor predeterminado como null para el **mensaje**.</span><span class="sxs-lookup"><span data-stu-id="b899f-157">Not used and defaulted as null for **message**.</span></span> <span data-ttu-id="b899f-158">Para obtener las menciones que en un mensaje, vea la propiedad **bodyPreview** del mensaje en su lugar.</span><span class="sxs-lookup"><span data-stu-id="b899f-158">To get the mentions in a message, see the **bodyPreview** property of the message instead.</span></span> |
|<span data-ttu-id="b899f-159">serverCreatedDateTime</span><span class="sxs-lookup"><span data-stu-id="b899f-159">serverCreatedDateTime</span></span> | <span data-ttu-id="b899f-160">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b899f-160">DateTimeOffset</span></span> | <span data-ttu-id="b899f-161">La fecha y hora en que se creó la mención en el servidor.</span><span class="sxs-lookup"><span data-stu-id="b899f-161">The date and time that the mention is created on the server.</span></span> <span data-ttu-id="b899f-162">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b899f-162">Optional.</span></span> <span data-ttu-id="b899f-163">No utilizado y el valor predeterminado como null para el **mensaje**.</span><span class="sxs-lookup"><span data-stu-id="b899f-163">Not used and defaulted as null for **message**.</span></span> |

## <a name="relationships"></a><span data-ttu-id="b899f-164">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b899f-164">Relationships</span></span>
<span data-ttu-id="b899f-165">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b899f-165">None</span></span>


## <a name="methods"></a><span data-ttu-id="b899f-166">Métodos</span><span class="sxs-lookup"><span data-stu-id="b899f-166">Methods</span></span>

| <span data-ttu-id="b899f-167">Método</span><span class="sxs-lookup"><span data-stu-id="b899f-167">Method</span></span>           | <span data-ttu-id="b899f-168">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b899f-168">Return Type</span></span>    |<span data-ttu-id="b899f-169">Descripción</span><span class="sxs-lookup"><span data-stu-id="b899f-169">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b899f-170">[POST](../api/user-sendmail.md#request-2) y enviar</span><span class="sxs-lookup"><span data-stu-id="b899f-170">[Post](../api/user-sendmail.md#request-2) and send</span></span> | <span data-ttu-id="b899f-171">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b899f-171">None</span></span> | <span data-ttu-id="b899f-172">Crear y enviar menciones como parte de un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="b899f-172">Create and send mentions as part of a new message.</span></span>|
|<span data-ttu-id="b899f-173">[Post](../api/user-post-messages.md#request-2) a un borrador de la nueva</span><span class="sxs-lookup"><span data-stu-id="b899f-173">[Post](../api/user-post-messages.md#request-2) to a new draft</span></span> | <span data-ttu-id="b899f-174">[mensaje](../resources/message.md) que contiene uno o más objetos de **mencionar** .</span><span class="sxs-lookup"><span data-stu-id="b899f-174">[message](../resources/message.md) that contains one or more **mention** objects.</span></span> | <span data-ttu-id="b899f-175">Crear un borrador de un nuevo mensaje e incluir uno o más objetos de **mencionar** .</span><span class="sxs-lookup"><span data-stu-id="b899f-175">Create a draft of a new message and include one or more **mention** objects.</span></span>|
|<span data-ttu-id="b899f-176">[Obtener](../api/user-list-messages.md#request-2) mensajes mencionarme</span><span class="sxs-lookup"><span data-stu-id="b899f-176">[Get](../api/user-list-messages.md#request-2) messages mentioning me</span></span> | <span data-ttu-id="b899f-177">Colección [message](../resources/message.md)</span><span class="sxs-lookup"><span data-stu-id="b899f-177">[message](../resources/message.md) collection</span></span> | <span data-ttu-id="b899f-178">Obtener todos los mensajes en el buzón del usuario que ha iniciado sesión que contienen un **indiquen** de este usuario.</span><span class="sxs-lookup"><span data-stu-id="b899f-178">Get all the messages in the signed-in user's mailbox that contain a **mention** of this user.</span></span>|
|<span data-ttu-id="b899f-179">[Obtener](../api/message-get.md#request-2) un mensaje y sus menciones</span><span class="sxs-lookup"><span data-stu-id="b899f-179">[Get](../api/message-get.md#request-2) a message and its mentions</span></span> | <span data-ttu-id="b899f-180">Colección [message](../resources/message.md)</span><span class="sxs-lookup"><span data-stu-id="b899f-180">[message](../resources/message.md) collection</span></span> | <span data-ttu-id="b899f-181">Recibe un mensaje y expanda los detalles de cada **mencionar** en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="b899f-181">Get a message and expand the details of each **mention** in the message.</span></span>|
|<span data-ttu-id="b899f-182">[Eliminar](../api/message-delete.md#request-2) una mención</span><span class="sxs-lookup"><span data-stu-id="b899f-182">[Delete](../api/message-delete.md#request-2) a mention</span></span> | <span data-ttu-id="b899f-183">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b899f-183">None</span></span> |<span data-ttu-id="b899f-184">Elimina la mención especificada en el mensaje especificado en el buzón del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="b899f-184">Deletes the specified mention in the specified message in the signed-in user's mailbox.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mention resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->