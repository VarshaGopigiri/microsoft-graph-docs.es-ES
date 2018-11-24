# <a name="add-app-to-team"></a><span data-ttu-id="66cb7-101">Agregar la aplicación al equipo</span><span class="sxs-lookup"><span data-stu-id="66cb7-101">Add app to team</span></span>



<span data-ttu-id="66cb7-102">Instala una [aplicación](../resources/teamsapp.md) en el [equipo](../resources/team.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="66cb7-102">Installs an [app](../resources/teamsapp.md) to the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="66cb7-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="66cb7-103">Permissions</span></span>
<span data-ttu-id="66cb7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="66cb7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="66cb7-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="66cb7-106">Permission type</span></span>      | <span data-ttu-id="66cb7-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="66cb7-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="66cb7-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="66cb7-108">Delegated (work or school account)</span></span> | <span data-ttu-id="66cb7-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="66cb7-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="66cb7-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="66cb7-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="66cb7-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="66cb7-111">Not supported.</span></span>    |
|<span data-ttu-id="66cb7-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="66cb7-112">Application</span></span> | <span data-ttu-id="66cb7-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="66cb7-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="66cb7-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="66cb7-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /teams/{id}/installedApps
```

## <a name="request-headers"></a><span data-ttu-id="66cb7-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="66cb7-115">Request headers</span></span>
| <span data-ttu-id="66cb7-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66cb7-116">Header</span></span>       | <span data-ttu-id="66cb7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="66cb7-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="66cb7-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="66cb7-118">Authorization</span></span>  | <span data-ttu-id="66cb7-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="66cb7-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="66cb7-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="66cb7-121">Request body</span></span>

| <span data-ttu-id="66cb7-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66cb7-122">Property</span></span>     | <span data-ttu-id="66cb7-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="66cb7-123">Type</span></span>   |<span data-ttu-id="66cb7-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="66cb7-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="66cb7-125">teamsApp</span><span class="sxs-lookup"><span data-stu-id="66cb7-125">teamsApp</span></span>| [<span data-ttu-id="66cb7-126">teamsApp</span><span class="sxs-lookup"><span data-stu-id="66cb7-126">teamsApp</span></span>](../resources/teamsapp.md) |<span data-ttu-id="66cb7-127">Para agregar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="66cb7-127">The app to add.</span></span>|


## <a name="response"></a><span data-ttu-id="66cb7-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66cb7-128">Response</span></span>

<span data-ttu-id="66cb7-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="66cb7-129">If successful, this method returns a `200 OK` response code.</span></span>

## <a name="example"></a><span data-ttu-id="66cb7-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="66cb7-130">Example</span></span>
#### <a name="request"></a><span data-ttu-id="66cb7-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="66cb7-131">Request</span></span>
<span data-ttu-id="66cb7-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="66cb7-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{id}/installedApps
{
   "teamsApp@odata.bind":"https://graph.microsoft.com/beta/appCatalogs/teamsApps/12345678-9abc-def0-123456789a"
}
```
#### <a name="response"></a><span data-ttu-id="66cb7-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66cb7-133">Response</span></span>
<span data-ttu-id="66cb7-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66cb7-134">The following is an example of the response.</span></span> <span data-ttu-id="66cb7-135">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="66cb7-135">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="66cb7-136">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="66cb7-136">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: xxx

{
}
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

## <a name="see-also"></a><span data-ttu-id="66cb7-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="66cb7-137">See also</span></span>

