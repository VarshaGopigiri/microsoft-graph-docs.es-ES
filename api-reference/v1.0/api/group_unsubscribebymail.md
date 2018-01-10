# <a name="group-unsubscribebymail"></a><span data-ttu-id="bc70f-101">group: unsubscribeByMail</span><span class="sxs-lookup"><span data-stu-id="bc70f-101">group: unsubscribeByMail</span></span>
<span data-ttu-id="bc70f-p101">La llamada a este método impedirá que el usuario actual reciba notificaciones por correo electrónico para este grupo, sobre nuevos eventos, publicaciones y archivos de ese grupo. Solo es compatible con Grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="bc70f-p101">Calling this method will prevent the current user from receiving email notifications for this group about new posts, events, and files in that group. Supported for only Office 365 groups.</span></span> 

## <a name="permissions"></a><span data-ttu-id="bc70f-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="bc70f-104">Permissions</span></span>
<span data-ttu-id="bc70f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bc70f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="bc70f-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bc70f-107">Permission type</span></span>      | <span data-ttu-id="bc70f-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bc70f-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bc70f-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bc70f-109">Delegated (work or school account)</span></span> | <span data-ttu-id="bc70f-110">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bc70f-110">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="bc70f-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bc70f-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bc70f-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc70f-112">Not supported.</span></span>    |
|<span data-ttu-id="bc70f-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bc70f-113">Application</span></span> | <span data-ttu-id="bc70f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc70f-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="bc70f-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bc70f-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/unsubscribeByMail
```
## <a name="request-headers"></a><span data-ttu-id="bc70f-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bc70f-116">Request headers</span></span>
| <span data-ttu-id="bc70f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc70f-117">Header</span></span>       | <span data-ttu-id="bc70f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bc70f-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="bc70f-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="bc70f-119">Authorization</span></span>  | <span data-ttu-id="bc70f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bc70f-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="bc70f-122">Prefer</span><span class="sxs-lookup"><span data-stu-id="bc70f-122">Prefer</span></span> | <span data-ttu-id="bc70f-123">return=minimal.</span><span class="sxs-lookup"><span data-stu-id="bc70f-123">return=minimal.</span></span> <span data-ttu-id="bc70f-124">Si el encabezado de respuesta “mínimo” se incluye en el encabezado de solicitud, una respuesta correcta devolverá un código `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="bc70f-124">If minimal response header is included in the request header, then a successful response returns `204 No Content` code.</span></span> <span data-ttu-id="bc70f-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bc70f-125">Optional.</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="bc70f-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bc70f-126">Request body</span></span>
<span data-ttu-id="bc70f-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bc70f-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bc70f-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc70f-128">Response</span></span>
<span data-ttu-id="bc70f-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc70f-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bc70f-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bc70f-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="bc70f-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bc70f-132">Request</span></span>
<span data-ttu-id="bc70f-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bc70f-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_unsubscribebymail"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/unsubscribeByMail
```

#### <a name="response"></a><span data-ttu-id="bc70f-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc70f-134">Response</span></span>
<span data-ttu-id="bc70f-135">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc70f-135">The following is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: unsubscribeByMail",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
