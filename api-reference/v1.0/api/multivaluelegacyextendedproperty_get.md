# <a name="get-multivaluelegacyextendedproperty"></a><span data-ttu-id="9b0ed-101">Obtener multiValueLegacyExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="9b0ed-101">Get multiValueLegacyExtendedProperty</span></span>

<span data-ttu-id="9b0ed-102">Obtenga una instancia de recursos que contiene una propiedad extendida de varios valores mediante el uso de `$expand`.</span><span class="sxs-lookup"><span data-stu-id="9b0ed-102">Get a resource instance that contains a multi-value extended property by using `$expand`.</span></span>

<span data-ttu-id="9b0ed-103">El uso del parámetro de consulta `$expand` le permite expandir la instancia especificada con la propiedad extendida indicada.</span><span class="sxs-lookup"><span data-stu-id="9b0ed-103">Using the query parameter `$expand` allows you to get the specified instance expanded with the indicated extended property. This is currently the only way to get the singleValueLegacyExtendedProperty object that represents an extended property.</span></span> <span data-ttu-id="9b0ed-104">Actualmente, esta es la única forma de obtener el objeto [multiValueLegacyExtendedProperty](../resources/multiValueLegacyExtendedProperty.md) que representa una propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="9b0ed-104">Using the query parameter  allows you to get the specified instance expanded with the indicated extended property. This is currently the only way to get the [singleValueLegacyExtendedProperty](../resources/multiValueLegacyExtendedProperty.md) object that represents an extended property.</span></span>

<span data-ttu-id="9b0ed-105">Se admiten los siguientes recursos de usuario:</span><span class="sxs-lookup"><span data-stu-id="9b0ed-105">The following user resources are supported:</span></span>

- [<span data-ttu-id="9b0ed-106">message</span><span class="sxs-lookup"><span data-stu-id="9b0ed-106">message</span></span>](../resources/message.md)
- [<span data-ttu-id="9b0ed-107">mailFolder</span><span class="sxs-lookup"><span data-stu-id="9b0ed-107">mailFolder</span></span>](../resources/mailfolder.md)
- [<span data-ttu-id="9b0ed-108">event</span><span class="sxs-lookup"><span data-stu-id="9b0ed-108">event</span></span>](../resources/event.md)
- [<span data-ttu-id="9b0ed-109">calendar</span><span class="sxs-lookup"><span data-stu-id="9b0ed-109">calendar</span></span>](../resources/calendar.md)
- [<span data-ttu-id="9b0ed-110">contact</span><span class="sxs-lookup"><span data-stu-id="9b0ed-110">contact</span></span>](../resources/contact.md)
- [<span data-ttu-id="9b0ed-111">contactFolder</span><span class="sxs-lookup"><span data-stu-id="9b0ed-111">contactFolder</span></span>](../resources/contactfolder.md) 

<span data-ttu-id="9b0ed-112">También los siguientes recursos de grupo:</span><span class="sxs-lookup"><span data-stu-id="9b0ed-112">As well as the following group resources:</span></span>

- <span data-ttu-id="9b0ed-113">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="9b0ed-113">group [event](../resources/event.md)</span></span>
- <span data-ttu-id="9b0ed-114">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="9b0ed-114">group [calendar](../resources/calendar.md)</span></span>
- <span data-ttu-id="9b0ed-115">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="9b0ed-115">group [post](../resources/post.md)</span></span> 

<span data-ttu-id="9b0ed-116">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="9b0ed-116">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span>

## <a name="permissions"></a><span data-ttu-id="9b0ed-117">Permisos</span><span class="sxs-lookup"><span data-stu-id="9b0ed-117">Permissions</span></span>
<span data-ttu-id="9b0ed-p102">Según el recurso que seleccione, se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9b0ed-p102">One of the following permissions is required to call this API, depending on the resource you're getting. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

