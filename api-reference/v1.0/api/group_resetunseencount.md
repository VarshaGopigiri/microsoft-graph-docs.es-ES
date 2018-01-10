# <a name="group-resetunseencount"></a><span data-ttu-id="b32dd-101">group: resetUnseenCount</span><span class="sxs-lookup"><span data-stu-id="b32dd-101">group: resetUnseenCount</span></span>
<span data-ttu-id="b32dd-p101">Restablece el valor de unseenCount de todas las publicaciones que el usuario actual no vio desde su última visita. Solo es compatible con Grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="b32dd-p101">Reset the unseenCount of all the posts that the current user has not seen since their last visit. Supported for only Office 365 groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="b32dd-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="b32dd-104">Permissions</span></span>
<span data-ttu-id="b32dd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b32dd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b32dd-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b32dd-107">Permission type</span></span>      | <span data-ttu-id="b32dd-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b32dd-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b32dd-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b32dd-109">Delegated (work or school account)</span></span> | <span data-ttu-id="b32dd-110">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b32dd-110">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="b32dd-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b32dd-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b32dd-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b32dd-112">Not supported.</span></span>    |
|<span data-ttu-id="b32dd-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b32dd-113">Application</span></span> | <span data-ttu-id="b32dd-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b32dd-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b32dd-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b32dd-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/resetUnseenCount
```
## <a name="request-headers"></a><span data-ttu-id="b32dd-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b32dd-116">Request headers</span></span>
| <span data-ttu-id="b32dd-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b32dd-117">Header</span></span>       | <span data-ttu-id="b32dd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b32dd-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b32dd-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="b32dd-119">Authorization</span></span>  | <span data-ttu-id="b32dd-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b32dd-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="b32dd-122">Prefer</span><span class="sxs-lookup"><span data-stu-id="b32dd-122">Prefer</span></span> | <span data-ttu-id="b32dd-123">return=minimal.</span><span class="sxs-lookup"><span data-stu-id="b32dd-123">return=minimal.</span></span> <span data-ttu-id="b32dd-124">Si el encabezado de respuesta “mínimo” se incluye en el encabezado de solicitud, una respuesta correcta devolverá un código `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="b32dd-124">If minimal response header is included in the request header, then a successful response returns `204 No Content` code.</span></span> <span data-ttu-id="b32dd-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b32dd-125">Optional.</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="b32dd-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b32dd-126">Request body</span></span>
<span data-ttu-id="b32dd-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b32dd-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b32dd-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b32dd-128">Response</span></span>
<span data-ttu-id="b32dd-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b32dd-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b32dd-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b32dd-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="b32dd-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b32dd-132">Request</span></span>
<span data-ttu-id="b32dd-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b32dd-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_resetunseencount"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/resetUnseenCount
```

#### <a name="response"></a><span data-ttu-id="b32dd-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b32dd-134">Response</span></span>
<span data-ttu-id="b32dd-135">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b32dd-135">The following is an example of the response.</span></span> 
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
  "description": "group: resetUnseenCount",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
