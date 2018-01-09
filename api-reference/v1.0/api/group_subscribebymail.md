# <a name="group-subscribebymail"></a><span data-ttu-id="bc7ab-101">group: subscribeByMail</span><span class="sxs-lookup"><span data-stu-id="bc7ab-101">group: subscribeByMail</span></span>

<span data-ttu-id="bc7ab-p101">La llamada a este método permitirá al usuario actual recibir notificaciones por correo electrónico de este grupo sobre nuevos eventos, publicaciones y archivos. Solo es compatible con Grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-p101">Calling this method will enable the current user to receive email notifications for this group, about new posts, events, and files in that group. Supported for only Office 365 groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="bc7ab-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="bc7ab-104">Permissions</span></span>
<span data-ttu-id="bc7ab-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bc7ab-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="bc7ab-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bc7ab-107">Permission type</span></span>      | <span data-ttu-id="bc7ab-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bc7ab-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bc7ab-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bc7ab-109">Delegated (work or school account)</span></span> | <span data-ttu-id="bc7ab-110">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bc7ab-110">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="bc7ab-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bc7ab-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bc7ab-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-112">Not supported.</span></span>    |
|<span data-ttu-id="bc7ab-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bc7ab-113">Application</span></span> | <span data-ttu-id="bc7ab-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="bc7ab-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bc7ab-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/subscribeByMail
```
## <a name="request-headers"></a><span data-ttu-id="bc7ab-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bc7ab-116">Request headers</span></span>
| <span data-ttu-id="bc7ab-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc7ab-117">Header</span></span>       | <span data-ttu-id="bc7ab-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bc7ab-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="bc7ab-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="bc7ab-119">Authorization</span></span>  | <span data-ttu-id="bc7ab-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="bc7ab-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bc7ab-122">Request body</span></span>
<span data-ttu-id="bc7ab-123">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-123">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bc7ab-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc7ab-124">Response</span></span>
<span data-ttu-id="bc7ab-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bc7ab-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bc7ab-127">Example</span></span>
<span data-ttu-id="bc7ab-128">Este es un ejemplo de cómo realizar una llamada a esta API.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-128">Here is an example of how to call this API.</span></span>

#### <a name="request"></a><span data-ttu-id="bc7ab-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bc7ab-129">Request</span></span>
<span data-ttu-id="bc7ab-130">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-130">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>
<!-- {
  "blockType": "request",
  "name": "group_subscribebymail"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/subscribeByMail
```

#### <a name="response"></a><span data-ttu-id="bc7ab-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc7ab-131">Response</span></span>
<span data-ttu-id="bc7ab-132">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc7ab-132">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: subscribeByMail",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->