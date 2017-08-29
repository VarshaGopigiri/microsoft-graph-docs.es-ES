# <a name="group-subscribebymail"></a><span data-ttu-id="d7af1-101">group: subscribeByMail</span><span class="sxs-lookup"><span data-stu-id="d7af1-101">group: subscribeByMail</span></span>

<span data-ttu-id="d7af1-p101">La llamada a este método permitirá al usuario actual recibir notificaciones de correo  para este grupo, sobre nuevos eventos, publicaciones y archivos de ese grupo. Compatible solo con grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="d7af1-p101">Calling this method will enable the current user to receive email notifications for this group, about new posts, events, and files in that group. Supported for only Office 365 groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="d7af1-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="d7af1-104">Permissions</span></span>
<span data-ttu-id="d7af1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d7af1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="d7af1-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d7af1-107">Permission type</span></span>      | <span data-ttu-id="d7af1-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d7af1-108">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="d7af1-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d7af1-109">Delegated (work or school account)</span></span> | <span data-ttu-id="d7af1-110">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d7af1-110">Group.ReadWrite.All</span></span>    | 
|<span data-ttu-id="d7af1-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d7af1-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d7af1-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d7af1-112">Not supported.</span></span>    | 
|<span data-ttu-id="d7af1-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d7af1-113">Application</span></span> | <span data-ttu-id="d7af1-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d7af1-114">Group.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="d7af1-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d7af1-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/subscribeByMail
```
## <a name="request-headers"></a><span data-ttu-id="d7af1-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d7af1-116">Request headers</span></span>
| <span data-ttu-id="d7af1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7af1-117">Header</span></span>       | <span data-ttu-id="d7af1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d7af1-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d7af1-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="d7af1-119">Authorization</span></span>  | <span data-ttu-id="d7af1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d7af1-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d7af1-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d7af1-122">Request body</span></span>

## <a name="response"></a><span data-ttu-id="d7af1-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7af1-123">Response</span></span>
<span data-ttu-id="d7af1-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7af1-p104">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d7af1-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d7af1-126">Example</span></span>
<span data-ttu-id="d7af1-127">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d7af1-127">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="d7af1-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d7af1-128">Request</span></span>
<span data-ttu-id="d7af1-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d7af1-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_subscribebymail"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/subscribeByMail
```

##### <a name="response"></a><span data-ttu-id="d7af1-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7af1-130">Response</span></span>
<span data-ttu-id="d7af1-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7af1-131">Here is an example of the response.</span></span> 
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