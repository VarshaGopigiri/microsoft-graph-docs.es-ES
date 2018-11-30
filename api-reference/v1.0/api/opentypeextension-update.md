---
title: Actualizar extensión abierta
description: 'Actualice una extensión abierta (objeto openTypeExtension) con las propiedades del cuerpo de la solicitud:'
ms.openlocfilehash: 986e5a466577aeb571e893b49a6b734c77027cb7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029270"
---
# <a name="update-open-extension"></a><span data-ttu-id="5cedf-103">Actualizar extensión abierta</span><span class="sxs-lookup"><span data-stu-id="5cedf-103">Update open extension</span></span>

<span data-ttu-id="5cedf-104">Actualice una extensión abierta (objeto [openTypeExtension](../resources/opentypeextension.md)) con las propiedades del cuerpo de la solicitud:</span><span class="sxs-lookup"><span data-stu-id="5cedf-104">Update an open extension ([openTypeExtension](../resources/opentypeextension.md) object) with the properties in the request body:</span></span>

- <span data-ttu-id="5cedf-105">Si una propiedad del cuerpo de la solicitud coincide con el nombre de una propiedad existente en la extensión, se actualizan los datos de la extensión.</span><span class="sxs-lookup"><span data-stu-id="5cedf-105">If a property in the request body matches the name of an existing property in the extension, the data in the extension is updated.</span></span>
- <span data-ttu-id="5cedf-106">De lo contrario, esa propiedad y sus datos se agregan a la extensión.</span><span class="sxs-lookup"><span data-stu-id="5cedf-106">Otherwise that property and its data are added to the extension.</span></span> 

<span data-ttu-id="5cedf-107">Los datos de una extensión pueden ser de tipo primitivo o matrices de tipos primitivos.</span><span class="sxs-lookup"><span data-stu-id="5cedf-107">The data in an extension can be primitive types, or arrays of primitive types.</span></span>

## <a name="permissions"></a><span data-ttu-id="5cedf-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="5cedf-108">Permissions</span></span>

