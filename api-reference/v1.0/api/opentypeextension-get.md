---
title: Obtener extensión abierta
description: Obtenga una extensión abierta (objeto openTypeExtension) identificada por nombre o por nombre completo.
ms.openlocfilehash: 1de9921bb9b2275d852de6fa92c1b6230a671555
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028567"
---
# <a name="get-open-extension"></a><span data-ttu-id="b6593-103">Obtener extensión abierta</span><span class="sxs-lookup"><span data-stu-id="b6593-103">Get open extension</span></span>

<span data-ttu-id="b6593-104">Obtenga una extensión abierta (objeto [openTypeExtension](../resources/opentypeextension.md)) identificada por nombre o por nombre completo.</span><span class="sxs-lookup"><span data-stu-id="b6593-104">Get an open extension ([openTypeExtension](../resources/opentypeextension.md) object) identified by name or fully qualified name.</span></span>

<span data-ttu-id="b6593-105">En la tabla siguiente, se enumeran tres escenarios en los que puede obtener una extensión abierta de una instancia de recurso admitida.</span><span class="sxs-lookup"><span data-stu-id="b6593-105">The following table lists the three scenarios where you can get an open extension from a supported resource instance.</span></span>

|<span data-ttu-id="b6593-106">**Escenario de GET**</span><span class="sxs-lookup"><span data-stu-id="b6593-106">**GET scenario**</span></span>|<span data-ttu-id="b6593-107">**Recursos admitidos**</span><span class="sxs-lookup"><span data-stu-id="b6593-107">**Supported resources**</span></span>|<span data-ttu-id="b6593-108">**Cuerpo de la respuesta**</span><span class="sxs-lookup"><span data-stu-id="b6593-108">**Response body**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b6593-109">Obtenga una extensión específica de una instancia de recurso conocida.</span><span class="sxs-lookup"><span data-stu-id="b6593-109">Get a specific extension from a known resource instance.</span></span>| <span data-ttu-id="b6593-110">[Dispositivo](../resources/device.md), [evento](../resources/event.md), [grupo](../resources/group.md), [evento de grupo](../resources/event.md), [publicación de grupo](../resources/post.md), [mensaje](../resources/message.md), [organización](../resources/organization.md), [contacto personal](../resources/contact.md), [usuario](../resources/user.md)</span><span class="sxs-lookup"><span data-stu-id="b6593-110">[Device](../resources/device.md), [event](../resources/event.md), [group](../resources/group.md), [group event](../resources/event.md), [group post](../resources/post.md), [message](../resources/message.md), [organization](../resources/organization.md), [personal contact](../resources/contact.md), [user](../resources/user.md)</span></span> | <span data-ttu-id="b6593-111">Solo extensiones abiertas.</span><span class="sxs-lookup"><span data-stu-id="b6593-111">Open extension only.</span></span>|
|<span data-ttu-id="b6593-112">Expanda una instancia de recurso conocida con una extensión específica.</span><span class="sxs-lookup"><span data-stu-id="b6593-112">Get a known resource instance expanded with a specific extension.</span></span>|<span data-ttu-id="b6593-113">Dispositivo, evento, grupo, evento de grupo, publicación de grupo, mensaje, organización, contacto personal, usuario</span><span class="sxs-lookup"><span data-stu-id="b6593-113">Device, event, group, group event, group post, message, organization, personal contact, user</span></span> |<span data-ttu-id="b6593-114">Una instancia de recurso expandida con la extensión abierta.</span><span class="sxs-lookup"><span data-stu-id="b6593-114">A resource instance expanded with the open extension.</span></span>|
|<span data-ttu-id="b6593-115">Busque y expanda las instancias de recurso con una extensión específica.</span><span class="sxs-lookup"><span data-stu-id="b6593-115">Find and expand resource instances with a specific extension.</span></span> |<span data-ttu-id="b6593-116">Evento, evento de grupo, publicación de grupo, mensaje, contacto personal</span><span class="sxs-lookup"><span data-stu-id="b6593-116">Event, group event, group post, message, personal contact</span></span>|<span data-ttu-id="b6593-117">Instancias de recurso expandidas con la extensión abierta.</span><span class="sxs-lookup"><span data-stu-id="b6593-117">Resource instances expanded with the open extension.</span></span>|

## <a name="permissions"></a><span data-ttu-id="b6593-118">Permisos</span><span class="sxs-lookup"><span data-stu-id="b6593-118">Permissions</span></span>

