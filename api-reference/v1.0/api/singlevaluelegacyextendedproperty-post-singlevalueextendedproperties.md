---
title: Crear propiedad extendida de valor único
description: 'Cree una o varias propiedades extendidas de valor único en una instancia nueva o existente de un recurso. '
ms.openlocfilehash: 3dee727cb238241aba971cb077495f02514b77dc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030972"
---
# <a name="create-single-value-extended-property"></a><span data-ttu-id="d5f26-103">Crear propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="d5f26-103">Create single-value extended property</span></span>

<span data-ttu-id="d5f26-104">Cree una o varias propiedades extendidas de valor único en una instancia nueva o existente de un recurso.</span><span class="sxs-lookup"><span data-stu-id="d5f26-104">Create one or more single-value extended properties in a new or existing instance of a resource.</span></span> 

<span data-ttu-id="d5f26-105">Se admiten los siguientes recursos de usuario:</span><span class="sxs-lookup"><span data-stu-id="d5f26-105">The following user resources are supported:</span></span>

- [<span data-ttu-id="d5f26-106">calendar</span><span class="sxs-lookup"><span data-stu-id="d5f26-106">calendar</span></span>](../resources/calendar.md)
- [<span data-ttu-id="d5f26-107">contact</span><span class="sxs-lookup"><span data-stu-id="d5f26-107">contact</span></span>](../resources/contact.md)
- [<span data-ttu-id="d5f26-108">contactFolder</span><span class="sxs-lookup"><span data-stu-id="d5f26-108">contactFolder</span></span>](../resources/contactfolder.md) 
- [<span data-ttu-id="d5f26-109">event</span><span class="sxs-lookup"><span data-stu-id="d5f26-109">event</span></span>](../resources/event.md)
- [<span data-ttu-id="d5f26-110">mailFolder</span><span class="sxs-lookup"><span data-stu-id="d5f26-110">mailFolder</span></span>](../resources/mailfolder.md)
- [<span data-ttu-id="d5f26-111">message</span><span class="sxs-lookup"><span data-stu-id="d5f26-111">message</span></span>](../resources/message.md)

<span data-ttu-id="d5f26-112">También los siguientes recursos de grupo:</span><span class="sxs-lookup"><span data-stu-id="d5f26-112">As well as the following group resources:</span></span>

- <span data-ttu-id="d5f26-113">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="d5f26-113">group [calendar](../resources/calendar.md)</span></span>
- <span data-ttu-id="d5f26-114">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="d5f26-114">group [event](../resources/event.md)</span></span>
- <span data-ttu-id="d5f26-115">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="d5f26-115">group [post](../resources/post.md)</span></span> 

<span data-ttu-id="d5f26-116">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="d5f26-116">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span>

