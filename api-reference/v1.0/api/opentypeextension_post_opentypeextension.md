# <a name="create-open-extension"></a><span data-ttu-id="cf026-101">Crear extensión abierta</span><span class="sxs-lookup"><span data-stu-id="cf026-101">Create open extension</span></span>

<span data-ttu-id="cf026-102">Crea una extensión abierta (objeto [openTypeExtension](../resources/openTypeExtension.md)) y agrega propiedades personalizadas en una instancia nueva o existente de un recurso.</span><span class="sxs-lookup"><span data-stu-id="cf026-102">Create an open extension ([openTypeExtension](../resources/openTypeExtension.md) object) and add custom properties in a new or existing instance of a resource.</span></span>

> <span data-ttu-id="cf026-103">**Nota:** Si está creando extensiones abiertas en recursos de Outlook, consulte **Consideraciones específicas de Outlook** en [tipo de recurso openTypeExtension](../resources/opentypeextension.md#outlook-specific-considerations).</span><span class="sxs-lookup"><span data-stu-id="cf026-103">**Note:** If you're creating open extensions on Outlook resources, see **Outlook-specific considerations** in [openTypeExtension resource type](../resources/opentypeextension.md#outlook-specific-considerations).</span></span>

## <a name="permissions"></a><span data-ttu-id="cf026-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="cf026-104">Permissions</span></span>

<span data-ttu-id="cf026-p101">Según el recurso en el que se cree la extensión, se requiere uno de los siguientes permisos para llamar a esta API: Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="cf026-p101">One of the following permissions is required to call this API, depending on the resource you're creating the extension in. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="cf026-107">**Recurso admitido**</span><span class="sxs-lookup"><span data-stu-id="cf026-107">**Supported resource**</span></span>|<span data-ttu-id="cf026-108">**Permiso**</span><span class="sxs-lookup"><span data-stu-id="cf026-108">**Permission**</span></span>|<span data-ttu-id="cf026-109">**Recurso admitido**</span><span class="sxs-lookup"><span data-stu-id="cf026-109">**Supported resource**</span></span>|<span data-ttu-id="cf026-110">**Permiso**</span><span class="sxs-lookup"><span data-stu-id="cf026-110">**Permission**</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="cf026-111">dispositivo</span><span class="sxs-lookup"><span data-stu-id="cf026-111">device</span></span>](../resources/device.md) | <span data-ttu-id="cf026-112">Device.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cf026-112">Device.ReadWrite.All</span></span> | [<span data-ttu-id="cf026-113">evento</span><span class="sxs-lookup"><span data-stu-id="cf026-113">event</span></span>](../resources/event.md) | <span data-ttu-id="cf026-114">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cf026-114">Calendars.ReadWrite</span></span> |
| [<span data-ttu-id="cf026-115">grupo</span><span class="sxs-lookup"><span data-stu-id="cf026-115">group</span></span>](../resources/group.md) | <span data-ttu-id="cf026-116">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cf026-116">Group.ReadWrite.All</span></span> | [<span data-ttu-id="cf026-117">evento de grupo</span><span class="sxs-lookup"><span data-stu-id="cf026-117">group event</span></span>](../resources/event.md) | <span data-ttu-id="cf026-118">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cf026-118">Group.ReadWrite.All</span></span> |
| [<span data-ttu-id="cf026-119">publicación de grupo</span><span class="sxs-lookup"><span data-stu-id="cf026-119">group post</span></span>](../resources/post.md) | <span data-ttu-id="cf026-120">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cf026-120">Group.ReadWrite.All</span></span> | [<span data-ttu-id="cf026-121">mensaje</span><span class="sxs-lookup"><span data-stu-id="cf026-121">message</span></span>](../resources/message.md) | <span data-ttu-id="cf026-122">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cf026-122">Mail.ReadWrite</span></span> |
| [<span data-ttu-id="cf026-123">organización</span><span class="sxs-lookup"><span data-stu-id="cf026-123">organization</span></span>](../resources/organization.md) | <span data-ttu-id="cf026-124">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="cf026-124">Directory.AccessAsUser.All</span></span> | [<span data-ttu-id="cf026-125">contacto personal</span><span class="sxs-lookup"><span data-stu-id="cf026-125">personal contact</span></span>](../resources/contact.md) | <span data-ttu-id="cf026-126">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cf026-126">Contacts.ReadWrite</span></span> |
| [<span data-ttu-id="cf026-127">usuario</span><span class="sxs-lookup"><span data-stu-id="cf026-127">user</span></span>](../resources/user.md) | <span data-ttu-id="cf026-128">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="cf026-128">Directory.AccessAsUser.All</span></span> | | |

## <a name="http-request"></a><span data-ttu-id="cf026-129">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cf026-129">HTTP request</span></span>

### <a name="create-an-extension-in-a-new-resource-instance"></a><span data-ttu-id="cf026-130">Crear una extensión en una instancia de recurso nueva</span><span class="sxs-lookup"><span data-stu-id="cf026-130">Create an extension in a new resource instance</span></span>

<span data-ttu-id="cf026-131">Use la misma solicitud REST que utilice para crear la instancia.</span><span class="sxs-lookup"><span data-stu-id="cf026-131">Use the same REST request that you use to create the instance.</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST /users/{id|userPrincipalName}/events
POST /users/{id|userPrincipalName}/messages
POST /groups/{id}/events
POST /groups/{id}/threads/{id}/posts/{id}/reply
POST /users/{id|userPrincipalName}/contacts
```

><span data-ttu-id="cf026-132">**Nota:** Esta sintaxis muestra algunas formas comunes para crear las instancias de recursos admitidos.</span><span class="sxs-lookup"><span data-stu-id="cf026-132">**Note:** This syntax shows some common ways to create the supported resource instances.</span></span> <span data-ttu-id="cf026-133">Todas las otras sintaxis POST que le permiten crear estas instancias de recursos admiten crear extensiones abiertas en ellas de forma similar.</span><span class="sxs-lookup"><span data-stu-id="cf026-133">Note: The above syntax shows some common ways to create the supported resource instances. All other POST syntax that allows you to create these resource instances supports creating open extensions in them in a similar way.</span></span>

<span data-ttu-id="cf026-134">Consulte la sección [Cuerpo de la solicitud](#request-body) para obtener información sobre cómo incluir las propiedades de la nueva instancia de recurso _y la extensión_ en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf026-134">See the [Request body](#request-body) section about including the properties of the new resource instance _and the extension_ in the request body.</span></span>

### <a name="create-an-extension-in-an-existing-resource-instance"></a><span data-ttu-id="cf026-135">Crear una extensión en una instancia de recurso existente</span><span class="sxs-lookup"><span data-stu-id="cf026-135">Create an extension in an existing resource instance</span></span>

<span data-ttu-id="cf026-136">Identifique la instancia del recurso en la solicitud y haga una `POST` a la propiedad de navegación de **extensiones**.</span><span class="sxs-lookup"><span data-stu-id="cf026-136">Identify the resource instance in the request and do a `POST` to the **extensions** navigation property.</span></span>

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

><span data-ttu-id="cf026-137">**Nota:** Esta sintaxis muestra algunas formas comunes para identificar una instancia del recurso, con el fin de crear una extensión en ella.</span><span class="sxs-lookup"><span data-stu-id="cf026-137">**Note:** The above syntax shows some common ways to identify a resource instance, in order to create an extension in it. All other syntax that allows you to identify these resource instances supports creating open extensions in them in a similar way.</span></span> <span data-ttu-id="cf026-138">Todas las otras sintaxis que permiten identificar estas instancias de recursos admiten la creación de extensiones abiertas en ellas de forma similar.</span><span class="sxs-lookup"><span data-stu-id="cf026-138">Note: The above syntax shows some common ways to create the supported resource instances. All other POST syntax that allows you to create these resource instances supports creating open extensions in them in a similar way.</span></span>

<span data-ttu-id="cf026-139">Consulte la sección [Cuerpo de la solicitud](#request-body) para obtener información sobre cómo incluir _la extensión_ en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf026-139">See the [Request body](#request-body) section about including _the extension_ in the request body.</span></span>

## <a name="path-parameters"></a><span data-ttu-id="cf026-140">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="cf026-140">Path parameters</span></span>
|<span data-ttu-id="cf026-141">Parámetro</span><span class="sxs-lookup"><span data-stu-id="cf026-141">Parameter</span></span>|<span data-ttu-id="cf026-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf026-142">Type</span></span>|<span data-ttu-id="cf026-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf026-143">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cf026-144">id</span><span class="sxs-lookup"><span data-stu-id="cf026-144">id</span></span>|<span data-ttu-id="cf026-145">cadena</span><span class="sxs-lookup"><span data-stu-id="cf026-145">string</span></span>|<span data-ttu-id="cf026-p104">Un identificador único para un objeto en la colección correspondiente. Necesario.</span><span class="sxs-lookup"><span data-stu-id="cf026-p104">A unique identifier for an object in the corresponding collection. Required.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="cf026-148">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cf026-148">Request headers</span></span>

| <span data-ttu-id="cf026-149">Nombre</span><span class="sxs-lookup"><span data-stu-id="cf026-149">Name</span></span>       | <span data-ttu-id="cf026-150">Valor</span><span class="sxs-lookup"><span data-stu-id="cf026-150">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="cf026-151">Authorization</span><span class="sxs-lookup"><span data-stu-id="cf026-151">Authorization</span></span> | <span data-ttu-id="cf026-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cf026-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="cf026-154">Content-Type</span><span class="sxs-lookup"><span data-stu-id="cf026-154">Content-Type</span></span> | <span data-ttu-id="cf026-155">application/json</span><span class="sxs-lookup"><span data-stu-id="cf026-155">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="cf026-156">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cf026-156">Request body</span></span>

<span data-ttu-id="cf026-p106">Proporcione un cuerpo JSON de [openTypeExtension](../resources/openTypeExtension.md) con los siguientes pares de nombre y valor necesarios y con cualquier dato personalizado adicional. Los datos de la carga JSON pueden ser de tipo primitivo o matrices de tipo primitivo.</span><span class="sxs-lookup"><span data-stu-id="cf026-p106">Provide a JSON body of an [openTypeExtension](../resources/openTypeExtension.md), with the following required name-value pairs, and any additional custom data. The data in the JSON payload can be primitive types, or arrays of primitive types.</span></span>

| <span data-ttu-id="cf026-159">Nombre</span><span class="sxs-lookup"><span data-stu-id="cf026-159">Name</span></span>       | <span data-ttu-id="cf026-160">Valor</span><span class="sxs-lookup"><span data-stu-id="cf026-160">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="cf026-161">@odata.type</span><span class="sxs-lookup"><span data-stu-id="cf026-161">@odata.type</span></span> | <span data-ttu-id="cf026-162">microsoft.graph.openTypeExtension</span><span class="sxs-lookup"><span data-stu-id="cf026-162">Microsoft.Graph.OpenTypeExtension</span></span> |
| <span data-ttu-id="cf026-163">extensionName</span><span class="sxs-lookup"><span data-stu-id="cf026-163">extensionName</span></span> | <span data-ttu-id="cf026-164">%unique_string%</span><span class="sxs-lookup"><span data-stu-id="cf026-164">%unique_string%</span></span> |

<span data-ttu-id="cf026-165">Al crear una extensión en una instancia de recurso _nueva_, además del nuevo objeto **openTypeExtension**, proporcione una representación JSON de las propiedades relevantes para crear esa instancia de recurso.</span><span class="sxs-lookup"><span data-stu-id="cf026-165">When creating an extension in a _new_ resource instance, in addition to the new **openTypeExtension** object, provide a JSON representation of the relevant properties to create such a resource instance.</span></span>

## <a name="response"></a><span data-ttu-id="cf026-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf026-166">Response</span></span>

### <a name="response-code"></a><span data-ttu-id="cf026-167">Código de respuesta</span><span class="sxs-lookup"><span data-stu-id="cf026-167">Response code</span></span>

<span data-ttu-id="cf026-168">Dependiendo de la operación, el código de respuesta puede ser `201 Created` o `202 Accepted`.</span><span class="sxs-lookup"><span data-stu-id="cf026-168">Depending on the operation, the response code can be `201 Created` or `202 Accepted`.</span></span>

<span data-ttu-id="cf026-169">Cuando se crea una extensión usando la misma operación que se utiliza para crear una instancia de recurso, la operación devuelve el mismo código de respuesta que devuelve cuando se usa la operación para crear la instancia de recurso sin la extensión.</span><span class="sxs-lookup"><span data-stu-id="cf026-169">When you create an extension using the same operation that you use to create a resource instance, the operation returns the same response code that it returns when you use the operation to create the resource instance without the extension.</span></span>
<span data-ttu-id="cf026-170">Consulte los temas correspondientes para la creación de la instancia, como se enumeran [anteriormente](#create-an-extension-in-a-new-resource-instance).</span><span class="sxs-lookup"><span data-stu-id="cf026-170">Refer to the corresponding topics for creating the instance, as listed [above](#create-an-extension-in-a-new-resource-instance).</span></span>

### <a name="response-body"></a><span data-ttu-id="cf026-171">Cuerpo de la respuesta</span><span class="sxs-lookup"><span data-stu-id="cf026-171">Response body</span></span>

| <span data-ttu-id="cf026-172">Escenario</span><span class="sxs-lookup"><span data-stu-id="cf026-172">Scenario</span></span>       | <span data-ttu-id="cf026-173">Recurso</span><span class="sxs-lookup"><span data-stu-id="cf026-173">Resource</span></span>  | <span data-ttu-id="cf026-174">Cuerpo de la respuesta</span><span class="sxs-lookup"><span data-stu-id="cf026-174">Response body</span></span> |
|:---------------|:----------|:--------------|
| <span data-ttu-id="cf026-175">Crear una extensión al crear explícitamente una _nueva_ instancia de recursos</span><span class="sxs-lookup"><span data-stu-id="cf026-175">Creating an extension while explicitly creating a _new_ resource instance</span></span> | <span data-ttu-id="cf026-176">[contacto](../resources/contact.md), [evento](../resources/event.md), [mensaje](../resources/message.md)</span><span class="sxs-lookup"><span data-stu-id="cf026-176">[contact](../resources/contact.md), [event](../resources/event.md), [message](../resources/message.md)</span></span> | <span data-ttu-id="cf026-177">Incluye la nueva instancia ampliada con el objeto [openTypeExtension](../resources/openTypeExtension.md).</span><span class="sxs-lookup"><span data-stu-id="cf026-177">Includes the new instance expanded with the [openTypeExtension](../resources/openTypeExtension.md) object.</span></span> |
| <span data-ttu-id="cf026-178">Crear una extensión al crear implícitamente una instancia de recursos</span><span class="sxs-lookup"><span data-stu-id="cf026-178">Creating an extension while implicitly creating a resource instance</span></span> | [<span data-ttu-id="cf026-179">post</span><span class="sxs-lookup"><span data-stu-id="cf026-179">post</span></span>](../resources/post.md) | <span data-ttu-id="cf026-180">La respuesta incluye sólo un código de respuesta, pero no un cuerpo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf026-180">The response includes only a response code but not a response body.</span></span> |
| <span data-ttu-id="cf026-181">Crear una extensión en una instancia de recurso _existente_</span><span class="sxs-lookup"><span data-stu-id="cf026-181">Creating an extension in an _existing_ resource instance</span></span> | <span data-ttu-id="cf026-182">Todos los recursos admitidos</span><span class="sxs-lookup"><span data-stu-id="cf026-182">All supported resources</span></span> | <span data-ttu-id="cf026-183">Incluye el objeto **openTypeExtension**.</span><span class="sxs-lookup"><span data-stu-id="cf026-183">Includes the **openTypeExtension** object.</span></span> |

## <a name="example"></a><span data-ttu-id="cf026-184">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cf026-184">Example</span></span>

### <a name="request-1"></a><span data-ttu-id="cf026-185">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="cf026-185">Request 1</span></span>

<span data-ttu-id="cf026-p108">El primer ejemplo crea un mensaje y una extensión en la misma llamada. El cuerpo de la solicitud incluye:</span><span class="sxs-lookup"><span data-stu-id="cf026-p108">The first example creates a message and an extension in the same call. The request body includes the following:</span></span>

- <span data-ttu-id="cf026-188">Las propiedades **subject**, **body** y **toRecipients** típicas de un nuevo mensaje.</span><span class="sxs-lookup"><span data-stu-id="cf026-188">The **subject**, **body**, and **toRecipients** properties typical of a new message.</span></span>
- <span data-ttu-id="cf026-189">Y en cuanto a la extensión:</span><span class="sxs-lookup"><span data-stu-id="cf026-189">And for the extension:</span></span>

  - <span data-ttu-id="cf026-190">El tipo `microsoft.graph.openTypeExtension`.</span><span class="sxs-lookup"><span data-stu-id="cf026-190">The type `microsoft.graph.openTypeExtension`.</span></span>
  - <span data-ttu-id="cf026-191">El nombre de la extensión "Com.Contoso.Referral".</span><span class="sxs-lookup"><span data-stu-id="cf026-191">The extension name "Com.Contoso.Referral".</span></span>
  - <span data-ttu-id="cf026-192">Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga útil JSON: `companyName`, `expirationDate` y `dealValue`.</span><span class="sxs-lookup"><span data-stu-id="cf026-192">Additional data to be stored as 3 custom properties in the JSON payload: `companyName`, `expirationDate`, and `dealValue`.</span></span>

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

### <a name="response-1"></a><span data-ttu-id="cf026-193">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="cf026-193">Response 1</span></span>

<span data-ttu-id="cf026-p109">Aquí tiene la respuesta del primer ejemplo. El cuerpo de la respuesta incluye las propiedades del mensaje nuevo y lo siguiente para la nueva extensión:</span><span class="sxs-lookup"><span data-stu-id="cf026-p109">Here is the response for the first example. The response body includes properties of the new message, and the following for the new extension:</span></span>

- <span data-ttu-id="cf026-196">La propiedad **id** con el nombre completo `Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral`.</span><span class="sxs-lookup"><span data-stu-id="cf026-196">The **id** property with the fully qualified name of `Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral`.</span></span>
- <span data-ttu-id="cf026-197">La propiedad predeterminada **extensionName** especificada en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf026-197">The default property **extensionName** specified in the request.</span></span>
- <span data-ttu-id="cf026-198">Los datos personalizados especificados en la solicitud y almacenados como 3 propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="cf026-198">The custom data specified in the request stored as 3 custom properties.</span></span>

<span data-ttu-id="cf026-p110">Nota: Puede que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cf026-p110">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

### <a name="request-2"></a><span data-ttu-id="cf026-201">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="cf026-201">Request 2</span></span>

<span data-ttu-id="cf026-p111">El segundo ejemplo crea una extensión en el mensaje especificado. El cuerpo de la solicitud incluye lo siguiente para la extensión:</span><span class="sxs-lookup"><span data-stu-id="cf026-p111">The second example creates an extension in the specified message. The request body includes the following for the extension:</span></span>

- <span data-ttu-id="cf026-204">El tipo `microsoft.graph.openTypeExtension`.</span><span class="sxs-lookup"><span data-stu-id="cf026-204">The type `microsoft.graph.openTypeExtension`.</span></span>
- <span data-ttu-id="cf026-205">El nombre de la extensión "Com.Contoso.Referral".</span><span class="sxs-lookup"><span data-stu-id="cf026-205">The extension name "Com.Contoso.Referral".</span></span>
- <span data-ttu-id="cf026-206">Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `dealValue` y `expirationDate`.</span><span class="sxs-lookup"><span data-stu-id="cf026-206">Additional data to be stored as 3 custom properties in the JSON payload: `companyName`, `dealValue`, and `expirationDate`.</span></span>

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

### <a name="response-2"></a><span data-ttu-id="cf026-207">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="cf026-207">Response 2</span></span>

<span data-ttu-id="cf026-p112">Aquí tiene la respuesta del segundo ejemplo. El cuerpo de la respuesta incluye lo siguiente para la nueva extensión:</span><span class="sxs-lookup"><span data-stu-id="cf026-p112">Here is the response for the second example. The response body includes the following for the new extension:</span></span>

- <span data-ttu-id="cf026-210">La propiedad predeterminada **extensionName**.</span><span class="sxs-lookup"><span data-stu-id="cf026-210">The default property **extensionName**.</span></span>
- <span data-ttu-id="cf026-211">La propiedad **id** con el nombre completo `Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral`.</span><span class="sxs-lookup"><span data-stu-id="cf026-211">The **id** property with the fully qualified name of `Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral`.</span></span>
- <span data-ttu-id="cf026-212">Los datos personalizados que se almacenarán.</span><span class="sxs-lookup"><span data-stu-id="cf026-212">The custom data to be stored.</span></span>

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

### <a name="request-3"></a><span data-ttu-id="cf026-213">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="cf026-213">Request 3</span></span>

<span data-ttu-id="cf026-p113">El tercer ejemplo crea una extensión en el evento de grupo especificado. El cuerpo de la solicitud incluye lo siguiente para la extensión:</span><span class="sxs-lookup"><span data-stu-id="cf026-p113">The third example creates an extension in the specified group event. The request body includes the following for the extension:</span></span>

- <span data-ttu-id="cf026-216">El tipo `microsoft.graph.openTypeExtension`.</span><span class="sxs-lookup"><span data-stu-id="cf026-216">The type `microsoft.graph.openTypeExtension`.</span></span>
- <span data-ttu-id="cf026-217">El nombre de la extensión "Com.Contoso.Deal".</span><span class="sxs-lookup"><span data-stu-id="cf026-217">The extension name "Com.Contoso.Deal".</span></span>
- <span data-ttu-id="cf026-218">Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `dealValue` y `expirationDate`.</span><span class="sxs-lookup"><span data-stu-id="cf026-218">Additional data to be stored as 3 custom properties in the JSON payload: `companyName`, `dealValue`, and `expirationDate`.</span></span>

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

### <a name="response-3"></a><span data-ttu-id="cf026-219">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="cf026-219">Response 3</span></span>

<span data-ttu-id="cf026-220">Aquí tiene la respuesta del tercer ejemplo de solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf026-220">Here is the response from the third example request.</span></span>

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

### <a name="request-4"></a><span data-ttu-id="cf026-221">Solicitud 4</span><span class="sxs-lookup"><span data-stu-id="cf026-221">Request 4</span></span>

<span data-ttu-id="cf026-p114">El cuarto ejemplo crea una extensión en una nueva publicación de grupo mediante la misma llamada de acción de **respuesta** a una publicación de grupo existente. La acción de **respuesta** crea una nueva publicación y una nueva extensión insertada en la publicación. El cuerpo de la solicitud contiene una propiedad **post** que, a su vez, contiene el **cuerpo** de la nueva publicación y los siguientes datos de la nueva extensión:</span><span class="sxs-lookup"><span data-stu-id="cf026-p114">The fourth example creates an extension in a new group post, using the same **reply** action call to an existing group post. The **reply** action creates a new post, and a new extension embedded in the post. The request body includes a **post** property, which in turn contains the **body** of the new post, and the following data for the new extension:</span></span>

- <span data-ttu-id="cf026-225">El tipo `microsoft.graph.openTypeExtension`.</span><span class="sxs-lookup"><span data-stu-id="cf026-225">The type `microsoft.graph.openTypeExtension`.</span></span>
- <span data-ttu-id="cf026-226">El nombre de la extensión "Com.Contoso.HR".</span><span class="sxs-lookup"><span data-stu-id="cf026-226">The extension name "Com.Contoso.HR".</span></span>
- <span data-ttu-id="cf026-227">Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `expirationDate` y la matriz de cadenas `topPicks`.</span><span class="sxs-lookup"><span data-stu-id="cf026-227">Additional data to be stored as 3 custom properties in the JSON payload: `companyName`, `expirationDate`, and the array of strings `topPicks`.</span></span>

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

### <a name="response-4"></a><span data-ttu-id="cf026-228">Respuesta 4</span><span class="sxs-lookup"><span data-stu-id="cf026-228">Response 4</span></span>

<span data-ttu-id="cf026-p115">Aquí tiene la respuesta del cuarto ejemplo. Si se crea correctamente una extensión en una nueva publicación de grupo, el resultado es solo el código de respuesta HTTP 202.</span><span class="sxs-lookup"><span data-stu-id="cf026-p115">Here is the response from the fourth example. Successfully creating an extension in a new group post results in only the HTTP 202 response code.</span></span>

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

### <a name="request-5"></a><span data-ttu-id="cf026-231">Solicitud 5</span><span class="sxs-lookup"><span data-stu-id="cf026-231">Request 5</span></span>

<span data-ttu-id="cf026-p116">El quinto ejemplo crea una extensión en una nueva publicación de grupo mediante la misma operación POST que para crear una conversación. La operación POST crea una nueva conversación, un nuevo hilo, una nueva publicación e inserta una nueva extensión en la publicación. El cuerpo de la solicitud incluye las propiedades **Topic** y **Threads** y un objeto **post** de elemento secundario para la nueva conversación. El objeto **post** contiene a su vez el **cuerpo** de la nueva publicación y los siguientes datos de la extensión:</span><span class="sxs-lookup"><span data-stu-id="cf026-p116">The fifth example creates an extension in a new group post using the same POST operation to create a conversation. The POST operation creates a new conversation, thread and post, and a new extension embedded in the post. The request body includes the **Topic** and **Threads** properties, and a child **post** object for the new conversation. The **post** object in turn contains the **body** of the new post, and the following data for the extension:</span></span>

- <span data-ttu-id="cf026-236">El tipo `microsoft.graph.openTypeExtension`.</span><span class="sxs-lookup"><span data-stu-id="cf026-236">The type `microsoft.graph.openTypeExtension`.</span></span>
- <span data-ttu-id="cf026-237">El nombre de la extensión "Com.Contoso.HR".</span><span class="sxs-lookup"><span data-stu-id="cf026-237">The extension name "Com.Contoso.HR".</span></span>
- <span data-ttu-id="cf026-238">Los datos adicionales se almacenan como 3 propiedades personalizadas en la carga JSON: `companyName`, `expirationDate` y la matriz de cadenas `topPicks`.</span><span class="sxs-lookup"><span data-stu-id="cf026-238">Additional data to be stored as 3 custom properties in the JSON payload: `companyName`, `expirationDate`, and the array of strings `topPicks`.</span></span>

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

### <a name="response-5"></a><span data-ttu-id="cf026-239">Respuesta 5</span><span class="sxs-lookup"><span data-stu-id="cf026-239">Response 5</span></span>

<span data-ttu-id="cf026-p117">Aquí está la respuesta del quinto ejemplo que contiene la nueva conversación y un identificador del hilo. Este nuevo hilo contiene una publicación creada automáticamente, que a su vez contiene la nueva extensión.</span><span class="sxs-lookup"><span data-stu-id="cf026-p117">Here is the response from the fifth example which contains the new conversation and a thread ID. This new thread contains an automatically created post, which in turn contains the new extension.</span></span>

<span data-ttu-id="cf026-p118">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cf026-p118">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<span data-ttu-id="cf026-p119">Para obtener la nueva extensión, primero debe [obtener todas las publicaciones](../api/conversationthread_list_posts.md) de este hilo, inicialmente debería haber solo una. A continuación, aplique el identificador de la publicación y el nombre de la extensión `Com.Contoso.Benefits` para [obtener la extensión](../api/opentypeextension_get.md).</span><span class="sxs-lookup"><span data-stu-id="cf026-p119">To get the new extension, first [get all the posts](../api/conversationthread_list_posts.md) in this thread, and initially there should be only one. Then apply the post ID and the extension name `Com.Contoso.Benefits` to [get the extension](../api/opentypeextension_get.md).</span></span>

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