<span data-ttu-id="b6593-119">Dependiendo del recurso que contiene la extensión y el permiso solicitado tipo (delegada o de la aplicación), el permiso especificado en la tabla siguiente es la con privilegios mínimos necesarios para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b6593-119">Depending on the resource that contains the extension and the permission type (delegated or application) requested, the permission specified in the following table is the least privileged required to call this API.</span></span> <span data-ttu-id="b6593-120">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b6593-120">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="b6593-121">Recurso admitido</span><span class="sxs-lookup"><span data-stu-id="b6593-121">Supported resource</span></span> | <span data-ttu-id="b6593-122">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b6593-122">Delegated (work or school account)</span></span> | <span data-ttu-id="b6593-123">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b6593-123">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b6593-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b6593-124">Application</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="b6593-125">device</span><span class="sxs-lookup"><span data-stu-id="b6593-125">device</span></span>](../resources/device.md) | <span data-ttu-id="b6593-126">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="b6593-126">Directory.Read.All</span></span> | <span data-ttu-id="b6593-127">No admitido</span><span class="sxs-lookup"><span data-stu-id="b6593-127">Not supported</span></span> | <span data-ttu-id="b6593-128">Device.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b6593-128">Device.ReadWrite.All</span></span> |
| [<span data-ttu-id="b6593-129">evento</span><span class="sxs-lookup"><span data-stu-id="b6593-129">event</span></span>](../resources/event.md) | <span data-ttu-id="b6593-130">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="b6593-130">Calendars.Read</span></span> | <span data-ttu-id="b6593-131">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="b6593-131">Calendars.Read</span></span> | <span data-ttu-id="b6593-132">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="b6593-132">Calendars.Read</span></span> |
| [<span data-ttu-id="b6593-133">group</span><span class="sxs-lookup"><span data-stu-id="b6593-133">group</span></span>](../resources/group.md) | <span data-ttu-id="b6593-134">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="b6593-134">Group.Read.All</span></span> | <span data-ttu-id="b6593-135">No admitido</span><span class="sxs-lookup"><span data-stu-id="b6593-135">Not supported</span></span> | <span data-ttu-id="b6593-136">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="b6593-136">Group.Read.All</span></span> |
| [<span data-ttu-id="b6593-137">evento de grupo</span><span class="sxs-lookup"><span data-stu-id="b6593-137">group event</span></span>](../resources/event.md) | <span data-ttu-id="b6593-138">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="b6593-138">Group.Read.All</span></span> | <span data-ttu-id="b6593-139">No admitido</span><span class="sxs-lookup"><span data-stu-id="b6593-139">Not supported</span></span> | <span data-ttu-id="b6593-140">No admitido</span><span class="sxs-lookup"><span data-stu-id="b6593-140">Not supported</span></span> |
| [<span data-ttu-id="b6593-141">publicación de grupo</span><span class="sxs-lookup"><span data-stu-id="b6593-141">group post</span></span>](../resources/post.md) | <span data-ttu-id="b6593-142">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="b6593-142">Group.Read.All</span></span> | <span data-ttu-id="b6593-143">No admitido</span><span class="sxs-lookup"><span data-stu-id="b6593-143">Not supported</span></span> | <span data-ttu-id="b6593-144">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="b6593-144">Group.Read.All</span></span> |
| [<span data-ttu-id="b6593-145">message</span><span class="sxs-lookup"><span data-stu-id="b6593-145">message</span></span>](../resources/message.md) | <span data-ttu-id="b6593-146">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="b6593-146">Mail.Read</span></span> | <span data-ttu-id="b6593-147">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="b6593-147">Mail.Read</span></span> | <span data-ttu-id="b6593-148">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="b6593-148">Mail.Read</span></span> | 
| [<span data-ttu-id="b6593-149">organization</span><span class="sxs-lookup"><span data-stu-id="b6593-149">organization</span></span>](../resources/organization.md) | <span data-ttu-id="b6593-150">User.Read</span><span class="sxs-lookup"><span data-stu-id="b6593-150">User.Read</span></span> | <span data-ttu-id="b6593-151">No admitido</span><span class="sxs-lookup"><span data-stu-id="b6593-151">Not supported</span></span> | <span data-ttu-id="b6593-152">No admitido</span><span class="sxs-lookup"><span data-stu-id="b6593-152">Not supported</span></span> |
| [<span data-ttu-id="b6593-153">contacto personal</span><span class="sxs-lookup"><span data-stu-id="b6593-153">personal contact</span></span>](../resources/contact.md) | <span data-ttu-id="b6593-154">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="b6593-154">Contacts.Read</span></span> | <span data-ttu-id="b6593-155">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="b6593-155">Contacts.Read</span></span> | <span data-ttu-id="b6593-156">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="b6593-156">Contacts.Read</span></span> |
| [<span data-ttu-id="b6593-157">user</span><span class="sxs-lookup"><span data-stu-id="b6593-157">user</span></span>](../resources/user.md) | <span data-ttu-id="b6593-158">User.Read</span><span class="sxs-lookup"><span data-stu-id="b6593-158">User.Read</span></span> | <span data-ttu-id="b6593-159">User.Read</span><span class="sxs-lookup"><span data-stu-id="b6593-159">User.Read</span></span> | <span data-ttu-id="b6593-160">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="b6593-160">User.Read.All</span></span> |


