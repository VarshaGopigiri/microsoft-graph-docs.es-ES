---
title: Crear extensión abierta
description: Crear una extensión open (objeto openTypeExtension) y agregar propiedades personalizadas
localization_priority: Normal
author: dkershaw10
ms.openlocfilehash: 58df4ab2898abe0e49563de4b655eccacfdc91fd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27948572"
---
# <a name="create-open-extension"></a><span data-ttu-id="0b5ed-103">Crear extensión abierta</span><span class="sxs-lookup"><span data-stu-id="0b5ed-103">Create open extension</span></span>

> <span data-ttu-id="0b5ed-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0b5ed-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0b5ed-106">Crear una extensión open (objeto[openTypeExtension](../resources/opentypeextension.md) ) y agregar propiedades personalizadas en una instancia nueva o existente de un recurso admitido.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-106">Create an open extension ([openTypeExtension](../resources/opentypeextension.md) object) and add custom properties in a new or existing instance of a supported resource.</span></span>

> <span data-ttu-id="0b5ed-107">**Nota:** Si está creando extensiones open en recursos de Outlook, consulte **Consideraciones sobre específica de Outlook** en [openTypeExtension el tipo de recurso](../resources/opentypeextension.md#outlook-specific-considerations).</span><span class="sxs-lookup"><span data-stu-id="0b5ed-107">**Note:** If you're creating open extensions on Outlook resources, see **Outlook-specific considerations** in [openTypeExtension resource type](../resources/opentypeextension.md#outlook-specific-considerations).</span></span>

## <a name="permissions"></a><span data-ttu-id="0b5ed-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="0b5ed-108">Permissions</span></span>

<span data-ttu-id="0b5ed-109">Según el recurso que está creando la extensión y el permiso solicitado tipo (delegada o de la aplicación), el permiso especificado en la tabla siguiente es la con privilegios mínimos necesarios para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-109">Depending on the resource you're creating the extension in and the permission type (delegated or application) requested, the permission specified in the following table is the least privileged required to call this API.</span></span> <span data-ttu-id="0b5ed-110">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0b5ed-110">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="0b5ed-111">Recurso admitido</span><span class="sxs-lookup"><span data-stu-id="0b5ed-111">Supported resource</span></span> | <span data-ttu-id="0b5ed-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0b5ed-112">Delegated (work or school account)</span></span> | <span data-ttu-id="0b5ed-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0b5ed-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0b5ed-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0b5ed-114">Application</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="0b5ed-115">device</span><span class="sxs-lookup"><span data-stu-id="0b5ed-115">device</span></span>](../resources/device.md) | <span data-ttu-id="0b5ed-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="0b5ed-116">Directory.AccessAsUser.All</span></span> | <span data-ttu-id="0b5ed-117">No admitido</span><span class="sxs-lookup"><span data-stu-id="0b5ed-117">Not supported</span></span> | <span data-ttu-id="0b5ed-118">Device.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0b5ed-118">Device.ReadWrite.All</span></span> |
| [<span data-ttu-id="0b5ed-119">evento</span><span class="sxs-lookup"><span data-stu-id="0b5ed-119">event</span></span>](../resources/event.md) | <span data-ttu-id="0b5ed-120">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0b5ed-120">Calendars.ReadWrite</span></span> | <span data-ttu-id="0b5ed-121">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0b5ed-121">Calendars.ReadWrite</span></span> | <span data-ttu-id="0b5ed-122">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0b5ed-122">Calendars.ReadWrite</span></span> |
| [<span data-ttu-id="0b5ed-123">grupo</span><span class="sxs-lookup"><span data-stu-id="0b5ed-123">group</span></span>](../resources/group.md) | <span data-ttu-id="0b5ed-124">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0b5ed-124">Group.ReadWrite.All</span></span> | <span data-ttu-id="0b5ed-125">No admitido</span><span class="sxs-lookup"><span data-stu-id="0b5ed-125">Not supported</span></span> | <span data-ttu-id="0b5ed-126">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0b5ed-126">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="0b5ed-127">evento de grupo</span><span class="sxs-lookup"><span data-stu-id="0b5ed-127">group event</span></span>](../resources/event.md) | <span data-ttu-id="0b5ed-128">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0b5ed-128">Group.ReadWrite.All</span></span> | <span data-ttu-id="0b5ed-129">No admitido</span><span class="sxs-lookup"><span data-stu-id="0b5ed-129">Not supported</span></span> | <span data-ttu-id="0b5ed-130">No admitido</span><span class="sxs-lookup"><span data-stu-id="0b5ed-130">Not supported</span></span> |
| [<span data-ttu-id="0b5ed-131">publicación de grupo</span><span class="sxs-lookup"><span data-stu-id="0b5ed-131">group post</span></span>](../resources/post.md) | <span data-ttu-id="0b5ed-132">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0b5ed-132">Group.ReadWrite.All</span></span> | <span data-ttu-id="0b5ed-133">No admitido</span><span class="sxs-lookup"><span data-stu-id="0b5ed-133">Not supported</span></span> | <span data-ttu-id="0b5ed-134">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0b5ed-134">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="0b5ed-135">mensaje</span><span class="sxs-lookup"><span data-stu-id="0b5ed-135">message</span></span>](../resources/message.md) | <span data-ttu-id="0b5ed-136">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0b5ed-136">Mail.ReadWrite</span></span> | <span data-ttu-id="0b5ed-137">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0b5ed-137">Mail.ReadWrite</span></span> | <span data-ttu-id="0b5ed-138">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0b5ed-138">Mail.ReadWrite</span></span> | 
| [<span data-ttu-id="0b5ed-139">organización</span><span class="sxs-lookup"><span data-stu-id="0b5ed-139">organization</span></span>](../resources/organization.md) | <span data-ttu-id="0b5ed-140">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="0b5ed-140">Directory.AccessAsUser.All</span></span> | <span data-ttu-id="0b5ed-141">No admitido</span><span class="sxs-lookup"><span data-stu-id="0b5ed-141">Not supported</span></span> | <span data-ttu-id="0b5ed-142">No admitido</span><span class="sxs-lookup"><span data-stu-id="0b5ed-142">Not supported</span></span> |
| [<span data-ttu-id="0b5ed-143">contacto personal</span><span class="sxs-lookup"><span data-stu-id="0b5ed-143">personal contact</span></span>](../resources/contact.md) | <span data-ttu-id="0b5ed-144">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0b5ed-144">Contacts.ReadWrite</span></span> | <span data-ttu-id="0b5ed-145">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0b5ed-145">Contacts.ReadWrite</span></span> | <span data-ttu-id="0b5ed-146">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0b5ed-146">Contacts.ReadWrite</span></span> |
| [<span data-ttu-id="0b5ed-147">usuario</span><span class="sxs-lookup"><span data-stu-id="0b5ed-147">user</span></span>](../resources/user.md) | <span data-ttu-id="0b5ed-148">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0b5ed-148">User.ReadWrite.All</span></span> | <span data-ttu-id="0b5ed-149">User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0b5ed-149">User.ReadWrite</span></span> | <span data-ttu-id="0b5ed-150">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0b5ed-150">User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0b5ed-151">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0b5ed-151">HTTP request</span></span>

