# <a name="patch-channel"></a><span data-ttu-id="d6132-101">Canal de revisión</span><span class="sxs-lookup"><span data-stu-id="d6132-101">Patch channel</span></span>



<span data-ttu-id="d6132-102">Actualizar las propiedades del [canal](../resources/channel.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="d6132-102">Update the properties of the specified [channel](../resources/channel.md).</span></span>

> <span data-ttu-id="d6132-103">**Nota**: hay un problema conocido con permisos de la aplicación y esta API.</span><span class="sxs-lookup"><span data-stu-id="d6132-103">**Note**: There is a known issue with application permissions and this API.</span></span> <span data-ttu-id="d6132-104">Para obtener información detallada, vea el [conocido lista de problemas](../../../concepts/known_issues.md#application-permissions).</span><span class="sxs-lookup"><span data-stu-id="d6132-104">For details, see the [known issues list](../../../concepts/known_issues.md#application-permissions).</span></span>

## <a name="permissions"></a><span data-ttu-id="d6132-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="d6132-105">Permissions</span></span>
<span data-ttu-id="d6132-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d6132-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d6132-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d6132-108">Permission type</span></span>      | <span data-ttu-id="d6132-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d6132-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d6132-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d6132-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d6132-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d6132-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="d6132-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d6132-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d6132-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d6132-113">Not supported.</span></span>    |
|<span data-ttu-id="d6132-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d6132-114">Application</span></span> | <span data-ttu-id="d6132-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d6132-115">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d6132-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d6132-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /teams/{id}/channels/{id}
```
## <a name="request-headers"></a><span data-ttu-id="d6132-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d6132-117">Request headers</span></span>
| <span data-ttu-id="d6132-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6132-118">Header</span></span>       | <span data-ttu-id="d6132-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d6132-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d6132-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="d6132-120">Authorization</span></span>  | <span data-ttu-id="d6132-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d6132-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="d6132-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d6132-123">Content-Type</span></span>  | <span data-ttu-id="d6132-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d6132-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d6132-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d6132-125">Request body</span></span>
<span data-ttu-id="d6132-126">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [canal](../resources/channel.md) .</span><span class="sxs-lookup"><span data-stu-id="d6132-126">In the request body, supply a JSON representation of [channel](../resources/channel.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="d6132-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6132-127">Response</span></span>

<span data-ttu-id="d6132-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="d6132-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="d6132-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d6132-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d6132-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d6132-130">Request</span></span>
<span data-ttu-id="d6132-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d6132-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "patch_channel"
}-->
```http
PATCH https://graph.microsoft.com/beta/teams/{id}/channels/{id}
```
##### <a name="response"></a><span data-ttu-id="d6132-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6132-132">Response</span></span>
<span data-ttu-id="d6132-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d6132-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.channel"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 201

{
    "description": "description-value",
    "displayName": "display-name-value",
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Patch channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
