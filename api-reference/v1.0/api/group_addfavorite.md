# <a name="group-addfavorite"></a><span data-ttu-id="68251-101">group: addFavorite</span><span class="sxs-lookup"><span data-stu-id="68251-101">group: addFavorite</span></span>
<span data-ttu-id="68251-p101">Agrega el grupo a la lista de grupos favoritos del usuario actual. Compatible solo con grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="68251-p101">Add the group to the list of the current user's favorite groups. Supported for only Office 365 groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="68251-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="68251-104">Permissions</span></span>
<span data-ttu-id="68251-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="68251-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="68251-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="68251-107">Permission type</span></span>      | <span data-ttu-id="68251-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="68251-108">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="68251-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="68251-109">Delegated (work or school account)</span></span> | <span data-ttu-id="68251-110">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="68251-110">Group.ReadWrite.All</span></span>    | 
|<span data-ttu-id="68251-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="68251-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="68251-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="68251-112">Not supported.</span></span>    | 
|<span data-ttu-id="68251-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="68251-113">Application</span></span> | <span data-ttu-id="68251-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="68251-114">Group.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="68251-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="68251-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/addFavorite
```
## <a name="request-headers"></a><span data-ttu-id="68251-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="68251-116">Request headers</span></span>
| <span data-ttu-id="68251-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68251-117">Header</span></span>       | <span data-ttu-id="68251-118">Valor</span><span class="sxs-lookup"><span data-stu-id="68251-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="68251-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="68251-119">Authorization</span></span>  | <span data-ttu-id="68251-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="68251-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="68251-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="68251-122">Request body</span></span>
<span data-ttu-id="68251-123">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="68251-123">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="68251-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68251-124">Response</span></span>

<span data-ttu-id="68251-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68251-p104">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="68251-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="68251-127">Example</span></span>
<span data-ttu-id="68251-128">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="68251-128">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="68251-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="68251-129">Request</span></span>
<span data-ttu-id="68251-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="68251-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_addfavorite"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/addFavorite
```

##### <a name="response"></a><span data-ttu-id="68251-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68251-131">Response</span></span>
<span data-ttu-id="68251-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68251-132">Here is an example of the response.</span></span>
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
  "description": "group: addFavorite",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->