---
title: Crear extensión abierta
description: Crea una extensión abierta (objeto openTypeExtension) y agrega propiedades personalizadas en una instancia nueva o existente de un recurso.
ms.openlocfilehash: c30942092bc3d8804af8193658d11fe561f77503
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031590"
---
# <a name="create-open-extension"></a><span data-ttu-id="d1f82-103">Crear extensión abierta</span><span class="sxs-lookup"><span data-stu-id="d1f82-103">Create open extension</span></span>

<span data-ttu-id="d1f82-104">Crea una extensión abierta (objeto [openTypeExtension](../resources/opentypeextension.md)) y agrega propiedades personalizadas en una instancia nueva o existente de un recurso.</span><span class="sxs-lookup"><span data-stu-id="d1f82-104">Create an open extension ([openTypeExtension](../resources/opentypeextension.md) object) and add custom properties in a new or existing instance of a resource.</span></span>

> <span data-ttu-id="d1f82-105">**Nota:** Si está creando extensiones open en recursos de Outlook, consulte **Consideraciones sobre específica de Outlook** en [openTypeExtension el tipo de recurso](../resources/opentypeextension.md#outlook-specific-considerations).</span><span class="sxs-lookup"><span data-stu-id="d1f82-105">**Note:** If you're creating open extensions on Outlook resources, see **Outlook-specific considerations** in [openTypeExtension resource type](../resources/opentypeextension.md#outlook-specific-considerations).</span></span>

## <a name="permissions"></a><span data-ttu-id="d1f82-106">Permissions</span><span class="sxs-lookup"><span data-stu-id="d1f82-106">Permissions</span></span>

<span data-ttu-id="d1f82-107">Según el recurso que está creando la extensión y el permiso solicitado tipo (delegada o de la aplicación), el permiso especificado en la tabla siguiente es la con privilegios mínimos necesarios para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d1f82-107">Depending on the resource you're creating the extension in and the permission type (delegated or application) requested, the permission specified in the following table is the least privileged required to call this API.</span></span> <span data-ttu-id="d1f82-108">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d1f82-108">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="d1f82-109">Recurso admitido</span><span class="sxs-lookup"><span data-stu-id="d1f82-109">Supported resource</span></span> | <span data-ttu-id="d1f82-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d1f82-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d1f82-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d1f82-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d1f82-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d1f82-112">Application</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="d1f82-113">device</span><span class="sxs-lookup"><span data-stu-id="d1f82-113">device</span></span>](../resources/device.md) | <span data-ttu-id="d1f82-114">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="d1f82-114">Directory.AccessAsUser.All</span></span> | <span data-ttu-id="d1f82-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="d1f82-115">Not supported</span></span> | <span data-ttu-id="d1f82-116">Device.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d1f82-116">Device.ReadWrite.All</span></span> |
| [<span data-ttu-id="d1f82-117">evento</span><span class="sxs-lookup"><span data-stu-id="d1f82-117">event</span></span>](../resources/event.md) | <span data-ttu-id="d1f82-118">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d1f82-118">Calendars.ReadWrite</span></span> | <span data-ttu-id="d1f82-119">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d1f82-119">Calendars.ReadWrite</span></span> | <span data-ttu-id="d1f82-120">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d1f82-120">Calendars.ReadWrite</span></span> |
| [<span data-ttu-id="d1f82-121">grupo</span><span class="sxs-lookup"><span data-stu-id="d1f82-121">group</span></span>](../resources/group.md) | <span data-ttu-id="d1f82-122">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d1f82-122">Group.ReadWrite.All</span></span> | <span data-ttu-id="d1f82-123">No admitido</span><span class="sxs-lookup"><span data-stu-id="d1f82-123">Not supported</span></span> | <span data-ttu-id="d1f82-124">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d1f82-124">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="d1f82-125">evento de grupo</span><span class="sxs-lookup"><span data-stu-id="d1f82-125">group event</span></span>](../resources/event.md) | <span data-ttu-id="d1f82-126">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d1f82-126">Group.ReadWrite.All</span></span> | <span data-ttu-id="d1f82-127">No admitido</span><span class="sxs-lookup"><span data-stu-id="d1f82-127">Not supported</span></span> | <span data-ttu-id="d1f82-128">No admitido</span><span class="sxs-lookup"><span data-stu-id="d1f82-128">Not supported</span></span> |
| [<span data-ttu-id="d1f82-129">publicación de grupo</span><span class="sxs-lookup"><span data-stu-id="d1f82-129">group post</span></span>](../resources/post.md) | <span data-ttu-id="d1f82-130">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d1f82-130">Group.ReadWrite.All</span></span> | <span data-ttu-id="d1f82-131">No admitido</span><span class="sxs-lookup"><span data-stu-id="d1f82-131">Not supported</span></span> | <span data-ttu-id="d1f82-132">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d1f82-132">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="d1f82-133">mensaje</span><span class="sxs-lookup"><span data-stu-id="d1f82-133">message</span></span>](../resources/message.md) | <span data-ttu-id="d1f82-134">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d1f82-134">Mail.ReadWrite</span></span> | <span data-ttu-id="d1f82-135">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d1f82-135">Mail.ReadWrite</span></span> | <span data-ttu-id="d1f82-136">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d1f82-136">Mail.ReadWrite</span></span> | 
| [<span data-ttu-id="d1f82-137">organización</span><span class="sxs-lookup"><span data-stu-id="d1f82-137">organization</span></span>](../resources/organization.md) | <span data-ttu-id="d1f82-138">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="d1f82-138">Directory.AccessAsUser.All</span></span> | <span data-ttu-id="d1f82-139">No admitido</span><span class="sxs-lookup"><span data-stu-id="d1f82-139">Not supported</span></span> | <span data-ttu-id="d1f82-140">No admitido</span><span class="sxs-lookup"><span data-stu-id="d1f82-140">Not supported</span></span> |
| [<span data-ttu-id="d1f82-141">contacto personal</span><span class="sxs-lookup"><span data-stu-id="d1f82-141">personal contact</span></span>](../resources/contact.md) | <span data-ttu-id="d1f82-142">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d1f82-142">Contacts.ReadWrite</span></span> | <span data-ttu-id="d1f82-143">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d1f82-143">Contacts.ReadWrite</span></span> | <span data-ttu-id="d1f82-144">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d1f82-144">Contacts.ReadWrite</span></span> |
| [<span data-ttu-id="d1f82-145">usuario</span><span class="sxs-lookup"><span data-stu-id="d1f82-145">user</span></span>](../resources/user.md) | <span data-ttu-id="d1f82-146">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d1f82-146">User.ReadWrite.All</span></span> | <span data-ttu-id="d1f82-147">User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d1f82-147">User.ReadWrite</span></span> | <span data-ttu-id="d1f82-148">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d1f82-148">User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d1f82-149">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d1f82-149">HTTP request</span></span>

