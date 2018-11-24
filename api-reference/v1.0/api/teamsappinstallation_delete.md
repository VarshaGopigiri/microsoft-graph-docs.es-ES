# <a name="delete-app-from-team"></a><span data-ttu-id="201e2-101">Eliminar aplicación de equipo</span><span class="sxs-lookup"><span data-stu-id="201e2-101">Delete app from team</span></span>



<span data-ttu-id="201e2-102">Desinstala una [aplicación](../resources/teamsappinstallation.md) desde el [equipo](../resources/team.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="201e2-102">Uninstalls an [app](../resources/teamsappinstallation.md) from the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="201e2-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="201e2-103">Permissions</span></span>
<span data-ttu-id="201e2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="201e2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="201e2-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="201e2-106">Permission type</span></span>      | <span data-ttu-id="201e2-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="201e2-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="201e2-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="201e2-108">Delegated (work or school account)</span></span> | <span data-ttu-id="201e2-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="201e2-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="201e2-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="201e2-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="201e2-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="201e2-111">Not supported.</span></span>    |
|<span data-ttu-id="201e2-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="201e2-112">Application</span></span> | <span data-ttu-id="201e2-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="201e2-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="201e2-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="201e2-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /teams/{id}/installedApps/{id}
```

## <a name="request-headers"></a><span data-ttu-id="201e2-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="201e2-115">Request headers</span></span>
| <span data-ttu-id="201e2-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="201e2-116">Header</span></span>       | <span data-ttu-id="201e2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="201e2-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="201e2-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="201e2-118">Authorization</span></span>  | <span data-ttu-id="201e2-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="201e2-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="201e2-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="201e2-121">Request body</span></span>
<span data-ttu-id="201e2-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="201e2-122">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="201e2-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="201e2-123">Response</span></span>

<span data-ttu-id="201e2-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="201e2-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="201e2-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="201e2-126">Example</span></span>
#### <a name="request"></a><span data-ttu-id="201e2-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="201e2-127">Request</span></span>
<span data-ttu-id="201e2-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="201e2-128">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
DELETE https://graph.microsoft.com/beta/teams/{id}/installedApps/{id}
```
#### <a name="response"></a><span data-ttu-id="201e2-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="201e2-129">Response</span></span>
<span data-ttu-id="201e2-130">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="201e2-130">The following is an example of the response.</span></span> <span data-ttu-id="201e2-131">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="201e2-131">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="201e2-132">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="201e2-132">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