## <a name="http-request"></a><span data-ttu-id="b6593-161">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b6593-161">HTTP request</span></span>

<span data-ttu-id="b6593-162">En esta sección, se muestra la sintaxis de cada uno de los tres escenarios de `GET` descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b6593-162">This section lists the syntax for each of the three `GET` scenarios described above.</span></span>

### <a name="get-a-specific-extension-in-a-known-resource-instance"></a><span data-ttu-id="b6593-163">Obtener una extensión específica en una instancia de recurso conocida.</span><span class="sxs-lookup"><span data-stu-id="b6593-163">Get a specific extension in a known resource instance</span></span>

<span data-ttu-id="b6593-164">Utilice la misma solicitud REST que para la instancia de recurso e identifique la extensión utilizando la propiedad de navegación **extensiones** de esa instancia.</span><span class="sxs-lookup"><span data-stu-id="b6593-164">Use the same REST request as getting the resource instance, and identify the extension using the **extensions** navigation property of that instance.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /devices/{Id}/extensions/{extensionId}
GET /users/{Id|userPrincipalName}/events/{Id}/extensions/{extensionId}
GET /groups/{Id}/extensions/{extensionId}
GET /groups/{Id}/events/{Id}/extensions/{extensionId}
GET /groups/{Id}/threads/{Id}/posts/{Id}/extensions/{extensionId}
GET /users/{Id|userPrincipalName}/messages/{Id}/extensions/{extensionId}
GET /organization/{Id}/extensions/{extensionId}
GET /users/{Id|userPrincipalName}/contacts/{Id}/extensions/{extensionId}
GET /users/{Id|userPrincipalName}/extensions/{extensionId}
```


### <a name="get-a-known-resource-instance-expanded-with-a-matching-extension"></a><span data-ttu-id="b6593-165">Expanda una instancia de recurso conocida con una extensión coincidente.</span><span class="sxs-lookup"><span data-stu-id="b6593-165">Get a known resource instance expanded with a matching extension</span></span> 

<span data-ttu-id="b6593-p102">Para los tipos de recurso evento, evento de grupo, publicación de grupo, mensaje y contacto personal, utilice la misma solicitud REST que al obtener la instancia de recurso, busque una extensión que coincida con un filtro en su propiedad **id** y expanda la instancia con la extensión. La respuesta incluye la mayoría de las propiedades del recurso.</span><span class="sxs-lookup"><span data-stu-id="b6593-p102">For the event, group event, group post, message, personal contact resource types, you can use the same REST request as getting the resource instance, look for an extension that matches a filter on its **id** property, and expand the instance with the extension. The response includes most of the resource properties.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Id|userPrincipalName}/events/{Id}?$expand=extensions($filter=id eq '{extensionId}')
GET /groups/{Id}/events/{Id}?$expand=extensions($filter=id eq '{extensionId}')
GET /groups/{Id}/threads/{Id}/posts/{Id}?$expand=extensions($filter=id eq '{extensionId}')
GET /users/{Id|userPrincipalName}/messages/{Id}?$expand=extensions($filter=id eq '{extensionId}')
GET /users/{Id|userPrincipalName}/contacts/{Id}?$expand=extensions($filter=id eq '{extensionId}')
```


