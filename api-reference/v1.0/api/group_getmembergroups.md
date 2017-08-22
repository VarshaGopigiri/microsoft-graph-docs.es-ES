# <a name="group-getmembergroups"></a><span data-ttu-id="9b3ae-101">grupo: getMemberGroups</span><span class="sxs-lookup"><span data-stu-id="9b3ae-101">group: getMemberGroups</span></span>
<span data-ttu-id="9b3ae-p101">Devuelve todos los grupos de los que el grupo que se especifique sea miembro. La comprobación es transitiva, a diferencia de la lectura de la propiedad de navegación [memberOf](../api/group_list_memberof.md), que devuelve solo los grupos de los que el grupo es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-p101">Return all the groups that the specified group is a member of. The check is transitive, unlike reading the [memberOf](../api/group_list_memberof.md) navigation property, which returns only the groups that the group is a direct member of.</span></span>

<span data-ttu-id="9b3ae-p102">Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. El número máximo de grupos que puede devolver cada solicitud es de 2046. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-p102">This function supports Office 365 and other types of groups provisioned in Azure AD. The maximum number of groups each request can return is 2046. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9b3ae-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9b3ae-108">Prerequisites</span></span>
<span data-ttu-id="9b3ae-109">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.Read.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="9b3ae-109">One of the following **scopes** is required to execute this API: *Group.Read.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="9b3ae-110">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b3ae-110">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/getMemberGroups
```
## <a name="request-headers"></a><span data-ttu-id="9b3ae-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b3ae-111">Request headers</span></span>
| <span data-ttu-id="9b3ae-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="9b3ae-112">Name</span></span>       | <span data-ttu-id="9b3ae-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b3ae-113">Type</span></span> | <span data-ttu-id="9b3ae-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b3ae-114">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="9b3ae-115">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b3ae-115">Authorization</span></span>  | <span data-ttu-id="9b3ae-116">string</span><span class="sxs-lookup"><span data-stu-id="9b3ae-116">string</span></span>  | <span data-ttu-id="9b3ae-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9b3ae-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b3ae-119">Request body</span></span>
<span data-ttu-id="9b3ae-120">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-120">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="9b3ae-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9b3ae-121">Parameter</span></span>    | <span data-ttu-id="9b3ae-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b3ae-122">Type</span></span>   |<span data-ttu-id="9b3ae-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b3ae-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9b3ae-124">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="9b3ae-124">securityEnabledOnly</span></span>|<span data-ttu-id="9b3ae-125">Boolean</span><span class="sxs-lookup"><span data-stu-id="9b3ae-125">Boolean</span></span>|<span data-ttu-id="9b3ae-p104">Establecer en **false**. La devolución solo de grupos con la seguridad activada solo es compatible para usuarios.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-p104">Set to **false**. Returning only security-enabled groups is supported for users only.</span></span>|

## <a name="response"></a><span data-ttu-id="9b3ae-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b3ae-128">Response</span></span>

<span data-ttu-id="9b3ae-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y la colección String en el cuerpo de la respuesta que contiene los identificadores de los grupos de los que el grupo sea miembro.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-129">If successful, this method returns `200, OK` response code and String collection in the response body that contains the IDs of the groups that the group is a member of.</span></span>

## <a name="example"></a><span data-ttu-id="9b3ae-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b3ae-130">Example</span></span>
<span data-ttu-id="9b3ae-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="9b3ae-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b3ae-132">Request</span></span>
<span data-ttu-id="9b3ae-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-133">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="9b3ae-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b3ae-134">Response</span></span>
<span data-ttu-id="9b3ae-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9b3ae-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
