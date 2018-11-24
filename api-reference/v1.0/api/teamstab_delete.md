# <a name="delete-tab-from-channel"></a><span data-ttu-id="a8698-101">Eliminar ficha de canal</span><span class="sxs-lookup"><span data-stu-id="a8698-101">Delete tab from channel</span></span>



<span data-ttu-id="a8698-102">Quita (libera) una ficha desde el [canal](../resources/channel.md) especificado dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="a8698-102">Removes (unpins) a tab from the specified [channel](../resources/channel.md) within a [team](../resources/team.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="a8698-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="a8698-103">Permissions</span></span>
<span data-ttu-id="a8698-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a8698-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a8698-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a8698-106">Permission type</span></span>      | <span data-ttu-id="a8698-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a8698-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a8698-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a8698-108">Delegated (work or school account)</span></span> | <span data-ttu-id="a8698-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a8698-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="a8698-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a8698-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a8698-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a8698-111">Not supported.</span></span>    |
|<span data-ttu-id="a8698-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a8698-112">Application</span></span> | <span data-ttu-id="a8698-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a8698-113">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a8698-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a8698-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /teams/{id}/channels/{id}/tabs/{id}
```

## <a name="request-headers"></a><span data-ttu-id="a8698-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a8698-115">Request headers</span></span>
| <span data-ttu-id="a8698-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8698-116">Header</span></span>       | <span data-ttu-id="a8698-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a8698-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a8698-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="a8698-118">Authorization</span></span>  | <span data-ttu-id="a8698-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a8698-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a8698-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a8698-121">Request body</span></span>
<span data-ttu-id="a8698-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a8698-122">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a8698-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a8698-123">Response</span></span>

<span data-ttu-id="a8698-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a8698-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a8698-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a8698-126">Example</span></span>
#### <a name="request"></a><span data-ttu-id="a8698-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a8698-127">Request</span></span>
<span data-ttu-id="a8698-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a8698-128">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
DELETE https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs/{id}
```
#### <a name="response"></a><span data-ttu-id="a8698-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a8698-129">Response</span></span>
<span data-ttu-id="a8698-130">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a8698-130">The following is an example of the response.</span></span> <span data-ttu-id="a8698-131">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="a8698-131">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="a8698-132">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a8698-132">All of the properties will be returned from an actual call.</span></span>
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete tab from channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