<span data-ttu-id="b6593-168">Para los tipos de recurso dispositivo, grupo, organización y usuario, también debe usar un parámetro `$select` para incluir la propiedad **id** y las demás propiedades que desee de la instancia del recurso:</span><span class="sxs-lookup"><span data-stu-id="b6593-168">For the device, group, organization, and user resource types, you must also use a `$select` parameter to include the **id** property and any other properties you want from the resource instance:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /devices/{Id}?$expand=extensions($filter=id eq '{extensionId}')&$select=id,{property_1},{property_n}
GET /groups/{Id}?$expand=extensions($filter=id eq '{extensionId}')&$select=id,{property_1},{property_n}
GET /organization/{Id}?$expand=extensions($filter=id eq '{extensionId}')&$select=id,{property_1},{property_n}
GET /users/{Id|userPrincipalName}?$expand=extensions($filter=id eq '{extensionId}')&$select=id,{property_1},{property_n}
```

### <a name="filter-for-resource-instances-expanded-with-a-matching-extension"></a><span data-ttu-id="b6593-169">Filtre una instancia de recurso con una extensión coincidente.</span><span class="sxs-lookup"><span data-stu-id="b6593-169">Filter for resource instances expanded with a matching extension</span></span> 

<span data-ttu-id="b6593-170">Use la misma solicitud REST que al obtener una colección del recurso admitido, filtre la colección por instancias que contengan una extensión con una propiedad **id** coincidente y expándalas con la extensión.</span><span class="sxs-lookup"><span data-stu-id="b6593-170">Use the same REST request as getting a collection of the supported resource, filter the collection for instances that contain an extension with a matching **id** property, and expand these instances with the extension.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Id|userPrincipalName}/events?$filter=Extensions/any(f:f/id eq '{extensionId}')&$expand=Extensions($filter=id eq '{extensionId}')
GET /groups/{Id}/events?$filter=Extensions/any(f:f/id eq '{extensionId}')&$expand=Extensions($filter=id eq '{extensionId}')
GET /groups/{Id}/threads/{Id}/posts?$filter=Extensions/any(f:f/id eq '{extensionId}')&$expand=Extensions($filter=id eq '{extensionId}')
GET /users/{Id|userPrincipalName}/messages?$filter=Extensions/any(f:f/id eq '{extensionId}')&$expand=Extensions($filter=id eq '{extensionId}')
GET /users/{Id|userPrincipalName}/contacts?$filter=Extensions/any(f:f/id eq '{extensionId}')&$expand=Extensions($filter=id eq '{extensionId}')
```

><span data-ttu-id="b6593-p103">**Nota:** La sintaxis anterior muestra algunas formas comunes para identificar una instancia del recurso o colección, con el fin de obtener una extensión de él. Todas las otras formas de sintaxis que le permiten identificar estas instancias o colecciones de recursos admiten la obtención de extensiones abiertas de ellas de una manera similar.</span><span class="sxs-lookup"><span data-stu-id="b6593-p103">**Note:** The above syntax shows some common ways to identify a resource instance or collection, in order to get an extension from it. All other syntax that allows you to identify these resource instances or collections supports getting open extensions from them in a similar way.</span></span>

## <a name="path-parameters"></a><span data-ttu-id="b6593-173">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="b6593-173">Path parameters</span></span>
|<span data-ttu-id="b6593-174">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b6593-174">Parameter</span></span>|<span data-ttu-id="b6593-175">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6593-175">Type</span></span>|<span data-ttu-id="b6593-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6593-176">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b6593-177">Id</span><span class="sxs-lookup"><span data-stu-id="b6593-177">Id</span></span>|<span data-ttu-id="b6593-178">string</span><span class="sxs-lookup"><span data-stu-id="b6593-178">string</span></span>|<span data-ttu-id="b6593-p104">Marcador de posición de un identificador único para un objeto en la colección correspondiente, como mensajes, contactos o eventos. Necesario. No se debe confundir con la propiedad **id** de una **openTypeExtension**.</span><span class="sxs-lookup"><span data-stu-id="b6593-p104">Placeholder for a unique identifier for an object in the corresponding collection such as messages, events, contacts. Required. Not to be confused with the **id** property of an **openTypeExtension**.</span></span>|
|<span data-ttu-id="b6593-182">extensionId</span><span class="sxs-lookup"><span data-stu-id="b6593-182">extensionId</span></span>|<span data-ttu-id="b6593-183">string</span><span class="sxs-lookup"><span data-stu-id="b6593-183">string</span></span>|<span data-ttu-id="b6593-p105">Marcador de posición para un nombre de extensión que es un identificador de texto único de una extensión o un nombre completo que concatena el tipo de extensión y un identificador de texto único. Se devuelve el nombre completo de la propiedad **id** cuando crea la extensión. Necesario.</span><span class="sxs-lookup"><span data-stu-id="b6593-p105">Placeholder for an extension name which is a unique text identifier for an extension, or a fully qualified name which concatenates the extension type and unique text identifier. The fully qualified name is returned in the **id** property when you create the extension. Required.</span></span>|

## <a name="optional-query-parameters"></a><span data-ttu-id="b6593-187">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b6593-187">Optional query parameters</span></span>

