# <a name="group-subscribebymail"></a><span data-ttu-id="d849d-101">group: subscribeByMail</span><span class="sxs-lookup"><span data-stu-id="d849d-101">group: subscribeByMail</span></span>

<span data-ttu-id="d849d-p101">La llamada a este método permitirá al usuario actual recibir notificaciones de correo  para este grupo, sobre nuevos eventos, publicaciones y archivos de ese grupo. Compatible solo con grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="d849d-p101">Calling this method will enable the current user to receive email notifications for this group, about new posts, events, and files in that group. Supported for only Office 365 groups.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d849d-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d849d-104">Prerequisites</span></span>
<span data-ttu-id="d849d-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All* 
*Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="d849d-105">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All* 
*Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="d849d-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d849d-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/subscribeByMail
```
## <a name="request-headers"></a><span data-ttu-id="d849d-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d849d-107">Request headers</span></span>
| <span data-ttu-id="d849d-108">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d849d-108">Header</span></span>       | <span data-ttu-id="d849d-109">Valor</span><span class="sxs-lookup"><span data-stu-id="d849d-109">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d849d-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="d849d-110">Authorization</span></span>  | <span data-ttu-id="d849d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d849d-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d849d-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d849d-113">Request body</span></span>

## <a name="response"></a><span data-ttu-id="d849d-114">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d849d-114">Response</span></span>

<span data-ttu-id="d849d-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d849d-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d849d-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d849d-117">Example</span></span>
<span data-ttu-id="d849d-118">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d849d-118">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="d849d-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d849d-119">Request</span></span>
<span data-ttu-id="d849d-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d849d-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_subscribebymail"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/subscribeByMail
```

##### <a name="response"></a><span data-ttu-id="d849d-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d849d-121">Response</span></span>
<span data-ttu-id="d849d-122">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d849d-122">Here is an example of the response.</span></span> 
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
  "description": "group: subscribeByMail",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->