- <span data-ttu-id="9b0ed-120">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="9b0ed-120">Mail.Read</span></span>
- <span data-ttu-id="9b0ed-121">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="9b0ed-121">Calendars.Read</span></span>
- <span data-ttu-id="9b0ed-122">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="9b0ed-122">Contacts.Read</span></span>
- <span data-ttu-id="9b0ed-123">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="9b0ed-123">Group.Read.All</span></span> 
 
## <a name="http-request"></a><span data-ttu-id="9b0ed-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b0ed-124">HTTP request</span></span>

<span data-ttu-id="9b0ed-p103">Expanda una instancia de recurso con la propiedad extendida que coincida con un filtro en la propiedad **id**. Asegúrese de aplicar la [codificación de direcciones URL]((http://www.w3schools.com/tags/ref_urlencode.asp)) a los caracteres de espacio de la cadena de filtro.</span><span class="sxs-lookup"><span data-stu-id="9b0ed-p103">Get a resource instance expanded with the extended property which matches a filter on the **id** property. Make sure you apply [URL encoding]((http://www.w3schools.com/tags/ref_urlencode.asp)) to the space characters in the filter string.</span></span>

<span data-ttu-id="9b0ed-127">Obtener una instancia de **message**:</span><span class="sxs-lookup"><span data-stu-id="9b0ed-127">Get a **message** instance:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/messages/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /me/mailFolders/{id}/messages/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="9b0ed-128">Obtener una instancia de **mailFolder**:</span><span class="sxs-lookup"><span data-stu-id="9b0ed-128">Get a **mailFolder** instance:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/mailFolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="9b0ed-129">Obtener una instancia de **event**:</span><span class="sxs-lookup"><span data-stu-id="9b0ed-129">Get an **event** instance:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/events/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/events/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="9b0ed-130">Obtener una instancia de **calendar**:</span><span class="sxs-lookup"><span data-stu-id="9b0ed-130">Get a **calendar** instance:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/calendars/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/calendars/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="9b0ed-131">Obtener una instancia de **contact**:</span><span class="sxs-lookup"><span data-stu-id="9b0ed-131">Get a **contact** instance:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contacts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /me/contactFolders/{id}/contacts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}/contacts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="9b0ed-132">Obtener una instancia de **contactFolder**:</span><span class="sxs-lookup"><span data-stu-id="9b0ed-132">Get a **contactFolder** instance:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contactfolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="9b0ed-133">Obtener una instancia de **event** de grupo:</span><span class="sxs-lookup"><span data-stu-id="9b0ed-133">Get a group **event** instance:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/events/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="9b0ed-134">Obtener una instancia de **post** de grupo:</span><span class="sxs-lookup"><span data-stu-id="9b0ed-134">Get a group **post** instance:</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}/posts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```

## <a name="parameters"></a><span data-ttu-id="9b0ed-135">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b0ed-135">Parameters</span></span>
|<span data-ttu-id="9b0ed-136">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="9b0ed-136">**Parameter**</span></span>|<span data-ttu-id="9b0ed-137">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9b0ed-137">**Type**</span></span>|<span data-ttu-id="9b0ed-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9b0ed-138">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9b0ed-139">_Parámetros de dirección URL_</span><span class="sxs-lookup"><span data-stu-id="9b0ed-139">_URL parameters_</span></span>|
|<span data-ttu-id="9b0ed-140">id_value</span><span class="sxs-lookup"><span data-stu-id="9b0ed-140">id_value</span></span>|<span data-ttu-id="9b0ed-141">String</span><span class="sxs-lookup"><span data-stu-id="9b0ed-141">String</span></span>|<span data-ttu-id="9b0ed-p104">El identificador de la propiedad extendida que debe coincidir. Debe tener uno de los formatos compatibles. Consulte la [Información general de las propiedades extendidas de Outlook](../resources/extended-properties-overview.md) para obtener más información. Necesario.</span><span class="sxs-lookup"><span data-stu-id="9b0ed-p104">The ID of the extended property to match. It must follow one of the supported formats. See [Outlook extended properties overview](../resources/extended-properties-overview.md) for more information. Required.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="9b0ed-146">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b0ed-146">Request headers</span></span>
| <span data-ttu-id="9b0ed-147">Nombre</span><span class="sxs-lookup"><span data-stu-id="9b0ed-147">Name</span></span>      |<span data-ttu-id="9b0ed-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b0ed-148">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="9b0ed-149">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b0ed-149">Authorization</span></span>  | <span data-ttu-id="9b0ed-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b0ed-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9b0ed-152">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b0ed-152">Request body</span></span>
<span data-ttu-id="9b0ed-153">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9b0ed-153">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9b0ed-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b0ed-154">Response</span></span>

<span data-ttu-id="9b0ed-155">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="9b0ed-155">If successful, this method returns a `200 OK` response code.</span></span> 

<span data-ttu-id="9b0ed-156">El cuerpo de la respuesta incluye un objeto que representa la instancia de recurso solicitada y expandida con el objeto coincidente [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="9b0ed-156">The response body includes an object representing the requested resource instance, expanded with the matching [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) object.</span></span>

## <a name="example"></a><span data-ttu-id="9b0ed-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b0ed-157">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9b0ed-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b0ed-158">Request</span></span>
<span data-ttu-id="9b0ed-p106">Este ejemplo obtiene y expande el evento especificado al incluir una propiedad extendida de varios valores. El filtro devuelve la propiedad extendida con un **id** que coincide con la cadena `StringArray {66f5a359-4659-4830-9070-00050ec6ac6e} Name Recreation` (la codificación de dirección URL se ha eliminado aquí para facilitar la lectura).</span><span class="sxs-lookup"><span data-stu-id="9b0ed-p106">This example gets and expands the specified event by including a multi-value extended property. The filter returns the extended property that has its **id** matching the string `StringArray {66f5a359-4659-4830-9070-00050ec6ac6e} Name Recreation` (with URL encoding removed here for ease of reading).</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/events('AAMkAGE1M2_bs88AACbuFiiAAA=')?$expand=multiValueExtendedProperties($filter=id%20eq%20'StringArray%20{66f5a359-4659-4830-9070-00050ec6ac6e}%20Name%20Recreation')
```
##### <a name="response"></a><span data-ttu-id="9b0ed-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b0ed-161">Response</span></span>