<span data-ttu-id="5cedf-109">Según el recurso que se creó la extensión en y el permiso solicitado tipo (delegada o de la aplicación), el permiso especificado en la tabla siguiente es la con privilegios mínimos necesarios para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="5cedf-109">Depending on the resource that the extension was created in and the permission type (delegated or application) requested, the permission specified in the following table is the least privileged required to call this API.</span></span> <span data-ttu-id="5cedf-110">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5cedf-110">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="5cedf-111">Recurso admitido</span><span class="sxs-lookup"><span data-stu-id="5cedf-111">Supported resource</span></span> | <span data-ttu-id="5cedf-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5cedf-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5cedf-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5cedf-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5cedf-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5cedf-114">Application</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="5cedf-115">device</span><span class="sxs-lookup"><span data-stu-id="5cedf-115">device</span></span>](../resources/device.md) | <span data-ttu-id="5cedf-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="5cedf-116">Directory.AccessAsUser.All</span></span> | <span data-ttu-id="5cedf-117">No admitido</span><span class="sxs-lookup"><span data-stu-id="5cedf-117">Not supported</span></span> | <span data-ttu-id="5cedf-118">Device.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5cedf-118">Device.ReadWrite.All</span></span> |
| [<span data-ttu-id="5cedf-119">evento</span><span class="sxs-lookup"><span data-stu-id="5cedf-119">event</span></span>](../resources/event.md) | <span data-ttu-id="5cedf-120">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5cedf-120">Calendars.ReadWrite</span></span> | <span data-ttu-id="5cedf-121">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5cedf-121">Calendars.ReadWrite</span></span> | <span data-ttu-id="5cedf-122">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5cedf-122">Calendars.ReadWrite</span></span> |
| [<span data-ttu-id="5cedf-123">grupo</span><span class="sxs-lookup"><span data-stu-id="5cedf-123">group</span></span>](../resources/group.md) | <span data-ttu-id="5cedf-124">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5cedf-124">Group.ReadWrite.All</span></span> | <span data-ttu-id="5cedf-125">No admitido</span><span class="sxs-lookup"><span data-stu-id="5cedf-125">Not supported</span></span> | <span data-ttu-id="5cedf-126">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5cedf-126">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="5cedf-127">evento de grupo</span><span class="sxs-lookup"><span data-stu-id="5cedf-127">group event</span></span>](../resources/event.md) | <span data-ttu-id="5cedf-128">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5cedf-128">Group.ReadWrite.All</span></span> | <span data-ttu-id="5cedf-129">No admitido</span><span class="sxs-lookup"><span data-stu-id="5cedf-129">Not supported</span></span> | <span data-ttu-id="5cedf-130">No admitido</span><span class="sxs-lookup"><span data-stu-id="5cedf-130">Not supported</span></span> |
| [<span data-ttu-id="5cedf-131">publicación de grupo</span><span class="sxs-lookup"><span data-stu-id="5cedf-131">group post</span></span>](../resources/post.md) | <span data-ttu-id="5cedf-132">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5cedf-132">Group.ReadWrite.All</span></span> | <span data-ttu-id="5cedf-133">No admitido</span><span class="sxs-lookup"><span data-stu-id="5cedf-133">Not supported</span></span> | <span data-ttu-id="5cedf-134">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5cedf-134">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="5cedf-135">mensaje</span><span class="sxs-lookup"><span data-stu-id="5cedf-135">message</span></span>](../resources/message.md) | <span data-ttu-id="5cedf-136">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5cedf-136">Mail.ReadWrite</span></span> | <span data-ttu-id="5cedf-137">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5cedf-137">Mail.ReadWrite</span></span> | <span data-ttu-id="5cedf-138">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5cedf-138">Mail.ReadWrite</span></span> | 
| [<span data-ttu-id="5cedf-139">organización</span><span class="sxs-lookup"><span data-stu-id="5cedf-139">organization</span></span>](../resources/organization.md) | <span data-ttu-id="5cedf-140">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="5cedf-140">Directory.AccessAsUser.All</span></span> | <span data-ttu-id="5cedf-141">No admitido</span><span class="sxs-lookup"><span data-stu-id="5cedf-141">Not supported</span></span> | <span data-ttu-id="5cedf-142">No admitido</span><span class="sxs-lookup"><span data-stu-id="5cedf-142">Not supported</span></span> |
| [<span data-ttu-id="5cedf-143">contacto personal</span><span class="sxs-lookup"><span data-stu-id="5cedf-143">personal contact</span></span>](../resources/contact.md) | <span data-ttu-id="5cedf-144">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5cedf-144">Contacts.ReadWrite</span></span> | <span data-ttu-id="5cedf-145">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5cedf-145">Contacts.ReadWrite</span></span> | <span data-ttu-id="5cedf-146">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5cedf-146">Contacts.ReadWrite</span></span> |
| [<span data-ttu-id="5cedf-147">usuario</span><span class="sxs-lookup"><span data-stu-id="5cedf-147">user</span></span>](../resources/user.md) | <span data-ttu-id="5cedf-148">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5cedf-148">User.ReadWrite.All</span></span> | <span data-ttu-id="5cedf-149">User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5cedf-149">User.ReadWrite</span></span> | <span data-ttu-id="5cedf-150">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5cedf-150">User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5cedf-151">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5cedf-151">HTTP request</span></span>
<span data-ttu-id="5cedf-152">En la solicitud, identifique la instancia de recurso, utilice la propiedad de navegación **extensiones** de esa instancia para identificar y realizar un `PATCH` en esa instancia de extensión.</span><span class="sxs-lookup"><span data-stu-id="5cedf-152">In the request, identify the resource instance, use the **extensions** navigation property of that instance to identify the extension, and do a `PATCH` on that extension instance.</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH /devices/{Id}/extensions/{extensionId}
PATCH /users/{id|userPrincipalName}/events/{id}/extensions/{extensionId}
PATCH /groups/{id}/extensions/{extensionId}
PATCH /groups/{id}/events/{id}/extensions/{extensionId}
PATCH /groups/{id}/threads/{id}/posts/{id}/extensions/{extensionId}
PATCH /users/{id|userPrincipalName}/messages/{id}/extensions/{extensionId}
PATCH /organization/{Id}/extensions/{extensionId}
PATCH /users/{id|userPrincipalName}/contacts/{id}/extensions/{extensionId}
PATCH /users/{id|userPrincipalName}/extensions/{extensionId}
```

><span data-ttu-id="5cedf-p102">**Nota:** La sintaxis anterior muestra algunas formas comunes para identificar una instancia de recurso, con el fin de actualizar una extensión en él. Todas las otras formas de sintaxis que le permiten identificar estas instancias de recurso admiten la actualización de extensiones abiertas en ellas de una manera similar.</span><span class="sxs-lookup"><span data-stu-id="5cedf-p102">**Note:** The above syntax shows some common ways to identify a resource instance, in order to update an extension in it. All other syntax that allows you to identify these resource instances supports updating open extensions in them in a similar way.</span></span>

<span data-ttu-id="5cedf-155">Consulte la sección [Cuerpo de la solicitud](#request-body) sobre cómo incluir en el cuerpo de petición cualquier dato personalizado para cambiar o agregar a esa extensión.</span><span class="sxs-lookup"><span data-stu-id="5cedf-155">See the [Request body](#request-body) section about including in the request body any custom data to change or add to that extension.</span></span>


## <a name="path-parameters"></a><span data-ttu-id="5cedf-156">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="5cedf-156">Path parameters</span></span>
|<span data-ttu-id="5cedf-157">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5cedf-157">Parameter</span></span>|<span data-ttu-id="5cedf-158">Tipo</span><span class="sxs-lookup"><span data-stu-id="5cedf-158">Type</span></span>|<span data-ttu-id="5cedf-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cedf-159">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5cedf-160">id</span><span class="sxs-lookup"><span data-stu-id="5cedf-160">id</span></span>|<span data-ttu-id="5cedf-161">string</span><span class="sxs-lookup"><span data-stu-id="5cedf-161">string</span></span>|<span data-ttu-id="5cedf-p103">Un identificador único para una instancia de la colección correspondiente. Necesario.</span><span class="sxs-lookup"><span data-stu-id="5cedf-p103">A unique identifier for an instance of the corresponding collection. Required.</span></span>|
|<span data-ttu-id="5cedf-164">extensionId</span><span class="sxs-lookup"><span data-stu-id="5cedf-164">extensionId</span></span>|<span data-ttu-id="5cedf-165">string</span><span class="sxs-lookup"><span data-stu-id="5cedf-165">string</span></span>|<span data-ttu-id="5cedf-p104">Puede ser un nombre de extensión, que es un identificador de texto único de una extensión, o un nombre completo que concatena el tipo de extensión y un identificador de texto único. Se devuelve el nombre completo de la propiedad `id` al crear la extensión. Necesario.</span><span class="sxs-lookup"><span data-stu-id="5cedf-p104">This can be an extension name which is a unique text identifier for an extension, or a fully qualified name which concatenates the extension type and unique text identifier. The fully qualified name is returned in the `id` property when you create the extension. Required.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="5cedf-169">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5cedf-169">Request headers</span></span>
| <span data-ttu-id="5cedf-170">Nombre</span><span class="sxs-lookup"><span data-stu-id="5cedf-170">Name</span></span>       | <span data-ttu-id="5cedf-171">Valor</span><span class="sxs-lookup"><span data-stu-id="5cedf-171">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="5cedf-172">Authorization</span><span class="sxs-lookup"><span data-stu-id="5cedf-172">Authorization</span></span> | <span data-ttu-id="5cedf-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5cedf-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5cedf-175">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5cedf-175">Content-Type</span></span> | <span data-ttu-id="5cedf-176">application/json</span><span class="sxs-lookup"><span data-stu-id="5cedf-176">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="5cedf-177">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5cedf-177">Request body</span></span>

<span data-ttu-id="5cedf-p106">Proporcione un cuerpo JSON del objeto [openTypeExtension](../resources/opentypeextension.md) con los siguientes pares nombre-valor necesarios y con cualquier dato personalizado que se cambiará o agregará a la extensión. Los datos de la carga JSON pueden ser de tipo primitivo o matrices de tipos primitivos.</span><span class="sxs-lookup"><span data-stu-id="5cedf-p106">Provide a JSON body of an [openTypeExtension](../resources/opentypeextension.md) object, with the following required name-value pairs, and any custom data to change or add to that extension. The data in the JSON payload can be primitive types, or arrays of primitive types.</span></span>

| <span data-ttu-id="5cedf-180">Nombre</span><span class="sxs-lookup"><span data-stu-id="5cedf-180">Name</span></span>       | <span data-ttu-id="5cedf-181">Valor</span><span class="sxs-lookup"><span data-stu-id="5cedf-181">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="5cedf-182">@odata.type</span><span class="sxs-lookup"><span data-stu-id="5cedf-182">@odata.type</span></span> | <span data-ttu-id="5cedf-183">microsoft.graph.openTypeExtension</span><span class="sxs-lookup"><span data-stu-id="5cedf-183">microsoft.graph.openTypeExtension</span></span> |
| <span data-ttu-id="5cedf-184">extensionName</span><span class="sxs-lookup"><span data-stu-id="5cedf-184">extensionName</span></span> | <span data-ttu-id="5cedf-185">%unique_string%</span><span class="sxs-lookup"><span data-stu-id="5cedf-185">%unique_string%</span></span> |

## <a name="response"></a><span data-ttu-id="5cedf-186">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5cedf-186">Response</span></span>

<span data-ttu-id="5cedf-187">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [openTypeExtension](../resources/opentypeextension.md) actualizado.</span><span class="sxs-lookup"><span data-stu-id="5cedf-187">If successful, this method returns a `200 OK` response code and the updated [openTypeExtension](../resources/opentypeextension.md) object.</span></span>


## <a name="example"></a><span data-ttu-id="5cedf-188">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5cedf-188">Example</span></span>
#### <a name="request-1"></a><span data-ttu-id="5cedf-189">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="5cedf-189">Request 1</span></span>

<span data-ttu-id="5cedf-p107">En el primer ejemplo, se muestra cómo actualizar una extensión en un mensaje. Inicialmente, la extensión se representa mediante la siguiente carga JSON:</span><span class="sxs-lookup"><span data-stu-id="5cedf-p107">The first example shows how to update an extension in a message. The extension is initially represented by the following JSON payload:</span></span>

<!-- { "blockType": "ignored" } -->
```http
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

