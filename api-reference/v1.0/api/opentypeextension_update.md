# <a name="update-open-extension"></a><span data-ttu-id="09d2b-101">Actualizar extensión abierta</span><span class="sxs-lookup"><span data-stu-id="09d2b-101">Update open extension</span></span>

<span data-ttu-id="09d2b-102">Actualice una extensión abierta (objeto [openTypeExtension](../resources/openTypeExtension.md)) con las propiedades del cuerpo de la solicitud:</span><span class="sxs-lookup"><span data-stu-id="09d2b-102">Update an open extension ([openTypeExtension](../resources/openTypeExtension.md) object) with the properties in the request body:</span></span>

- <span data-ttu-id="09d2b-103">Si una propiedad del cuerpo de la solicitud coincide con el nombre de una propiedad existente en la extensión, se actualizan los datos de la extensión.</span><span class="sxs-lookup"><span data-stu-id="09d2b-103">If a property in the request body matches the name of an existing property in the extension, the data in the extension is updated.</span></span>
- <span data-ttu-id="09d2b-104">De lo contrario, esa propiedad y sus datos se agregan a la extensión.</span><span class="sxs-lookup"><span data-stu-id="09d2b-104">Otherwise that property and its data are added to the extension.</span></span> 

<span data-ttu-id="09d2b-105">Los datos de una extensión pueden ser de tipo primitivo o matrices de tipos primitivos.</span><span class="sxs-lookup"><span data-stu-id="09d2b-105">The data in an extension can be primitive types, or arrays of primitive types.</span></span>

## <a name="permissions"></a><span data-ttu-id="09d2b-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="09d2b-106">Permissions</span></span>

<span data-ttu-id="09d2b-p101">Según el recurso en el que se creó la extensión, se requiere uno de los siguientes permisos para llamar a esta API: Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="09d2b-p101">One of the following permissions is required to call this API, depending on the resource that the extension was created in. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="09d2b-109">**Recurso admitido**</span><span class="sxs-lookup"><span data-stu-id="09d2b-109">**Supported resource**</span></span>|<span data-ttu-id="09d2b-110">**Permiso**</span><span class="sxs-lookup"><span data-stu-id="09d2b-110">**Permission**</span></span>|<span data-ttu-id="09d2b-111">**Recurso admitido**</span><span class="sxs-lookup"><span data-stu-id="09d2b-111">**Supported resource**</span></span>|<span data-ttu-id="09d2b-112">**Permiso**</span><span class="sxs-lookup"><span data-stu-id="09d2b-112">**Permission**</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="09d2b-113">dispositivo</span><span class="sxs-lookup"><span data-stu-id="09d2b-113">device</span></span>](../resources/device.md) | <span data-ttu-id="09d2b-114">Device.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="09d2b-114">Device.ReadWrite.All</span></span> | [<span data-ttu-id="09d2b-115">evento</span><span class="sxs-lookup"><span data-stu-id="09d2b-115">event</span></span>](../resources/event.md) | <span data-ttu-id="09d2b-116">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="09d2b-116">Calendars.ReadWrite</span></span> |
| [<span data-ttu-id="09d2b-117">grupo</span><span class="sxs-lookup"><span data-stu-id="09d2b-117">group</span></span>](../resources/group.md) | <span data-ttu-id="09d2b-118">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="09d2b-118">Group.ReadWrite.All</span></span> | [<span data-ttu-id="09d2b-119">evento de grupo</span><span class="sxs-lookup"><span data-stu-id="09d2b-119">group event</span></span>](../resources/event.md) | <span data-ttu-id="09d2b-120">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="09d2b-120">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="09d2b-121">publicación de grupo</span><span class="sxs-lookup"><span data-stu-id="09d2b-121">group post</span></span>](../resources/post.md) | <span data-ttu-id="09d2b-122">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="09d2b-122">Group.ReadWrite.All</span></span> | [<span data-ttu-id="09d2b-123">mensaje</span><span class="sxs-lookup"><span data-stu-id="09d2b-123">message</span></span>](../resources/message.md) | <span data-ttu-id="09d2b-124">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="09d2b-124">Mail.ReadWrite</span></span> |
| [<span data-ttu-id="09d2b-125">organización</span><span class="sxs-lookup"><span data-stu-id="09d2b-125">organization</span></span>](../resources/organization.md) | <span data-ttu-id="09d2b-126">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="09d2b-126">Directory.AccessAsUser.All</span></span> | [<span data-ttu-id="09d2b-127">contacto personal</span><span class="sxs-lookup"><span data-stu-id="09d2b-127">personal contact</span></span>](../resources/contact.md) | <span data-ttu-id="09d2b-128">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="09d2b-128">Contacts.ReadWrite</span></span> |
| [<span data-ttu-id="09d2b-129">usuario</span><span class="sxs-lookup"><span data-stu-id="09d2b-129">user</span></span>](../resources/user.md) | <span data-ttu-id="09d2b-130">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="09d2b-130">Directory.AccessAsUser.All</span></span> | | |