<span data-ttu-id="b6593-188">Asegúrese de aplicar [la codificación de direcciones URL](https://www.w3schools.com/tags/ref_urlencode.asp) a los caracteres de espacio de la cadena `$filter`.</span><span class="sxs-lookup"><span data-stu-id="b6593-188">Make sure you apply [URL encoding](https://www.w3schools.com/tags/ref_urlencode.asp) to the space characters in the `$filter` string.</span></span>

|<span data-ttu-id="b6593-189">Nombre</span><span class="sxs-lookup"><span data-stu-id="b6593-189">Name</span></span>|<span data-ttu-id="b6593-190">Valor</span><span class="sxs-lookup"><span data-stu-id="b6593-190">Value</span></span>|<span data-ttu-id="b6593-191">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6593-191">Description</span></span>|
|:---------------|:--------|:-------|
|<span data-ttu-id="b6593-192">$filter</span><span class="sxs-lookup"><span data-stu-id="b6593-192">$filter</span></span>|<span data-ttu-id="b6593-193">string</span><span class="sxs-lookup"><span data-stu-id="b6593-193">string</span></span>|<span data-ttu-id="b6593-194">Devuelve una extensión cuyo **identificador** coincide con el valor de parámetro `extensionId`.</span><span class="sxs-lookup"><span data-stu-id="b6593-194">Returns an extension with its **id** matching the `extensionId` parameter value.</span></span>|
|<span data-ttu-id="b6593-195">$filter con **cualquier** operador</span><span class="sxs-lookup"><span data-stu-id="b6593-195">$filter with **any** operator</span></span>|<span data-ttu-id="b6593-196">string</span><span class="sxs-lookup"><span data-stu-id="b6593-196">string</span></span>|<span data-ttu-id="b6593-197">Devuelve instancias de una colección de recursos que contienen una extensión cuyo **identificador** coincide con el valor de parámetro `extensionId`.</span><span class="sxs-lookup"><span data-stu-id="b6593-197">Returns instances of a resource collection that contain an extension with its **id** matching the `extensionId` parameter value.</span></span>|
|<span data-ttu-id="b6593-198">$expand</span><span class="sxs-lookup"><span data-stu-id="b6593-198">$expand</span></span>|<span data-ttu-id="b6593-199">string</span><span class="sxs-lookup"><span data-stu-id="b6593-199">string</span></span>|<span data-ttu-id="b6593-200">Expande una instancia de recurso para incluir una extensión.</span><span class="sxs-lookup"><span data-stu-id="b6593-200">Expands a resource instance to include an extension.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="b6593-201">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b6593-201">Request headers</span></span>
| <span data-ttu-id="b6593-202">Nombre</span><span class="sxs-lookup"><span data-stu-id="b6593-202">Name</span></span>       | <span data-ttu-id="b6593-203">Valor</span><span class="sxs-lookup"><span data-stu-id="b6593-203">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="b6593-204">Authorization</span><span class="sxs-lookup"><span data-stu-id="b6593-204">Authorization</span></span> | <span data-ttu-id="b6593-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b6593-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b6593-207">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b6593-207">Request body</span></span>
<span data-ttu-id="b6593-208">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b6593-208">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b6593-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6593-209">Response</span></span>

<span data-ttu-id="b6593-p107">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [openTypeExtension](../resources/opentypeextension.md) en el cuerpo de la respuesta. El cuerpo exacto de la respuesta variará según la consulta GET.</span><span class="sxs-lookup"><span data-stu-id="b6593-p107">If successful, this method returns a `200 OK` response code and [openTypeExtension](../resources/opentypeextension.md) object in the response body. Depending on the GET query, the exact response body differs.</span></span>
## <a name="example"></a><span data-ttu-id="b6593-212">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6593-212">Example</span></span>

#### <a name="request-1"></a><span data-ttu-id="b6593-213">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="b6593-213">Request 1</span></span>

<span data-ttu-id="b6593-p108">El primer ejemplo muestra 2 formas para hacer referencia a una extensión y obtiene la extensión en el mensaje especificado. La respuesta es la misma independientemente de la forma utilizada para hacer referencia a la extensión.</span><span class="sxs-lookup"><span data-stu-id="b6593-p108">The first example shows 2 ways of referencing an extension and gets the extension in the specified message. The response is the same regardless of the way used to reference the extension.</span></span>

<span data-ttu-id="b6593-216">En primer lugar, por su nombre:</span><span class="sxs-lookup"><span data-stu-id="b6593-216">First, by its name:</span></span> 

<!-- {
  "blockType": "request",
  "sampleKeys": ["Com.Contoso.Referral", "AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl==="],
  "name": "get_opentypeextension_1"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===/extensions/Com.Contoso.Referral
```

<span data-ttu-id="b6593-217">En segundo lugar, por su identificador (nombre completo):</span><span class="sxs-lookup"><span data-stu-id="b6593-217">Second, by its ID (fully qualified name):</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/messages/AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===/extensions/Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral
```

#### <a name="response-1"></a><span data-ttu-id="b6593-218">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="b6593-218">Response 1</span></span>
<span data-ttu-id="b6593-219">Aquí tiene la respuesta del primer ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b6593-219">Here is the response for the first example.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.openTypeExtension"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions/$entity",
    "@odata.type": "#microsoft.graph.openTypeExtension",
    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfc984d-b826-40d7-b48b-57002df85e00@1717f226-49d1-4d0c-9d74-709fad6677b4')/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions
('Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')",
    "extensionName": "Com.Contoso.Referral",
    "id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral",
    "companyName": "Wingtip Toys",
    "dealValue": 500050,
    "expirationDate": "2015-12-03T10:00:00Z"
}
```

****


#### <a name="request-2"></a><span data-ttu-id="b6593-220">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="b6593-220">Request 2</span></span>

<span data-ttu-id="b6593-221">El segundo ejemplo hace referencia a una extensión por su nombre y obtiene la extensión en el evento de grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="b6593-221">The second example references an extension by its name and gets the extension in the specified group event.</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["Com.Contoso.Deal", "f5480dfd-7d77-4d0b-ba2e-3391953cc74a", "AAMkADVl17IsAAA="],
  "name": "get_opentypeextension_2"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/f5480dfd-7d77-4d0b-ba2e-3391953cc74a/events/AAMkADVl17IsAAA=/extensions/Com.Contoso.Deal/
```

#### <a name="response-2"></a><span data-ttu-id="b6593-222">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="b6593-222">Response 2</span></span>

<span data-ttu-id="b6593-223">Aquí tiene la respuesta del segundo ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b6593-223">Here is the response from the second example.</span></span>

<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.openTypeExtension"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#groups('f5480dfd-7d77-4d0b-ba2e-3391953cc74a')/events('AAMkADVl7IsAAA%3D')/extensions/$entity",
    "@odata.type": "#microsoft.graph.openTypeExtension",
    "id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Deal",
    "extensionName": "Com.Contoso.Deal",
    "companyName": "Alpine Skis",
    "dealValue": 1010100,
    "expirationDate": "2015-07-03T13:04:00Z"
}
```

****

#### <a name="request-3"></a><span data-ttu-id="b6593-224">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="b6593-224">Request 3</span></span>

<span data-ttu-id="b6593-p109">El tercer ejemplo obtiene y expande el mensaje especificado incluyendo la extensión devuelta desde un filtro. El filtro devuelve la extensión cuyo **identificador** coincide con un nombre completo.</span><span class="sxs-lookup"><span data-stu-id="b6593-p109">The third example gets and expands the specified message by including the extension returned from a filter. The filter returns the extension that has its **id** matching a fully qualified name.</span></span>

<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl==="],
  "name": "get_opentypeextension_3"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===?$expand=extensions($filter=id%20eq%20'Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')
```