<span data-ttu-id="9b0ed-162">El cuerpo de la respuesta incluye todas las propiedades del evento especificado y devuelve la propiedad extendida del filtro.</span><span class="sxs-lookup"><span data-stu-id="9b0ed-162">The response body includes all the properties of the specified event and extended property returned from the filter.</span></span>

<span data-ttu-id="9b0ed-p107">Nota: El objeto **event** que aparece aquí está truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9b0ed-p107">Note: The **event** object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
Content-type: application/json
{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/events/$entity",
    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/events('AAMkAGE1M2_bs88AACbuFiiAAA=')",
    "@odata.etag": "W/\"mODEKWhc/Um6lA3uPm7PPAAAm8k15A==\"",
    "id": "AAMkAGE1M2_bs88AACbuFiiAAA=",
    "start": {
        "dateTime": "2015-11-26T17:00:00.0000000",
        "timeZone": "UTC"
    },
    "end": {
        "dateTime": "2015-11-30T05:00:00.0000000",
        "timeZone": "UTC"
    },
    "organizer": {
        "emailAddress": {
            "name": "Christine Irwin",
            "address": "christine@contoso.com"
        }
    },
    "multiValueExtendedProperties@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/events('AAMkAGE1M2_bs88AACbuFiiAAA%3D')/multiValueExtendedProperties",
    "multiValueExtendedProperties": [
        {
            "id": "StringArray {66f5a359-4659-4830-9070-00050ec6ac6e} Name Recreation",
            "value": [
                "Food",
                "Hiking",
                "Swimming"
            ]
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get multiValueLegacyExtendedProperty",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->