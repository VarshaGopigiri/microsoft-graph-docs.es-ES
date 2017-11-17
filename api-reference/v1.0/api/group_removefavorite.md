# <a name="group-removefavorite"></a><span data-ttu-id="a1af7-101">group: removeFavorite</span><span class="sxs-lookup"><span data-stu-id="a1af7-101">group: removeFavorite</span></span>
<span data-ttu-id="a1af7-p101">Quita el grupo de la lista de grupos favoritos del usuario actual. Compatible solo con grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="a1af7-p101">Remove the group from the list of the current user's favorite groups. Supported for only Office 365 groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="a1af7-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="a1af7-104">Permissions</span></span>
<span data-ttu-id="a1af7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a1af7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a1af7-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a1af7-107">Permission type</span></span>      | <span data-ttu-id="a1af7-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a1af7-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a1af7-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a1af7-109">Delegated (work or school account)</span></span> | <span data-ttu-id="a1af7-110">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a1af7-110">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="a1af7-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a1af7-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a1af7-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a1af7-112">Not supported.</span></span>    |
|<span data-ttu-id="a1af7-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a1af7-113">Application</span></span> | <span data-ttu-id="a1af7-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a1af7-114">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a1af7-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a1af7-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/removeFavorite
```
## <a name="request-headers"></a><span data-ttu-id="a1af7-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a1af7-116">Request headers</span></span>
| <span data-ttu-id="a1af7-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1af7-117">Header</span></span>       | <span data-ttu-id="a1af7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a1af7-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a1af7-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="a1af7-119">Authorization</span></span>  | <span data-ttu-id="a1af7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a1af7-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a1af7-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a1af7-122">Request body</span></span>
<span data-ttu-id="a1af7-123">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a1af7-123">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a1af7-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1af7-124">Response</span></span>

<span data-ttu-id="a1af7-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a1af7-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a1af7-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a1af7-127">Example</span></span>
<span data-ttu-id="a1af7-128">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a1af7-128">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="a1af7-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a1af7-129">Request</span></span>
<span data-ttu-id="a1af7-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a1af7-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_removefavorite"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/removeFavorite
```

##### <a name="response"></a><span data-ttu-id="a1af7-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1af7-131">Response</span></span>
<span data-ttu-id="a1af7-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a1af7-132">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: removeFavorite",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->