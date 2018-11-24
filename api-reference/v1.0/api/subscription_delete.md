# <a name="delete-subscription"></a><span data-ttu-id="4e36a-101">Delete subscription</span><span class="sxs-lookup"><span data-stu-id="4e36a-101">Delete subscription</span></span>

<span data-ttu-id="4e36a-102">Elimina una suscripción.</span><span class="sxs-lookup"><span data-stu-id="4e36a-102">Delete a subscription.</span></span>

## <a name="permissions"></a><span data-ttu-id="4e36a-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="4e36a-103">Permissions</span></span>

<span data-ttu-id="4e36a-p101">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4e36a-p101">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="4e36a-106">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="4e36a-106">Resource type / Item</span></span>        | <span data-ttu-id="4e36a-107">Permiso</span><span class="sxs-lookup"><span data-stu-id="4e36a-107">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="4e36a-108">Contactos</span><span class="sxs-lookup"><span data-stu-id="4e36a-108">Contacts</span></span>                    | <span data-ttu-id="4e36a-109">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="4e36a-109">Contacts.Read</span></span>       |
| <span data-ttu-id="4e36a-110">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="4e36a-110">Conversations</span></span>               | <span data-ttu-id="4e36a-111">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="4e36a-111">Group.Read.All</span></span>      |
| <span data-ttu-id="4e36a-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="4e36a-112">Events</span></span>                      | <span data-ttu-id="4e36a-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="4e36a-113">Calendars.Read</span></span>      |
| <span data-ttu-id="4e36a-114">Mensajes</span><span class="sxs-lookup"><span data-stu-id="4e36a-114">Messages</span></span>                    | <span data-ttu-id="4e36a-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="4e36a-115">Mail.Read</span></span>           |
| <span data-ttu-id="4e36a-116">Groups</span><span class="sxs-lookup"><span data-stu-id="4e36a-116">Groups</span></span>                      | <span data-ttu-id="4e36a-117">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="4e36a-117">Group.Read.All</span></span>      |
| <span data-ttu-id="4e36a-118">Users</span><span class="sxs-lookup"><span data-stu-id="4e36a-118">Users</span></span>                       | <span data-ttu-id="4e36a-119">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="4e36a-119">User.Read.All</span></span>       |
| <span data-ttu-id="4e36a-120">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="4e36a-120">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="4e36a-121">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4e36a-121">Files.ReadWrite</span></span>     |
| <span data-ttu-id="4e36a-122">Unidades (contenido de SharePoint compartido y unidades)</span><span class="sxs-lookup"><span data-stu-id="4e36a-122">Drives (SharePoint shared content and drives)</span></span> | <span data-ttu-id="4e36a-123">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4e36a-123">Files.ReadWrite.All</span></span> |
|<span data-ttu-id="4e36a-124">Alerta de seguridad</span><span class="sxs-lookup"><span data-stu-id="4e36a-124">Security alert</span></span>| <span data-ttu-id="4e36a-125">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4e36a-125">SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4e36a-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4e36a-126">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /subscriptions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="4e36a-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4e36a-127">Request headers</span></span>

| <span data-ttu-id="4e36a-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="4e36a-128">Name</span></span>       | <span data-ttu-id="4e36a-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="4e36a-129">Type</span></span> | <span data-ttu-id="4e36a-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e36a-130">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="4e36a-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="4e36a-131">Authorization</span></span>  | <span data-ttu-id="4e36a-132">string</span><span class="sxs-lookup"><span data-stu-id="4e36a-132">string</span></span>  | <span data-ttu-id="4e36a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4e36a-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4e36a-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4e36a-135">Request body</span></span>

<span data-ttu-id="4e36a-136">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4e36a-136">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4e36a-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4e36a-137">Response</span></span>

<span data-ttu-id="4e36a-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="4e36a-138">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="4e36a-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4e36a-139">Example</span></span>

##### <a name="request"></a><span data-ttu-id="4e36a-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4e36a-140">Request</span></span>

<span data-ttu-id="4e36a-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4e36a-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_subscription"
}-->

```http
DELETE https://graph.microsoft.com/v1.0/subscriptions/{id}
```

##### <a name="response"></a><span data-ttu-id="4e36a-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4e36a-142">Response</span></span>

<span data-ttu-id="4e36a-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4e36a-143">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.subscription"
} -->

```http
HTTP/1.1 204 No Content
```

<!-- {
  "type": "#page.annotation",
  "description": "Delete subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