### <a name="create-an-extension-in-a-new-resource-instance"></a><span data-ttu-id="d1f82-150">Crear una extensión en una instancia de recurso nueva</span><span class="sxs-lookup"><span data-stu-id="d1f82-150">Create an extension in a new resource instance</span></span>

<span data-ttu-id="d1f82-151">Use la misma solicitud REST que utilice para crear la instancia.</span><span class="sxs-lookup"><span data-stu-id="d1f82-151">Use the same REST request that you use to create the instance.</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /users/{id|userPrincipalName}/events
POST /users/{id|userPrincipalName}/messages
POST /groups/{id}/events
POST /groups/{id}/threads/{id}/posts/{id}/reply
POST /users/{id|userPrincipalName}/contacts
```

><span data-ttu-id="d1f82-152">**Nota:** Esta sintaxis muestran algunas formas comunes para crear las instancias de recursos admitidos.</span><span class="sxs-lookup"><span data-stu-id="d1f82-152">**Note:** This syntax shows some common ways to create the supported resource instances.</span></span> <span data-ttu-id="d1f82-153">Todos los otras sintaxis POST que le permite crear estas instancias de recursos admite crear extensiones open en ellos de forma similar.</span><span class="sxs-lookup"><span data-stu-id="d1f82-153">All other POST syntaxes that allows you to create these resource instances supports creating open extensions in them in a similar way.</span></span>

<span data-ttu-id="d1f82-154">Consulte la sección [Cuerpo de la solicitud](#request-body) para obtener información sobre cómo incluir las propiedades de la nueva instancia de recurso _y la extensión_ en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d1f82-154">See the [Request body](#request-body) section about including the properties of the new resource instance _and the extension_ in the request body.</span></span>

### <a name="create-an-extension-in-an-existing-resource-instance"></a><span data-ttu-id="d1f82-155">Crear una extensión en una instancia de recurso existente</span><span class="sxs-lookup"><span data-stu-id="d1f82-155">Create an extension in an existing resource instance</span></span>

<span data-ttu-id="d1f82-156">Identifique la instancia del recurso en la solicitud y haga una `POST` a la propiedad de navegación de **extensiones**.</span><span class="sxs-lookup"><span data-stu-id="d1f82-156">Identify the resource instance in the request and do a `POST` to the **extensions** navigation property.</span></span>

<!-- { "blockType": "ignored" } -->
```http
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