#### <a name="response-3"></a><span data-ttu-id="b6593-227">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="b6593-227">Response 3</span></span>

<span data-ttu-id="b6593-p110">Y aquí tiene la respuesta del tercer ejemplo. Nota: Puede que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b6593-p110">And here is the response from the third example. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/messages/$entity",
    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfc984d-b826-40d7-b48b-57002df85e00@1717f226-49d1-4d0c-9d74-709fad6677b4')/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')",
    "@odata.etag": "W/\"CQAAABYAAACY4MQpaFz9SbqUDe4+bs88AABNsWMM\"",
    "id": "AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===",
    "changeKey": "CQAAABYAAACY4MQpaFz9SbqUDe4+bs88AABNsWMM",
    "categories": [
    ],
    "createDateTime": "2015-06-19T02:03:31Z",
    "lastModifiedDateTime": "2015-08-13T02:28:00Z",
    "subject": "Attached is the requested info",
    "bodyPreview": "See the images attached.",
    "body": {
        "contentType": "HTML",
        "content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n<style type=\"text/css\" style=\"display:none;\"><!-- P {margin-top:0;margin-bottom:0;} --></style>\r\n</head>\r\n<body dir=\"ltr\">\r\n<div id=\"divtagdefaultwrapper\" style=\"font-size:12pt;color:#000000;background-color:#FFFFFF;font-family:Calibri,Arial,Helvetica,sans-serif;\">\r\n<p>See the images attached. <br>\r\n</p>\r\n</div>\r\n</body>\r\n</html>\r\n"
    },
    "importance": "Normal",
    "hasAttachments": true,
    "parentFolderId": "AQMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===QAAAA==",
    "from": {
        "emailAddress": {
            "address": "desmond@contoso.com",
            "name": "Desmond Raley"
        }
    },
    "sender": {
        "emailAddress": {
            "address": "desmond@contoso.com",
            "name": "Desmond Raley"
        }
    },
    "toRecipients": [
        {
            "emailAddress": {
                "address": "wendy@contoso.com",
                "name": "Wendy Molina"
            }
        }
    ],
    "ccRecipients": [
    ],
    "bccRecipients": [
    ],
    "replyTo": [
    ],
    "conversationId": "AAQkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===mivdTmQ=",
    "receivedDateTime": "2015-06-19T02:05:04Z",
    "sentDateTime": "2015-06-19T02:04:59Z",
    "isDeliveryReceiptRequested": false,
    "isReadReceiptRequested": false,
    "isDraft": false,
    "isRead": true,
    "webLink": "https://outlook.office.com/owa/?ItemID=AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===%2FNJTqt5NqHlVnKVBwCY4MQpaFz9SbqUDe4%2Bbs88AAAAAAEJAACY4MQpaFz9SbqUDe4%2Bbs88AAApA4JMAAA%3D&exvsurl=1&viewmodel=ReadMessageItem",
    "inferenceClassification": "Focused",
    "extensions@odata.context": "https://graph.microsoft.com/v1.0/$metadata#users('desmond40contoso.com')/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions", 
    "extensions": [ 
      { 
        "@odata.type": "#microsoft.graph.openTypeExtension",
        "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfc984d-b826-40d7-b48b-57002df85e00@1717f226-49d1-4d0c-9d74-709fad6677b4')/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions('Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')",
        "extensionName": "Com.Contoso.Referral",
        "id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral",
        "companyName": "Wingtip Toys",
        "dealValue": 500050,
        "expirationDate": "2015-12-03T10:00:00Z"
      }
     ]
}
```

****

#### <a name="request-4"></a><span data-ttu-id="b6593-231">Solicitud 4</span><span class="sxs-lookup"><span data-stu-id="b6593-231">Request 4</span></span>

<span data-ttu-id="b6593-232">El cuarto ejemplo hace referencia a una extensión por su nombre completo y obtiene la extensión en la publicación de grupo especificada.</span><span class="sxs-lookup"><span data-stu-id="b6593-232">The fourth example references an extension by its fully qualified name and gets the extension in the specified group post.</span></span>

<!-- {
  "blockType": "ignored",
  "name": "get_opentypeextension_4"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/37df2ff0-0de0-4c33-8aee-75289364aef6/threads/AAQkADJizZJpEWwqDHsEpV_KA==/posts/AAMkADJiUg96QZUkA-ICwMubAADDEd7UAAA=/extensions/Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Estimate
```