<span data-ttu-id="5cedf-192">Puede hacer referencia a la extensión por su nombre:</span><span class="sxs-lookup"><span data-stu-id="5cedf-192">You can reference the extension by its name:</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH https://graph.microsoft.com/v1.0/me/messages/AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===/extensions/Com.Contoso.Referral
```

<span data-ttu-id="5cedf-193">O puede hacer referencia a la extensión por su nombre completo:</span><span class="sxs-lookup"><span data-stu-id="5cedf-193">Or you can reference the extension by its fully qualified name:</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH https://graph.microsoft.com/v1.0/me/messages/AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===/extensions/Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral
```

<span data-ttu-id="5cedf-194">Puede usar cualquier solicitud de ejemplo y el cuerpo de la solicitud siguiente para actualizar la extensión anterior:</span><span class="sxs-lookup"><span data-stu-id="5cedf-194">You can use either example request and the following request body to update the above extension by:</span></span>
- <span data-ttu-id="5cedf-195">Cambiar `companyName` de `Wingtip Toys` a `Wingtip Toys (USA)`</span><span class="sxs-lookup"><span data-stu-id="5cedf-195">Changing `companyName` from `Wingtip Toys` to `Wingtip Toys (USA)`</span></span>
- <span data-ttu-id="5cedf-196">Cambiar `dealValue` de `500050` a `500100`</span><span class="sxs-lookup"><span data-stu-id="5cedf-196">Changing `dealValue` from `500050` to `500100`</span></span>
- <span data-ttu-id="5cedf-197">Agregar nuevos datos como la propiedad personalizada `updated`</span><span class="sxs-lookup"><span data-stu-id="5cedf-197">Adding new data as the custom property `updated`</span></span>

