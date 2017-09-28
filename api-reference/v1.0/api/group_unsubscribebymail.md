# <a name="group-unsubscribebymail"></a><span data-ttu-id="e64b8-101">group: unsubscribeByMail</span><span class="sxs-lookup"><span data-stu-id="e64b8-101">group: unsubscribeByMail</span></span>

<span data-ttu-id="e64b8-p101">La llamada a este método impedirá que el usuario actual reciba notificaciones de correo para este grupo, sobre nuevos eventos, publicaciones y archivos de ese grupo. Compatible solo con grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="e64b8-p101">Calling this method will prevent the current user from receiving email notifications for this group about new posts, events, and files in that group. Supported for only Office 365 groups.</span></span> 
## <a name="permissions"></a><span data-ttu-id="e64b8-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="e64b8-104">Permissions</span></span>
<span data-ttu-id="e64b8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e64b8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="e64b8-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e64b8-107">Permission type</span></span>      | <span data-ttu-id="e64b8-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e64b8-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e64b8-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e64b8-109">Delegated (work or school account)</span></span> | <span data-ttu-id="e64b8-110">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e64b8-110">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="e64b8-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e64b8-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e64b8-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e64b8-112">Not supported.</span></span>    |
|<span data-ttu-id="e64b8-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e64b8-113">Application</span></span> | <span data-ttu-id="e64b8-114">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e64b8-114">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e64b8-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e64b8-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/unsubscribeByMail
```
## <a name="request-headers"></a><span data-ttu-id="e64b8-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e64b8-116">Request headers</span></span>
| <span data-ttu-id="e64b8-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e64b8-117">Header</span></span>       | <span data-ttu-id="e64b8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e64b8-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e64b8-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="e64b8-119">Authorization</span></span>  | <span data-ttu-id="e64b8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e64b8-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e64b8-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e64b8-122">Request body</span></span>
<span data-ttu-id="e64b8-123">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e64b8-123">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e64b8-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e64b8-124">Response</span></span>
<span data-ttu-id="e64b8-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e64b8-p104">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e64b8-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e64b8-127">Example</span></span>
<span data-ttu-id="e64b8-128">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="e64b8-128">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="e64b8-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e64b8-129">Request</span></span>
<span data-ttu-id="e64b8-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e64b8-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_unsubscribebymail"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/unsubscribeByMail
```

##### <a name="response"></a><span data-ttu-id="e64b8-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e64b8-131">Response</span></span>
<span data-ttu-id="e64b8-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e64b8-132">Here is an example of the response.</span></span> 
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
