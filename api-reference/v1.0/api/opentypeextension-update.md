---
title: Actualizar extensión abierta
description: 'Actualice una extensión abierta (objeto openTypeExtension) con las propiedades del cuerpo de la solicitud:'
localization_priority: Normal
ms.openlocfilehash: 5765dc8eb32950e3eb5cab951535cbc92bab0c58
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27891521"
---
# <a name="update-open-extension"></a><span data-ttu-id="d0833-103">Actualizar extensión abierta</span><span class="sxs-lookup"><span data-stu-id="d0833-103">Update open extension</span></span>

<span data-ttu-id="d0833-104">Actualice una extensión abierta (objeto [openTypeExtension](../resources/opentypeextension.md)) con las propiedades del cuerpo de la solicitud:</span><span class="sxs-lookup"><span data-stu-id="d0833-104">Update an open extension ([openTypeExtension](../resources/opentypeextension.md) object) with the properties in the request body:</span></span>

- <span data-ttu-id="d0833-105">Si una propiedad del cuerpo de la solicitud coincide con el nombre de una propiedad existente en la extensión, se actualizan los datos de la extensión.</span><span class="sxs-lookup"><span data-stu-id="d0833-105">If a property in the request body matches the name of an existing property in the extension, the data in the extension is updated.</span></span>
- <span data-ttu-id="d0833-106">De lo contrario, esa propiedad y sus datos se agregan a la extensión.</span><span class="sxs-lookup"><span data-stu-id="d0833-106">Otherwise that property and its data are added to the extension.</span></span> 

<span data-ttu-id="d0833-107">Los datos de una extensión pueden ser de tipo primitivo o matrices de tipos primitivos.</span><span class="sxs-lookup"><span data-stu-id="d0833-107">The data in an extension can be primitive types, or arrays of primitive types.</span></span>

## <a name="permissions"></a><span data-ttu-id="d0833-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="d0833-108">Permissions</span></span>

