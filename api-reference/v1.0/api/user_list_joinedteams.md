# <a name="list-joinedteams"></a><span data-ttu-id="a1913-101">Lista joinedTeams</span><span class="sxs-lookup"><span data-stu-id="a1913-101">List joinedTeams</span></span>



<span data-ttu-id="a1913-102">Obtenga los [equipos](../resources/team.md) en Microsoft Teams que el usuario es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="a1913-102">Get the [teams](../resources/team.md) in Microsoft Teams that the user is a direct member of.</span></span>
 
## <a name="permissions"></a><span data-ttu-id="a1913-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="a1913-103">Permissions</span></span>
<span data-ttu-id="a1913-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a1913-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a1913-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a1913-106">Permission type</span></span>      | <span data-ttu-id="a1913-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a1913-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a1913-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a1913-108">Delegated (work or school account)</span></span> | <span data-ttu-id="a1913-109">User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a1913-109">User.Read.All, User.ReadWrite.All</span></span>    |
|<span data-ttu-id="a1913-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a1913-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a1913-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a1913-111">Not supported.</span></span>    |
|<span data-ttu-id="a1913-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a1913-112">Application</span></span> | <span data-ttu-id="a1913-113">User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a1913-113">User.Read.All, User.ReadWrite.All</span></span> |

> <span data-ttu-id="a1913-114">Con permisos de usuario delegado esta operación sólo funciona para el 'me' usuario.</span><span class="sxs-lookup"><span data-stu-id="a1913-114">With user delegated permissions this operation only works for the 'me' user.</span></span> 
> <span data-ttu-id="a1913-115">Con permisos de aplicación, funciona para todos los usuarios especificando el identificador de usuario específico. ('' alias no seguirá compatible con los permisos de aplicación)</span><span class="sxs-lookup"><span data-stu-id="a1913-115">With application permissions, it works for all users by specifying  the specific user id. ('me' alias is not supported with application permissions)</span></span>

## <a name="http-request"></a><span data-ttu-id="a1913-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a1913-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/joinedTeams
or
GET /users/{id}/joinedTeams
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a1913-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a1913-117">Optional query parameters</span></span>
<span data-ttu-id="a1913-118">Los [Parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) actualmente no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="a1913-118">The [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) are not currently supported.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a1913-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a1913-119">Request headers</span></span>
| <span data-ttu-id="a1913-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1913-120">Header</span></span>       | <span data-ttu-id="a1913-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a1913-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a1913-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="a1913-122">Authorization</span></span>  | <span data-ttu-id="a1913-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a1913-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="a1913-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a1913-125">Accept</span></span>  | <span data-ttu-id="a1913-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a1913-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a1913-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a1913-127">Request body</span></span>
<span data-ttu-id="a1913-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a1913-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a1913-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1913-129">Response</span></span>

<span data-ttu-id="a1913-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a1913-130">If successful, this method returns a `200 OK` response code and collection of [group](../resources/group.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a1913-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a1913-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a1913-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a1913-132">Request</span></span>
<span data-ttu-id="a1913-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a1913-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_joinedteams"
}-->
```http
GET https://graph.microsoft.com/beta/me/joinedTeams
```
##### <a name="response"></a><span data-ttu-id="a1913-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1913-134">Response</span></span>
<span data-ttu-id="a1913-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a1913-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```

## <a name="see-also"></a><span data-ttu-id="a1913-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1913-138">See also</span></span>
[<span data-ttu-id="a1913-139">Lista de todos los equipos</span><span class="sxs-lookup"><span data-stu-id="a1913-139">List all teams</span></span>](../../../concepts/teams_list_all_teams.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List joinedTeams",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
