# <a name="get-singlevaluelegacyextendedproperty"></a><span data-ttu-id="ddfc0-101">Obtener singleValueLegacyExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="ddfc0-101">Get singleValueLegacyExtendedProperty</span></span>

<span data-ttu-id="ddfc0-102">Obtenga instancias de recurso que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`.</span><span class="sxs-lookup"><span data-stu-id="ddfc0-102">Get resource instances that contain a single-value extended property by using `$expand` or `$filter`.</span></span>

<span data-ttu-id="ddfc0-p101">El uso del parámetro de consulta `$expand` permite expandir la instancia especificada con la propiedad extendida indicada. Actualmente, esta es la única manera de obtener el objeto [singleValueLegacyExtendedProperty](../resources/singleValueLegacyExtendedProperty.md) que representa una propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="ddfc0-p101">Using the query parameter `$expand` allows you to get the specified instance expanded with the indicated extended property. This is currently the only way to get the [singleValueLegacyExtendedProperty](../resources/singleValueLegacyExtendedProperty.md) object that represents an extended property.</span></span>

<span data-ttu-id="ddfc0-p102">El uso del parámetro de consulta `$filter` permite obtener todas las instancias del recurso especificado con una propiedad extendida que coincide con un filtro en las propiedades **id** y **value**. El filtro se aplica a todas las instancias del recurso en el buzón del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="ddfc0-p102">Using the query parameter `$filter` allows you to get all the instances of the specified resource that have an extended property matching a filter on the **id** and **value** properties. The filter is applied to all instances of the resource in the signed-in user's mailbox.</span></span>

<span data-ttu-id="ddfc0-107">Se admiten los siguientes recursos de usuario:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-107">The following user resources are supported:</span></span>

- [<span data-ttu-id="ddfc0-108">message</span><span class="sxs-lookup"><span data-stu-id="ddfc0-108">message</span></span>](../resources/message.md)
- [<span data-ttu-id="ddfc0-109">mailFolder</span><span class="sxs-lookup"><span data-stu-id="ddfc0-109">mailFolder</span></span>](../resources/mailfolder.md)
- [<span data-ttu-id="ddfc0-110">event</span><span class="sxs-lookup"><span data-stu-id="ddfc0-110">Event</span></span>](../resources/event.md)
- [<span data-ttu-id="ddfc0-111">calendar</span><span class="sxs-lookup"><span data-stu-id="ddfc0-111">calendar</span></span>](../resources/calendar.md)
- [<span data-ttu-id="ddfc0-112">contact</span><span class="sxs-lookup"><span data-stu-id="ddfc0-112">Contact</span></span>](../resources/contact.md)
- [<span data-ttu-id="ddfc0-113">contactFolder</span><span class="sxs-lookup"><span data-stu-id="ddfc0-113">contactFolder</span></span>](../resources/contactfolder.md) 

<span data-ttu-id="ddfc0-114">También los siguientes recursos de grupo:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-114">As well as the following group resources:</span></span>

- <span data-ttu-id="ddfc0-115">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="ddfc0-115">group [event](../resources/event.md)</span></span>
- <span data-ttu-id="ddfc0-116">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="ddfc0-116">group [calendar](../resources/calendar.md)</span></span>
- <span data-ttu-id="ddfc0-117">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="ddfc0-117">group post</span></span> 

<span data-ttu-id="ddfc0-118">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="ddfc0-118">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ddfc0-119">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ddfc0-119">Prerequisites</span></span>
<span data-ttu-id="ddfc0-120">Según el recurso que quiera obtener, se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-120">One of the following **scopes** is required to execute this API, depending on the resource you're getting:</span></span>

- <span data-ttu-id="ddfc0-121">_Mail.Read_</span><span class="sxs-lookup"><span data-stu-id="ddfc0-121">_Mail.Read_</span></span>
- <span data-ttu-id="ddfc0-122">_Calendars.Read_</span><span class="sxs-lookup"><span data-stu-id="ddfc0-122">_Calendars.Read_</span></span>
- <span data-ttu-id="ddfc0-123">_Contacts.Read_</span><span class="sxs-lookup"><span data-stu-id="ddfc0-123">_Contacts.Read_</span></span>
- <span data-ttu-id="ddfc0-124">_Group.Read.All_</span><span class="sxs-lookup"><span data-stu-id="ddfc0-124">_Group.Read.All_</span></span> 

## <a name="http-request"></a><span data-ttu-id="ddfc0-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ddfc0-125">HTTP request</span></span>

#### <a name="get-a-resource-instance-using-expand"></a><span data-ttu-id="ddfc0-126">GET (OBTENER) una instancia de recurso mediante el uso de `$expand`</span><span class="sxs-lookup"><span data-stu-id="ddfc0-126">GET a resource instance using `$expand`</span></span>
<span data-ttu-id="ddfc0-p103">Expanda una instancia de recurso con la propiedad extendida que coincida con un filtro en la propiedad **id**. Asegúrese de aplicar [la codificación de direcciones URL](http://www.w3schools.com/tags/ref_urlencode.asp) a los caracteres de espacio de la cadena de filtro.</span><span class="sxs-lookup"><span data-stu-id="ddfc0-p103">Get a resource instance expanded with the extended property which matches a filter on the **id** property. Make sure you apply [URL encoding](http://www.w3schools.com/tags/ref_urlencode.asp) to the space characters in the filter string.</span></span>

<span data-ttu-id="ddfc0-129">Obtener una instancia de **message**:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-129">Get a **message** instance:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/messages/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /me/mailFolders/{id}/messages/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="ddfc0-130">Obtener una instancia de **mailFolder**:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-130">Get a **mailFolder** instance:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/mailFolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="ddfc0-131">Obtener una instancia de **event**:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-131">Get an **event** instance:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/events/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/events/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="ddfc0-132">Obtener una instancia de **calendar**:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-132">Get a **calendar** instance:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendars/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/calendars/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="ddfc0-133">Obtener una instancia de **contact**:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-133">Get a **contact** instance:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contacts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /me/contactFolders/{id}/contacts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}/contacts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="ddfc0-134">Obtener una instancia de **contactFolder**:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-134">Get a **contactFolder** instance:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contactfolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="ddfc0-135">Obtener una instancia de **event** de grupo:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-135">Get a group **event** instance:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/events/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="ddfc0-136">Obtener una instancia de **publicación** de grupo:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-136">Get a group **post** instance:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}/posts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}?$expand=singleValueExtendedProperties($filter=id eq '{id_value}')
```

