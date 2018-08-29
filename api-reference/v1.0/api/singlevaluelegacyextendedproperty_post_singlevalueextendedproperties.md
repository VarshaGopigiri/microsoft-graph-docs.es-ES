# <a name="create-single-value-extended-property"></a><span data-ttu-id="a3865-101">Crear propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="a3865-101">Create single-value extended property</span></span>

<span data-ttu-id="a3865-102">Cree una o varias propiedades extendidas de valor único en una instancia nueva o existente de un recurso.</span><span class="sxs-lookup"><span data-stu-id="a3865-102">Create one or more single-value extended properties in a new or existing instance of a resource.</span></span> 

<span data-ttu-id="a3865-103">Se admiten los siguientes recursos de usuario:</span><span class="sxs-lookup"><span data-stu-id="a3865-103">The following user resources are supported:</span></span>

- [<span data-ttu-id="a3865-104">message</span><span class="sxs-lookup"><span data-stu-id="a3865-104">message</span></span>](../resources/message.md)
- [<span data-ttu-id="a3865-105">mailFolder</span><span class="sxs-lookup"><span data-stu-id="a3865-105">mailFolder</span></span>](../resources/mailfolder.md)
- [<span data-ttu-id="a3865-106">event</span><span class="sxs-lookup"><span data-stu-id="a3865-106">event</span></span>](../resources/event.md)
- [<span data-ttu-id="a3865-107">calendar</span><span class="sxs-lookup"><span data-stu-id="a3865-107">calendar</span></span>](../resources/calendar.md)
- [<span data-ttu-id="a3865-108">contact</span><span class="sxs-lookup"><span data-stu-id="a3865-108">contact</span></span>](../resources/contact.md)
- [<span data-ttu-id="a3865-109">contactFolder</span><span class="sxs-lookup"><span data-stu-id="a3865-109">contactFolder</span></span>](../resources/contactfolder.md) 

<span data-ttu-id="a3865-110">También los siguientes recursos de grupo:</span><span class="sxs-lookup"><span data-stu-id="a3865-110">As well as the following group resources:</span></span>

- <span data-ttu-id="a3865-111">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a3865-111">group [event](../resources/event.md)</span></span>
- <span data-ttu-id="a3865-112">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a3865-112">group [calendar](../resources/calendar.md)</span></span>
- <span data-ttu-id="a3865-113">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a3865-113">group [post](../resources/post.md)</span></span> 

<span data-ttu-id="a3865-114">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="a3865-114">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span>

## <a name="permissions"></a><span data-ttu-id="a3865-115">Permisos</span><span class="sxs-lookup"><span data-stu-id="a3865-115">Permissions</span></span>
<span data-ttu-id="a3865-p101">Según el recurso en el que cree la propiedad extendida, se requiere uno de los siguientes ámbitos para ejecutar esta API: Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a3865-p101">One of the following permissions is required to call this API, depending on the resource you're creating the extended property in. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

- <span data-ttu-id="a3865-118">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a3865-118">Mail.ReadWrite</span></span>
- <span data-ttu-id="a3865-119">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a3865-119">Calendars.ReadWrite</span></span>
- <span data-ttu-id="a3865-120">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a3865-120">Contacts.ReadWrite</span></span>
- <span data-ttu-id="a3865-121">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a3865-121">Group.ReadWrite.All</span></span>
 
## <a name="http-request"></a><span data-ttu-id="a3865-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a3865-122">HTTP request</span></span>
<span data-ttu-id="a3865-123">Puede crear propiedades extendidas en una instancia de recurso nueva o existente.</span><span class="sxs-lookup"><span data-stu-id="a3865-123">You can create extended properties in a new or existing resource instance.</span></span>