### <a name="create-an-extension-in-a-new-resource-instance"></a><span data-ttu-id="0b5ed-152">Crear una extensión en una instancia de recurso nueva</span><span class="sxs-lookup"><span data-stu-id="0b5ed-152">Create an extension in a new resource instance</span></span>

<span data-ttu-id="0b5ed-153">Use la misma solicitud REST que utilice para crear la instancia.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-153">Use the same REST request that you use to create the instance.</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /users/{id|userPrincipalName}/events
POST /users/{id|userPrincipalName}/messages
POST /groups/{id}/events
POST /groups/{id}/threads/{id}/posts/{id}/reply
POST /users/{id|userPrincipalName}/contacts
```

><span data-ttu-id="0b5ed-154">**Nota:** Esta sintaxis muestran algunas formas comunes para crear las instancias de recursos admitidos.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-154">**Note:** This syntax shows some common ways to create the supported resource instances.</span></span> <span data-ttu-id="0b5ed-155">Todos los otras sintaxis POST que le permite crear estas instancias de recursos admite crear extensiones open en ellos de forma similar.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-155">All other POST syntaxes that allows you to create these resource instances supports creating open extensions in them in a similar way.</span></span>

<span data-ttu-id="0b5ed-156">Consulte la sección [Cuerpo de la solicitud](#request-body) para obtener información sobre cómo incluir las propiedades de la nueva instancia de recurso _y la extensión_ en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-156">See the [Request body](#request-body) section about including the properties of the new resource instance _and the extension_ in the request body.</span></span>

### <a name="create-an-extension-in-an-existing-resource-instance"></a><span data-ttu-id="0b5ed-157">Crear una extensión en una instancia de recurso existente</span><span class="sxs-lookup"><span data-stu-id="0b5ed-157">Create an extension in an existing resource instance</span></span>

<span data-ttu-id="0b5ed-158">Identifique la instancia del recurso en la solicitud y haga una `POST` a la propiedad de navegación de **extensiones**.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-158">Identify the resource instance in the request and do a `POST` to the **extensions** navigation property.</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /administrativeunits/{id}/extensions
POST /devices/{id}/extensions
POST /users/{id|userPrincipalName}/events/{id}/extensions
POST /groups/{id}/extensions
POST /groups/{id}/events/{id}/extensions
POST /groups/{id}/threads/{id}/posts/{id}/extensions
POST /users/{id|userPrincipalName}/messages/{id}/extensions
POST /organization/{id}/extensions
POST /users/{id|userPrincipalName}/contacts/{id}/extensions
POST /users/{id|userPrincipalName}/extensions
```