<span data-ttu-id="d0833-109">Según el recurso que se creó la extensión en y el permiso solicitado tipo (delegada o de la aplicación), el permiso especificado en la tabla siguiente es la con privilegios mínimos necesarios para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d0833-109">Depending on the resource that the extension was created in and the permission type (delegated or application) requested, the permission specified in the following table is the least privileged required to call this API.</span></span> <span data-ttu-id="d0833-110">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d0833-110">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="d0833-111">Recurso admitido</span><span class="sxs-lookup"><span data-stu-id="d0833-111">Supported resource</span></span> | <span data-ttu-id="d0833-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d0833-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d0833-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d0833-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d0833-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d0833-114">Application</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="d0833-115">device</span><span class="sxs-lookup"><span data-stu-id="d0833-115">device</span></span>](../resources/device.md) | <span data-ttu-id="d0833-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="d0833-116">Directory.AccessAsUser.All</span></span> | <span data-ttu-id="d0833-117">No admitido</span><span class="sxs-lookup"><span data-stu-id="d0833-117">Not supported</span></span> | <span data-ttu-id="d0833-118">Device.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0833-118">Device.ReadWrite.All</span></span> |
| [<span data-ttu-id="d0833-119">evento</span><span class="sxs-lookup"><span data-stu-id="d0833-119">event</span></span>](../resources/event.md) | <span data-ttu-id="d0833-120">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d0833-120">Calendars.ReadWrite</span></span> | <span data-ttu-id="d0833-121">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d0833-121">Calendars.ReadWrite</span></span> | <span data-ttu-id="d0833-122">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d0833-122">Calendars.ReadWrite</span></span> |
| [<span data-ttu-id="d0833-123">grupo</span><span class="sxs-lookup"><span data-stu-id="d0833-123">group</span></span>](../resources/group.md) | <span data-ttu-id="d0833-124">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0833-124">Group.ReadWrite.All</span></span> | <span data-ttu-id="d0833-125">No admitido</span><span class="sxs-lookup"><span data-stu-id="d0833-125">Not supported</span></span> | <span data-ttu-id="d0833-126">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0833-126">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="d0833-127">evento de grupo</span><span class="sxs-lookup"><span data-stu-id="d0833-127">group event</span></span>](../resources/event.md) | <span data-ttu-id="d0833-128">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0833-128">Group.ReadWrite.All</span></span> | <span data-ttu-id="d0833-129">No admitido</span><span class="sxs-lookup"><span data-stu-id="d0833-129">Not supported</span></span> | <span data-ttu-id="d0833-130">No admitido</span><span class="sxs-lookup"><span data-stu-id="d0833-130">Not supported</span></span> |
| [<span data-ttu-id="d0833-131">publicación de grupo</span><span class="sxs-lookup"><span data-stu-id="d0833-131">group post</span></span>](../resources/post.md) | <span data-ttu-id="d0833-132">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0833-132">Group.ReadWrite.All</span></span> | <span data-ttu-id="d0833-133">No admitido</span><span class="sxs-lookup"><span data-stu-id="d0833-133">Not supported</span></span> | <span data-ttu-id="d0833-134">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0833-134">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="d0833-135">mensaje</span><span class="sxs-lookup"><span data-stu-id="d0833-135">message</span></span>](../resources/message.md) | <span data-ttu-id="d0833-136">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d0833-136">Mail.ReadWrite</span></span> | <span data-ttu-id="d0833-137">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d0833-137">Mail.ReadWrite</span></span> | <span data-ttu-id="d0833-138">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d0833-138">Mail.ReadWrite</span></span> | 
| [<span data-ttu-id="d0833-139">organización</span><span class="sxs-lookup"><span data-stu-id="d0833-139">organization</span></span>](../resources/organization.md) | <span data-ttu-id="d0833-140">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="d0833-140">Directory.AccessAsUser.All</span></span> | <span data-ttu-id="d0833-141">No admitido</span><span class="sxs-lookup"><span data-stu-id="d0833-141">Not supported</span></span> | <span data-ttu-id="d0833-142">No admitido</span><span class="sxs-lookup"><span data-stu-id="d0833-142">Not supported</span></span> |
| [<span data-ttu-id="d0833-143">contacto personal</span><span class="sxs-lookup"><span data-stu-id="d0833-143">personal contact</span></span>](../resources/contact.md) | <span data-ttu-id="d0833-144">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d0833-144">Contacts.ReadWrite</span></span> | <span data-ttu-id="d0833-145">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d0833-145">Contacts.ReadWrite</span></span> | <span data-ttu-id="d0833-146">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d0833-146">Contacts.ReadWrite</span></span> |
| [<span data-ttu-id="d0833-147">usuario</span><span class="sxs-lookup"><span data-stu-id="d0833-147">user</span></span>](../resources/user.md) | <span data-ttu-id="d0833-148">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0833-148">User.ReadWrite.All</span></span> | <span data-ttu-id="d0833-149">User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d0833-149">User.ReadWrite</span></span> | <span data-ttu-id="d0833-150">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0833-150">User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d0833-151">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d0833-151">HTTP request</span></span>
<span data-ttu-id="d0833-152">En la solicitud, identifique la instancia de recurso, utilice la propiedad de navegación **extensiones** de esa instancia para identificar y realizar un `PATCH` en esa instancia de extensión.</span><span class="sxs-lookup"><span data-stu-id="d0833-152">In the request, identify the resource instance, use the **extensions** navigation property of that instance to identify the extension, and do a `PATCH` on that extension instance.</span></span>

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

><span data-ttu-id="d0833-p102">**Nota:** La sintaxis anterior muestra algunas formas comunes para identificar una instancia de recurso, con el fin de actualizar una extensión en él. Todas las otras formas de sintaxis que le permiten identificar estas instancias de recurso admiten la actualización de extensiones abiertas en ellas de una manera similar.</span><span class="sxs-lookup"><span data-stu-id="d0833-p102">**Note:** The above syntax shows some common ways to identify a resource instance, in order to update an extension in it. All other syntax that allows you to identify these resource instances supports updating open extensions in them in a similar way.</span></span>

