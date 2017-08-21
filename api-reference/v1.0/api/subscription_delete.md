# <a name="delete-subscription"></a><span data-ttu-id="f2fab-101">Delete subscription</span><span class="sxs-lookup"><span data-stu-id="f2fab-101">Delete subscription</span></span>

<span data-ttu-id="f2fab-102">Elimina una suscripción.</span><span class="sxs-lookup"><span data-stu-id="f2fab-102">Delete a subscription.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f2fab-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f2fab-103">Prerequisites</span></span>

<span data-ttu-id="f2fab-104">En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso.</span><span class="sxs-lookup"><span data-stu-id="f2fab-104">The following table lists the suggested permission needed for each resource.</span></span>

| <span data-ttu-id="f2fab-105">Tipo de recurso o elemento</span><span class="sxs-lookup"><span data-stu-id="f2fab-105">Resource type / Item</span></span>        | <span data-ttu-id="f2fab-106">Ámbito</span><span class="sxs-lookup"><span data-stu-id="f2fab-106">Scope</span></span>               |
|-----------------------------|---------------------|
| <span data-ttu-id="f2fab-107">Contactos</span><span class="sxs-lookup"><span data-stu-id="f2fab-107">Contacts</span></span>                    | <span data-ttu-id="f2fab-108">Contacts.Read</span><span class="sxs-lookup"><span data-stu-id="f2fab-108">Contacts.Read</span></span>       |
| <span data-ttu-id="f2fab-109">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="f2fab-109">Conversations</span></span>               | <span data-ttu-id="f2fab-110">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="f2fab-110">Group.Read.All</span></span>      |
| <span data-ttu-id="f2fab-111">Eventos</span><span class="sxs-lookup"><span data-stu-id="f2fab-111">Events</span></span>                      | <span data-ttu-id="f2fab-112">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="f2fab-112">Calendars.Read</span></span>      |
| <span data-ttu-id="f2fab-113">Mensajes</span><span class="sxs-lookup"><span data-stu-id="f2fab-113">Messages</span></span>                    | <span data-ttu-id="f2fab-114">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="f2fab-114">Mail.Read</span></span>           |
| <span data-ttu-id="f2fab-115">Unidad de disco (OneDrive del usuario)</span><span class="sxs-lookup"><span data-stu-id="f2fab-115">Drive  (User's OneDrive)</span></span>    | <span data-ttu-id="f2fab-116">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f2fab-116">Files.ReadWrite</span></span>     |
| <span data-ttu-id="f2fab-117">Unidades de disco (unidades de disco y contenido compartido de SharePoint)</span><span class="sxs-lookup"><span data-stu-id="f2fab-117">Drives (Sharepoint shared content and drives)</span></span> | <span data-ttu-id="f2fab-118">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f2fab-118">Files.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f2fab-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f2fab-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /subscriptions/{subscriptionId}
```
## <a name="request-headers"></a><span data-ttu-id="f2fab-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f2fab-120">Request headers</span></span>
| <span data-ttu-id="f2fab-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="f2fab-121">Name</span></span>       | <span data-ttu-id="f2fab-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="f2fab-122">Type</span></span> | <span data-ttu-id="f2fab-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2fab-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="f2fab-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="f2fab-124">Authorization</span></span>  | <span data-ttu-id="f2fab-125">string</span><span class="sxs-lookup"><span data-stu-id="f2fab-125">string</span></span>  | <span data-ttu-id="f2fab-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f2fab-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f2fab-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f2fab-128">Request body</span></span>
<span data-ttu-id="f2fab-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f2fab-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f2fab-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f2fab-130">Response</span></span>

<span data-ttu-id="f2fab-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="f2fab-131">If successful, this method returns a `204 No Content` response code.</span></span>
## <a name="example"></a><span data-ttu-id="f2fab-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f2fab-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f2fab-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f2fab-133">Request</span></span>
<span data-ttu-id="f2fab-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f2fab-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_subscription"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/subscriptions/{subscriptionId}
```
##### <a name="response"></a><span data-ttu-id="f2fab-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f2fab-135">Response</span></span>
<span data-ttu-id="f2fab-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f2fab-136">Here is an example of the response.</span></span>
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
