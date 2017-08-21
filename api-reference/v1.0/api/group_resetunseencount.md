# <a name="group-resetunseencount"></a><span data-ttu-id="71413-101">group: resetUnseenCount</span><span class="sxs-lookup"><span data-stu-id="71413-101">group: resetUnseenCount</span></span>

<span data-ttu-id="71413-p101">Restablece la unseenCount de todas las publicaciones que el usuario actual no ha visto desde su última visita. Compatible solo con grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="71413-p101">Reset the unseenCount of all the posts that the current user has not seen since their last visit. Supported for only Office 365 groups.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="71413-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="71413-104">Prerequisites</span></span>
<span data-ttu-id="71413-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="71413-105">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All*</span></span> 
## <a name="http-request"></a><span data-ttu-id="71413-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71413-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/resetUnseenCount
```
## <a name="request-headers"></a><span data-ttu-id="71413-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71413-107">Request headers</span></span>
| <span data-ttu-id="71413-108">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71413-108">Header</span></span>       | <span data-ttu-id="71413-109">Valor</span><span class="sxs-lookup"><span data-stu-id="71413-109">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="71413-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="71413-110">Authorization</span></span>  | <span data-ttu-id="71413-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="71413-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="71413-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71413-113">Request body</span></span>
<span data-ttu-id="71413-114">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="71413-114">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="71413-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71413-115">Response</span></span>

<span data-ttu-id="71413-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71413-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="71413-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71413-118">Example</span></span>
<span data-ttu-id="71413-119">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="71413-119">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="71413-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71413-120">Request</span></span>
<span data-ttu-id="71413-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="71413-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_resetunseencount"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/resetUnseenCount
```

##### <a name="response"></a><span data-ttu-id="71413-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71413-122">Response</span></span>
<span data-ttu-id="71413-123">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71413-123">Here is an example of the response.</span></span> 
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