<span data-ttu-id="d0833-155">Consulte la sección [Cuerpo de la solicitud](#request-body) sobre cómo incluir en el cuerpo de petición cualquier dato personalizado para cambiar o agregar a esa extensión.</span><span class="sxs-lookup"><span data-stu-id="d0833-155">See the [Request body](#request-body) section about including in the request body any custom data to change or add to that extension.</span></span>


## <a name="path-parameters"></a><span data-ttu-id="d0833-156">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="d0833-156">Path parameters</span></span>
|<span data-ttu-id="d0833-157">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d0833-157">Parameter</span></span>|<span data-ttu-id="d0833-158">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0833-158">Type</span></span>|<span data-ttu-id="d0833-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0833-159">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d0833-160">id</span><span class="sxs-lookup"><span data-stu-id="d0833-160">id</span></span>|<span data-ttu-id="d0833-161">string</span><span class="sxs-lookup"><span data-stu-id="d0833-161">string</span></span>|<span data-ttu-id="d0833-p103">Un identificador único para una instancia de la colección correspondiente. Necesario.</span><span class="sxs-lookup"><span data-stu-id="d0833-p103">A unique identifier for an instance of the corresponding collection. Required.</span></span>|
|<span data-ttu-id="d0833-164">extensionId</span><span class="sxs-lookup"><span data-stu-id="d0833-164">extensionId</span></span>|<span data-ttu-id="d0833-165">string</span><span class="sxs-lookup"><span data-stu-id="d0833-165">string</span></span>|<span data-ttu-id="d0833-p104">Puede ser un nombre de extensión, que es un identificador de texto único de una extensión, o un nombre completo que concatena el tipo de extensión y un identificador de texto único. Se devuelve el nombre completo de la propiedad `id` al crear la extensión. Necesario.</span><span class="sxs-lookup"><span data-stu-id="d0833-p104">This can be an extension name which is a unique text identifier for an extension, or a fully qualified name which concatenates the extension type and unique text identifier. The fully qualified name is returned in the `id` property when you create the extension. Required.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="d0833-169">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d0833-169">Request headers</span></span>
| <span data-ttu-id="d0833-170">Nombre</span><span class="sxs-lookup"><span data-stu-id="d0833-170">Name</span></span>       | <span data-ttu-id="d0833-171">Valor</span><span class="sxs-lookup"><span data-stu-id="d0833-171">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="d0833-172">Authorization</span><span class="sxs-lookup"><span data-stu-id="d0833-172">Authorization</span></span> | <span data-ttu-id="d0833-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d0833-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d0833-175">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d0833-175">Content-Type</span></span> | <span data-ttu-id="d0833-176">application/json</span><span class="sxs-lookup"><span data-stu-id="d0833-176">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="d0833-177">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d0833-177">Request body</span></span>

<span data-ttu-id="d0833-p106">Proporcione un cuerpo JSON del objeto [openTypeExtension](../resources/opentypeextension.md) con los siguientes pares nombre-valor necesarios y con cualquier dato personalizado que se cambiará o agregará a la extensión. Los datos de la carga JSON pueden ser de tipo primitivo o matrices de tipos primitivos.</span><span class="sxs-lookup"><span data-stu-id="d0833-p106">Provide a JSON body of an [openTypeExtension](../resources/opentypeextension.md) object, with the following required name-value pairs, and any custom data to change or add to that extension. The data in the JSON payload can be primitive types, or arrays of primitive types.</span></span>

| <span data-ttu-id="d0833-180">Nombre</span><span class="sxs-lookup"><span data-stu-id="d0833-180">Name</span></span>       | <span data-ttu-id="d0833-181">Valor</span><span class="sxs-lookup"><span data-stu-id="d0833-181">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="d0833-182">@odata.type</span><span class="sxs-lookup"><span data-stu-id="d0833-182">@odata.type</span></span> | <span data-ttu-id="d0833-183">microsoft.graph.openTypeExtension</span><span class="sxs-lookup"><span data-stu-id="d0833-183">microsoft.graph.openTypeExtension</span></span> |
| <span data-ttu-id="d0833-184">extensionName</span><span class="sxs-lookup"><span data-stu-id="d0833-184">extensionName</span></span> | <span data-ttu-id="d0833-185">%unique_string%</span><span class="sxs-lookup"><span data-stu-id="d0833-185">%unique_string%</span></span> |

## <a name="response"></a><span data-ttu-id="d0833-186">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0833-186">Response</span></span>

<span data-ttu-id="d0833-187">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [openTypeExtension](../resources/opentypeextension.md) actualizado.</span><span class="sxs-lookup"><span data-stu-id="d0833-187">If successful, this method returns a `200 OK` response code and the updated [openTypeExtension](../resources/opentypeextension.md) object.</span></span>


## <a name="example"></a><span data-ttu-id="d0833-188">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0833-188">Example</span></span>
#### <a name="request-1"></a><span data-ttu-id="d0833-189">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="d0833-189">Request 1</span></span>

<span data-ttu-id="d0833-p107">En el primer ejemplo, se muestra cómo actualizar una extensión en un mensaje. Inicialmente, la extensión se representa mediante la siguiente carga JSON:</span><span class="sxs-lookup"><span data-stu-id="d0833-p107">The first example shows how to update an extension in a message. The extension is initially represented by the following JSON payload:</span></span>

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

<span data-ttu-id="d0833-192">Puede hacer referencia a la extensión por su nombre:</span><span class="sxs-lookup"><span data-stu-id="d0833-192">You can reference the extension by its name:</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH https://graph.microsoft.com/v1.0/me/messages/AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===/extensions/Com.Contoso.Referral
```

<span data-ttu-id="d0833-193">O puede hacer referencia a la extensión por su nombre completo:</span><span class="sxs-lookup"><span data-stu-id="d0833-193">Or you can reference the extension by its fully qualified name:</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH https://graph.microsoft.com/v1.0/me/messages/AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===/extensions/Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral
```

<span data-ttu-id="d0833-194">Puede usar cualquier solicitud de ejemplo y el cuerpo de la solicitud siguiente para actualizar la extensión anterior:</span><span class="sxs-lookup"><span data-stu-id="d0833-194">You can use either example request and the following request body to update the above extension by:</span></span>
- <span data-ttu-id="d0833-195">Cambiar `companyName` de `Wingtip Toys` a `Wingtip Toys (USA)`</span><span class="sxs-lookup"><span data-stu-id="d0833-195">Changing `companyName` from `Wingtip Toys` to `Wingtip Toys (USA)`</span></span>
- <span data-ttu-id="d0833-196">Cambiar `dealValue` de `500050` a `500100`</span><span class="sxs-lookup"><span data-stu-id="d0833-196">Changing `dealValue` from `500050` to `500100`</span></span>
- <span data-ttu-id="d0833-197">Agregar nuevos datos como la propiedad personalizada `updated`</span><span class="sxs-lookup"><span data-stu-id="d0833-197">Adding new data as the custom property `updated`</span></span>

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


#### <a name="response-1"></a><span data-ttu-id="d0833-198">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="d0833-198">Response 1</span></span>

<span data-ttu-id="d0833-199">Esta es la respuesta, que es la misma independientemente de la forma usada para hacer referencia a la extensión.</span><span class="sxs-lookup"><span data-stu-id="d0833-199">Here is the response which is the same regardless of the way used to reference the extension.</span></span>

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

#### <a name="request-2"></a><span data-ttu-id="d0833-200">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="d0833-200">Request 2</span></span>

<span data-ttu-id="d0833-p108">En el segundo ejemplo, se muestra cómo actualizar una extensión en una publicación de grupo. Inicialmente, la extensión se representa mediante la siguiente carga JSON, con un valor `expirationDate` de `2015-07-03T13:04:00Z`:</span><span class="sxs-lookup"><span data-stu-id="d0833-p108">The second example shows how to update an extension in a group post. The extension is initially represented by the following JSON payload, with an `expirationDate` value of `2015-07-03T13:04:00Z`:</span></span>

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

<span data-ttu-id="d0833-203">En la siguiente solicitud y cuerpo de la solicitud, tiene que cambiar la propiedad `expirationDate` por `2016-07-30T11:00:00Z`:</span><span class="sxs-lookup"><span data-stu-id="d0833-203">The following is the request and request body to change the `expirationDate` to `2016-07-30T11:00:00Z`:</span></span>

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

#### <a name="response-2"></a><span data-ttu-id="d0833-204">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="d0833-204">Response 2</span></span>

<span data-ttu-id="d0833-205">Esta es la respuesta del segundo ejemplo que muestra la propiedad `expirationDate` actualizada en la extensión.</span><span class="sxs-lookup"><span data-stu-id="d0833-205">Here is the response of the second example which shows the updated `expirationDate` in the extension.</span></span>

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