#### <a name="response-4"></a><span data-ttu-id="b6593-233">Respuesta 4</span><span class="sxs-lookup"><span data-stu-id="b6593-233">Response 4</span></span>

<span data-ttu-id="b6593-234">Aquí tiene la respuesta del cuarto ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b6593-234">Here is the response from the fourth example.</span></span> 

<!-- {
  "blockType": "ignored",
  "truncated": false,
  "@odata.type": "microsoft.graph.openTypeExtension"
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#groups('37df2ff0-0de0-4c33-8aee-75289364aef6')/threads('AAQkADJizZJpEWwqDHsEpV_KA%3D%3D')/posts('AAMkADJiUg96QZUkA-ICwMubAADDEd7UAAA%3D')/extensions/$entity",
    "@odata.type": "#microsoft.graph.openTypeExtension",
    "id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Estimate",
    "extensionName": "Com.Contoso.Estimate",
    "companyName": "Contoso",
    "expirationDate": "2015-07-03T13:04:00Z",
    "Strings@odata.type": "#Collection(String)",
    "topPicks": [
        "Employees only",
        "Add spouse or guest",
        "Add family"
    ]
}
```


#### <a name="request-5"></a><span data-ttu-id="b6593-235">Solicitud 5</span><span class="sxs-lookup"><span data-stu-id="b6593-235">Request 5</span></span>

<span data-ttu-id="b6593-p111">El quinto ejemplo examina todos los mensajes en el buzón del usuario que inició sesión para buscar aquellos con una extensión que coincide con un filtro y los expande con la extensión. El filtro devuelve las extensiones cuya propiedad **id** coincide con el nombre de extensión `Com.Contoso.Referral`.</span><span class="sxs-lookup"><span data-stu-id="b6593-p111">The fifth example looks at all messages in the signed-in user's mailbox to find those that contain an extension matching a filter, and expands them by including the extension. The filter returns extensions that has the **id** property matching the extension name `Com.Contoso.Referral`.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_opentypeextension_5"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages?$filter=Extensions/any(f:f/id%20eq%20'Com.Contoso.Referral')&$expand=Extensions($filter=id%20eq%20'Com.Contoso.Referral')
```