#### <a name="get-resource-instances-using-filter"></a><span data-ttu-id="ddfc0-137">GET (OBTENER) instancias de recurso mediante el uso de `$filter`</span><span class="sxs-lookup"><span data-stu-id="ddfc0-137">GET resource instances using `$filter`</span></span>

<span data-ttu-id="ddfc0-p104">Obtenga instancias de un recurso compatible con la propiedad extendida que coincide con un filtro en las propiedades **id** y **value**. Asegúrese de aplicar [la codificación de direcciones URL](http://www.w3schools.com/tags/ref_urlencode.asp) a los siguientes caracteres de la cadena de filtro: barra diagonal y espacio .</span><span class="sxs-lookup"><span data-stu-id="ddfc0-p104">Get instances of a supported resource that have the extended property matching a filter on the **id** and **value** properties. Make sure you apply [URL encoding](http://www.w3schools.com/tags/ref_urlencode.asp) to the following characters in the filter string - forward slash and space.</span></span>


<span data-ttu-id="ddfc0-140">Obtener instancias de **mensaje**:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-140">Get **message** instances:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /me/mailFolders/{id}/messages?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
<span data-ttu-id="ddfc0-141">Obtener instancias de **mailFolder**:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-141">Get **mailFolder** instances:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/mailFolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```

<span data-ttu-id="ddfc0-142">Obtener instancias de **evento**:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-142">Get **event** instances:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
<span data-ttu-id="ddfc0-143">Obtener instancias de **calendario**:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-143">Get **calendar** instances:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendars?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/calendars?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
<span data-ttu-id="ddfc0-144">Obtener instancias de **contacto**:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-144">Get **contact** instances:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/contacts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /me/contactFolders/{id}/contacts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}/contacts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
<span data-ttu-id="ddfc0-145">Obtener instancias de **contactFolder**:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-145">Get **contactFolder** instances:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contactfolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /users/{id|userPrincipalName}/contactFolders?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```
<span data-ttu-id="ddfc0-146">Obtener instancias de **evento** de grupo:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-146">Get group **event** instances:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/events?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```

<span data-ttu-id="ddfc0-147">Obtener instancias de **publicación** de grupo:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-147">Get group **post** instances:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}/posts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
GET /groups/{id}/conversations/{id}/threads/{id}/posts?$filter=singleValueExtendedProperties/Any(ep: ep/id eq '{id_value}' and ep/value eq '{property_value}')
```

## <a name="parameters"></a><span data-ttu-id="ddfc0-148">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ddfc0-148">Parameters</span></span>
|<span data-ttu-id="ddfc0-149">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="ddfc0-149">**Parameter**</span></span>|<span data-ttu-id="ddfc0-150">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ddfc0-150">**Type**</span></span>|<span data-ttu-id="ddfc0-151">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ddfc0-151">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ddfc0-152">_Parámetros de dirección URL_</span><span class="sxs-lookup"><span data-stu-id="ddfc0-152">_URL parameters_</span></span>|
|<span data-ttu-id="ddfc0-153">id_value</span><span class="sxs-lookup"><span data-stu-id="ddfc0-153">id_value</span></span>|<span data-ttu-id="ddfc0-154">String</span><span class="sxs-lookup"><span data-stu-id="ddfc0-154">String</span></span>|<span data-ttu-id="ddfc0-p105">El identificador de la propiedad extendida que debe coincidir. Debe tener uno de los formatos compatibles. Consulte la [Información general de las propiedades extendidas de Outlook](../resources/extended-properties-overview.md) para obtener más información. Necesario.</span><span class="sxs-lookup"><span data-stu-id="ddfc0-p105">The ID of the extended property to match. It must follow one of the supported formats. See [Outlook extended properties overview](../resources/extended-properties-overview.md) for more information. Required.</span></span>|
|<span data-ttu-id="ddfc0-159">property_value</span><span class="sxs-lookup"><span data-stu-id="ddfc0-159">property_value</span></span>|<span data-ttu-id="ddfc0-160">Cadena</span><span class="sxs-lookup"><span data-stu-id="ddfc0-160">String</span></span>|<span data-ttu-id="ddfc0-p106">El valor de la propiedad extendida que debe coincidir. Es necesario donde aparece en la sección anterior de la **solicitud HTTP**.</span><span class="sxs-lookup"><span data-stu-id="ddfc0-p106">The value of the extended property to match. Required where listed in the **HTTP request** section above.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="ddfc0-163">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ddfc0-163">Request headers</span></span>
| <span data-ttu-id="ddfc0-164">Nombre</span><span class="sxs-lookup"><span data-stu-id="ddfc0-164">Name</span></span>      |<span data-ttu-id="ddfc0-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddfc0-165">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="ddfc0-166">Authorization</span><span class="sxs-lookup"><span data-stu-id="ddfc0-166">Authorization</span></span>  | <span data-ttu-id="ddfc0-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ddfc0-p107">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="ddfc0-169">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ddfc0-169">Request body</span></span>
<span data-ttu-id="ddfc0-170">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ddfc0-170">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ddfc0-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ddfc0-171">Response</span></span>

<span data-ttu-id="ddfc0-172">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="ddfc0-172">If successful, this method returns a `200 OK` response code.</span></span>

#### <a name="get-resource-instance-using-expand"></a><span data-ttu-id="ddfc0-173">GET (OBTENER) una instancia de recurso mediante el uso de `$expand`</span><span class="sxs-lookup"><span data-stu-id="ddfc0-173">GET resource instance using `$expand`</span></span>
<span data-ttu-id="ddfc0-174">El cuerpo de la respuesta incluye un objeto que representa la instancia de recurso solicitada y expandida con el objeto coincidente [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="ddfc0-174">The response body includes an object representing the requested resource instance, expanded with the matching [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md) object.</span></span>
  
#### <a name="get-resource-instances-using-filter"></a><span data-ttu-id="ddfc0-175">GET (OBTENER) instancias de recurso mediante el uso de `$filter`</span><span class="sxs-lookup"><span data-stu-id="ddfc0-175">GET resource instances using `$filter`</span></span>
<span data-ttu-id="ddfc0-p108">El cuerpo de la respuesta incluye uno o varios objetos que representan las instancias de recurso que contienen la propiedad extendida coincidente. El cuerpo de la respuesta no incluye la propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="ddfc0-p108">The response body includes one or more objects representing the resource instances that contain the matching extended property. The response body does not include the extended property.</span></span>

## <a name="example"></a><span data-ttu-id="ddfc0-178">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ddfc0-178">Example</span></span>
#### <a name="request-1"></a><span data-ttu-id="ddfc0-179">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="ddfc0-179">Request 1</span></span>

<span data-ttu-id="ddfc0-p109">El primer ejemplo obtiene y expande el mensaje especificado al incluir una propiedad extendida de valor único. El filtro devuelve la propiedad extendida cuyo **identificador** coincide con la cadena `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (la codificación de dirección URL se ha eliminado aquí para facilitar la lectura).</span><span class="sxs-lookup"><span data-stu-id="ddfc0-p109">The first example gets and expands the specified message by including a single-value extended property. The filter returns the extended property that has its **id** matching the string `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (with URL encoding removed here for ease of reading).</span></span>

<!-- {
  "blockType": "request",
  "name": "get_singlevaluelegacyextendedproperty_1"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages('AAMkAGE1M2_bs88AACHsLqWAAA=')?$expand=singleValueExtendedProperties($filter=id%20eq%20'String%20{66f5a359-4659-4830-9070-00047ec6ac6e}%20Name%20Color')
```
##### <a name="response-1"></a><span data-ttu-id="ddfc0-182">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="ddfc0-182">Response 1</span></span>
<span data-ttu-id="ddfc0-183">El cuerpo de la respuesta incluye todas las propiedades del mensaje especificado y devuelve la propiedad extendida del filtro.</span><span class="sxs-lookup"><span data-stu-id="ddfc0-183">The response body includes all the properties of the specified message and extended property returned from the filter.</span></span>

<span data-ttu-id="ddfc0-p110">Nota: El objeto del **mensaje** que aparece aquí está truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ddfc0-p110">Note: The **message** object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/messages('AAMkAGE1M2_bs88AACHsLqWAAA=')",
    "@odata.etag": "W/\"CQAAABYAAACY4MQpaFz9SbqUDe4+bs88AACbyS4H\"",
    "id": "AAMkAGE1M2_bs88AACHsLqWAAA=",
    "subject": "RE: Talk about emergency prep",
    "sender": {
        "emailAddress": {
            "name": "Christine Irwin",
            "address": "christine@contoso.com"
        }
    },
    "from": null,
    "toRecipients": [
        {
            "emailAddress": {
                "name": "Christine Irwin",
                "address": "christine@contoso.com"
            }
        }
    ],
    "singleValueExtendedProperties@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/messages('AAMkAGE1M2_bs88AACHsLqWAAA%3D')/singleValueExtendedProperties",
    "singleValueExtendedProperties": [
        {
            "id": "String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color",
            "value": "Green"
        }
    ]
}
```

****

#### <a name="request-2"></a><span data-ttu-id="ddfc0-186">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="ddfc0-186">Request 2</span></span>

<span data-ttu-id="ddfc0-p111">El segundo ejemplo obtiene mensajes con la propiedad extendida de valor único especificada en el filtro. El filtro devuelve la propiedad extendida:</span><span class="sxs-lookup"><span data-stu-id="ddfc0-p111">The second example gets messages that have the single-value extended property specified in the filter. The filter returns the extended property that has:</span></span>
- <span data-ttu-id="ddfc0-189">Cuyo **identificado** coincide con la cadena `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (la codificación de dirección URL se ha eliminado aquí para facilitar la lectura).</span><span class="sxs-lookup"><span data-stu-id="ddfc0-189">Its **id** matching the string `String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color` (with URL encoding removed here for ease of reading).</span></span>
- <span data-ttu-id="ddfc0-190">Cuyo **valor** es `Green`.</span><span class="sxs-lookup"><span data-stu-id="ddfc0-190">Its **value** being `Green`.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/api/v1.0/Me/messages?$filter=singleValueExtendedProperties%2FAny(ep%3A%20ep%2Fid%20eq%20'String%20{66f5a359-4659-4830-9070-00047ec6ac6e}%20Name%20Color'%20and%20ep%2Fvalue%20eq%20'Green')
```

##### <a name="response-2"></a><span data-ttu-id="ddfc0-191">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="ddfc0-191">Response 2</span></span>

<span data-ttu-id="ddfc0-p112">Un código de respuesta `HTTP 200 OK` indica una respuesta correcta y el cuerpo de la respuesta incluye todas las propiedades de los mensajes cuya propiedad extendida coincide con el filtro. El cuerpo de la respuesta es similar a la respuesta al [obtener una colección de mensajes](../api/user_list_messages.md). El cuerpo de la respuesta no incluye la propiedad extendida coincidente.</span><span class="sxs-lookup"><span data-stu-id="ddfc0-p112">A successful response is indicated by an `HTTP 200 OK` response code, and the response body includes all the properties of the messages that have the extended property matching the filter. The response body is similar to the response from [getting a message collection](../api/user_list_messages.md). The response does not include the matching extended property.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get singleValueLegacyExtendedProperty",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->