## <a name="http-request"></a><span data-ttu-id="09d2b-131">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="09d2b-131">HTTP request</span></span>
<span data-ttu-id="09d2b-132">En la solicitud, identifique la instancia de recurso, utilice la propiedad de navegación **extensiones** de esa instancia para identificar y realizar un `PATCH` en esa instancia de extensión.</span><span class="sxs-lookup"><span data-stu-id="09d2b-132">In the request, identify the resource instance, use the **extensions** navigation property of that instance to identify the extension, and do a `PATCH` on that extension instance.</span></span>

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

><span data-ttu-id="09d2b-p102">**Nota:** La sintaxis anterior muestra algunas formas comunes para identificar una instancia de recurso, con el fin de actualizar una extensión en él. Todas las otras formas de sintaxis que le permiten identificar estas instancias de recurso admiten la actualización de extensiones abiertas en ellas de una manera similar.</span><span class="sxs-lookup"><span data-stu-id="09d2b-p102">**Note:** The above syntax shows some common ways to identify a resource instance, in order to update an extension in it. All other syntax that allows you to identify these resource instances supports updating open extensions in them in a similar way.</span></span>

<span data-ttu-id="09d2b-135">Consulte la sección [Cuerpo de la solicitud](#request-body) sobre cómo incluir en el cuerpo de petición cualquier dato personalizado para cambiar o agregar a esa extensión.</span><span class="sxs-lookup"><span data-stu-id="09d2b-135">See the [Request body](#request-body) section about including in the request body any custom data to change or add to that extension.</span></span>


## <a name="path-parameters"></a><span data-ttu-id="09d2b-136">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="09d2b-136">Path parameters</span></span>
|<span data-ttu-id="09d2b-137">Parámetro</span><span class="sxs-lookup"><span data-stu-id="09d2b-137">Parameter</span></span>|<span data-ttu-id="09d2b-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="09d2b-138">Type</span></span>|<span data-ttu-id="09d2b-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="09d2b-139">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="09d2b-140">id</span><span class="sxs-lookup"><span data-stu-id="09d2b-140">id</span></span>|<span data-ttu-id="09d2b-141">cadena</span><span class="sxs-lookup"><span data-stu-id="09d2b-141">string</span></span>|<span data-ttu-id="09d2b-p103">Un identificador único para una instancia de la colección correspondiente. Necesario.</span><span class="sxs-lookup"><span data-stu-id="09d2b-p103">A unique identifier for an instance of the corresponding collection. Required.</span></span>|
|<span data-ttu-id="09d2b-144">extensionId</span><span class="sxs-lookup"><span data-stu-id="09d2b-144">extensionId</span></span>|<span data-ttu-id="09d2b-145">cadena</span><span class="sxs-lookup"><span data-stu-id="09d2b-145">string</span></span>|<span data-ttu-id="09d2b-p104">Puede ser un nombre de extensión, que es un identificador de texto único de una extensión, o un nombre completo que concatena el tipo de extensión y un identificador de texto único. Se devuelve el nombre completo de la propiedad `id` al crear la extensión. Necesario.</span><span class="sxs-lookup"><span data-stu-id="09d2b-p104">This can be an extension name which is a unique text identifier for an extension, or a fully qualified name which concatenates the extension type and unique text identifier. The fully qualified name is returned in the `id` property when you create the extension. Required.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="09d2b-149">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="09d2b-149">Request headers</span></span>
| <span data-ttu-id="09d2b-150">Nombre</span><span class="sxs-lookup"><span data-stu-id="09d2b-150">Name</span></span>       | <span data-ttu-id="09d2b-151">Valor</span><span class="sxs-lookup"><span data-stu-id="09d2b-151">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="09d2b-152">Authorization</span><span class="sxs-lookup"><span data-stu-id="09d2b-152">Authorization</span></span> | <span data-ttu-id="09d2b-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="09d2b-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="09d2b-155">Content-Type</span><span class="sxs-lookup"><span data-stu-id="09d2b-155">Content-Type</span></span> | <span data-ttu-id="09d2b-156">application/json</span><span class="sxs-lookup"><span data-stu-id="09d2b-156">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="09d2b-157">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="09d2b-157">Request body</span></span>

<span data-ttu-id="09d2b-p106">Proporcione un cuerpo JSON del objeto [openTypeExtension](../resources/openTypeExtension.md) con los siguientes pares nombre-valor necesarios y con cualquier dato personalizado que se cambiará o agregará a la extensión. Los datos de la carga JSON pueden ser de tipo primitivo o matrices de tipos primitivos.</span><span class="sxs-lookup"><span data-stu-id="09d2b-p106">Provide a JSON body of an [openTypeExtension](../resources/openTypeExtension.md) object, with the following required name-value pairs, and any custom data to change or add to that extension. The data in the JSON payload can be primitive types, or arrays of primitive types.</span></span>

| <span data-ttu-id="09d2b-160">Nombre</span><span class="sxs-lookup"><span data-stu-id="09d2b-160">Name</span></span>       | <span data-ttu-id="09d2b-161">Valor</span><span class="sxs-lookup"><span data-stu-id="09d2b-161">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="09d2b-162">@odata.type</span><span class="sxs-lookup"><span data-stu-id="09d2b-162">@odata.type</span></span> | <span data-ttu-id="09d2b-163">microsoft.graph.openTypeExtension</span><span class="sxs-lookup"><span data-stu-id="09d2b-163">Microsoft.Graph.OpenTypeExtension</span></span> |
| <span data-ttu-id="09d2b-164">extensionName</span><span class="sxs-lookup"><span data-stu-id="09d2b-164">extensionName</span></span> | <span data-ttu-id="09d2b-165">%unique_string%</span><span class="sxs-lookup"><span data-stu-id="09d2b-165">%unique_string%</span></span> |

## <a name="response"></a><span data-ttu-id="09d2b-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="09d2b-166">Response</span></span>

<span data-ttu-id="09d2b-167">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [openTypeExtension](../resources/openTypeExtension.md) actualizado.</span><span class="sxs-lookup"><span data-stu-id="09d2b-167">If successful, this method returns a `200 OK` response code and the updated [openTypeExtension](../resources/openTypeExtension.md) object.</span></span>


## <a name="example"></a><span data-ttu-id="09d2b-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="09d2b-168">Example</span></span>
#### <a name="request-1"></a><span data-ttu-id="09d2b-169">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="09d2b-169">Request 1</span></span>

<span data-ttu-id="09d2b-p107">En el primer ejemplo, se muestra cómo actualizar una extensión en un mensaje. Inicialmente, la extensión se representa mediante la siguiente carga JSON:</span><span class="sxs-lookup"><span data-stu-id="09d2b-p107">The first example shows how to update an extension in a message. The extension is initially represented by the following JSON payload:</span></span>

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

<span data-ttu-id="09d2b-172">Puede hacer referencia a la extensión por su nombre:</span><span class="sxs-lookup"><span data-stu-id="09d2b-172">You can reference the extension by its name:</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH https://graph.microsoft.com/v1.0/me/messages/AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===/extensions/Com.Contoso.Referral
```

<span data-ttu-id="09d2b-173">O puede hacer referencia a la extensión por su nombre completo:</span><span class="sxs-lookup"><span data-stu-id="09d2b-173">Or you can reference the extension by its fully qualified name:</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH https://graph.microsoft.com/v1.0/me/messages/AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===/extensions/Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral
```

<span data-ttu-id="09d2b-174">Puede usar cualquier solicitud de ejemplo y el cuerpo de la solicitud siguiente para actualizar la extensión anterior:</span><span class="sxs-lookup"><span data-stu-id="09d2b-174">You can use either example request and the following request body to update the above extension by:</span></span>
- <span data-ttu-id="09d2b-175">Cambiar `companyName` de `Wingtip Toys` a `Wingtip Toys (USA)`</span><span class="sxs-lookup"><span data-stu-id="09d2b-175">Changing `companyName` from `Wingtip Toys` to `Wingtip Toys (USA)`</span></span>
- <span data-ttu-id="09d2b-176">Cambiar `dealValue` de `500050` a `500100`</span><span class="sxs-lookup"><span data-stu-id="09d2b-176">Changing `dealValue` from `500050` to `500100`</span></span>
- <span data-ttu-id="09d2b-177">Agregar nuevos datos como la propiedad personalizada `updated`</span><span class="sxs-lookup"><span data-stu-id="09d2b-177">Adding new data as the custom property `updated`</span></span>

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


#### <a name="response-1"></a><span data-ttu-id="09d2b-178">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="09d2b-178">Response 1</span></span>

<span data-ttu-id="09d2b-179">Esta es la respuesta, que es la misma independientemente de la forma usada para hacer referencia a la extensión.</span><span class="sxs-lookup"><span data-stu-id="09d2b-179">Here is the response which is the same regardless of the way used to reference the extension.</span></span>

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

#### <a name="request-2"></a><span data-ttu-id="09d2b-180">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="09d2b-180">Request 2</span></span>

<span data-ttu-id="09d2b-p108">En el segundo ejemplo, se muestra cómo actualizar una extensión en una publicación de grupo. Inicialmente, la extensión se representa mediante la siguiente carga JSON, con un valor `expirationDate` de `2015-07-03T13:04:00Z`:</span><span class="sxs-lookup"><span data-stu-id="09d2b-p108">The second example shows how to update an extension in a group post. The extension is initially represented by the following JSON payload, with an `expirationDate` value of `2015-07-03T13:04:00Z`:</span></span>

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

<span data-ttu-id="09d2b-183">En la siguiente solicitud y cuerpo de la solicitud, tiene que cambiar la propiedad `expirationDate` por `2016-07-30T11:00:00Z`:</span><span class="sxs-lookup"><span data-stu-id="09d2b-183">The following is the request and request body to change the `expirationDate` to `2016-07-30T11:00:00Z`:</span></span>

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

#### <a name="response-2"></a><span data-ttu-id="09d2b-184">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="09d2b-184">Response 2</span></span>

<span data-ttu-id="09d2b-185">Esta es la respuesta del segundo ejemplo que muestra la propiedad `expirationDate` actualizada en la extensión.</span><span class="sxs-lookup"><span data-stu-id="09d2b-185">Here is the response of the second example which shows the updated `expirationDate` in the extension.</span></span>

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
