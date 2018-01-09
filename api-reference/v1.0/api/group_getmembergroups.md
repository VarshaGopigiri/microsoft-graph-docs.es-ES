# <a name="group-getmembergroups"></a><span data-ttu-id="d2ea2-101">grupo: getMemberGroups</span><span class="sxs-lookup"><span data-stu-id="d2ea2-101">group: getMemberGroups</span></span>
<span data-ttu-id="d2ea2-p101">Devuelve todos los grupos de los que el grupo que se especifique sea miembro. La comprobación es transitiva, a diferencia de la lectura de la propiedad de navegación [memberOf](../api/group_list_memberof.md), que devuelve solo los grupos de los que el grupo es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-p101">Return all the groups that the specified group is a member of. The check is transitive, unlike reading the [memberOf](../api/group_list_memberof.md) navigation property, which returns only the groups that the group is a direct member of.</span></span>

<span data-ttu-id="d2ea2-p102">Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. El número máximo de grupos que puede devolver cada solicitud es de 2046. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-p102">This function supports Office 365 and other types of groups provisioned in Azure AD. The maximum number of groups each request can return is 2046. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span>

## <a name="permissions"></a><span data-ttu-id="d2ea2-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="d2ea2-108">Permissions</span></span>
<span data-ttu-id="d2ea2-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d2ea2-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d2ea2-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2ea2-111">Permission type</span></span>      | <span data-ttu-id="d2ea2-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2ea2-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d2ea2-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2ea2-113">Delegated (work or school account)</span></span> | <span data-ttu-id="d2ea2-114">Group.Read.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="d2ea2-114">Group.Read.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="d2ea2-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2ea2-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d2ea2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-116">Not supported.</span></span>    |
|<span data-ttu-id="d2ea2-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2ea2-117">Application</span></span> | <span data-ttu-id="d2ea2-118">Group.Read.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d2ea2-118">Group.Read.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d2ea2-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2ea2-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/getMemberGroups
```
## <a name="request-headers"></a><span data-ttu-id="d2ea2-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2ea2-120">Request headers</span></span>
| <span data-ttu-id="d2ea2-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="d2ea2-121">Name</span></span>       | <span data-ttu-id="d2ea2-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2ea2-122">Type</span></span> | <span data-ttu-id="d2ea2-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2ea2-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="d2ea2-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="d2ea2-124">Authorization</span></span>  | <span data-ttu-id="d2ea2-125">string</span><span class="sxs-lookup"><span data-stu-id="d2ea2-125">string</span></span>  | <span data-ttu-id="d2ea2-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d2ea2-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2ea2-128">Request body</span></span>
<span data-ttu-id="d2ea2-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d2ea2-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d2ea2-130">Parameter</span></span>    | <span data-ttu-id="d2ea2-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2ea2-131">Type</span></span>   |<span data-ttu-id="d2ea2-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2ea2-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d2ea2-133">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="d2ea2-133">securityEnabledOnly</span></span>|<span data-ttu-id="d2ea2-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="d2ea2-134">Boolean</span></span>|<span data-ttu-id="d2ea2-p105">Establecer en **false**. La devolución solo de grupos con la seguridad activada solo es compatible para usuarios.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-p105">Set to **false**. Returning only security-enabled groups is supported for users only.</span></span>|

## <a name="response"></a><span data-ttu-id="d2ea2-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2ea2-137">Response</span></span>
<span data-ttu-id="d2ea2-138">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la colección String en el cuerpo de la respuesta que contiene los identificadores de los grupos de los que el grupo sea miembro.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-138">If successful, this method returns `200 OK` response code and String collection in the response body that contains the IDs of the groups that the group is a member of.</span></span>

## <a name="example"></a><span data-ttu-id="d2ea2-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2ea2-139">Example</span></span>
#### <a name="request"></a><span data-ttu-id="d2ea2-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2ea2-140">Request</span></span>
<span data-ttu-id="d2ea2-141">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-141">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>
<!-- {
  "blockType": "request",
  "name": "group_getmembergroups"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/getMemberGroups
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": false
}
```

#### <a name="response"></a><span data-ttu-id="d2ea2-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2ea2-142">Response</span></span>
<span data-ttu-id="d2ea2-143">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-143">Here is an example of the response.</span></span>
><span data-ttu-id="d2ea2-144">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-144">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="d2ea2-145">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-145">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "string",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "value": [
    "string-value"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: getMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
