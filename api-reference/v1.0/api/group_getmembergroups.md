# <a name="group-getmembergroups"></a><span data-ttu-id="52405-101">grupo: getMemberGroups</span><span class="sxs-lookup"><span data-stu-id="52405-101">group: getMemberGroups</span></span>
<span data-ttu-id="52405-p101">Devuelve todos los grupos de los que el grupo que se especifique sea miembro. La comprobación es transitiva, a diferencia de la lectura de la propiedad de navegación [memberOf](../api/group_list_memberof.md), que devuelve solo los grupos de los que el grupo es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="52405-p101">Return all the groups that the specified group is a member of. The check is transitive, unlike reading the [memberOf](../api/group_list_memberof.md) navigation property, which returns only the groups that the group is a direct member of.</span></span>

<span data-ttu-id="52405-p102">Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. El número máximo de grupos que puede devolver cada solicitud es de 2046. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="52405-p102">This function supports Office 365 and other types of groups provisioned in Azure AD. The maximum number of groups each request can return is 2046. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span>

## <a name="permissions"></a><span data-ttu-id="52405-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="52405-108">Permissions</span></span>
<span data-ttu-id="52405-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="52405-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="52405-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="52405-111">Permission type</span></span>      | <span data-ttu-id="52405-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="52405-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="52405-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="52405-113">Delegated (work or school account)</span></span> | <span data-ttu-id="52405-114">Group.Read.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="52405-114">One of the following scopes is required to execute this API: Group.Read.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="52405-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="52405-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="52405-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="52405-116">Not supported.</span></span>    |
|<span data-ttu-id="52405-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="52405-117">Application</span></span> | <span data-ttu-id="52405-118">Group.Read.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="52405-118">Group.Read.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="52405-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="52405-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/getMemberGroups
```
## <a name="request-headers"></a><span data-ttu-id="52405-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="52405-120">Request headers</span></span>
| <span data-ttu-id="52405-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="52405-121">Name</span></span>       | <span data-ttu-id="52405-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="52405-122">Type</span></span> | <span data-ttu-id="52405-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="52405-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="52405-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="52405-124">Authorization</span></span>  | <span data-ttu-id="52405-125">string</span><span class="sxs-lookup"><span data-stu-id="52405-125">string</span></span>  | <span data-ttu-id="52405-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="52405-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="52405-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="52405-128">Request body</span></span>
<span data-ttu-id="52405-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="52405-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="52405-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="52405-130">Parameter</span></span>    | <span data-ttu-id="52405-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="52405-131">Type</span></span>   |<span data-ttu-id="52405-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="52405-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="52405-133">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="52405-133">securityEnabledOnly</span></span>|<span data-ttu-id="52405-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="52405-134">Boolean</span></span>|<span data-ttu-id="52405-p105">Establecer en **false**. La devolución solo de grupos con la seguridad activada solo es compatible para usuarios.</span><span class="sxs-lookup"><span data-stu-id="52405-p105">Set to **false**. Returning only security-enabled groups is supported for users only.</span></span>|

## <a name="response"></a><span data-ttu-id="52405-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52405-137">Response</span></span>

<span data-ttu-id="52405-138">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y la colección String en el cuerpo de la respuesta que contiene los identificadores de los grupos de los que el grupo sea miembro.</span><span class="sxs-lookup"><span data-stu-id="52405-138">If successful, this method returns `200, OK` response code and String collection in the response body that contains the IDs of the groups that the group is a member of.</span></span>

## <a name="example"></a><span data-ttu-id="52405-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="52405-139">Example</span></span>
<span data-ttu-id="52405-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="52405-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="52405-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="52405-141">Request</span></span>
<span data-ttu-id="52405-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="52405-142">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="52405-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52405-143">Response</span></span>
<span data-ttu-id="52405-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="52405-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
