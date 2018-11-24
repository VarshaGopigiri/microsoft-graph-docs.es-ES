# <a name="get-multivaluelegacyextendedproperty"></a><span data-ttu-id="a0c70-101">Obtener multiValueLegacyExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="a0c70-101">Get multiValueLegacyExtendedProperty</span></span>

<span data-ttu-id="a0c70-102">Obtenga una instancia de recursos que contiene una propiedad extendida de varios valores mediante el uso de `$expand`.</span><span class="sxs-lookup"><span data-stu-id="a0c70-102">Get a resource instance that contains a multi-value extended property by using `$expand`.</span></span>

<span data-ttu-id="a0c70-103">El uso del parámetro de consulta `$expand` le permite expandir la instancia especificada con la propiedad extendida indicada.</span><span class="sxs-lookup"><span data-stu-id="a0c70-103">Using the query parameter `$expand` allows you to get the specified instance expanded with the indicated extended property.</span></span> <span data-ttu-id="a0c70-104">Actualmente, esta es la única forma de obtener el objeto [multiValueLegacyExtendedProperty](../resources/multiValueLegacyExtendedProperty.md) que representa una propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="a0c70-104">This is currently the only way to get the [multiValueLegacyExtendedProperty](../resources/multiValueLegacyExtendedProperty.md) object that represents an extended property.</span></span>

<span data-ttu-id="a0c70-105">Se admiten los siguientes recursos de usuario:</span><span class="sxs-lookup"><span data-stu-id="a0c70-105">The following user resources are supported:</span></span>

- [<span data-ttu-id="a0c70-106">calendar</span><span class="sxs-lookup"><span data-stu-id="a0c70-106">calendar</span></span>](../resources/calendar.md)
- [<span data-ttu-id="a0c70-107">contact</span><span class="sxs-lookup"><span data-stu-id="a0c70-107">contact</span></span>](../resources/contact.md)
- [<span data-ttu-id="a0c70-108">contactFolder</span><span class="sxs-lookup"><span data-stu-id="a0c70-108">contactFolder</span></span>](../resources/contactfolder.md) 
- [<span data-ttu-id="a0c70-109">event</span><span class="sxs-lookup"><span data-stu-id="a0c70-109">event</span></span>](../resources/event.md)
- [<span data-ttu-id="a0c70-110">mailFolder</span><span class="sxs-lookup"><span data-stu-id="a0c70-110">mailFolder</span></span>](../resources/mailfolder.md)
- [<span data-ttu-id="a0c70-111">message</span><span class="sxs-lookup"><span data-stu-id="a0c70-111">message</span></span>](../resources/message.md) 

<span data-ttu-id="a0c70-112">También los siguientes recursos de grupo:</span><span class="sxs-lookup"><span data-stu-id="a0c70-112">As well as the following group resources:</span></span>

- <span data-ttu-id="a0c70-113">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a0c70-113">group [calendar](../resources/calendar.md)</span></span>
- <span data-ttu-id="a0c70-114">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a0c70-114">group [event](../resources/event.md)</span></span>
- <span data-ttu-id="a0c70-115">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a0c70-115">group [post](../resources/post.md)</span></span>

<span data-ttu-id="a0c70-116">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="a0c70-116">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span>