><span data-ttu-id="0b5ed-159">**Nota:** Esta sintaxis muestran algunas formas comunes para identificar una instancia del recurso, con el fin de crear una extensión en ella.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-159">**Note:** This syntax shows some common ways to identify a resource instance, in order to create an extension in it.</span></span> <span data-ttu-id="0b5ed-160">Todos los otras sintaxis que permite identificar estas instancias de recursos admite la creación de extensiones de open en ellos de forma similar.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-160">All other syntaxes that allows you to identify these resource instances supports creating open extensions in them in a similar way.</span></span>

<span data-ttu-id="0b5ed-161">Consulte la sección [Cuerpo de la solicitud](#request-body) para obtener información sobre cómo incluir _la extensión_ en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-161">See the [Request body](#request-body) section about including _the extension_ in the request body.</span></span>

## <a name="path-parameters"></a><span data-ttu-id="0b5ed-162">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="0b5ed-162">Path parameters</span></span>

|<span data-ttu-id="0b5ed-163">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="0b5ed-163">**Parameter**</span></span>|<span data-ttu-id="0b5ed-164">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0b5ed-164">**Type**</span></span>|<span data-ttu-id="0b5ed-165">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0b5ed-165">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0b5ed-166">id</span><span class="sxs-lookup"><span data-stu-id="0b5ed-166">id</span></span>|<span data-ttu-id="0b5ed-167">string</span><span class="sxs-lookup"><span data-stu-id="0b5ed-167">string</span></span>|<span data-ttu-id="0b5ed-p105">Un identificador único para un objeto en la colección correspondiente. Necesario.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-p105">A unique identifier for an object in the corresponding collection. Required.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="0b5ed-170">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0b5ed-170">Request headers</span></span>

| <span data-ttu-id="0b5ed-171">Nombre</span><span class="sxs-lookup"><span data-stu-id="0b5ed-171">Name</span></span>       | <span data-ttu-id="0b5ed-172">Valor</span><span class="sxs-lookup"><span data-stu-id="0b5ed-172">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="0b5ed-173">Authorization</span><span class="sxs-lookup"><span data-stu-id="0b5ed-173">Authorization</span></span> | <span data-ttu-id="0b5ed-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-p106">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0b5ed-176">Content-Type</span><span class="sxs-lookup"><span data-stu-id="0b5ed-176">Content-Type</span></span> | <span data-ttu-id="0b5ed-177">application/json</span><span class="sxs-lookup"><span data-stu-id="0b5ed-177">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="0b5ed-178">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0b5ed-178">Request body</span></span>

<span data-ttu-id="0b5ed-179">Proporcione un cuerpo JSON de un [openTypeExtension](../resources/opentypeextension.md), con los siguientes pares de nombre y valor necesarios y los datos personalizados adicionales.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-179">Provide a JSON body of an [openTypeExtension](../resources/opentypeextension.md), with the following required name-value pairs and any additional custom data.</span></span> <span data-ttu-id="0b5ed-180">Los datos de la carga JSON pueden ser tipos primitivos o matrices de tipos primitivos.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-180">The data in the JSON payload can be primitive types, or arrays of primitive types.</span></span>

| <span data-ttu-id="0b5ed-181">Nombre</span><span class="sxs-lookup"><span data-stu-id="0b5ed-181">Name</span></span>       | <span data-ttu-id="0b5ed-182">Valor</span><span class="sxs-lookup"><span data-stu-id="0b5ed-182">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="0b5ed-183">@odata.type</span><span class="sxs-lookup"><span data-stu-id="0b5ed-183">@odata.type</span></span> | <span data-ttu-id="0b5ed-184">Microsoft.Graph.OpenTypeExtension</span><span class="sxs-lookup"><span data-stu-id="0b5ed-184">Microsoft.Graph.OpenTypeExtension</span></span> |
| <span data-ttu-id="0b5ed-185">extensionName</span><span class="sxs-lookup"><span data-stu-id="0b5ed-185">extensionName</span></span> | <span data-ttu-id="0b5ed-186">%unique_string%</span><span class="sxs-lookup"><span data-stu-id="0b5ed-186">%unique_string%</span></span> |

<span data-ttu-id="0b5ed-187">Al crear una extensión en una instancia de recurso _nueva_, además del nuevo objeto **openTypeExtension**, proporcione una representación JSON de las propiedades relevantes para crear esa instancia de recurso.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-187">When creating an extension in a _new_ resource instance, in addition to the new **openTypeExtension** object, provide a JSON representation of the relevant properties to create such a resource instance.</span></span>

## <a name="response"></a><span data-ttu-id="0b5ed-188">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0b5ed-188">Response</span></span>

### <a name="response-code"></a><span data-ttu-id="0b5ed-189">Código de respuesta</span><span class="sxs-lookup"><span data-stu-id="0b5ed-189">Response code</span></span>

<span data-ttu-id="0b5ed-190">Dependiendo de la operación, el código de respuesta puede ser `201 Created` o `202 Accepted`.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-190">Depending on the operation, the response code can be `201 Created` or `202 Accepted`.</span></span>

<span data-ttu-id="0b5ed-191">Cuando se crea una extensión de uso de la misma operación que se utiliza para crear una instancia de recursos, la operación devuelve el mismo código de respuesta que devuelve cuando se usa la operación para crear la instancia de recurso sin la extensión.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-191">When you create an extension using the same operation that you use to create a resource instance, the operation returns the same response code that it returns when you use the operation to create the resource instance without the extension.</span></span>
<span data-ttu-id="0b5ed-192">Consulte los temas correspondientes para la creación de la instancia, como enumerados [anteriormente](#create-an-extension-in-a-new-resource-instance).</span><span class="sxs-lookup"><span data-stu-id="0b5ed-192">Refer to the corresponding topics for creating the instance, as listed [above](#create-an-extension-in-a-new-resource-instance).</span></span>

### <a name="response-body"></a><span data-ttu-id="0b5ed-193">Cuerpo de la respuesta</span><span class="sxs-lookup"><span data-stu-id="0b5ed-193">Response body</span></span>

| <span data-ttu-id="0b5ed-194">Escenario</span><span class="sxs-lookup"><span data-stu-id="0b5ed-194">Scenario</span></span>       | <span data-ttu-id="0b5ed-195">Recurso</span><span class="sxs-lookup"><span data-stu-id="0b5ed-195">Resource</span></span>  | <span data-ttu-id="0b5ed-196">Cuerpo de la respuesta</span><span class="sxs-lookup"><span data-stu-id="0b5ed-196">Response body</span></span> |
|:---------------|:----------|:--------------|
| <span data-ttu-id="0b5ed-197">Crear una extensión al crear explícitamente una _nueva_ instancia de recursos</span><span class="sxs-lookup"><span data-stu-id="0b5ed-197">Creating an extension while explicitly creating a _new_ resource instance</span></span> | <span data-ttu-id="0b5ed-198">[contacto](../resources/contact.md), [evento](../resources/event.md), [mensaje](../resources/message.md)</span><span class="sxs-lookup"><span data-stu-id="0b5ed-198">[contact](../resources/contact.md), [event](../resources/event.md), [message](../resources/message.md)</span></span> | <span data-ttu-id="0b5ed-199">Incluye la nueva instancia ampliada con el objeto [openTypeExtension](../resources/opentypeextension.md).</span><span class="sxs-lookup"><span data-stu-id="0b5ed-199">Includes the new instance expanded with the [openTypeExtension](../resources/opentypeextension.md) object.</span></span> |
| <span data-ttu-id="0b5ed-200">Crear una extensión al crear implícitamente una instancia de recursos</span><span class="sxs-lookup"><span data-stu-id="0b5ed-200">Creating an extension while implicitly creating a resource instance</span></span> | [<span data-ttu-id="0b5ed-201">post</span><span class="sxs-lookup"><span data-stu-id="0b5ed-201">post</span></span>](../resources/post.md) | <span data-ttu-id="0b5ed-202">La respuesta incluye sólo un código de respuesta, pero no un cuerpo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-202">The response includes only a response code but not a response body.</span></span> |
| <span data-ttu-id="0b5ed-203">Crear una extensión en una instancia de recurso _existente_</span><span class="sxs-lookup"><span data-stu-id="0b5ed-203">Creating an extension in an _existing_ resource instance</span></span> | <span data-ttu-id="0b5ed-204">Todos los recursos admitidos</span><span class="sxs-lookup"><span data-stu-id="0b5ed-204">All supported resources</span></span> | <span data-ttu-id="0b5ed-205">Incluye el objeto **openTypeExtension**.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-205">Includes the **openTypeExtension** object.</span></span> |

## <a name="example"></a><span data-ttu-id="0b5ed-206">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0b5ed-206">Example</span></span>

### <a name="request-1"></a><span data-ttu-id="0b5ed-207">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="0b5ed-207">Request 1</span></span>

<span data-ttu-id="0b5ed-p109">El primer ejemplo crea un mensaje y una extensión en la misma llamada. El cuerpo de la solicitud incluye:</span><span class="sxs-lookup"><span data-stu-id="0b5ed-p109">The first example creates a message and an extension in the same call. The request body includes the following:</span></span>

- <span data-ttu-id="0b5ed-210">Las propiedades **subject**, **body** y **toRecipients** típicas de un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-210">The **subject**, **body**, and **toRecipients** properties typical of a new message.</span></span>
- <span data-ttu-id="0b5ed-211">Y en cuanto a la extensión:</span><span class="sxs-lookup"><span data-stu-id="0b5ed-211">And for the extension:</span></span>

  - <span data-ttu-id="0b5ed-212">El tipo `Microsoft.Graph.OpenTypeExtension`.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-212">The type `Microsoft.Graph.OpenTypeExtension`.</span></span>
  - <span data-ttu-id="0b5ed-213">El nombre de la extensión "Com.Contoso.Referral".</span><span class="sxs-lookup"><span data-stu-id="0b5ed-213">The extension name "Com.Contoso.Referral".</span></span>
  - <span data-ttu-id="0b5ed-214">Datos adicionales que se almacenan como tres propiedades personalizadas en la carga JSON: `companyName`, `expirationDate`, y `dealValue`.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-214">Additional data to be stored as three custom properties in the JSON payload: `companyName`, `expirationDate`, and `dealValue`.</span></span>

<!-- {
  "blockType": "request",
  "name": "post_opentypeextension_1"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages

{
  "subject": "Annual review",
  "body": {
    "contentType": "HTML",
    "content": "You should be proud!"
  },
  "toRecipients": [
    {
      "emailAddress": {
        "address": "rufus@contoso.com"
      }
    }
  ],
  "extensions": [
    {
      "@odata.type": "Microsoft.Graph.OpenTypeExtension",
      "extensionName": "Com.Contoso.Referral",
      "companyName": "Wingtip Toys",
      "expirationDate": "2015-12-30T11:00:00.000Z",
      "dealValue": 10000
    }
  ]
}
```

### <a name="response-1"></a><span data-ttu-id="0b5ed-215">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="0b5ed-215">Response 1</span></span>

<span data-ttu-id="0b5ed-p110">Aquí tiene la respuesta del primer ejemplo. El cuerpo de la respuesta incluye las propiedades del mensaje nuevo y lo siguiente para la nueva extensión:</span><span class="sxs-lookup"><span data-stu-id="0b5ed-p110">Here is the response for the first example. The response body includes properties of the new message, and the following for the new extension:</span></span>

- <span data-ttu-id="0b5ed-218">La propiedad **id** con el nombre completo `Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral`.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-218">The **id** property with the fully qualified name of `Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral`.</span></span>
- <span data-ttu-id="0b5ed-219">La propiedad predeterminada **extensionName** especificada en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-219">The default property **extensionName** specified in the request.</span></span>
- <span data-ttu-id="0b5ed-220">Los datos personalizados especificados en la solicitud y almacenados como 3 propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-220">The custom data specified in the request stored as 3 custom properties.</span></span>

<span data-ttu-id="0b5ed-p111">Nota: Puede que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-p111">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/messages/$entity",
  "@odata.id": "https://graph.microsoft.com/beta/users('ddfc984d-b826-40d7-b48b-57002df800e5@1717f226-49d1-4d0c-9d74-709fad664b77')/messages
('AAMkAGEbs88AAB84uLuAAA=')",
  "@odata.etag": "W/\"CQAAABYAAACY4MQpaFz9SbqUDe4+bs88AAB88LOj\"",
  "id": "AAMkAGEbs88AAB84uLuAAA=",
  "createdDateTime": "2015-10-30T03:03:43Z",
  "lastModifiedDateTime": "2015-10-30T03:03:43Z",
  "changeKey": "CQAAABYAAACY4MQpaFz9SbqUDe4+bs88AAB88LOj",
  "categories": [ ],
  "receivedDateTime": "2015-10-30T03:03:43Z",
  "sentDateTime": "2015-10-30T03:03:43Z",
  "hasAttachments": false,
  "subject": "Annual review",
  "body": {
    "contentType": "HTML",
    "content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r
\n<meta content=\"text/html; charset=us-ascii\">\r\n</head>\r\n<body>\r\nYou should be proud!\r\n</body>\r
\n</html>\r\n"
  },
  "bodyPreview": "You should be proud!",
  "importance": "Normal",
  "parentFolderId": "AQMkAGEwAAAIBDwAAAA==",
  "sender": null,
  "from": null,
  "toRecipients": [
    {
      "emailAddress": {
        "address": "rufus@contoso.com",
        "name": "John Doe"
      }
    }
  ],
  "ccRecipients": [ ],
  "bccRecipients": [ ],
  "replyTo": [ ],
  "conversationId": "AAQkAGEFGugh3SVdMzzc=",
  "isDeliveryReceiptRequested": false,
  "isReadReceiptRequested": false,
  "isRead": true,
  "isDraft": true,
  "webLink": "https://outlook.office.com/owa/?
ItemID=AAMkAGEbs88AAB84uLuAAA%3D&exvsurl=1&viewmodel=ReadMessageItem",
  "inferenceClassification": "Focused",
  "extensions@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/messages
('AAMkAGEbs88AAB84uLuAAA%3D')/extensions",
  "extensions": [
    {
      "@odata.type": "#Microsoft.Graph.OpenTypeExtension",
      "@odata.id": "https://graph.microsoft.com/beta/users('ddfc984d-b826-40d7-b48b-57002df800e5@1717f226-49d1-4d0c-9d74-709fad664b77')/messages
('AAMkAGEbs88AAB84uLuAAA=')/extensions('Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')",
      "id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral",
      "extensionName": "Com.Contoso.Referral",
      "companyName": "Wingtip Toys",
      "expirationDate": "2015-12-30T11:00:00.000Z",
      "dealValue": 10000
    }
  ]
}
```

****

### <a name="request-2"></a><span data-ttu-id="0b5ed-223">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="0b5ed-223">Request 2</span></span>

<span data-ttu-id="0b5ed-p112">El segundo ejemplo crea una extensión en el mensaje especificado. El cuerpo de la solicitud incluye lo siguiente para la extensión:</span><span class="sxs-lookup"><span data-stu-id="0b5ed-p112">The second example creates an extension in the specified message. The request body includes the following for the extension:</span></span>

- <span data-ttu-id="0b5ed-226">El tipo `Microsoft.Graph.OpenTypeExtension`.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-226">The type `Microsoft.Graph.OpenTypeExtension`.</span></span>
- <span data-ttu-id="0b5ed-227">El nombre de la extensión "Com.Contoso.Referral".</span><span class="sxs-lookup"><span data-stu-id="0b5ed-227">The extension name "Com.Contoso.Referral".</span></span>
- <span data-ttu-id="0b5ed-228">Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `dealValue` y `expirationDate`.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-228">Additional data to be stored as 3 custom properties in the JSON payload: `companyName`, `dealValue`, and `expirationDate`.</span></span>

<!-- {
  "blockType": "request",
  "name": "post_opentypeextension_2"
}-->
```http
POST https://graph.microsoft.com/beta/me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions

{
  "@odata.type" : "Microsoft.Graph.OpenTypeExtension",
  "extensionName" : "Com.Contoso.Referral",
  "companyName" : "Wingtip Toys",
  "dealValue" : 500050,
  "expirationDate" : "2015-12-03T10:00:00.000Z"
}
```

### <a name="response-2"></a><span data-ttu-id="0b5ed-229">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="0b5ed-229">Response 2</span></span>

<span data-ttu-id="0b5ed-p113">Aquí tiene la respuesta del segundo ejemplo. El cuerpo de la respuesta incluye lo siguiente para la nueva extensión:</span><span class="sxs-lookup"><span data-stu-id="0b5ed-p113">Here is the response for the second example. The response body includes the following for the new extension:</span></span>

- <span data-ttu-id="0b5ed-232">La propiedad predeterminada **extensionName**.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-232">The default property **extensionName**.</span></span>
- <span data-ttu-id="0b5ed-233">La propiedad **id** con el nombre completo `Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral`.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-233">The **id** property with the fully qualified name of `Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral`.</span></span>
- <span data-ttu-id="0b5ed-234">Los datos personalizados que se almacenarán.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-234">The custom data to be stored.</span></span>

<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.opentypeextension"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions/$entity",
    "@odata.type": "#Microsoft.Graph.OpenTypeExtension",
    "@odata.id": "https://graph.microsoft.com/beta/users('ddfc984d-b826-40d7-b48b-57002df85e00@1717f226-49d1-4d0c-9d74-709fad6677b4')/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions
('Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')",
    "extensionName": "Com.Contoso.Referral",
    "id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral",
    "companyName": "Wingtip Toys",
    "dealValue": 500050,
    "expirationDate": "2015-12-03T10:00:00.000Z"
}
```

****

### <a name="request-3"></a><span data-ttu-id="0b5ed-235">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="0b5ed-235">Request 3</span></span>

<span data-ttu-id="0b5ed-p114">El tercer ejemplo crea una extensión en el evento de grupo especificado. El cuerpo de la solicitud incluye lo siguiente para la extensión:</span><span class="sxs-lookup"><span data-stu-id="0b5ed-p114">The third example creates an extension in the specified group event. The request body includes the following for the extension:</span></span>

- <span data-ttu-id="0b5ed-238">El tipo `Microsoft.Graph.OpenTypeExtension`.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-238">The type `Microsoft.Graph.OpenTypeExtension`.</span></span>
- <span data-ttu-id="0b5ed-239">El nombre de la extensión "Com.Contoso.Deal".</span><span class="sxs-lookup"><span data-stu-id="0b5ed-239">The extension name "Com.Contoso.Deal".</span></span>
- <span data-ttu-id="0b5ed-240">Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `dealValue` y `expirationDate`.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-240">Additional data to be stored as 3 custom properties in the JSON payload: `companyName`, `dealValue`, and `expirationDate`.</span></span>

<!-- {
  "blockType": "request",
  "name": "post_opentypeextension_3"
}-->
```http
POST https://graph.microsoft.com/beta/groups('f5480dfd-7d77-4d0b-ba2e-3391953cc74a')/events('AAMkADVl17IsAAA=')/extensions

{
  "@odata.type" : "Microsoft.Graph.OpenTypeExtension",
  "extensionName" : "Com.Contoso.Deal",
  "companyName" : "Alpine Skis",
  "dealValue" : 1010100,
  "expirationDate" : "2015-07-03T13:04:00.000Z"
}
```

### <a name="response-3"></a><span data-ttu-id="0b5ed-241">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="0b5ed-241">Response 3</span></span>

<span data-ttu-id="0b5ed-242">Aquí tiene la respuesta del tercer ejemplo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-242">Here is the response from the third example request.</span></span>

<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.opentypeextension"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#groups('f5480dfd-7d77-4d0b-ba2e-3391953cc74a')/events('AAMkADVl7IsAAA%3D')/extensions/$entity",
    "@odata.type": "#Microsoft.Graph.OpenTypeExtension",
    "id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Deal",
    "extensionName": "Com.Contoso.Deal",
    "companyName": "Alpine Skis",
    "dealValue": 1010100,
    "expirationDate": "2015-07-03T13:04:00Z"
}
```

****

### <a name="request-4"></a><span data-ttu-id="0b5ed-243">Solicitud 4</span><span class="sxs-lookup"><span data-stu-id="0b5ed-243">Request 4</span></span>

<span data-ttu-id="0b5ed-p115">El cuarto ejemplo crea una extensión en una nueva publicación de grupo mediante la misma llamada de acción de **respuesta** a una publicación de grupo existente. La acción de **respuesta** crea una nueva publicación y una nueva extensión insertada en la publicación. El cuerpo de la solicitud contiene una propiedad **post** que, a su vez, contiene el **cuerpo** de la nueva publicación y los siguientes datos de la nueva extensión:</span><span class="sxs-lookup"><span data-stu-id="0b5ed-p115">The fourth example creates an extension in a new group post, using the same **reply** action call to an existing group post. The **reply** action creates a new post, and a new extension embedded in the post. The request body includes a **post** property, which in turn contains the **body** of the new post, and the following data for the new extension:</span></span>

- <span data-ttu-id="0b5ed-247">El tipo `Microsoft.Graph.OpenTypeExtension`.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-247">The type `Microsoft.Graph.OpenTypeExtension`.</span></span>
- <span data-ttu-id="0b5ed-248">El nombre de la extensión "Com.Contoso.HR".</span><span class="sxs-lookup"><span data-stu-id="0b5ed-248">The extension name "Com.Contoso.HR".</span></span>
- <span data-ttu-id="0b5ed-249">Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `expirationDate` y la matriz de cadenas `topPicks`.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-249">Additional data to be stored as 3 custom properties in the JSON payload: `companyName`, `expirationDate`, and the array of strings `topPicks`.</span></span>

<!-- {
  "blockType": "request",
  "name": "post_opentypeextension_4"
}-->
```http
POST https://graph.microsoft.com/beta/groups('37df2ff0-0de0-4c33-8aee-75289364aef6')/threads('AAQkADJizZJpEWwqDHsEpV_KA==')/posts('AAMkADJiUg96QZUkA-ICwMubAAC1heiSAAA=')/reply

{
  "post": {
    "body": {
      "contentType": "html",
      "content": "<html><body><div><div><div><div>When and where? </div></div></div></div></body></html>"
    },
  "extensions": [
    {
      "@odata.type": "Microsoft.OutlookServices.OpenTypeExtension",
      "extensionName": "Com.Contoso.HR",
      "companyName": "Contoso",
      "expirationDate": "2015-07-03T13:04:00.000Z",
      "topPicks": [
        "Employees only",
        "Add spouse or guest",
        "Add family"
      ]
    }
  ]
  }
}
```

### <a name="response-4"></a><span data-ttu-id="0b5ed-250">Respuesta 4</span><span class="sxs-lookup"><span data-stu-id="0b5ed-250">Response 4</span></span>

<span data-ttu-id="0b5ed-p116">Aquí tiene la respuesta del cuarto ejemplo. Si se crea correctamente una extensión en una nueva publicación de grupo, el resultado es solo el código de respuesta HTTP 202.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-p116">Here is the response from the fourth example. Successfully creating an extension in a new group post results in only the HTTP 202 response code.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 202 Accepted
Content-type: text/plain
Content-Length: 0
```

****

### <a name="request-5"></a><span data-ttu-id="0b5ed-253">Solicitud 5</span><span class="sxs-lookup"><span data-stu-id="0b5ed-253">Request 5</span></span>

<span data-ttu-id="0b5ed-p117">El quinto ejemplo crea una extensión en una nueva publicación de grupo mediante la misma operación POST que para crear una conversación. La operación POST crea una nueva conversación, un nuevo hilo, una nueva publicación e inserta una nueva extensión en la publicación. El cuerpo de la solicitud incluye las propiedades **Topic** y **Threads** y un objeto **post** de elemento secundario para la nueva conversación. El objeto **post** contiene a su vez el **cuerpo** de la nueva publicación y los siguientes datos de la extensión:</span><span class="sxs-lookup"><span data-stu-id="0b5ed-p117">The fifth example creates an extension in a new group post using the same POST operation to create a conversation. The POST operation creates a new conversation, thread and post, and a new extension embedded in the post. The request body includes the **Topic** and **Threads** properties, and a child **post** object for the new conversation. The **post** object in turn contains the **body** of the new post, and the following data for the extension:</span></span>

- <span data-ttu-id="0b5ed-258">El tipo `Microsoft.Graph.OpenTypeExtension`.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-258">The type `Microsoft.Graph.OpenTypeExtension`.</span></span>
- <span data-ttu-id="0b5ed-259">El nombre de la extensión "Com.Contoso.HR".</span><span class="sxs-lookup"><span data-stu-id="0b5ed-259">The extension name "Com.Contoso.HR".</span></span>
- <span data-ttu-id="0b5ed-260">Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `expirationDate` y la matriz de cadenas `topPicks`.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-260">Additional data to be stored as 3 custom properties in the JSON payload: `companyName`, `expirationDate`, and the array of strings `topPicks`.</span></span>

<!-- {
  "blockType": "request",
  "name": "post_opentypeextension_5"
}-->
```http
POST https://graph.microsoft.com/beta/groups('37df2ff0-0de0-4c33-8aee-75289364aef6')/conversations

{
  "Topic": "Does anyone have a second?",
  "Threads": [
    {
      "Posts": [
        {
          "Body": {
            "ContentType": "HTML",
            "Content": "This is urgent!"
          },
          "Extensions": [
            {
              "@odata.type": "Microsoft.OutlookServices.OpenTypeExtension",
              "extensionName": "Com.Contoso.Benefits",
              "companyName": "Contoso",
              "expirationDate": "2016-08-03T11:00:00.000Z",
              "topPicks": [
                "Employees only",
                "Add spouse or guest",
                "Add family"
              ]
            }
          ]
        }
      ]
    }
  ]
}
```

### <a name="response-5"></a><span data-ttu-id="0b5ed-261">Respuesta 5</span><span class="sxs-lookup"><span data-stu-id="0b5ed-261">Response 5</span></span>

<span data-ttu-id="0b5ed-p118">Aquí está la respuesta del quinto ejemplo que contiene la nueva conversación y un identificador del hilo. Este nuevo hilo contiene una publicación creada automáticamente, que a su vez contiene la nueva extensión.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-p118">Here is the response from the fifth example which contains the new conversation and a thread ID. This new thread contains an automatically created post, which in turn contains the new extension.</span></span>

<span data-ttu-id="0b5ed-p119">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0b5ed-p119">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<span data-ttu-id="0b5ed-p120">Para obtener la nueva extensión, primero debe [obtener todas las publicaciones](../api/conversationthread-list-posts.md) de este hilo, inicialmente debería haber solo una. A continuación, aplique el identificador de la publicación y el nombre de la extensión `Com.Contoso.Benefits` para [obtener la extensión](../api/opentypeextension-get.md).</span><span class="sxs-lookup"><span data-stu-id="0b5ed-p120">To get the new extension, first [get all the posts](../api/conversationthread-list-posts.md) in this thread, and initially there should be only one. Then apply the post ID and the extension name `Com.Contoso.Benefits` to [get the extension](../api/opentypeextension-get.md).</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversation"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#groups('37df2ff0-0de0-4c33-8aee-75289364aef6')/conversations/$entity",
    "id": "AAQkADJToRlbJ5Mg7TFM7H-j3Y=",
    "threads@odata.context": "https://graph.microsoft.com/beta/$metadata#groups('37df2ff0-0de0-4c33-8aee-75289364aef6')/conversations('AAQkADJToRlbJ5Mg7TFM7H-j3Y%3D')/threads",
    "threads": [
        {
            "id": "AAQkADJDtMUzsf_PdhAAswJOhGVsnkyDtMUzsf_Pdg=="
        }
    ]
}

```

<!-- This page was manually created. -->
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create extension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
