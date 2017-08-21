# <a name="group-addfavorite"></a><span data-ttu-id="cc986-101">group: addFavorite</span><span class="sxs-lookup"><span data-stu-id="cc986-101">group: addFavorite</span></span>
<span data-ttu-id="cc986-p101">Agrega el grupo a la lista de grupos favoritos del usuario actual. Compatible solo con grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="cc986-p101">Add the group to the list of the current user's favorite groups. Supported for only Office 365 groups.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cc986-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cc986-104">Prerequisites</span></span>
<span data-ttu-id="cc986-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="cc986-105">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="cc986-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cc986-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/addFavorite
```
## <a name="request-headers"></a><span data-ttu-id="cc986-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cc986-107">Request headers</span></span>
| <span data-ttu-id="cc986-108">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc986-108">Header</span></span>       | <span data-ttu-id="cc986-109">Valor</span><span class="sxs-lookup"><span data-stu-id="cc986-109">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="cc986-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="cc986-110">Authorization</span></span>  | <span data-ttu-id="cc986-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cc986-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="cc986-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cc986-113">Request body</span></span>
<span data-ttu-id="cc986-114">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cc986-114">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cc986-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc986-115">Response</span></span>

<span data-ttu-id="cc986-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc986-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cc986-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cc986-118">Example</span></span>
<span data-ttu-id="cc986-119">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="cc986-119">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="cc986-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cc986-120">Request</span></span>
<span data-ttu-id="cc986-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cc986-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_addfavorite"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/addFavorite
```

##### <a name="response"></a><span data-ttu-id="cc986-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc986-122">Response</span></span>
<span data-ttu-id="cc986-123">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc986-123">Here is an example of the response.</span></span>
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