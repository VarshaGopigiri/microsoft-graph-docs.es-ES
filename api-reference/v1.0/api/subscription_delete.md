# <a name="delete-subscription"></a><span data-ttu-id="57cf2-101">Delete subscription</span><span class="sxs-lookup"><span data-stu-id="57cf2-101">Delete subscription</span></span>

<span data-ttu-id="57cf2-102">Elimina una suscripción.</span><span class="sxs-lookup"><span data-stu-id="57cf2-102">Delete a subscription.</span></span>

## <a name="permissions"></a><span data-ttu-id="57cf2-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="57cf2-103">Permissions</span></span>

<span data-ttu-id="57cf2-p101">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="57cf2-p101">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="57cf2-106">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="57cf2-106">Resource type / Item</span></span>        | <span data-ttu-id="57cf2-107">Permiso</span><span class="sxs-lookup"><span data-stu-id="57cf2-107">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="57cf2-108">Contactos</span><span class="sxs-lookup"><span data-stu-id="57cf2-108">Contacts</span></span>                    | <span data-ttu-id="57cf2-109">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="57cf2-109">Contacts.Read</span></span>       |
| <span data-ttu-id="57cf2-110">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="57cf2-110">Conversations</span></span>               | <span data-ttu-id="57cf2-111">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="57cf2-111">Group.Read.All</span></span>      |
| <span data-ttu-id="57cf2-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="57cf2-112">Events</span></span>                      | <span data-ttu-id="57cf2-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="57cf2-113">Calendars.Read</span></span>      |
| <span data-ttu-id="57cf2-114">Mensajes</span><span class="sxs-lookup"><span data-stu-id="57cf2-114">Messages</span></span>                    | <span data-ttu-id="57cf2-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="57cf2-115">Mail.Read</span></span>           |
| <span data-ttu-id="57cf2-116">Grupos</span><span class="sxs-lookup"><span data-stu-id="57cf2-116">Groups</span></span>                      | <span data-ttu-id="57cf2-117">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="57cf2-117">Group.Read.All</span></span>      |
| <span data-ttu-id="57cf2-118">Usuarios</span><span class="sxs-lookup"><span data-stu-id="57cf2-118">Users</span></span>                       | <span data-ttu-id="57cf2-119">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="57cf2-119">User.Read.All</span></span>       |
| <span data-ttu-id="57cf2-120">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="57cf2-120">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="57cf2-121">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="57cf2-121">Files.ReadWrite</span></span>     |
| <span data-ttu-id="57cf2-122">Unidades de disco (unidades de disco y contenido compartido de SharePoint)</span><span class="sxs-lookup"><span data-stu-id="57cf2-122">Drives (Sharepoint shared content and drives)</span></span> | <span data-ttu-id="57cf2-123">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="57cf2-123">Files.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="57cf2-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="57cf2-124">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /subscriptions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="57cf2-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="57cf2-125">Request headers</span></span>

| <span data-ttu-id="57cf2-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="57cf2-126">Name</span></span>       | <span data-ttu-id="57cf2-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="57cf2-127">Type</span></span> | <span data-ttu-id="57cf2-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="57cf2-128">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="57cf2-129">Autorización</span><span class="sxs-lookup"><span data-stu-id="57cf2-129">Authorization</span></span>  | <span data-ttu-id="57cf2-130">cadena</span><span class="sxs-lookup"><span data-stu-id="57cf2-130">string</span></span>  | <span data-ttu-id="57cf2-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="57cf2-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="57cf2-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="57cf2-133">Request body</span></span>

<span data-ttu-id="57cf2-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="57cf2-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="57cf2-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="57cf2-135">Response</span></span>

<span data-ttu-id="57cf2-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="57cf2-136">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="57cf2-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="57cf2-137">Example</span></span>

##### <a name="request"></a><span data-ttu-id="57cf2-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="57cf2-138">Request</span></span>

<span data-ttu-id="57cf2-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="57cf2-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_subscription"
}-->

```http
DELETE https://graph.microsoft.com/v1.0/subscriptions/{id}
```

##### <a name="response"></a><span data-ttu-id="57cf2-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="57cf2-140">Response</span></span>

<span data-ttu-id="57cf2-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="57cf2-141">Here is an example of the response.</span></span>
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
