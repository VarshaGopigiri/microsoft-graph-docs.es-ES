# <a name="group-checkmembergroups"></a><span data-ttu-id="3e9c1-101">group: checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="3e9c1-101">group: checkMemberGroups</span></span>
<span data-ttu-id="3e9c1-p101">Comprueba la pertenencia en la lista especificada de grupos. Devuelve de la lista los grupos en los que el grupo especificado tenga una pertenencia directa o transitiva.</span><span class="sxs-lookup"><span data-stu-id="3e9c1-p101">Check for membership in the specified list of groups. Returns from the list those groups of which the specified group has a direct or transitive membership.</span></span> 

<span data-ttu-id="3e9c1-p102">Puede comprobarse un máximo de 20 grupos por solicitud. Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="3e9c1-p102">You can check up to a maximum of 20 groups per request. This function supports Office 365 and other types of groups provisioned in Azure AD. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="3e9c1-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3e9c1-108">Prerequisites</span></span>
<span data-ttu-id="3e9c1-109">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="3e9c1-109">One of the following **scopes** is required to execute this API:</span></span>
## <a name="http-request"></a><span data-ttu-id="3e9c1-110">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3e9c1-110">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/checkMemberGroups
```
## <a name="request-headers"></a><span data-ttu-id="3e9c1-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3e9c1-111">Request headers</span></span>
| <span data-ttu-id="3e9c1-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="3e9c1-112">Name</span></span>       | <span data-ttu-id="3e9c1-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="3e9c1-113">Type</span></span> | <span data-ttu-id="3e9c1-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e9c1-114">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="3e9c1-115">Authorization</span><span class="sxs-lookup"><span data-stu-id="3e9c1-115">Authorization</span></span>  | <span data-ttu-id="3e9c1-116">string</span><span class="sxs-lookup"><span data-stu-id="3e9c1-116">string</span></span>  | <span data-ttu-id="3e9c1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3e9c1-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3e9c1-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3e9c1-119">Request body</span></span>
<span data-ttu-id="3e9c1-120">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="3e9c1-120">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="3e9c1-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3e9c1-121">Parameter</span></span>    | <span data-ttu-id="3e9c1-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="3e9c1-122">Type</span></span>   |<span data-ttu-id="3e9c1-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e9c1-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3e9c1-124">groupIds</span><span class="sxs-lookup"><span data-stu-id="3e9c1-124">groupIds</span></span>|<span data-ttu-id="3e9c1-125">String</span><span class="sxs-lookup"><span data-stu-id="3e9c1-125">String</span></span>|<span data-ttu-id="3e9c1-126">Matriz de identificadores de grupo</span><span class="sxs-lookup"><span data-stu-id="3e9c1-126">An array of group ids</span></span>|

## <a name="response"></a><span data-ttu-id="3e9c1-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3e9c1-127">Response</span></span>

<span data-ttu-id="3e9c1-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3e9c1-128">If successful, this method returns `200, OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3e9c1-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3e9c1-129">Example</span></span>
<span data-ttu-id="3e9c1-130">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="3e9c1-130">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="3e9c1-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3e9c1-131">Request</span></span>
<span data-ttu-id="3e9c1-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3e9c1-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_checkmembergroups"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/checkMemberGroups
Content-type: application/json
Content-length: 44

{
  "groupIds": [
    "groupIds-value"
  ]
}
```

##### <a name="response"></a><span data-ttu-id="3e9c1-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3e9c1-133">Response</span></span>
<span data-ttu-id="3e9c1-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3e9c1-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "group: checkMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