## <a name="permissions"></a><span data-ttu-id="d5f26-117">Permisos</span><span class="sxs-lookup"><span data-stu-id="d5f26-117">Permissions</span></span>
<span data-ttu-id="d5f26-118">Dependiendo del recurso que está creando la propiedad extendida en y el permiso escriba (delegada o de la aplicación) se solicitud, el permiso especificado en la tabla siguiente es el requisito mínimo para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d5f26-118">Depending on the resource you're creating the extended property in and the permission type (delegated or application) you request, the permission specified in the following table is the minimum required to call this API.</span></span> <span data-ttu-id="d5f26-119">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d5f26-119">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="d5f26-120">Recurso admitido</span><span class="sxs-lookup"><span data-stu-id="d5f26-120">Supported resource</span></span> | <span data-ttu-id="d5f26-121">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d5f26-121">Delegated (work or school account)</span></span> | <span data-ttu-id="d5f26-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d5f26-122">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d5f26-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d5f26-123">Application</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="d5f26-124">calendario</span><span class="sxs-lookup"><span data-stu-id="d5f26-124">calendar</span></span>](../resources/calendar.md) | <span data-ttu-id="d5f26-125">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-125">Calendars.ReadWrite</span></span> | <span data-ttu-id="d5f26-126">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-126">Calendars.ReadWrite</span></span> | <span data-ttu-id="d5f26-127">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-127">Calendars.ReadWrite</span></span> |
| [<span data-ttu-id="d5f26-128">contact</span><span class="sxs-lookup"><span data-stu-id="d5f26-128">contact</span></span>](../resources/contact.md) | <span data-ttu-id="d5f26-129">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-129">Contacts.ReadWrite</span></span> | <span data-ttu-id="d5f26-130">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-130">Contacts.ReadWrite</span></span> | <span data-ttu-id="d5f26-131">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-131">Contacts.ReadWrite</span></span> |
| [<span data-ttu-id="d5f26-132">contactFolder</span><span class="sxs-lookup"><span data-stu-id="d5f26-132">contactFolder</span></span>](../resources/contactfolder.md) | <span data-ttu-id="d5f26-133">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-133">Contacts.ReadWrite</span></span> | <span data-ttu-id="d5f26-134">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-134">Contacts.ReadWrite</span></span> | <span data-ttu-id="d5f26-135">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-135">Contacts.ReadWrite</span></span> |
| [<span data-ttu-id="d5f26-136">evento</span><span class="sxs-lookup"><span data-stu-id="d5f26-136">event</span></span>](../resources/event.md) | <span data-ttu-id="d5f26-137">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-137">Calendars.ReadWrite</span></span> | <span data-ttu-id="d5f26-138">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-138">Calendars.ReadWrite</span></span> |  <span data-ttu-id="d5f26-139">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-139">Calendars.ReadWrite</span></span>|
| <span data-ttu-id="d5f26-140">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="d5f26-140">group [calendar](../resources/calendar.md)</span></span> | <span data-ttu-id="d5f26-141">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d5f26-141">Group.ReadWrite.All</span></span> | <span data-ttu-id="d5f26-142">No admitido</span><span class="sxs-lookup"><span data-stu-id="d5f26-142">Not supported</span></span> | <span data-ttu-id="d5f26-143">No admitido</span><span class="sxs-lookup"><span data-stu-id="d5f26-143">Not supported</span></span> |
| <span data-ttu-id="d5f26-144">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="d5f26-144">group [event](../resources/event.md)</span></span> | <span data-ttu-id="d5f26-145">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d5f26-145">Group.ReadWrite.All</span></span> | <span data-ttu-id="d5f26-146">No admitido</span><span class="sxs-lookup"><span data-stu-id="d5f26-146">Not supported</span></span> | <span data-ttu-id="d5f26-147">No admitido</span><span class="sxs-lookup"><span data-stu-id="d5f26-147">Not supported</span></span> |
| <span data-ttu-id="d5f26-148">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="d5f26-148">group [post](../resources/post.md)</span></span> | <span data-ttu-id="d5f26-149">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d5f26-149">Group.ReadWrite.All</span></span> | <span data-ttu-id="d5f26-150">No admitido</span><span class="sxs-lookup"><span data-stu-id="d5f26-150">Not supported</span></span> | <span data-ttu-id="d5f26-151">No admitido</span><span class="sxs-lookup"><span data-stu-id="d5f26-151">Not supported</span></span> |
| [<span data-ttu-id="d5f26-152">mailFolder</span><span class="sxs-lookup"><span data-stu-id="d5f26-152">mailFolder</span></span>](../resources/mailfolder.md) | <span data-ttu-id="d5f26-153">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-153">Mail.ReadWrite</span></span> | <span data-ttu-id="d5f26-154">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-154">Mail.ReadWrite</span></span> | <span data-ttu-id="d5f26-155">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-155">Mail.ReadWrite</span></span> |
| [<span data-ttu-id="d5f26-156">mensaje</span><span class="sxs-lookup"><span data-stu-id="d5f26-156">message</span></span>](../resources/message.md) | <span data-ttu-id="d5f26-157">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-157">Mail.ReadWrite</span></span> | <span data-ttu-id="d5f26-158">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-158">Mail.ReadWrite</span></span> | <span data-ttu-id="d5f26-159">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5f26-159">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="d5f26-160">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d5f26-160">HTTP request</span></span>
<span data-ttu-id="d5f26-161">Puede crear propiedades extendidas en una instancia de recurso nueva o existente.</span><span class="sxs-lookup"><span data-stu-id="d5f26-161">You can create extended properties in a new or existing resource instance.</span></span>