## <a name="permissions"></a><span data-ttu-id="a0c70-117">Permisos</span><span class="sxs-lookup"><span data-stu-id="a0c70-117">Permissions</span></span>
<span data-ttu-id="a0c70-118">Dependiendo del recurso está obteniendo la propiedad extendida desde y el permiso escriba (delegada o de la aplicación) se solicitud, el permiso especificado en la tabla siguiente es el requisito mínimo para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a0c70-118">Depending on the resource you're getting the extended property from and the permission type (delegated or application) you request, the permission specified in the following table is the minimum required to call this API.</span></span> <span data-ttu-id="a0c70-119">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a0c70-119">To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="a0c70-120">Recurso admitido</span><span class="sxs-lookup"><span data-stu-id="a0c70-120">Supported resource</span></span> | <span data-ttu-id="a0c70-121">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a0c70-121">Delegated (work or school account)</span></span> | <span data-ttu-id="a0c70-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a0c70-122">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a0c70-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a0c70-123">Application</span></span> |
|:-----|:-----|:-----|:-----|
| [<span data-ttu-id="a0c70-124">calendario</span><span class="sxs-lookup"><span data-stu-id="a0c70-124">calendar</span></span>](../resources/calendar.md) | <span data-ttu-id="a0c70-125">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-125">Calendars.Read</span></span> | <span data-ttu-id="a0c70-126">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-126">Calendars.Read</span></span> | <span data-ttu-id="a0c70-127">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-127">Calendars.Read</span></span> |
| [<span data-ttu-id="a0c70-128">contact</span><span class="sxs-lookup"><span data-stu-id="a0c70-128">contact</span></span>](../resources/contact.md) | <span data-ttu-id="a0c70-129">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-129">Contacts.Read</span></span> | <span data-ttu-id="a0c70-130">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-130">Contacts.Read</span></span> | <span data-ttu-id="a0c70-131">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-131">Contacts.Read</span></span> |
| [<span data-ttu-id="a0c70-132">contactFolder</span><span class="sxs-lookup"><span data-stu-id="a0c70-132">contactFolder</span></span>](../resources/contactfolder.md) | <span data-ttu-id="a0c70-133">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-133">Contacts.Read</span></span> | <span data-ttu-id="a0c70-134">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-134">Contacts.Read</span></span> | <span data-ttu-id="a0c70-135">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-135">Contacts.Read</span></span> |
| [<span data-ttu-id="a0c70-136">event</span><span class="sxs-lookup"><span data-stu-id="a0c70-136">event</span></span>](../resources/event.md) | <span data-ttu-id="a0c70-137">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-137">Calendars.Read</span></span> | <span data-ttu-id="a0c70-138">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-138">Calendars.Read</span></span> |  <span data-ttu-id="a0c70-139">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-139">Calendars.Read</span></span>|
| <span data-ttu-id="a0c70-140">[calendar](../resources/calendar.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a0c70-140">group [calendar](../resources/calendar.md)</span></span> | <span data-ttu-id="a0c70-141">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a0c70-141">Group.Read.All</span></span> | <span data-ttu-id="a0c70-142">No admitido</span><span class="sxs-lookup"><span data-stu-id="a0c70-142">Not supported</span></span> | <span data-ttu-id="a0c70-143">No admitido</span><span class="sxs-lookup"><span data-stu-id="a0c70-143">Not supported</span></span> |
| <span data-ttu-id="a0c70-144">[event](../resources/event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a0c70-144">group [event](../resources/event.md)</span></span> | <span data-ttu-id="a0c70-145">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a0c70-145">Group.Read.All</span></span> | <span data-ttu-id="a0c70-146">No admitido</span><span class="sxs-lookup"><span data-stu-id="a0c70-146">Not supported</span></span> | <span data-ttu-id="a0c70-147">No admitido</span><span class="sxs-lookup"><span data-stu-id="a0c70-147">Not supported</span></span> |
| <span data-ttu-id="a0c70-148">[post](../resources/post.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="a0c70-148">group [post](../resources/post.md)</span></span> | <span data-ttu-id="a0c70-149">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a0c70-149">Group.Read.All</span></span> | <span data-ttu-id="a0c70-150">No admitido</span><span class="sxs-lookup"><span data-stu-id="a0c70-150">Not supported</span></span> | <span data-ttu-id="a0c70-151">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="a0c70-151">Group.Read.All</span></span> |
| [<span data-ttu-id="a0c70-152">mailFolder</span><span class="sxs-lookup"><span data-stu-id="a0c70-152">mailFolder</span></span>](../resources/mailfolder.md) | <span data-ttu-id="a0c70-153">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-153">Mail.Read</span></span> | <span data-ttu-id="a0c70-154">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-154">Mail.Read</span></span> | <span data-ttu-id="a0c70-155">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-155">Mail.Read</span></span> |
| [<span data-ttu-id="a0c70-156">message</span><span class="sxs-lookup"><span data-stu-id="a0c70-156">message</span></span>](../resources/message.md) | <span data-ttu-id="a0c70-157">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-157">Mail.Read</span></span> | <span data-ttu-id="a0c70-158">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-158">Mail.Read</span></span> | <span data-ttu-id="a0c70-159">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="a0c70-159">Mail.Read</span></span> |
 
## <a name="http-request"></a><span data-ttu-id="a0c70-160">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a0c70-160">HTTP request</span></span>

<span data-ttu-id="a0c70-p103">Expanda una instancia de recurso con la propiedad extendida que coincida con un filtro en la propiedad **id**. Asegúrese de aplicar la [codificación de direcciones URL](https://www.w3schools.com/tags/ref_urlencode.asp) a los caracteres de espacio de la cadena de filtro.</span><span class="sxs-lookup"><span data-stu-id="a0c70-p103">Get a resource instance expanded with the extended property which matches a filter on the **id** property. Make sure you apply [URL encoding](https://www.w3schools.com/tags/ref_urlencode.asp) to the space characters in the filter string.</span></span>

<span data-ttu-id="a0c70-163">Obtener una instancia de **mensaje** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a0c70-163">Get a **message** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/messages/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/messages/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /me/mailFolders/{id}/messages/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="a0c70-164">Obtener una instancia de **mailFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a0c70-164">Get a **mailFolder** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/mailFolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/mailFolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="a0c70-165">Obtener una instancia de **evento** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a0c70-165">Get an **event** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/events/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/events/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="a0c70-166">Obtener una instancia de **calendario** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a0c70-166">Get a **calendar** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/calendars/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/calendars/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="a0c70-167">Obtener una instancia de **ponerse en contacto con** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a0c70-167">Get a **contact** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/contacts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contacts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /me/contactFolders/{id}/contacts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}/contacts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="a0c70-168">Obtener una instancia de **contactFolder** :<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a0c70-168">Get a **contactFolder** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /me/contactfolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /users/{id|userPrincipalName}/contactFolders/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```
<span data-ttu-id="a0c70-169">Obtener una instancia de **evento** de grupo:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a0c70-169">Get a group **event** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /groups/{id}/events/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```

<span data-ttu-id="a0c70-170">Obtener una instancia de **entrada** de grupo:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="a0c70-170">Get a group **post** instance: <!-- { "blockType": "ignored" } --></span></span>
```http
GET /groups/{id}/threads/{id}/posts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}?$expand=multiValueExtendedProperties($filter=id eq '{id_value}')
```

## <a name="path-parameters"></a><span data-ttu-id="a0c70-171">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="a0c70-171">Path parameters</span></span>
|<span data-ttu-id="a0c70-172">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a0c70-172">Parameter</span></span>|<span data-ttu-id="a0c70-173">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0c70-173">Type</span></span>|<span data-ttu-id="a0c70-174">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0c70-174">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a0c70-175">id_value</span><span class="sxs-lookup"><span data-stu-id="a0c70-175">id_value</span></span>|<span data-ttu-id="a0c70-176">String</span><span class="sxs-lookup"><span data-stu-id="a0c70-176">String</span></span>|<span data-ttu-id="a0c70-p104">El identificador de la propiedad extendida que debe coincidir. Debe tener uno de los formatos compatibles. Consulte la [Información general de las propiedades extendidas de Outlook](../resources/extended-properties-overview.md) para obtener más información. Necesario.</span><span class="sxs-lookup"><span data-stu-id="a0c70-p104">The ID of the extended property to match. It must follow one of the supported formats. See [Outlook extended properties overview](../resources/extended-properties-overview.md) for more information. Required.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="a0c70-181">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a0c70-181">Request headers</span></span>
| <span data-ttu-id="a0c70-182">Nombre</span><span class="sxs-lookup"><span data-stu-id="a0c70-182">Name</span></span>      |<span data-ttu-id="a0c70-183">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0c70-183">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a0c70-184">Authorization</span><span class="sxs-lookup"><span data-stu-id="a0c70-184">Authorization</span></span>  | <span data-ttu-id="a0c70-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a0c70-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a0c70-187">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a0c70-187">Request body</span></span>
<span data-ttu-id="a0c70-188">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a0c70-188">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a0c70-189">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0c70-189">Response</span></span>

<span data-ttu-id="a0c70-190">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="a0c70-190">If successful, this method returns a `200 OK` response code.</span></span> 

<span data-ttu-id="a0c70-191">El cuerpo de la respuesta incluye un objeto que representa la instancia de recurso solicitada y expandida con el objeto coincidente [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a0c70-191">The response body includes an object representing the requested resource instance, expanded with the matching [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) object.</span></span>

## <a name="example"></a><span data-ttu-id="a0c70-192">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0c70-192">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a0c70-193">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a0c70-193">Request</span></span>
<span data-ttu-id="a0c70-p106">Este ejemplo obtiene y expande el evento especificado al incluir una propiedad extendida de varios valores. El filtro devuelve la propiedad extendida con un **id** que coincide con la cadena `StringArray {66f5a359-4659-4830-9070-00050ec6ac6e} Name Recreation` (la codificación de dirección URL se ha eliminado aquí para facilitar la lectura).</span><span class="sxs-lookup"><span data-stu-id="a0c70-p106">This example gets and expands the specified event by including a multi-value extended property. The filter returns the extended property that has its **id** matching the string `StringArray {66f5a359-4659-4830-9070-00050ec6ac6e} Name Recreation` (with URL encoding removed here for ease of reading).</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/events('AAMkAGE1M2_bs88AACbuFiiAAA=')?$expand=multiValueExtendedProperties($filter=id%20eq%20'StringArray%20{66f5a359-4659-4830-9070-00050ec6ac6e}%20Name%20Recreation')
```
##### <a name="response"></a><span data-ttu-id="a0c70-196">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0c70-196">Response</span></span>

<span data-ttu-id="a0c70-197">El cuerpo de la respuesta incluye todas las propiedades del evento especificado y devuelve la propiedad extendida del filtro.</span><span class="sxs-lookup"><span data-stu-id="a0c70-197">The response body includes all the properties of the specified event and extended property returned from the filter.</span></span>

<span data-ttu-id="a0c70-p107">Nota: El objeto **event** que aparece aquí está truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a0c70-p107">Note: The **event** object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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