<!-- { "blockType": "ignored" } -->
```http
{
    "@odata.type": "microsoft.graph.openTypeExtension",
    "extensionName": "Com.Contoso.Referral",
    "companyName": "Wingtip Toys (USA)",
    "dealValue": "500100",
    "expirationDate": "2015-12-03T10:00:00.000Z",
    "updated": "2015-10-29T11:00:00.000Z"
} 
```


#### <a name="response-1"></a><span data-ttu-id="5cedf-198">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="5cedf-198">Response 1</span></span>

<span data-ttu-id="5cedf-199">Esta es la respuesta, que es la misma independientemente de la forma usada para hacer referencia a la extensión.</span><span class="sxs-lookup"><span data-stu-id="5cedf-199">Here is the response which is the same regardless of the way used to reference the extension.</span></span>

<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions/$entity",
    "@odata.type": "#microsoft.graph.openTypeExtension",
    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfc984d-b826-40d7-b48b-57002df85e00@1717f226-49d1-4d0c-9d74-709fad6677b4')/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions
('Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')",
    "id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral",
    "extensionName": "Com.Contoso.Referral",
    "companyName": "Wingtip Toys (USA)",
    "dealValue": 500100,
    "expirationDate": "2015-12-03T10:00:00Z",
    "updated": "2015-10-29T11:00:00.000Z"
}
```

****

#### <a name="request-2"></a><span data-ttu-id="5cedf-200">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="5cedf-200">Request 2</span></span>

<span data-ttu-id="5cedf-p108">En el segundo ejemplo, se muestra cómo actualizar una extensión en una publicación de grupo. Inicialmente, la extensión se representa mediante la siguiente carga JSON, con un valor `expirationDate` de `2015-07-03T13:04:00Z`:</span><span class="sxs-lookup"><span data-stu-id="5cedf-p108">The second example shows how to update an extension in a group post. The extension is initially represented by the following JSON payload, with an `expirationDate` value of `2015-07-03T13:04:00Z`:</span></span>

<!-- { "blockType": "ignored" } -->
```http
{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#groups('37df2ff0-0de0-4c33-8aee-75289364aef6')/threads('AAQkADJizZJpEWwqDHsEpV_KA%3D%3D')/posts('AAMkADJiUg96QZUkA-ICwMubAADDEd7UAAA%3D')/extensions/$entity",
    "@odata.type": "#microsoft.graph.openTypeExtension",
    "id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Estimate",
    "extensionName": "Com.Contoso.Estimate",
    "companyName": "Contoso",
    "expirationDate": "2015-07-03T13:04:00Z",
    "DealValue": 1010100,
    "Strings@odata.type": "#Collection(String)",
    "topPicks": [
        "Employees only",
        "Add spouse or guest",
        "Add family"
    ]
}
```

<span data-ttu-id="5cedf-203">En la siguiente solicitud y cuerpo de la solicitud, tiene que cambiar la propiedad `expirationDate` por `2016-07-30T11:00:00Z`:</span><span class="sxs-lookup"><span data-stu-id="5cedf-203">The following is the request and request body to change the `expirationDate` to `2016-07-30T11:00:00Z`:</span></span>

<!-- {
  "blockType": "ignored",
  "sampleKeys": ["Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Estimate"],
  "name": "update_opentypeextension"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/groups/37df2ff0-0de0-4c33-8aee-75289364aef6/threads/AAQkADJizZJpEWwqDHsEpV_KA==/posts/AAMkADJiUg96QZUkA-ICwMubAADDEd7UAAA=/extensions/Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Estimate
Content-type: application/json

{
   "@odata.type": "Microsoft.OutlookServices.OpenTypeExtension",
   "extensionName": "Com.Contoso.Estimate",
   "companyName": "Contoso",
   "expirationDate": "2016-07-30T11:00:00.000Z",
   "DealValue": 1010100,
   "topPicks": [
       "Employees only",
       "Add spouse or guest",
       "Add family"
    ]
}
```

#### <a name="response-2"></a><span data-ttu-id="5cedf-204">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="5cedf-204">Response 2</span></span>

<span data-ttu-id="5cedf-205">Esta es la respuesta del segundo ejemplo que muestra la propiedad `expirationDate` actualizada en la extensión.</span><span class="sxs-lookup"><span data-stu-id="5cedf-205">Here is the response of the second example which shows the updated `expirationDate` in the extension.</span></span>

<!-- {  
  "blockType": "ignored",  
  "truncated": true,  
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
    "expirationDate": "2016-07-30T11:00:00Z",
    "DealValue": 1010100,
    "Strings@odata.type": "#Collection(String)",
    "topPicks": [
        "Employees only",
        "Add spouse or guest",
        "Add family"
    ]
}
```

<!-- This page was manually created. -->
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update opentypeextension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
} -->
