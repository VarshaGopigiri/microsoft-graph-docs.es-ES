---
title: Crear propiedad extendida de varios valores
description: 'Cree una o más propiedades extendidas de varios valores en una instancia nueva o existente de un recurso. '
ms.openlocfilehash: 2eb3c337b89be8dc6109dc26de35fcaea88d6609
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032523"
---
# <a name="create-multi-value-extended-property"></a><span data-ttu-id="c433e-103">Crear propiedad extendida de varios valores</span><span class="sxs-lookup"><span data-stu-id="c433e-103">Create multi-value extended property</span></span>

<span data-ttu-id="c433e-104">Cree una o más propiedades extendidas de varios valores en una instancia nueva o existente de un recurso.</span><span class="sxs-lookup"><span data-stu-id="c433e-104">Create one or more multi-value extended properties in a new or existing instance of a resource.</span></span> 

<span data-ttu-id="c433e-105">Se admiten los siguientes recursos de usuario:</span><span class="sxs-lookup"><span data-stu-id="c433e-105">The following user resources are supported:</span></span>

- [<span data-ttu-id="c433e-106">calendar</span><span class="sxs-lookup"><span data-stu-id="c433e-106">calendar</span></span>](../resources/calendar.md)
- [<span data-ttu-id="c433e-107">contact</span><span class="sxs-lookup"><span data-stu-id="c433e-107">contact</span></span>](../resources/contact.md)
- [<span data-ttu-id="c433e-108">contactFolder</span><span class="sxs-lookup"><span data-stu-id="c433e-108">contactFolder</span></span>](../resources/contactfolder.md) 
- [<span data-ttu-id="c433e-109">event</span><span class="sxs-lookup"><span data-stu-id="c433e-109">event</span></span>](../resources/event.md)
- [<span data-ttu-id="c433e-110">mailFolder</span><span class="sxs-lookup"><span data-stu-id="c433e-110">mailFolder</span></span>](../resources/mailfolder.md)
- [<span data-ttu-id="c433e-111">message</span><span class="sxs-lookup"><span data-stu-id="c433e-111">message</span></span>](../resources/message.md)

<span data-ttu-id="c433e-112">También los siguientes recursos de grupo:</span><span class="sxs-lookup"><span data-stu-id="c433e-112">As well as the following group resources:</span></span>

- <span data-ttu-id="c433e-113">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="c433e-113">group [calendar](../resources/calendar.md)</span></span>
- <span data-ttu-id="c433e-114">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="c433e-114">group [event](../resources/event.md)</span></span>
- <span data-ttu-id="c433e-115">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="c433e-115">group [post](../resources/post.md)</span></span> 

<span data-ttu-id="c433e-116">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="c433e-116">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span>

