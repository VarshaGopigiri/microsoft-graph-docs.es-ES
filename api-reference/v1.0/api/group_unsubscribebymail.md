# <a name="group-unsubscribebymail"></a><span data-ttu-id="730aa-101">group: unsubscribeByMail</span><span class="sxs-lookup"><span data-stu-id="730aa-101">group: unsubscribeByMail</span></span>

<span data-ttu-id="730aa-p101">La llamada a este método impedirá que el usuario actual reciba notificaciones de correo para este grupo, sobre nuevos eventos, publicaciones y archivos de ese grupo. Compatible solo con grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="730aa-p101">Calling this method will prevent the current user from receiving email notifications for this group about new posts, events, and files in that group. Supported for only Office 365 groups.</span></span> 
## <a name="prerequisites"></a><span data-ttu-id="730aa-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="730aa-104">Prerequisites</span></span>
<span data-ttu-id="730aa-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.ReadWrite.All* 
*Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="730aa-105">One of the following **scopes** is required to execute this API: *Group.ReadWrite.All* 
*Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="730aa-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="730aa-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/unsubscribeByMail
```
## <a name="request-headers"></a><span data-ttu-id="730aa-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="730aa-107">Request headers</span></span>
| <span data-ttu-id="730aa-108">Encabezado</span><span class="sxs-lookup"><span data-stu-id="730aa-108">Header</span></span>       | <span data-ttu-id="730aa-109">Valor</span><span class="sxs-lookup"><span data-stu-id="730aa-109">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="730aa-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="730aa-110">Authorization</span></span>  | <span data-ttu-id="730aa-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="730aa-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="730aa-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="730aa-113">Request body</span></span>

## <a name="response"></a><span data-ttu-id="730aa-114">Respuesta</span><span class="sxs-lookup"><span data-stu-id="730aa-114">Response</span></span>

<span data-ttu-id="730aa-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="730aa-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="730aa-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="730aa-117">Example</span></span>
<span data-ttu-id="730aa-118">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="730aa-118">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="730aa-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="730aa-119">Request</span></span>
<span data-ttu-id="730aa-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="730aa-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_unsubscribebymail"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/unsubscribeByMail
```

##### <a name="response"></a><span data-ttu-id="730aa-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="730aa-121">Response</span></span>
<span data-ttu-id="730aa-122">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="730aa-122">Here is an example of the response.</span></span> 
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
