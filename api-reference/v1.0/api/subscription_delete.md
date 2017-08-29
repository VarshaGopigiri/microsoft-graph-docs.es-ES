# <a name="delete-subscription"></a><span data-ttu-id="2343e-101">Delete subscription</span><span class="sxs-lookup"><span data-stu-id="2343e-101">Delete subscription</span></span>

<span data-ttu-id="2343e-102">Elimina una suscripción.</span><span class="sxs-lookup"><span data-stu-id="2343e-102">Delete a subscription.</span></span>

## <a name="permissions"></a><span data-ttu-id="2343e-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="2343e-103">Permissions</span></span>

<span data-ttu-id="2343e-p101">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2343e-p101">The following table lists the suggested permission needed for each resource. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="2343e-106">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="2343e-106">Resource type / Item</span></span>        | <span data-ttu-id="2343e-107">Permiso</span><span class="sxs-lookup"><span data-stu-id="2343e-107">Permission</span></span>          |
|-----------------------------|---------------------|
| <span data-ttu-id="2343e-108">Contactos</span><span class="sxs-lookup"><span data-stu-id="2343e-108">Contacts</span></span>                    | <span data-ttu-id="2343e-109">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="2343e-109">Contacts.Read</span></span>       |
| <span data-ttu-id="2343e-110">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="2343e-110">Conversations</span></span>               | <span data-ttu-id="2343e-111">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="2343e-111">Group.Read.All</span></span>      |
| <span data-ttu-id="2343e-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="2343e-112">Events</span></span>                      | <span data-ttu-id="2343e-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="2343e-113">Calendars.Read</span></span>      |
| <span data-ttu-id="2343e-114">Mensajes</span><span class="sxs-lookup"><span data-stu-id="2343e-114">Messages</span></span>                    | <span data-ttu-id="2343e-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="2343e-115">Mail.Read</span></span>           |
| <span data-ttu-id="2343e-116">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="2343e-116">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="2343e-117">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2343e-117">Files.ReadWrite</span></span>     |
| <span data-ttu-id="2343e-118">Unidades de disco (unidades de disco y contenido compartido de SharePoint)</span><span class="sxs-lookup"><span data-stu-id="2343e-118">Drives (Sharepoint shared content and drives)</span></span> | <span data-ttu-id="2343e-119">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2343e-119">Files.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2343e-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2343e-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /subscriptions/{subscriptionId}
```
## <a name="request-headers"></a><span data-ttu-id="2343e-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2343e-121">Request headers</span></span>
| <span data-ttu-id="2343e-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="2343e-122">Name</span></span>       | <span data-ttu-id="2343e-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="2343e-123">Type</span></span> | <span data-ttu-id="2343e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="2343e-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="2343e-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="2343e-125">Authorization</span></span>  | <span data-ttu-id="2343e-126">string</span><span class="sxs-lookup"><span data-stu-id="2343e-126">string</span></span>  | <span data-ttu-id="2343e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2343e-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2343e-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2343e-129">Request body</span></span>
<span data-ttu-id="2343e-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2343e-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2343e-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2343e-131">Response</span></span>

<span data-ttu-id="2343e-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="2343e-132">If successful, this method returns a `204 No Content` response code.</span></span>
## <a name="example"></a><span data-ttu-id="2343e-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2343e-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2343e-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2343e-134">Request</span></span>
<span data-ttu-id="2343e-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2343e-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_subscription"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/subscriptions/{subscriptionId}
```
##### <a name="response"></a><span data-ttu-id="2343e-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2343e-136">Response</span></span>
<span data-ttu-id="2343e-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2343e-137">Here is an example of the response.</span></span>
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