## <a name="permissions"></a><span data-ttu-id="c433e-117">Permisos</span><span class="sxs-lookup"><span data-stu-id="c433e-117">Permissions</span></span>
<span data-ttu-id="c433e-118">Dependiendo del recurso que está creando la propiedad extendida en y el permiso escriba (delegada o de la aplicación) se solicitud, el permiso especificado en la tabla siguiente es el requisito mínimo para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c433e-118">Depending on the resource you're creating the extended property in and the permission type (delegated or application) you request, the permission specified in the following table is the minimum required to call this API.</span></span> <span data-ttu-id="c433e-119">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c433e-119">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="c433e-120">Recurso admitido</span><span class="sxs-lookup"><span data-stu-id="c433e-120">Supported resource</span></span> | <span data-ttu-id="c433e-121">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c433e-121">Delegated (work or school account)</span></span> | <span data-ttu-id="c433e-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c433e-122">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c433e-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c433e-123">Application</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="c433e-124">calendario</span><span class="sxs-lookup"><span data-stu-id="c433e-124">calendar</span></span>](../resources/calendar.md) | <span data-ttu-id="c433e-125">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-125">Calendars.ReadWrite</span></span> | <span data-ttu-id="c433e-126">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-126">Calendars.ReadWrite</span></span> | <span data-ttu-id="c433e-127">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-127">Calendars.ReadWrite</span></span> |
| [<span data-ttu-id="c433e-128">contact</span><span class="sxs-lookup"><span data-stu-id="c433e-128">contact</span></span>](../resources/contact.md) | <span data-ttu-id="c433e-129">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-129">Contacts.ReadWrite</span></span> | <span data-ttu-id="c433e-130">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-130">Contacts.ReadWrite</span></span> | <span data-ttu-id="c433e-131">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-131">Contacts.ReadWrite</span></span> |
| [<span data-ttu-id="c433e-132">contactFolder</span><span class="sxs-lookup"><span data-stu-id="c433e-132">contactFolder</span></span>](../resources/contactfolder.md) | <span data-ttu-id="c433e-133">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-133">Contacts.ReadWrite</span></span> | <span data-ttu-id="c433e-134">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-134">Contacts.ReadWrite</span></span> | <span data-ttu-id="c433e-135">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-135">Contacts.ReadWrite</span></span> |
| [<span data-ttu-id="c433e-136">evento</span><span class="sxs-lookup"><span data-stu-id="c433e-136">event</span></span>](../resources/event.md) | <span data-ttu-id="c433e-137">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-137">Calendars.ReadWrite</span></span> | <span data-ttu-id="c433e-138">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-138">Calendars.ReadWrite</span></span> |  <span data-ttu-id="c433e-139">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-139">Calendars.ReadWrite</span></span>|
| <span data-ttu-id="c433e-140">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="c433e-140">group [calendar](../resources/calendar.md)</span></span> | <span data-ttu-id="c433e-141">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c433e-141">Group.ReadWrite.All</span></span> | <span data-ttu-id="c433e-142">No admitido</span><span class="sxs-lookup"><span data-stu-id="c433e-142">Not supported</span></span> | <span data-ttu-id="c433e-143">No admitido</span><span class="sxs-lookup"><span data-stu-id="c433e-143">Not supported</span></span> |
| <span data-ttu-id="c433e-144">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="c433e-144">group [event](../resources/event.md)</span></span> | <span data-ttu-id="c433e-145">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c433e-145">Group.ReadWrite.All</span></span> | <span data-ttu-id="c433e-146">No admitido</span><span class="sxs-lookup"><span data-stu-id="c433e-146">Not supported</span></span> | <span data-ttu-id="c433e-147">No admitido</span><span class="sxs-lookup"><span data-stu-id="c433e-147">Not supported</span></span> |
| <span data-ttu-id="c433e-148">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="c433e-148">group [post](../resources/post.md)</span></span> | <span data-ttu-id="c433e-149">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c433e-149">Group.ReadWrite.All</span></span> | <span data-ttu-id="c433e-150">No admitido</span><span class="sxs-lookup"><span data-stu-id="c433e-150">Not supported</span></span> | <span data-ttu-id="c433e-151">No admitido</span><span class="sxs-lookup"><span data-stu-id="c433e-151">Not supported</span></span> |
| [<span data-ttu-id="c433e-152">mailFolder</span><span class="sxs-lookup"><span data-stu-id="c433e-152">mailFolder</span></span>](../resources/mailfolder.md) | <span data-ttu-id="c433e-153">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-153">Mail.ReadWrite</span></span> | <span data-ttu-id="c433e-154">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-154">Mail.ReadWrite</span></span> | <span data-ttu-id="c433e-155">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-155">Mail.ReadWrite</span></span> |
| [<span data-ttu-id="c433e-156">mensaje</span><span class="sxs-lookup"><span data-stu-id="c433e-156">message</span></span>](../resources/message.md) | <span data-ttu-id="c433e-157">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-157">Mail.ReadWrite</span></span> | <span data-ttu-id="c433e-158">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-158">Mail.ReadWrite</span></span> | <span data-ttu-id="c433e-159">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c433e-159">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="c433e-160">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c433e-160">HTTP request</span></span>
<span data-ttu-id="c433e-161">Puede crear propiedades extendidas en una instancia de recurso nueva o existente.</span><span class="sxs-lookup"><span data-stu-id="c433e-161">You can create extended properties in a new or existing resource instance.</span></span>