><span data-ttu-id="d1f82-157">**Nota:** Esta sintaxis muestran algunas formas comunes para identificar una instancia del recurso, con el fin de crear una extensión en ella.</span><span class="sxs-lookup"><span data-stu-id="d1f82-157">**Note:** This syntax shows some common ways to identify a resource instance, in order to create an extension in it.</span></span> <span data-ttu-id="d1f82-158">Todos los otras sintaxis que permite identificar estas instancias de recursos admite la creación de extensiones de open en ellos de forma similar.</span><span class="sxs-lookup"><span data-stu-id="d1f82-158">All other syntaxes that allows you to identify these resource instances supports creating open extensions in them in a similar way.</span></span>

<span data-ttu-id="d1f82-159">Consulte la sección [Cuerpo de la solicitud](#request-body) para obtener información sobre cómo incluir _la extensión_ en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d1f82-159">See the [Request body](#request-body) section about including _the extension_ in the request body.</span></span>

## <a name="path-parameters"></a><span data-ttu-id="d1f82-160">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="d1f82-160">Path parameters</span></span>
|<span data-ttu-id="d1f82-161">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d1f82-161">Parameter</span></span>|<span data-ttu-id="d1f82-162">Tipo</span><span class="sxs-lookup"><span data-stu-id="d1f82-162">Type</span></span>|<span data-ttu-id="d1f82-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1f82-163">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d1f82-164">id</span><span class="sxs-lookup"><span data-stu-id="d1f82-164">id</span></span>|<span data-ttu-id="d1f82-165">string</span><span class="sxs-lookup"><span data-stu-id="d1f82-165">string</span></span>|<span data-ttu-id="d1f82-p104">Un identificador único para un objeto en la colección correspondiente. Necesario.</span><span class="sxs-lookup"><span data-stu-id="d1f82-p104">A unique identifier for an object in the corresponding collection. Required.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="d1f82-168">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d1f82-168">Request headers</span></span>

| <span data-ttu-id="d1f82-169">Nombre</span><span class="sxs-lookup"><span data-stu-id="d1f82-169">Name</span></span>       | <span data-ttu-id="d1f82-170">Valor</span><span class="sxs-lookup"><span data-stu-id="d1f82-170">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="d1f82-171">Authorization</span><span class="sxs-lookup"><span data-stu-id="d1f82-171">Authorization</span></span> | <span data-ttu-id="d1f82-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d1f82-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d1f82-174">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d1f82-174">Content-Type</span></span> | <span data-ttu-id="d1f82-175">application/json</span><span class="sxs-lookup"><span data-stu-id="d1f82-175">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="d1f82-176">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d1f82-176">Request body</span></span>

<span data-ttu-id="d1f82-p106">Proporcione un cuerpo JSON de [openTypeExtension](../resources/opentypeextension.md) con los siguientes pares de nombre y valor necesarios y con cualquier dato personalizado adicional. Los datos de la carga JSON pueden ser de tipo primitivo o matrices de tipo primitivo.</span><span class="sxs-lookup"><span data-stu-id="d1f82-p106">Provide a JSON body of an [openTypeExtension](../resources/opentypeextension.md), with the following required name-value pairs, and any additional custom data. The data in the JSON payload can be primitive types, or arrays of primitive types.</span></span>

| <span data-ttu-id="d1f82-179">Nombre</span><span class="sxs-lookup"><span data-stu-id="d1f82-179">Name</span></span>       | <span data-ttu-id="d1f82-180">Valor</span><span class="sxs-lookup"><span data-stu-id="d1f82-180">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="d1f82-181">@odata.type</span><span class="sxs-lookup"><span data-stu-id="d1f82-181">@odata.type</span></span> | <span data-ttu-id="d1f82-182">microsoft.graph.openTypeExtension</span><span class="sxs-lookup"><span data-stu-id="d1f82-182">microsoft.graph.openTypeExtension</span></span> |
| <span data-ttu-id="d1f82-183">extensionName</span><span class="sxs-lookup"><span data-stu-id="d1f82-183">extensionName</span></span> | <span data-ttu-id="d1f82-184">%unique_string%</span><span class="sxs-lookup"><span data-stu-id="d1f82-184">%unique_string%</span></span> |

<span data-ttu-id="d1f82-185">Al crear una extensión en una instancia de recurso _nueva_, además del nuevo objeto **openTypeExtension**, proporcione una representación JSON de las propiedades relevantes para crear esa instancia de recurso.</span><span class="sxs-lookup"><span data-stu-id="d1f82-185">When creating an extension in a _new_ resource instance, in addition to the new **openTypeExtension** object, provide a JSON representation of the relevant properties to create such a resource instance.</span></span>

## <a name="response"></a><span data-ttu-id="d1f82-186">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d1f82-186">Response</span></span>

### <a name="response-code"></a><span data-ttu-id="d1f82-187">Código de respuesta</span><span class="sxs-lookup"><span data-stu-id="d1f82-187">Response code</span></span>

<span data-ttu-id="d1f82-188">Dependiendo de la operación, el código de respuesta puede ser `201 Created` o `202 Accepted`.</span><span class="sxs-lookup"><span data-stu-id="d1f82-188">Depending on the operation, the response code can be `201 Created` or `202 Accepted`.</span></span>

<span data-ttu-id="d1f82-189">Cuando se crea una extensión de uso de la misma operación que se utiliza para crear una instancia de recursos, la operación devuelve el mismo código de respuesta que devuelve cuando se usa la operación para crear la instancia de recurso sin la extensión.</span><span class="sxs-lookup"><span data-stu-id="d1f82-189">When you create an extension using the same operation that you use to create a resource instance, the operation returns the same response code that it returns when you use the operation to create the resource instance without the extension.</span></span>
<span data-ttu-id="d1f82-190">Consulte los temas correspondientes para la creación de la instancia, como enumerados [anteriormente](#create-an-extension-in-a-new-resource-instance).</span><span class="sxs-lookup"><span data-stu-id="d1f82-190">Refer to the corresponding topics for creating the instance, as listed [above](#create-an-extension-in-a-new-resource-instance).</span></span>

### <a name="response-body"></a><span data-ttu-id="d1f82-191">Cuerpo de la respuesta</span><span class="sxs-lookup"><span data-stu-id="d1f82-191">Response body</span></span>

| <span data-ttu-id="d1f82-192">Escenario</span><span class="sxs-lookup"><span data-stu-id="d1f82-192">Scenario</span></span>       | <span data-ttu-id="d1f82-193">Recurso</span><span class="sxs-lookup"><span data-stu-id="d1f82-193">Resource</span></span>  | <span data-ttu-id="d1f82-194">Cuerpo de la respuesta</span><span class="sxs-lookup"><span data-stu-id="d1f82-194">Response body</span></span> |
|:---------------|:----------|:--------------|
| <span data-ttu-id="d1f82-195">Crear una extensión al crear explícitamente una _nueva_ instancia de recursos</span><span class="sxs-lookup"><span data-stu-id="d1f82-195">Creating an extension while explicitly creating a _new_ resource instance</span></span> | <span data-ttu-id="d1f82-196">[contacto](../resources/contact.md), [evento](../resources/event.md), [mensaje](../resources/message.md)</span><span class="sxs-lookup"><span data-stu-id="d1f82-196">[contact](../resources/contact.md), [event](../resources/event.md), [message](../resources/message.md)</span></span> | <span data-ttu-id="d1f82-197">Incluye la nueva instancia ampliada con el objeto [openTypeExtension](../resources/opentypeextension.md).</span><span class="sxs-lookup"><span data-stu-id="d1f82-197">Includes the new instance expanded with the [openTypeExtension](../resources/opentypeextension.md) object.</span></span> |
| <span data-ttu-id="d1f82-198">Crear una extensión al crear implícitamente una instancia de recursos</span><span class="sxs-lookup"><span data-stu-id="d1f82-198">Creating an extension while implicitly creating a resource instance</span></span> | [<span data-ttu-id="d1f82-199">post</span><span class="sxs-lookup"><span data-stu-id="d1f82-199">post</span></span>](../resources/post.md) | <span data-ttu-id="d1f82-200">La respuesta incluye sólo un código de respuesta, pero no un cuerpo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="d1f82-200">The response includes only a response code but not a response body.</span></span> |
| <span data-ttu-id="d1f82-201">Crear una extensión en una instancia de recurso _existente_</span><span class="sxs-lookup"><span data-stu-id="d1f82-201">Creating an extension in an _existing_ resource instance</span></span> | <span data-ttu-id="d1f82-202">Todos los recursos admitidos</span><span class="sxs-lookup"><span data-stu-id="d1f82-202">All supported resources</span></span> | <span data-ttu-id="d1f82-203">Incluye el objeto **openTypeExtension**.</span><span class="sxs-lookup"><span data-stu-id="d1f82-203">Includes the **openTypeExtension** object.</span></span> |

## <a name="example"></a><span data-ttu-id="d1f82-204">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d1f82-204">Example</span></span>

### <a name="request-1"></a><span data-ttu-id="d1f82-205">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="d1f82-205">Request 1</span></span>

<span data-ttu-id="d1f82-p108">El primer ejemplo crea un mensaje y una extensión en la misma llamada. El cuerpo de la solicitud incluye:</span><span class="sxs-lookup"><span data-stu-id="d1f82-p108">The first example creates a message and an extension in the same call. The request body includes the following:</span></span>

- <span data-ttu-id="d1f82-208">Las propiedades **subject**, **body** y **toRecipients** típicas de un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="d1f82-208">The **subject**, **body**, and **toRecipients** properties typical of a new message.</span></span>
- <span data-ttu-id="d1f82-209">Y en cuanto a la extensión:</span><span class="sxs-lookup"><span data-stu-id="d1f82-209">And for the extension:</span></span>

  - <span data-ttu-id="d1f82-210">El tipo `microsoft.graph.openTypeExtension`.</span><span class="sxs-lookup"><span data-stu-id="d1f82-210">The type `microsoft.graph.openTypeExtension`.</span></span>
  - <span data-ttu-id="d1f82-211">El nombre de la extensión "Com.Contoso.Referral".</span><span class="sxs-lookup"><span data-stu-id="d1f82-211">The extension name "Com.Contoso.Referral".</span></span>
  - <span data-ttu-id="d1f82-212">Datos adicionales que se almacenan como tres propiedades personalizadas en la carga JSON: `companyName`, `expirationDate`, y `dealValue`.</span><span class="sxs-lookup"><span data-stu-id="d1f82-212">Additional data to be stored as three custom properties in the JSON payload: `companyName`, `expirationDate`, and `dealValue`.</span></span>

<!-- {
  "blockType": "ignored",
  "name": "post_opentypeextension_1"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages

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
      "@odata.type": "microsoft.graph.openTypeExtension",
      "extensionName": "Com.Contoso.Referral",
      "companyName": "Wingtip Toys",
      "expirationDate": "2015-12-30T11:00:00.000Z",
      "dealValue": 10000
    }
  ]
}
```

### <a name="response-1"></a><span data-ttu-id="d1f82-213">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="d1f82-213">Response 1</span></span>

<span data-ttu-id="d1f82-p109">Aquí tiene la respuesta del primer ejemplo. El cuerpo de la respuesta incluye las propiedades del mensaje nuevo y lo siguiente para la nueva extensión:</span><span class="sxs-lookup"><span data-stu-id="d1f82-p109">Here is the response for the first example. The response body includes properties of the new message, and the following for the new extension:</span></span>

- <span data-ttu-id="d1f82-216">La propiedad **id** con el nombre completo `Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral`.</span><span class="sxs-lookup"><span data-stu-id="d1f82-216">The **id** property with the fully qualified name of `Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral`.</span></span>
- <span data-ttu-id="d1f82-217">La propiedad predeterminada **extensionName** especificada en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d1f82-217">The default property **extensionName** specified in the request.</span></span>
- <span data-ttu-id="d1f82-218">Los datos personalizados especificados en la solicitud y almacenados como 3 propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="d1f82-218">The custom data specified in the request stored as 3 custom properties.</span></span>

<span data-ttu-id="d1f82-p110">Nota: Puede que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d1f82-p110">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/messages/$entity",
  "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfc984d-b826-40d7-b48b-57002df800e5@1717f226-49d1-4d0c-9d74-709fad664b77')/messages
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
  "extensions@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/messages
('AAMkAGEbs88AAB84uLuAAA%3D')/extensions",
  "extensions": [
    {
      "@odata.type": "#microsoft.graph.openTypeExtension",
      "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfc984d-b826-40d7-b48b-57002df800e5@1717f226-49d1-4d0c-9d74-709fad664b77')/messages
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

### <a name="request-2"></a><span data-ttu-id="d1f82-221">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="d1f82-221">Request 2</span></span>

<span data-ttu-id="d1f82-p111">El segundo ejemplo crea una extensión en el mensaje especificado. El cuerpo de la solicitud incluye lo siguiente para la extensión:</span><span class="sxs-lookup"><span data-stu-id="d1f82-p111">The second example creates an extension in the specified message. The request body includes the following for the extension:</span></span>

- <span data-ttu-id="d1f82-224">El tipo `microsoft.graph.openTypeExtension`.</span><span class="sxs-lookup"><span data-stu-id="d1f82-224">The type `microsoft.graph.openTypeExtension`.</span></span>
- <span data-ttu-id="d1f82-225">El nombre de la extensión "Com.Contoso.Referral".</span><span class="sxs-lookup"><span data-stu-id="d1f82-225">The extension name "Com.Contoso.Referral".</span></span>
- <span data-ttu-id="d1f82-226">Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `dealValue` y `expirationDate`.</span><span class="sxs-lookup"><span data-stu-id="d1f82-226">Additional data to be stored as 3 custom properties in the JSON payload: `companyName`, `dealValue`, and `expirationDate`.</span></span>

<!-- {
  "blockType": "ignored",
  "name": "post_opentypeextension_2"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===/extensions

{
  "@odata.type" : "microsoft.graph.openTypeExtension",
  "extensionName" : "Com.Contoso.Referral",
  "companyName" : "Wingtip Toys",
  "dealValue" : 500050,
  "expirationDate" : "2015-12-03T10:00:00.000Z"
}
```