<span data-ttu-id="d5f26-p102">Para crear una o varias propiedades extendidas en una instancia de recurso _nueva_, use la misma solicitud de REST que al crear la instancia e incluya las propiedades de la nueva instancia de recurso _y de la propiedad extendida_ en el cuerpo de la solicitud. Tenga en cuenta que algunos recursos admiten más de una forma de creación. Para obtener más información sobre cómo crear estas instancias de recurso, consulte los temas correspondientes para crear un [message](../resources/message.md), [mailFolder](../api/user-post-mailfolders.md), [event](../api/user-post-events.md), [calendar](../api/user-post-calendars.md), [contact](../api/user-post-contacts.md), [contactFolder](../api/user-post-contactfolders.md), [group event](../api/group-post-events.md) y [group post](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="d5f26-p102">To create one or more extended properties in a _new_ resource instance, use the same REST request as creating the instance, and include the properties of the new resource instance _and extended property_ in the request body. Note that some resources support creation in more than one way. For more information on creating these resource instances, see the corresponding topics for creating a [message](../resources/message.md), [mailFolder](../api/user-post-mailfolders.md), [event](../api/user-post-events.md), [calendar](../api/user-post-calendars.md), [contact](../api/user-post-contacts.md), [contactFolder](../api/user-post-contactfolders.md), [group event](../api/group-post-events.md), and [group post](../resources/post.md).</span></span> 
 
<span data-ttu-id="d5f26-165">A continuación tiene la sintaxis de las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="d5f26-165">The following is the syntax of the requests.</span></span> 

<!-- { "blockType": "ignored" } -->
```http
POST /me/messages
POST /users/{id|userPrincipalName}/messages
POST /me/mailFolders/{id}/messages

POST /me/mailFolders
POST /users/{id|userPrincipalName}/mailFolders

POST /me/events
POST /users/{id|userPrincipalName}/events

POST /me/calendars
POST /users/{id|userPrincipalName}/calendars

POST /me/contacts
POST /users/{id|userPrincipalName}/contacts

POST /me/contactFolders
POST /users/{id|userPrincipalName}/contactFolders

POST /groups/{id}/events

POST /groups/{id}/threads/{id}/posts/{id}/reply
POST /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/reply
POST /groups/{id}/threads/{id}/reply
POST /groups/{id}/conversations/{id}/threads/{id}/reply
POST /groups/{id}/threads
POST /groups/{id}/conversations
```

<span data-ttu-id="d5f26-166">Para crear una o varias propiedades extendidas en una instancia de recurso existente, especifique la instancia en la solicitud e incluya la propiedad extendida en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d5f26-166">To create one or more extended properties in an existing resource instance, specify the instance in the request, and include the extended property in the request body.</span></span>

<span data-ttu-id="d5f26-167">**Nota** No puede crear una propiedad extendida en una publicación de grupo existente.</span><span class="sxs-lookup"><span data-stu-id="d5f26-167">**Note** You cannot create an extended property in an existing group post.</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH /me/messages/{id}
PATCH /users/{id|userPrincipalName}/messages/{id}
PATCH /me/mailFolders/{id}/messages/{id}

PATCH /me/mailFolders/{id}
PATCH /users/{id|userPrincipalName}/mailFolders/{id}

PATCH /me/events/{id}
PATCH /users/{id|userPrincipalName}/events/{id}

PATCH /me/calendars/{id}
PATCH /users/{id|userPrincipalName}/calendars/{id}

PATCH /me/contacts/{id}
PATCH /users/{id|userPrincipalName}/contacts/{id}

PATCH /me/contactFolders/{id}
PATCH /users/{id|userPrincipalName}/contactFolders/{id}

PATCH /groups/{id}/events/{id}
```

## <a name="request-headers"></a><span data-ttu-id="d5f26-168">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d5f26-168">Request headers</span></span>
| <span data-ttu-id="d5f26-169">Nombre</span><span class="sxs-lookup"><span data-stu-id="d5f26-169">Name</span></span>       | <span data-ttu-id="d5f26-170">Valor</span><span class="sxs-lookup"><span data-stu-id="d5f26-170">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="d5f26-171">Authorization</span><span class="sxs-lookup"><span data-stu-id="d5f26-171">Authorization</span></span> | <span data-ttu-id="d5f26-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d5f26-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d5f26-174">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d5f26-174">Content-Type</span></span> | <span data-ttu-id="d5f26-175">application/json</span><span class="sxs-lookup"><span data-stu-id="d5f26-175">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="d5f26-176">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="d5f26-176">Request body</span></span>

<span data-ttu-id="d5f26-177">Proporcione un cuerpo JSON para cada objeto [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md) en la propiedad de la colección **singleValueExtendedProperties** de la instancia de recurso.</span><span class="sxs-lookup"><span data-stu-id="d5f26-177">Provide a JSON body of each [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md) object in the **singleValueExtendedProperties** collection property of the resource instance.</span></span>

|<span data-ttu-id="d5f26-178">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d5f26-178">Property</span></span>|<span data-ttu-id="d5f26-179">Tipo</span><span class="sxs-lookup"><span data-stu-id="d5f26-179">Type</span></span>|<span data-ttu-id="d5f26-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5f26-180">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d5f26-181">singleValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="d5f26-181">singleValueExtendedProperties</span></span>|<span data-ttu-id="d5f26-182">Colección [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="d5f26-182">[singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="d5f26-183">Una matriz de una o varias propiedades extendidas de valor único.</span><span class="sxs-lookup"><span data-stu-id="d5f26-183">An array of one or more single-valued extended properties.</span></span> |
|<span data-ttu-id="d5f26-184">id</span><span class="sxs-lookup"><span data-stu-id="d5f26-184">id</span></span>|<span data-ttu-id="d5f26-185">String</span><span class="sxs-lookup"><span data-stu-id="d5f26-185">String</span></span>|<span data-ttu-id="d5f26-p104">Para cada propiedad de la colección **singleValueExtendedProperties**, especifique esto para identificar la propiedad. Debe tener uno de los formatos compatibles. Consulte la [Información general de las propiedades extendidas de Outlook](../resources/extended-properties-overview.md) para obtener más información. Necesario.</span><span class="sxs-lookup"><span data-stu-id="d5f26-p104">For each property in the **singleValueExtendedProperties** collection, specify this to identify the property. It must follow one of the supported formats. See [Outlook extended properties overview](../resources/extended-properties-overview.md) for more information. Required.</span></span>|
|<span data-ttu-id="d5f26-190">value</span><span class="sxs-lookup"><span data-stu-id="d5f26-190">value</span></span>|<span data-ttu-id="d5f26-191">string</span><span class="sxs-lookup"><span data-stu-id="d5f26-191">string</span></span>|<span data-ttu-id="d5f26-p105">Para cada propiedad de la colección **singleValueExtendedProperties**, especifique el valor de la propiedad. Necesario.</span><span class="sxs-lookup"><span data-stu-id="d5f26-p105">For each property in the **singleValueExtendedProperties** collection, specify the property value. Required.</span></span>|

<span data-ttu-id="d5f26-194">Al crear una propiedad extendida en una instancia de recurso _nueva_, además de la nueva colección **singleValueExtendedProperties**, proporcione una representación JSON de esa instancia de recurso (es decir, un [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), etc.).</span><span class="sxs-lookup"><span data-stu-id="d5f26-194">When creating an extended property in a _new_ resource instance, in addition to the new **singleValueExtendedProperties** collection, provide a JSON representation of that resource instance (that is, a [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), etc.)</span></span>

## <a name="response"></a><span data-ttu-id="d5f26-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d5f26-195">Response</span></span>

#### <a name="response-code"></a><span data-ttu-id="d5f26-196">Código de respuesta</span><span class="sxs-lookup"><span data-stu-id="d5f26-196">Response code</span></span>
<span data-ttu-id="d5f26-197">Una operación que crea correctamente una propiedad extendida en una nueva instancia de recurso devuelve `201 Created`, excepto en un mensaje de grupo nuevo, ya que, según el método usado, la operación puede devolver `200 OK` o `202 Accepted`.</span><span class="sxs-lookup"><span data-stu-id="d5f26-197">An operation successful in creating an extended property in a new resource instance returns `201 Created`, except in a new group post, depending on the method used, the operation can return `200 OK` or `202 Accepted`.</span></span>

<span data-ttu-id="d5f26-198">En una instancia de recurso existente, una operación que se ejecuta correctamente devuelve `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="d5f26-198">In an existing resource instance, a successful create operation returns `200 OK`.</span></span> 


#### <a name="response-body"></a><span data-ttu-id="d5f26-199">Cuerpo de la respuesta</span><span class="sxs-lookup"><span data-stu-id="d5f26-199">Response body</span></span>

<span data-ttu-id="d5f26-p106">Al crear una propiedad extendida, la respuesta incluye solo la instancia nueva o existente, pero no la nueva propiedad extendida. Para ver la propiedad extendida recién creada, [expanda la instancia con la propiedad extendida](../api/singlevaluelegacyextendedproperty-get.md).</span><span class="sxs-lookup"><span data-stu-id="d5f26-p106">When creating an extended property, the response includes only the new or existing instance but not the new extended property. To see the newly created extended property, [get the instance expanded with the extended property](../api/singlevaluelegacyextendedproperty-get.md).</span></span>

<span data-ttu-id="d5f26-202">Al crear una propiedad extendida en una [publicación de grupo](../resources/post.md) _nueva_ al responder a un hilo o a una publicación, la respuesta incluye solo un código de respuesta, pero no la nueva publicación ni la propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="d5f26-202">When creating an extended property in a _new_ [group post](../resources/post.md) by replying to a thread or post, the response includes only a response code but not the new post nor the extended property.</span></span>



## <a name="example"></a><span data-ttu-id="d5f26-203">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d5f26-203">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="d5f26-204">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="d5f26-204">Request 1</span></span>

<span data-ttu-id="d5f26-p107">El primer ejemplo crea un evento nuevo y una propiedad extendida de valor único en la misma operación POST. Aparte de las propiedades que normalmente incluiría en un nuevo evento, el cuerpo de la solicitud incluye la colección **singleValueExtendedProperties** que contiene una propiedad extendida de valor único y lo siguiente para la propiedad:</span><span class="sxs-lookup"><span data-stu-id="d5f26-p107">The first example creates a new event and a single-value extended property in the same POST operation. Apart from the properties you'd normally include for a new event, the request body includes the **singleValueExtendedProperties** collection that contains one single-value extended property, and the following for the property:</span></span>
- <span data-ttu-id="d5f26-207">**id** especifica el tipo de propiedad como `String`, el GUID y la propiedad denominada `Fun`.</span><span class="sxs-lookup"><span data-stu-id="d5f26-207">**id** specifies the property type as `String`, the GUID, and the property named `Fun`.</span></span>
- <span data-ttu-id="d5f26-208">**value** especifica `Food` como el valor de la propiedad `Fun`.</span><span class="sxs-lookup"><span data-stu-id="d5f26-208">**value** specifies `Food` as the value of the `Fun` property.</span></span> 

<!-- { "blockType": "ignored" } -->
```http
POST https://graph.microsoft.com/v1.0/me/events
Content-Type: application/json

{
  "subject": "Celebrate Thanksgiving",
  "body": {
    "contentType": "HTML",
    "content": "Let's get together!"
  },
  "start": {
      "dateTime": "2015-11-26T18:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "end": {
      "dateTime": "2015-11-26T23:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "attendees": [
    {
      "emailAddress": {
        "address": "Terrie@contoso.com",
        "name": "Terrie Barrera"
      },
      "type": "Required"
    }
  ],
  "singleValueExtendedProperties": [
     {
           "id":"String {66f5a359-4659-4830-9070-00040ec6ac6e} Name Fun",
           "value":"Food"
     }
  ]
}
```

##### <a name="response-1"></a><span data-ttu-id="d5f26-209">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="d5f26-209">Response 1</span></span>

<span data-ttu-id="d5f26-p108">Una respuesta correcta se indica mediante un código de respuesta `HTTP 201 Created` e incluye el nuevo evento en el cuerpo de la respuesta. Es similar a la respuesta al [crear solo un evento](../api/user-post-events.md). El cuerpo de la respuesta no incluye ninguna propiedad extendida recién creada.</span><span class="sxs-lookup"><span data-stu-id="d5f26-p108">A successful response is indicated by an `HTTP 201 Created` response code, and includes the new event in the response body, similar to the response from [creating just an event](../api/user-post-events.md). The response does not include any newly created extended properties.</span></span>

<span data-ttu-id="d5f26-212">Para ver la propiedad extendida recién creada, [expanda el evento con la propiedad extendida](../api/singlevaluelegacyextendedproperty-get.md).</span><span class="sxs-lookup"><span data-stu-id="d5f26-212">To see the newly created extended property, [get the event expanded with the extended property](../api/singlevaluelegacyextendedproperty-get.md).</span></span>


****

##### <a name="request-2"></a><span data-ttu-id="d5f26-213">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="d5f26-213">Request 2</span></span>

<span data-ttu-id="d5f26-p109">El segundo ejemplo crea una propiedad extendida de valor único para el mensaje existente especificado. La propiedad extendida es el único elemento de la matriz **singleValueExtendedProperties**. El cuerpo de la solicitud incluye lo siguiente para la propiedad extendida:</span><span class="sxs-lookup"><span data-stu-id="d5f26-p109">The second example creates one single-value extended property for the specified existing message. That extended property is the only element in the **singleValueExtendedProperties** array. The request body includes the following for the extended property:</span></span>
- <span data-ttu-id="d5f26-217">**id** especifica el tipo de propiedad como `String`, el GUID y la propiedad denominada `Color`.</span><span class="sxs-lookup"><span data-stu-id="d5f26-217">**id** specifies the property type as `String`, the GUID, and the property named `Color`.</span></span>
- <span data-ttu-id="d5f26-218">**value** especifica `Green` como el valor de la propiedad `Color`.</span><span class="sxs-lookup"><span data-stu-id="d5f26-218">**value** specifies `Green` as the value of the `Color` property.</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH https://graph.microsoft.com/v1.0/me/messages/AAMkAGE1M2_bs88AACHsLqWAAA=

Content-Type: application/json

{
  "singleValueExtendedProperties": [
      {
         "id":"String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color",
         "value":"Green"
      }
    ]
}
```

##### <a name="response-2"></a><span data-ttu-id="d5f26-219">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="d5f26-219">Response 2</span></span>

<span data-ttu-id="d5f26-p110">Una respuesta correcta se indica mediante un código de respuesta `HTTP 200 OK` e incluye el mensaje especificado en el cuerpo de la respuesta. Es similar a la respuesta al [actualizar un mensaje](../api/message-update.md). El cuerpo de la respuesta no incluye la propiedad extendida recién creada.</span><span class="sxs-lookup"><span data-stu-id="d5f26-p110">A successful response is indicated by an `HTTP 200 OK` response code, and includes the specified message in the response body, similar to the response from [updating a message](../api/message-update.md). The response does not include the newly created extended property.</span></span>

<span data-ttu-id="d5f26-222">Para ver la propiedad extendida recién creada, [expanda el mensaje con la propiedad extendida](../api/singlevaluelegacyextendedproperty-get.md).</span><span class="sxs-lookup"><span data-stu-id="d5f26-222">To see the newly created extended property, [get the message expanded with the extended property](../api/singlevaluelegacyextendedproperty-get.md).</span></span>

<!-- This page was manually created. -->
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create a single-value extended property",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

