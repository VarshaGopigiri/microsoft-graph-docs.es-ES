# <a name="group-addfavorite"></a><span data-ttu-id="59588-101">group: addFavorite</span><span class="sxs-lookup"><span data-stu-id="59588-101">group: addFavorite</span></span>
<span data-ttu-id="59588-p101">Agrega el grupo a la lista de grupos favoritos del usuario actual. Solo es compatible con Grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="59588-p101">Add the group to the list of the current user's favorite groups. Supported for Office 365 groups only.</span></span>

## <a name="permissions"></a><span data-ttu-id="59588-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="59588-104">Permissions</span></span>
<span data-ttu-id="59588-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="59588-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="59588-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="59588-107">Permission type</span></span>      | <span data-ttu-id="59588-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="59588-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="59588-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="59588-109">Delegated (work or school account)</span></span> | <span data-ttu-id="59588-110">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="59588-110">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="59588-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="59588-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="59588-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="59588-112">Not supported.</span></span>    |
|<span data-ttu-id="59588-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="59588-113">Application</span></span> | <span data-ttu-id="59588-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="59588-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="59588-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="59588-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/addFavorite
```

## <a name="request-headers"></a><span data-ttu-id="59588-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="59588-116">Request headers</span></span>
| <span data-ttu-id="59588-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59588-117">Header</span></span>       | <span data-ttu-id="59588-118">Valor</span><span class="sxs-lookup"><span data-stu-id="59588-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="59588-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="59588-119">Authorization</span></span>  | <span data-ttu-id="59588-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="59588-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="59588-122">Prefer</span><span class="sxs-lookup"><span data-stu-id="59588-122">Prefer</span></span> | <span data-ttu-id="59588-123">return=minimal.</span><span class="sxs-lookup"><span data-stu-id="59588-123">return=minimal.</span></span> <span data-ttu-id="59588-124">Si el encabezado de respuesta “mínimo” se incluye en el encabezado de solicitud, una respuesta correcta devolverá un código `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="59588-124">If minimal response header is included in the request header, then a successful response returns `204 No Content` code.</span></span> <span data-ttu-id="59588-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="59588-125">Optional.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="59588-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="59588-126">Request body</span></span>
<span data-ttu-id="59588-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="59588-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="59588-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59588-128">Response</span></span>
<span data-ttu-id="59588-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="59588-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="59588-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="59588-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="59588-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="59588-132">Request</span></span>
<span data-ttu-id="59588-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="59588-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_addfavorite"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/addFavorite
```

#### <a name="response"></a><span data-ttu-id="59588-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59588-134">Response</span></span>
<span data-ttu-id="59588-135">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="59588-135">The following is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: addFavorite",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