####<a name="response-5"></a><span data-ttu-id="b6593-238">Respuesta 5</span><span class="sxs-lookup"><span data-stu-id="b6593-238">Response 5</span></span>

<span data-ttu-id="b6593-239">En esta respuesta del quinto ejemplo solo hay un mensaje en el buzón del usuario que tiene una extensión cuyo **identificador** es igual a `Com.Contoso.Referral`.</span><span class="sxs-lookup"><span data-stu-id="b6593-239">In this response for the fifth example, there is only one message in the user's mailbox that has an extension with its **id** equal to `Com.Contoso.Referral`.</span></span>

<span data-ttu-id="b6593-p112">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b6593-p112">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/messages",
  "value": [
  {

    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfc984d-b826-40d7-b48b-57002df85e00@1717f226-49d1-4d0c-9d74-709fad6677b4')/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')",
    "@odata.etag": "W/\"CQAAABYAAACY4MQpaFz9SbqUDe4+bs88AABNsWMM\"",
    "id": "AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===",
    "changeKey": "CQAAABYAAACY4MQpaFz9SbqUDe4+bs88AABNsWMM",
    "categories": [
    ],
    "createDateTime": "2015-06-19T02:03:31Z",
    "lastModifiedDateTime": "2015-08-13T02:28:00Z",
    "subject": "Attached is the requested info",
    "bodyPreview": "See the images attached.",
    "body": {
        "contentType": "HTML",
        "content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n<style type=\"text/css\" style=\"display:none;\"><!-- P {margin-top:0;margin-bottom:0;} --></style>\r\n</head>\r\n<body dir=\"ltr\">\r\n<div id=\"divtagdefaultwrapper\" style=\"font-size:12pt;color:#000000;background-color:#FFFFFF;font-family:Calibri,Arial,Helvetica,sans-serif;\">\r\n<p>See the images attached. <br>\r\n</p>\r\n</div>\r\n</body>\r\n</html>\r\n"
    },
    "importance": "Normal",
    "hasAttachments": true,
    "parentFolderId": "AQMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===QAAAA==",
    "from": {
        "emailAddress": {
            "address": "desmond@contoso.com",
            "name": "Desmond Raley"
        }
    },
    "sender": {
        "emailAddress": {
            "address": "desmond@contoso.com",
            "name": "Desmond Raley"
        }
    },
    "toRecipients": [
        {
            "emailAddress": {
                "address": "wendy@contoso.com",
                "name": "Wendy Molina"
            }
        }
    ],
    "ccRecipients": [
    ],
    "bccRecipients": [
    ],
    "replyTo": [
    ],
    "conversationId": "AAQkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===mivdTmQ=",
    "receivedDateTime": "2015-06-19T02:05:04Z",
    "sentDateTime": "2015-06-19T02:04:59Z",
    "isDeliveryReceiptRequested": false,
    "isReadReceiptRequested": false,
    "isDraft": false,
    "isRead": true,
    "webLink": "https://outlook.office.com/owa/?ItemID=AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===%2FNJTqt5NqHlVnKVBwCY4MQpaFz9SbqUDe4%2Bbs88AAAAAAEJAACY4MQpaFz9SbqUDe4%2Bbs88AAApA4JMAAA%3D&exvsurl=1&viewmodel=ReadMessageItem",
    "inferenceClassification": "Focused",
    "extensions@odata.context": "https://graph.microsoft.com/v1.0/$metadata#users('desmond40contoso.com')/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions", 
    "extensions": [ 
      { 
        "@odata.type": "#microsoft.graph.openTypeExtension",
        "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfc984d-b826-40d7-b48b-57002df85e00@1717f226-49d1-4d0c-9d74-709fad6677b4')/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions('Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')",
        "extensionName": "Com.Contoso.Referral",
        "id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral",
        "companyName": "Wingtip Toys",
        "dealValue": 500050,
        "expirationDate": "2015-12-03T10:00:00Z"
      }
     ]
  }
  ]
}

```



<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get openTypeExtension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->