<span data-ttu-id="a3865-p102">Para crear una o varias propiedades extendidas en una instancia de recurso _nueva_, use la misma solicitud de REST que al crear la instancia e incluya las propiedades de la nueva instancia de recurso _y de la propiedad extendida_ en el cuerpo de la solicitud. Tenga en cuenta que algunos recursos admiten más de una forma de creación. Para obtener más información sobre cómo crear estas instancias de recurso, consulte los temas correspondientes para crear un [message](../resources/message.md), [mailFolder](../api/user_post_mailfolders.md), [event](../api/user_post_events.md), [calendar](../api/user_post_calendars.md), [contact](../api/user_post_contacts.md), [contactFolder](../api/user_post_contactfolders.md), [group event](../api/group_post_events.md) y [group post](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="a3865-p102">To create one or more extended properties in a _new_ resource instance, use the same REST request as creating the instance, and include the properties of the new resource instance _and extended property_ in the request body. Note that some resources support creation in more than one way. For more information on creating these resource instances, see the corresponding topics for creating a [message](../resources/message.md), [mailFolder](../api/user_post_mailfolders.md), [event](../api/user_post_events.md), [calendar](../api/user_post_calendars.md), [contact](../api/user_post_contacts.md), [contactFolder](../api/user_post_contactfolders.md), [group event](../api/group_post_events.md), and [group post](../resources/post.md).</span></span> 
 
<span data-ttu-id="a3865-127">A continuación tiene la sintaxis de las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="a3865-127">The following is the syntax of the requests.</span></span> 

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

<span data-ttu-id="a3865-128">Para crear una o varias propiedades extendidas en una instancia de recurso existente, especifique la instancia en la solicitud e incluya la propiedad extendida en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a3865-128">To create one or more extended properties in an existing resource instance, specify the instance in the request, and include the extended property in the request body.</span></span>

<span data-ttu-id="a3865-129">**Nota** No puede crear una propiedad extendida en una publicación de grupo existente.</span><span class="sxs-lookup"><span data-stu-id="a3865-129">**Note** You cannot create an extended property in an existing group post.</span></span>

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

## <a name="request-headers"></a><span data-ttu-id="a3865-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a3865-130">Request headers</span></span>
| <span data-ttu-id="a3865-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="a3865-131">Name</span></span>       | <span data-ttu-id="a3865-132">Valor</span><span class="sxs-lookup"><span data-stu-id="a3865-132">Value</span></span> |
|:---------------|:----------|
| <span data-ttu-id="a3865-133">Authorization</span><span class="sxs-lookup"><span data-stu-id="a3865-133">Authorization</span></span> | <span data-ttu-id="a3865-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a3865-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a3865-136">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a3865-136">Content-Type</span></span> | <span data-ttu-id="a3865-137">application/json</span><span class="sxs-lookup"><span data-stu-id="a3865-137">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="a3865-138">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="a3865-138">Request body</span></span>

<span data-ttu-id="a3865-139">Proporcione un cuerpo JSON para cada objeto [singleValueLegacyExtendedProperty](../resources/singleValueLegacyExtendedProperty.md) en la propiedad de la colección **singleValueExtendedProperties** de la instancia de recurso.</span><span class="sxs-lookup"><span data-stu-id="a3865-139">Provide a JSON body of each [singleValueLegacyExtendedProperty](../resources/singleValueLegacyExtendedProperty.md) object in the **singleValueExtendedProperties** collection property of the resource instance.</span></span>

|<span data-ttu-id="a3865-140">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a3865-140">Property</span></span>|<span data-ttu-id="a3865-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="a3865-141">Type</span></span>|<span data-ttu-id="a3865-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3865-142">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a3865-143">singleValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="a3865-143">singleValueExtendedProperties</span></span>|<span data-ttu-id="a3865-144">Colección [singleValueLegacyExtendedProperty](../resources/singleValueLegacyExtendedProperty.md)</span><span class="sxs-lookup"><span data-stu-id="a3865-144">[singleValueLegacyExtendedProperty](../resources/singleValueLegacyExtendedProperty.md) collection</span></span>| <span data-ttu-id="a3865-145">Una matriz de una o varias propiedades extendidas de valor único.</span><span class="sxs-lookup"><span data-stu-id="a3865-145">An array of one or more single-valued extended properties.</span></span> |
|<span data-ttu-id="a3865-146">id</span><span class="sxs-lookup"><span data-stu-id="a3865-146">id</span></span>|<span data-ttu-id="a3865-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="a3865-147">String</span></span>|<span data-ttu-id="a3865-p104">Para cada propiedad de la colección **singleValueExtendedProperties**, especifique esto para identificar la propiedad. Debe tener uno de los formatos compatibles. Consulte la [Información general de las propiedades extendidas de Outlook](../resources/extended-properties-overview.md) para obtener más información. Necesario.</span><span class="sxs-lookup"><span data-stu-id="a3865-p104">For each property in the **singleValueExtendedProperties** collection, specify this to identify the property. It must follow one of the supported formats. See [Outlook extended properties overview](../resources/extended-properties-overview.md) for more information. Required.</span></span>|
|<span data-ttu-id="a3865-152">value</span><span class="sxs-lookup"><span data-stu-id="a3865-152">value</span></span>|<span data-ttu-id="a3865-153">cadena</span><span class="sxs-lookup"><span data-stu-id="a3865-153">string</span></span>|<span data-ttu-id="a3865-p105">Para cada propiedad de la colección **singleValueExtendedProperties**, especifique el valor de la propiedad. Necesario.</span><span class="sxs-lookup"><span data-stu-id="a3865-p105">For each property in the **singleValueExtendedProperties** collection, specify the property value. Required.</span></span>|

<span data-ttu-id="a3865-156">Al crear una propiedad extendida en una instancia de recurso _nueva_, además de la nueva colección **singleValueExtendedProperties**, proporcione una representación JSON de esa instancia de recurso (es decir, un [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), etc.).</span><span class="sxs-lookup"><span data-stu-id="a3865-156">When creating an extended property in a _new_ resource instance, in addition to the new **singleValueExtendedProperties** collection, provide a JSON representation of that resource instance (that is, a [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), etc.)</span></span>

## <a name="response"></a><span data-ttu-id="a3865-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a3865-157">Response</span></span>

#### <a name="response-code"></a><span data-ttu-id="a3865-158">Código de respuesta</span><span class="sxs-lookup"><span data-stu-id="a3865-158">Response code</span></span>
<span data-ttu-id="a3865-159">Una operación que crea correctamente una propiedad extendida en una nueva instancia de recurso devuelve `201 Created`, excepto en un mensaje de grupo nuevo, ya que, según el método usado, la operación puede devolver `200 OK` o `202 Accepted`.</span><span class="sxs-lookup"><span data-stu-id="a3865-159">An operation successful in creating an extended property in a new resource instance returns `201 Created`, except in a new group post, depending on the method used, the operation can return `200 OK` or `202 Accepted`.</span></span>

<span data-ttu-id="a3865-160">En una instancia de recurso existente, una operación que se ejecuta correctamente devuelve `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="a3865-160">In an existing resource instance, a successful create operation returns `200 OK`.</span></span> 


#### <a name="response-body"></a><span data-ttu-id="a3865-161">Cuerpo de la respuesta</span><span class="sxs-lookup"><span data-stu-id="a3865-161">Response body</span></span>

<span data-ttu-id="a3865-p106">Al crear una propiedad extendida, la respuesta incluye solo la instancia nueva o existente, pero no la nueva propiedad extendida. Para ver la propiedad extendida recién creada, [expanda la instancia con la propiedad extendida](../api/singlevaluelegacyextendedproperty_get.md).</span><span class="sxs-lookup"><span data-stu-id="a3865-p106">When creating an extended property, the response includes only the new or existing instance but not the new extended property. To see the newly created extended property, [get the instance expanded with the extended property](../api/singlevaluelegacyextendedproperty_get.md).</span></span>

<span data-ttu-id="a3865-164">Al crear una propiedad extendida en una [publicación de grupo](../resources/post.md) _nueva_ al responder a un hilo o a una publicación, la respuesta incluye solo un código de respuesta, pero no la nueva publicación ni la propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="a3865-164">When creating an extended property in a _new_ [group post](../resources/post.md) by replying to a thread or post, the response includes only a response code but not the new post nor the extended property.</span></span>



## <a name="example"></a><span data-ttu-id="a3865-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a3865-165">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="a3865-166">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="a3865-166">Request 1</span></span>

<span data-ttu-id="a3865-p107">El primer ejemplo crea un evento nuevo y una propiedad extendida de valor único en la misma operación POST. Aparte de las propiedades que normalmente incluiría en un nuevo evento, el cuerpo de la solicitud incluye la colección **singleValueExtendedProperties** que contiene una propiedad extendida de valor único y lo siguiente para la propiedad:</span><span class="sxs-lookup"><span data-stu-id="a3865-p107">The first example creates a new event and a single-value extended property in the same POST operation. Apart from the properties you'd normally include for a new event, the request body includes the **singleValueExtendedProperties** collection that contains one single-value extended property, and the following for the property:</span></span>
- <span data-ttu-id="a3865-169">**id** especifica el tipo de propiedad como `String`, el GUID y la propiedad denominada `Fun`.</span><span class="sxs-lookup"><span data-stu-id="a3865-169">**id** specifies the property type as `String`, the GUID, and the property named `Fun`.</span></span>
- <span data-ttu-id="a3865-170">**value** especifica `Food` como el valor de la propiedad `Fun`.</span><span class="sxs-lookup"><span data-stu-id="a3865-170">**value** specifies `Food` as the value of the `Fun` property.</span></span> 

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

##### <a name="response-1"></a><span data-ttu-id="a3865-171">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="a3865-171">Response 1</span></span>

<span data-ttu-id="a3865-p108">Una respuesta correcta se indica mediante un código de respuesta `HTTP 201 Created` e incluye el nuevo evento en el cuerpo de la respuesta. Es similar a la respuesta al [crear solo un evento](../api/user_post_events.md). El cuerpo de la respuesta no incluye ninguna propiedad extendida recién creada.</span><span class="sxs-lookup"><span data-stu-id="a3865-p108">A successful response is indicated by an `HTTP 201 Created` response code, and includes the new event in the response body, similar to the response from [creating just an event](../api/user_post_events.md). The response does not include any newly created extended properties.</span></span>

<span data-ttu-id="a3865-174">Para ver la propiedad extendida recién creada, [expanda el evento con la propiedad extendida](../api/singlevaluelegacyextendedproperty_get.md).</span><span class="sxs-lookup"><span data-stu-id="a3865-174">To see the newly created extended property, [get the event expanded with the extended property](../api/singlevaluelegacyextendedproperty_get.md).</span></span>


****

##### <a name="request-2"></a><span data-ttu-id="a3865-175">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="a3865-175">Request 2</span></span>

<span data-ttu-id="a3865-p109">El segundo ejemplo crea una propiedad extendida de valor único para el mensaje existente especificado. La propiedad extendida es el único elemento de la matriz **singleValueExtendedProperties**. El cuerpo de la solicitud incluye lo siguiente para la propiedad extendida:</span><span class="sxs-lookup"><span data-stu-id="a3865-p109">The second example creates one single-value extended property for the specified existing message. That extended property is the only element in the **singleValueExtendedProperties** array. The request body includes the following for the extended property:</span></span>
- <span data-ttu-id="a3865-179">**id** especifica el tipo de propiedad como `String`, el GUID y la propiedad denominada `Color`.</span><span class="sxs-lookup"><span data-stu-id="a3865-179">**id** specifies the property type as `String`, the GUID, and the property named `Color`.</span></span>
- <span data-ttu-id="a3865-180">**value** especifica `Green` como el valor de la propiedad `Color`.</span><span class="sxs-lookup"><span data-stu-id="a3865-180">**value** specifies `Green` as the value of the `Color` property.</span></span>

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

##### <a name="response-2"></a><span data-ttu-id="a3865-181">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="a3865-181">Response 2</span></span>

<span data-ttu-id="a3865-p110">Una respuesta correcta se indica mediante un código de respuesta `HTTP 200 OK` e incluye el mensaje especificado en el cuerpo de la respuesta. Es similar a la respuesta al [actualizar un mensaje](../api/message_update.md). El cuerpo de la respuesta no incluye la propiedad extendida recién creada.</span><span class="sxs-lookup"><span data-stu-id="a3865-p110">A successful response is indicated by an `HTTP 200 OK` response code, and includes the specified message in the response body, similar to the response from [updating a message](../api/message_update.md). The response does not include the newly created extended property.</span></span>

<span data-ttu-id="a3865-184">Para ver la propiedad extendida recién creada, [expanda el mensaje con la propiedad extendida](../api/singlevaluelegacyextendedproperty_get.md).</span><span class="sxs-lookup"><span data-stu-id="a3865-184">To see the newly created extended property, [get the message expanded with the extended property](../api/singlevaluelegacyextendedproperty_get.md).</span></span>

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

