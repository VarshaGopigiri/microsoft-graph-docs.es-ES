# <a name="get-subscription"></a><span data-ttu-id="0e99a-101">Get subscription</span><span class="sxs-lookup"><span data-stu-id="0e99a-101">Get subscription</span></span>

<span data-ttu-id="0e99a-102">Recupera las propiedades y relaciones de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="0e99a-102">Retrieve the properties and relationships of a subscription.</span></span>

## <a name="permissions"></a><span data-ttu-id="0e99a-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="0e99a-103">Permissions</span></span>

<span data-ttu-id="0e99a-p101">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0e99a-p101">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="0e99a-106">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="0e99a-106">Resource type / Item</span></span>        | <span data-ttu-id="0e99a-107">Permiso</span><span class="sxs-lookup"><span data-stu-id="0e99a-107">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="0e99a-108">Contactos</span><span class="sxs-lookup"><span data-stu-id="0e99a-108">Contacts</span></span>                    | <span data-ttu-id="0e99a-109">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="0e99a-109">Contacts.Read</span></span>       |
| <span data-ttu-id="0e99a-110">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="0e99a-110">Conversations</span></span>               | <span data-ttu-id="0e99a-111">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="0e99a-111">Group.Read.All</span></span>      |
| <span data-ttu-id="0e99a-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="0e99a-112">Events</span></span>                      | <span data-ttu-id="0e99a-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="0e99a-113">Calendars.Read</span></span>      |
| <span data-ttu-id="0e99a-114">Mensajes</span><span class="sxs-lookup"><span data-stu-id="0e99a-114">Messages</span></span>                    | <span data-ttu-id="0e99a-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="0e99a-115">Mail.Read</span></span>           |
| <span data-ttu-id="0e99a-116">Groups</span><span class="sxs-lookup"><span data-stu-id="0e99a-116">Groups</span></span>                      | <span data-ttu-id="0e99a-117">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="0e99a-117">Group.Read.All</span></span>      |
| <span data-ttu-id="0e99a-118">Users</span><span class="sxs-lookup"><span data-stu-id="0e99a-118">Users</span></span>                       | <span data-ttu-id="0e99a-119">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="0e99a-119">User.Read.All</span></span>       |
| <span data-ttu-id="0e99a-120">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="0e99a-120">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="0e99a-121">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0e99a-121">Files.ReadWrite</span></span>     |
| <span data-ttu-id="0e99a-122">Unidades (contenido de SharePoint compartido y unidades)</span><span class="sxs-lookup"><span data-stu-id="0e99a-122">Drives (SharePoint shared content and drives)</span></span> | <span data-ttu-id="0e99a-123">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0e99a-123">Files.ReadWrite.All</span></span> |
|<span data-ttu-id="0e99a-124">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="0e99a-124">Security alert</span></span>| <span data-ttu-id="0e99a-125">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0e99a-125">SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0e99a-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0e99a-126">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /subscriptions/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="0e99a-127">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0e99a-127">Optional query parameters</span></span>

<span data-ttu-id="0e99a-128">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e99a-128">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0e99a-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0e99a-129">Request headers</span></span>

| <span data-ttu-id="0e99a-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="0e99a-130">Name</span></span>       | <span data-ttu-id="0e99a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e99a-131">Type</span></span> | <span data-ttu-id="0e99a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e99a-132">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="0e99a-133">Authorization</span><span class="sxs-lookup"><span data-stu-id="0e99a-133">Authorization</span></span>  | <span data-ttu-id="0e99a-134">string</span><span class="sxs-lookup"><span data-stu-id="0e99a-134">string</span></span>  | <span data-ttu-id="0e99a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0e99a-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0e99a-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0e99a-137">Request body</span></span>

<span data-ttu-id="0e99a-138">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0e99a-138">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0e99a-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e99a-139">Response</span></span>

<span data-ttu-id="0e99a-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [subscription](../resources/subscription.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e99a-140">If successful, this method returns a `200 OK` response code and [subscription](../resources/subscription.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0e99a-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e99a-141">Example</span></span>

##### <a name="request"></a><span data-ttu-id="0e99a-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0e99a-142">Request</span></span>

<span data-ttu-id="0e99a-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0e99a-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_subscription"
}-->

```http
GET https://graph.microsoft.com/v1.0/subscriptions/{id}
```

##### <a name="response"></a><span data-ttu-id="0e99a-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e99a-144">Response</span></span>

<span data-ttu-id="0e99a-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e99a-145">Here is an example of the response.</span></span>
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