### <a name="response-2"></a><span data-ttu-id="d1f82-227">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="d1f82-227">Response 2</span></span>

<span data-ttu-id="d1f82-p112">Aquí tiene la respuesta del segundo ejemplo. El cuerpo de la respuesta incluye lo siguiente para la nueva extensión:</span><span class="sxs-lookup"><span data-stu-id="d1f82-p112">Here is the response for the second example. The response body includes the following for the new extension:</span></span>

- <span data-ttu-id="d1f82-230">La propiedad predeterminada **extensionName**.</span><span class="sxs-lookup"><span data-stu-id="d1f82-230">The default property **extensionName**.</span></span>
- <span data-ttu-id="d1f82-231">La propiedad **id** con el nombre completo `Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral`.</span><span class="sxs-lookup"><span data-stu-id="d1f82-231">The **id** property with the fully qualified name of `Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral`.</span></span>
- <span data-ttu-id="d1f82-232">Los datos personalizados que se almacenarán.</span><span class="sxs-lookup"><span data-stu-id="d1f82-232">The custom data to be stored.</span></span>

<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.openTypeExtension"
} -->
```http
HTTP/1.1 201 Created
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
    "expirationDate": "2015-12-03T10:00:00.000Z"
}
```

****

### <a name="request-3"></a><span data-ttu-id="d1f82-233">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="d1f82-233">Request 3</span></span>

