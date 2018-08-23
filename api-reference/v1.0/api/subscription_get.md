# <a name="get-subscription"></a><span data-ttu-id="18b28-101">Obtener suscripción</span><span class="sxs-lookup"><span data-stu-id="18b28-101">Get subscription</span></span>

<span data-ttu-id="18b28-102">Recupera las propiedades y relaciones de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="18b28-102">Retrieve the properties and relationships of a subscription.</span></span>

## <a name="permissions"></a><span data-ttu-id="18b28-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="18b28-103">Permissions</span></span>

<span data-ttu-id="18b28-p101">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="18b28-p101">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="18b28-106">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="18b28-106">Resource type / Item</span></span>        | <span data-ttu-id="18b28-107">Permiso</span><span class="sxs-lookup"><span data-stu-id="18b28-107">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="18b28-108">Contactos</span><span class="sxs-lookup"><span data-stu-id="18b28-108">Contacts</span></span>                    | <span data-ttu-id="18b28-109">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="18b28-109">Contacts.Read</span></span>       |
| <span data-ttu-id="18b28-110">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="18b28-110">Conversations</span></span>               | <span data-ttu-id="18b28-111">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="18b28-111">Group.Read.All</span></span>      |
| <span data-ttu-id="18b28-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="18b28-112">Events</span></span>                      | <span data-ttu-id="18b28-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="18b28-113">Calendars.Read</span></span>      |
| <span data-ttu-id="18b28-114">Mensajes</span><span class="sxs-lookup"><span data-stu-id="18b28-114">Messages</span></span>                    | <span data-ttu-id="18b28-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="18b28-115">Mail.Read</span></span>           |
| <span data-ttu-id="18b28-116">Grupos</span><span class="sxs-lookup"><span data-stu-id="18b28-116">Groups</span></span>                      | <span data-ttu-id="18b28-117">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="18b28-117">Group.Read.All</span></span>      |
| <span data-ttu-id="18b28-118">Usuarios</span><span class="sxs-lookup"><span data-stu-id="18b28-118">Users</span></span>                       | <span data-ttu-id="18b28-119">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="18b28-119">User.Read.All</span></span>       |
| <span data-ttu-id="18b28-120">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="18b28-120">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="18b28-121">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="18b28-121">Files.ReadWrite</span></span>     |
| <span data-ttu-id="18b28-122">Unidades de disco (unidades de disco y contenido compartido de SharePoint)</span><span class="sxs-lookup"><span data-stu-id="18b28-122">Drives (Sharepoint shared content and drives)</span></span> | <span data-ttu-id="18b28-123">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="18b28-123">Files.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="18b28-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="18b28-124">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /subscriptions/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="18b28-125">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="18b28-125">Optional query parameters</span></span>

<span data-ttu-id="18b28-126">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18b28-126">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="18b28-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="18b28-127">Request headers</span></span>

| <span data-ttu-id="18b28-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="18b28-128">Name</span></span>       | <span data-ttu-id="18b28-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="18b28-129">Type</span></span> | <span data-ttu-id="18b28-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="18b28-130">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="18b28-131">Autorización</span><span class="sxs-lookup"><span data-stu-id="18b28-131">Authorization</span></span>  | <span data-ttu-id="18b28-132">cadena</span><span class="sxs-lookup"><span data-stu-id="18b28-132">string</span></span>  | <span data-ttu-id="18b28-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18b28-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="18b28-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="18b28-135">Request body</span></span>

<span data-ttu-id="18b28-136">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="18b28-136">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="18b28-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18b28-137">Response</span></span>

<span data-ttu-id="18b28-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18b28-138">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="18b28-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="18b28-139">Example</span></span>

##### <a name="request"></a><span data-ttu-id="18b28-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="18b28-140">Request</span></span>

<span data-ttu-id="18b28-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18b28-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_subscription"
}-->

```http
GET https://graph.microsoft.com/v1.0/subscriptions/{id}
```

##### <a name="response"></a><span data-ttu-id="18b28-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18b28-142">Response</span></span>

<span data-ttu-id="18b28-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18b28-143">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.subscription"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 252

{
  "id":"7f105c7d-2dc5-4530-97cd-4e7ae6534c07",
  "resource":"me/messages",
  "applicationId" : "string",
  "changeType":"created,updated",
  "clientState":"secretClientValue",
  "notificationUrl":"https://webhook.azurewebsites.net/api/send/myNotifyClient",
  "expirationDateTime":"2016-11-20T18:23:45.9356913Z",
  "creatorId": "string"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