<span data-ttu-id="c433e-p102">Para crear una o varias propiedades extendidas en una instancia de recurso _nueva_, use la misma solicitud de REST que al crear la instancia e incluya las propiedades de la nueva instancia de recurso _y de la propiedad extendida_ en el cuerpo de la solicitud. Tenga en cuenta que algunos recursos admiten más de una forma de creación. Para obtener más información sobre cómo crear estas instancias de recurso, consulte los temas correspondientes para crear un [message](../resources/message.md), [mailFolder](../api/user-post-mailfolders.md), [event](../api/user-post-events.md), [calendar](../api/user-post-calendars.md), [contact](../api/user-post-contacts.md), [contactFolder](../api/user-post-contactfolders.md), [group event](../api/group-post-events.md) y [group post](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="c433e-p102">To create one or more extended properties in a _new_ resource instance, use the same REST request as creating the instance, and include the properties of the new resource instance _and extended property_ in the request body. Note that some resources support creation in more than one way. For more information on creating these resource instances, see the corresponding topics for creating a [message](../resources/message.md), [mailFolder](../api/user-post-mailfolders.md), [event](../api/user-post-events.md), [calendar](../api/user-post-calendars.md), [contact](../api/user-post-contacts.md), [contactFolder](../api/user-post-contactfolders.md), [group event](../api/group-post-events.md), and [group post](../resources/post.md).</span></span> 
 
<span data-ttu-id="c433e-165">A continuación tiene la sintaxis de las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="c433e-165">The following is the syntax of the requests.</span></span> 

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

<span data-ttu-id="c433e-166">Para crear una o varias propiedades extendidas en una instancia de recurso existente, especifique la instancia en la solicitud e incluya la propiedad extendida en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c433e-166">To create one or more extended properties in an existing resource instance, specify the instance in the request, and include the extended property in the request body.</span></span>

<span data-ttu-id="c433e-167">**Nota** No puede crear una propiedad extendida en una publicación de grupo existente.</span><span class="sxs-lookup"><span data-stu-id="c433e-167">**Note** You cannot create an extended property in an existing group post.</span></span>

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

## <a name="request-headers"></a><span data-ttu-id="c433e-168">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c433e-168">Request headers</span></span>
| <span data-ttu-id="c433e-169">Nombre</span><span class="sxs-lookup"><span data-stu-id="c433e-169">Name</span></span>       | <span data-ttu-id="c433e-170">Valor</span><span class="sxs-lookup"><span data-stu-id="c433e-170">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="c433e-171">Authorization</span><span class="sxs-lookup"><span data-stu-id="c433e-171">Authorization</span></span> | <span data-ttu-id="c433e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c433e-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c433e-174">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c433e-174">Content-Type</span></span> | <span data-ttu-id="c433e-175">application/json</span><span class="sxs-lookup"><span data-stu-id="c433e-175">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="c433e-176">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="c433e-176">Request body</span></span>

<span data-ttu-id="c433e-177">Proporcione un cuerpo JSON para cada objeto [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) en la propiedad de la colección **multiValueExtendedProperties** de la instancia de recurso.</span><span class="sxs-lookup"><span data-stu-id="c433e-177">Provide a JSON body of each [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) object in the **multiValueExtendedProperties** collection property of the resource instance.</span></span>

|<span data-ttu-id="c433e-178">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c433e-178">Property</span></span>|<span data-ttu-id="c433e-179">Tipo</span><span class="sxs-lookup"><span data-stu-id="c433e-179">Type</span></span>|<span data-ttu-id="c433e-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="c433e-180">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c433e-181">multiValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="c433e-181">multiValueExtendedProperties</span></span>|<span data-ttu-id="c433e-182">Colección [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="c433e-182">[multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="c433e-183">Una matriz de una o más propiedades extendidas con varios valores.</span><span class="sxs-lookup"><span data-stu-id="c433e-183">An array of one or more multi-valued extended properties.</span></span> |
|<span data-ttu-id="c433e-184">id</span><span class="sxs-lookup"><span data-stu-id="c433e-184">id</span></span>|<span data-ttu-id="c433e-185">String</span><span class="sxs-lookup"><span data-stu-id="c433e-185">String</span></span>|<span data-ttu-id="c433e-p104">Para cada propiedad de la colección **multiValueExtendedProperties**, especifique esto para identificar la propiedad. Debe tener uno de los formatos compatibles. Consulte la [Información general de las propiedades extendidas de Outlook](../resources/extended-properties-overview.md) para obtener más información. Necesario.</span><span class="sxs-lookup"><span data-stu-id="c433e-p104">For each property in the **multiValueExtendedProperties** collection, specify this to identify the property. It must follow one of the supported formats. See [Outlook extended properties overview](../resources/extended-properties-overview.md) for more information. Required.</span></span>|
|<span data-ttu-id="c433e-190">value</span><span class="sxs-lookup"><span data-stu-id="c433e-190">value</span></span>|<span data-ttu-id="c433e-191">cadena</span><span class="sxs-lookup"><span data-stu-id="c433e-191">string</span></span>|<span data-ttu-id="c433e-p105">Para cada propiedad de la colección **multiValueExtendedProperties**, especifique el valor de la propiedad. Necesario.</span><span class="sxs-lookup"><span data-stu-id="c433e-p105">For each property in the **multiValueExtendedProperties** collection, specify the property value. Required.</span></span>|

<span data-ttu-id="c433e-194">Al crear una propiedad extendida en una _nueva_ instancia de recursos, además de la nueva colección de **multiValueExtendedProperties** , proporcionan una representación JSON de esa instancia de recurso así como (es decir, un [mensaje](../resources/message.md), [mailFolder ](../resources/mailfolder.md), [evento](../resources/event.md), etcetera.).</span><span class="sxs-lookup"><span data-stu-id="c433e-194">When creating an extended property in a _new_ resource instance, in addition to the new **multiValueExtendedProperties** collection, provide a JSON representation of that resource instance as well (that is, a [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), etc.).</span></span>


## <a name="response"></a><span data-ttu-id="c433e-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c433e-195">Response</span></span>

#### <a name="response-code"></a><span data-ttu-id="c433e-196">Código de respuesta</span><span class="sxs-lookup"><span data-stu-id="c433e-196">Response code</span></span>
<span data-ttu-id="c433e-197">Una operación que crea correctamente una propiedad extendida en una nueva instancia de recurso devuelve `201 Created`, excepto en un mensaje de grupo nuevo, ya que, según el método usado, la operación puede devolver `200 OK` o `202 Accepted`.</span><span class="sxs-lookup"><span data-stu-id="c433e-197">An operation successful in creating an extended property in a new resource instance returns `201 Created`, except in a new group post, depending on the method used, the operation can return `200 OK` or `202 Accepted`.</span></span>

<span data-ttu-id="c433e-198">En una instancia de recurso existente, una operación que se ejecuta correctamente devuelve `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="c433e-198">In an existing resource instance, a successful create operation returns `200 OK`.</span></span> 


#### <a name="response-body"></a><span data-ttu-id="c433e-199">Cuerpo de la respuesta</span><span class="sxs-lookup"><span data-stu-id="c433e-199">Response body</span></span>

<span data-ttu-id="c433e-p106">Al crear una propiedad extendida en un recurso compatible distinto a la [publicación de grupo](../resources/post.md), la respuesta incluye solo la instancia nueva o existente, pero no la nueva propiedad extendida. Para ver la propiedad extendida recién creada, [expanda la instancia con la propiedad extendida](../api/multivaluelegacyextendedproperty-get.md).</span><span class="sxs-lookup"><span data-stu-id="c433e-p106">When creating an extended property in a supported resource other than [group post](../resources/post.md), the response includes only the new or existing instance but not the new extended property. To see the newly created extended property, [get the instance expanded with the extended property](../api/multivaluelegacyextendedproperty-get.md).</span></span>

<span data-ttu-id="c433e-p107">Al crear una propiedad extendida en una publicación de grupo _nueva_, la respuesta incluye solo un código de respuesta, pero no la nueva publicación ni la propiedad extendida. No puede crear una propiedad extendida en una publicación de grupo existente.</span><span class="sxs-lookup"><span data-stu-id="c433e-p107">When creating an extended property in a _new_ group post, the response includes only a response code but not the new post nor the extended property. You cannot create an extended property in an existing group post.</span></span>


## <a name="example"></a><span data-ttu-id="c433e-204">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c433e-204">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="c433e-205">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="c433e-205">Request 1</span></span>

<span data-ttu-id="c433e-p108">En el primer ejemplo se crea una propiedad extendida de varios valores en un nuevo evento durante la misma operación POST. Aparte de las propiedades que normalmente incluiría en un nuevo evento, el cuerpo de la solicitud incluye la colección **multiValueExtendedProperties** que contiene una propiedad extendida. El cuerpo de la solicitud incluye lo siguiente para esa propiedad extendida de varios valores:</span><span class="sxs-lookup"><span data-stu-id="c433e-p108">The first example creates a multi-value extended property in a new event all in the same POST operation. Apart from the properties you'd normally include for a new event, the request body includes the **multiValueExtendedProperties** collection which contains one extended property. The request body includes the following for that multi-value extended property:</span></span>

- <span data-ttu-id="c433e-209">**id**, que especifica la propiedad como una matriz de cadenas con el GUID especificado y el nombre `Recreation`.</span><span class="sxs-lookup"><span data-stu-id="c433e-209">**id** which specifies the property as an array of strings with the specified GUID and the name `Recreation`.</span></span> 
- <span data-ttu-id="c433e-210">**value**, que especifica `Recreation` como una matriz de 3 valores de cadena, `["Food", "Hiking", "Swimming"]`.</span><span class="sxs-lookup"><span data-stu-id="c433e-210">**value** which specifies `Recreation` as an array of 3 string values, `["Food", "Hiking", "Swimming"]`.</span></span>
 

<!-- { "blockType": "ignored" } -->
```http
POST https://graph.microsoft.com/v1.0/me/events
Content-Type: application/json

{
  "subject": "Family reunion",
  "body": {
    "contentType": "HTML",
    "content": "Let's get together this Thanksgiving!"
  },
  "start": {
      "dateTime": "2015-11-26T09:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "end": {
      "dateTime": "2015-11-29T21:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "attendees": [
    {
      "emailAddress": {
        "address": "Terrie@contoso.com",
        "name": "Terrie Barrera"
      },
      "type": "Required"
    },
    {
      "emailAddress": {
        "address": "Lauren@contoso.com",
        "name": "Lauren Solis"
      },
      "type": "Required"
    }
  ],
  "multiValueExtendedProperties": [
     {
           "id":"StringArray {66f5a359-4659-4830-9070-00050ec6ac6e} Name Recreation",
           "value": ["Food", "Hiking", "Swimming"]
     }
  ]
}
```

##### <a name="response-1"></a><span data-ttu-id="c433e-211">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="c433e-211">Response 1</span></span>

<span data-ttu-id="c433e-p109">Una respuesta correcta se indica mediante un código de respuesta `HTTP 201 Created` e incluye el nuevo evento en el cuerpo de la respuesta. Es similar a la respuesta al [crear solo un evento](../api/user-post-events.md). El cuerpo de la respuesta no incluye ninguna propiedad extendida recién creada.</span><span class="sxs-lookup"><span data-stu-id="c433e-p109">A successful response is indicated by an `HTTP 201 Created` response code, and includes the new event in the response body, similar to the response from [creating just an event](../api/user-post-events.md). The response does not include any newly created extended properties.</span></span>

<span data-ttu-id="c433e-214">Para ver la propiedad extendida recién creada, [expanda el evento con la propiedad extendida](../api/multivaluelegacyextendedproperty-get.md).</span><span class="sxs-lookup"><span data-stu-id="c433e-214">To see the newly created extended property, [get the event expanded with the extended property](../api/multivaluelegacyextendedproperty-get.md).</span></span>


****

##### <a name="request-2"></a><span data-ttu-id="c433e-215">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="c433e-215">Request 2</span></span>

<span data-ttu-id="c433e-p110">El segundo ejemplo crea una propiedad extendida de varios valores para el mensaje especificado. La propiedad extendida es el único elemento de la colección **multiValueExtendedProperties**. El cuerpo de la solicitud incluye lo siguiente para la propiedad extendida de varios valores:</span><span class="sxs-lookup"><span data-stu-id="c433e-p110">The second example creates one multi-value extended property for the specified message. That extended property is the only element in the **multiValueExtendedProperties** collection. The request body includes the following for the extended property:</span></span>

- <span data-ttu-id="c433e-219">**id** especifica la propiedad como una matriz de cadenas con el GUID especificado y el nombre `Palette`.</span><span class="sxs-lookup"><span data-stu-id="c433e-219">**id** specifies the property as an array of strings with the specified GUID and the name `Palette`.</span></span>
- <span data-ttu-id="c433e-220">**valor** especifica `Palette` como una matriz de 3 valores de cadena, `["Green", "Aqua", "Blue"]`.</span><span class="sxs-lookup"><span data-stu-id="c433e-220">**value** specifies `Palette` as an array of 3 string values, `["Green", "Aqua", "Blue"]`.</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH https://graph.microsoft.com/v1.0/me/messages('AAMkAGE1M2_as77AACHsLrBBBA=')

Content-Type: application/json

{
  "multiValueExtendedProperties": [
      {
         "id":"StringArray {66f5a359-4659-4830-9070-00049ec6ac6e} Name Palette",
         "value":["Green", "Aqua", "Blue"]
      }
    ]
}
```

##### <a name="response-2"></a><span data-ttu-id="c433e-221">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="c433e-221">Response 2</span></span>

<span data-ttu-id="c433e-p111">Una respuesta correcta se indica mediante un código de respuesta `HTTP 200 OK` e incluye el mensaje especificado en el cuerpo de la respuesta. Es similar a la respuesta al [actualizar un mensaje](../api/message-update.md). El cuerpo de la respuesta no incluye la propiedad extendida recién creada.</span><span class="sxs-lookup"><span data-stu-id="c433e-p111">A successful response is indicated by an `HTTP 200 OK` response code, and includes the specified message in the response body, similar to the response from [updating a message](../api/message-update.md). The response does not include the newly created extended property.</span></span>

<span data-ttu-id="c433e-224">Para ver la propiedad extendida recién creada, [expanda el mensaje con la propiedad extendida](../api/multivaluelegacyextendedproperty-get.md).</span><span class="sxs-lookup"><span data-stu-id="c433e-224">To see the newly created extended property, [get the message expanded with the extended property](../api/multivaluelegacyextendedproperty-get.md).</span></span>


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