<span data-ttu-id="d1f82-p113">El tercer ejemplo crea una extensión en el evento de grupo especificado. El cuerpo de la solicitud incluye lo siguiente para la extensión:</span><span class="sxs-lookup"><span data-stu-id="d1f82-p113">The third example creates an extension in the specified group event. The request body includes the following for the extension:</span></span>

- <span data-ttu-id="d1f82-236">El tipo `microsoft.graph.openTypeExtension`.</span><span class="sxs-lookup"><span data-stu-id="d1f82-236">The type `microsoft.graph.openTypeExtension`.</span></span>
- <span data-ttu-id="d1f82-237">El nombre de la extensión "Com.Contoso.Deal".</span><span class="sxs-lookup"><span data-stu-id="d1f82-237">The extension name "Com.Contoso.Deal".</span></span>
- <span data-ttu-id="d1f82-238">Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `dealValue` y `expirationDate`.</span><span class="sxs-lookup"><span data-stu-id="d1f82-238">Additional data to be stored as 3 custom properties in the JSON payload: `companyName`, `dealValue`, and `expirationDate`.</span></span>

<!-- {
  "blockType": "ignored",
  "name": "post_opentypeextension_3"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/f5480dfd-7d77-4d0b-ba2e-3391953cc74a/events/AAMkADVl17IsAAA=/extensions

{
  "@odata.type" : "microsoft.graph.openTypeExtension",
  "extensionName" : "Com.Contoso.Deal",
  "companyName" : "Alpine Skis",
  "dealValue" : 1010100,
  "expirationDate" : "2015-07-03T13:04:00.000Z"
}
```

### <a name="response-3"></a><span data-ttu-id="d1f82-239">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="d1f82-239">Response 3</span></span>

<span data-ttu-id="d1f82-240">Aquí tiene la respuesta del tercer ejemplo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="d1f82-240">Here is the response from the third example request.</span></span>

<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.openTypeExtension"
} -->
```http
HTTP/1.1 201 Created
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

### <a name="request-4"></a><span data-ttu-id="d1f82-241">Solicitud 4</span><span class="sxs-lookup"><span data-stu-id="d1f82-241">Request 4</span></span>

<span data-ttu-id="d1f82-p114">El cuarto ejemplo crea una extensión en una nueva publicación de grupo mediante la misma llamada de acción de **respuesta** a una publicación de grupo existente. La acción de **respuesta** crea una nueva publicación y una nueva extensión insertada en la publicación. El cuerpo de la solicitud contiene una propiedad **post** que, a su vez, contiene el **cuerpo** de la nueva publicación y los siguientes datos de la nueva extensión:</span><span class="sxs-lookup"><span data-stu-id="d1f82-p114">The fourth example creates an extension in a new group post, using the same **reply** action call to an existing group post. The **reply** action creates a new post, and a new extension embedded in the post. The request body includes a **post** property, which in turn contains the **body** of the new post, and the following data for the new extension:</span></span>

- <span data-ttu-id="d1f82-245">El tipo `microsoft.graph.openTypeExtension`.</span><span class="sxs-lookup"><span data-stu-id="d1f82-245">The type `microsoft.graph.openTypeExtension`.</span></span>
- <span data-ttu-id="d1f82-246">El nombre de la extensión "Com.Contoso.HR".</span><span class="sxs-lookup"><span data-stu-id="d1f82-246">The extension name "Com.Contoso.HR".</span></span>
- <span data-ttu-id="d1f82-247">Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `expirationDate` y la matriz de cadenas `topPicks`.</span><span class="sxs-lookup"><span data-stu-id="d1f82-247">Additional data to be stored as 3 custom properties in the JSON payload: `companyName`, `expirationDate`, and the array of strings `topPicks`.</span></span>

<!-- {
  "blockType": "ignored",
  "name": "post_opentypeextension_4"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/37df2ff0-0de0-4c33-8aee-75289364aef6/threads/AAQkADJizZJpEWwqDHsEpV_KA==/posts/AAMkADJiUg96QZUkA-ICwMubAAC1heiSAAA=/reply

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

### <a name="response-4"></a><span data-ttu-id="d1f82-248">Respuesta 4</span><span class="sxs-lookup"><span data-stu-id="d1f82-248">Response 4</span></span>

<span data-ttu-id="d1f82-p115">Aquí tiene la respuesta del cuarto ejemplo. Si se crea correctamente una extensión en una nueva publicación de grupo, el resultado es solo el código de respuesta HTTP 202.</span><span class="sxs-lookup"><span data-stu-id="d1f82-p115">Here is the response from the fourth example. Successfully creating an extension in a new group post results in only the HTTP 202 response code.</span></span>

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

### <a name="request-5"></a><span data-ttu-id="d1f82-251">Solicitud 5</span><span class="sxs-lookup"><span data-stu-id="d1f82-251">Request 5</span></span>

<span data-ttu-id="d1f82-p116">El quinto ejemplo crea una extensión en una nueva publicación de grupo mediante la misma operación POST que para crear una conversación. La operación POST crea una nueva conversación, un nuevo hilo, una nueva publicación e inserta una nueva extensión en la publicación. El cuerpo de la solicitud incluye las propiedades **Topic** y **Threads** y un objeto **post** de elemento secundario para la nueva conversación. El objeto **post** contiene a su vez el **cuerpo** de la nueva publicación y los siguientes datos de la extensión:</span><span class="sxs-lookup"><span data-stu-id="d1f82-p116">The fifth example creates an extension in a new group post using the same POST operation to create a conversation. The POST operation creates a new conversation, thread and post, and a new extension embedded in the post. The request body includes the **Topic** and **Threads** properties, and a child **post** object for the new conversation. The **post** object in turn contains the **body** of the new post, and the following data for the extension:</span></span>

- <span data-ttu-id="d1f82-256">El tipo `microsoft.graph.openTypeExtension`.</span><span class="sxs-lookup"><span data-stu-id="d1f82-256">The type `microsoft.graph.openTypeExtension`.</span></span>
- <span data-ttu-id="d1f82-257">El nombre de la extensión "Com.Contoso.HR".</span><span class="sxs-lookup"><span data-stu-id="d1f82-257">The extension name "Com.Contoso.HR".</span></span>
- <span data-ttu-id="d1f82-258">Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `expirationDate` y la matriz de cadenas `topPicks`.</span><span class="sxs-lookup"><span data-stu-id="d1f82-258">Additional data to be stored as 3 custom properties in the JSON payload: `companyName`, `expirationDate`, and the array of strings `topPicks`.</span></span>

<!-- {
  "blockType": "ignored",
  "name": "post_opentypeextension_5"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/37df2ff0-0de0-4c33-8aee-75289364aef6/conversations

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

### <a name="response-5"></a><span data-ttu-id="d1f82-259">Respuesta 5</span><span class="sxs-lookup"><span data-stu-id="d1f82-259">Response 5</span></span>

<span data-ttu-id="d1f82-p117">Aquí está la respuesta del quinto ejemplo que contiene la nueva conversación y un identificador del hilo. Este nuevo hilo contiene una publicación creada automáticamente, que a su vez contiene la nueva extensión.</span><span class="sxs-lookup"><span data-stu-id="d1f82-p117">Here is the response from the fifth example which contains the new conversation and a thread ID. This new thread contains an automatically created post, which in turn contains the new extension.</span></span>

<span data-ttu-id="d1f82-p118">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d1f82-p118">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<span data-ttu-id="d1f82-p119">Para obtener la nueva extensión, primero debe [obtener todas las publicaciones](../api/conversationthread-list-posts.md) de este hilo, inicialmente debería haber solo una. A continuación, aplique el identificador de la publicación y el nombre de la extensión `Com.Contoso.Benefits` para [obtener la extensión](../api/opentypeextension-get.md).</span><span class="sxs-lookup"><span data-stu-id="d1f82-p119">To get the new extension, first [get all the posts](../api/conversationthread-list-posts.md) in this thread, and initially there should be only one. Then apply the post ID and the extension name `Com.Contoso.Benefits` to [get the extension](../api/opentypeextension-get.md).</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversation"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#groups('37df2ff0-0de0-4c33-8aee-75289364aef6')/conversations/$entity",
    "id": "AAQkADJToRlbJ5Mg7TFM7H-j3Y=",
    "threads@odata.context": "https://graph.microsoft.com/v1.0/$metadata#groups('37df2ff0-0de0-4c33-8aee-75289364aef6')/conversations('AAQkADJToRlbJ5Mg7TFM7H-j3Y%3D')/threads",
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
