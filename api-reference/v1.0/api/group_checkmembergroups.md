# <a name="group-checkmembergroups"></a><span data-ttu-id="6d71d-101">group: checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="6d71d-101">group: checkMemberGroups</span></span>
<span data-ttu-id="6d71d-p101">Comprueba la pertenencia en la lista especificada de grupos. Devuelve de la lista los grupos en los que el grupo especificado tenga una pertenencia directa o transitiva.</span><span class="sxs-lookup"><span data-stu-id="6d71d-p101">Check for membership in the specified list of groups. Returns from the list those groups of which the specified group has a direct or transitive membership.</span></span> 

<span data-ttu-id="6d71d-p102">Puede comprobarse un máximo de 20 grupos por solicitud. Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="6d71d-p102">You can check up to a maximum of 20 groups per request. This function supports Office 365 and other types of groups provisioned in Azure AD. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span> 

## <a name="permissions"></a><span data-ttu-id="6d71d-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="6d71d-108">Permissions</span></span>
<span data-ttu-id="6d71d-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6d71d-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6d71d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6d71d-111">Permission type</span></span>      | <span data-ttu-id="6d71d-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6d71d-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6d71d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6d71d-113">Delegated (work or school account)</span></span> | <span data-ttu-id="6d71d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6d71d-114">Not supported.</span></span>    |
|<span data-ttu-id="6d71d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6d71d-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6d71d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6d71d-116">Not supported.</span></span>    |
|<span data-ttu-id="6d71d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6d71d-117">Application</span></span> | <span data-ttu-id="6d71d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6d71d-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6d71d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6d71d-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/checkMemberGroups
```
## <a name="request-headers"></a><span data-ttu-id="6d71d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6d71d-120">Request headers</span></span>
| <span data-ttu-id="6d71d-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="6d71d-121">Name</span></span>       | <span data-ttu-id="6d71d-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d71d-122">Type</span></span> | <span data-ttu-id="6d71d-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d71d-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="6d71d-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="6d71d-124">Authorization</span></span>  | <span data-ttu-id="6d71d-125">string</span><span class="sxs-lookup"><span data-stu-id="6d71d-125">string</span></span>  | <span data-ttu-id="6d71d-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6d71d-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6d71d-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6d71d-128">Request body</span></span>
<span data-ttu-id="6d71d-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="6d71d-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="6d71d-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6d71d-130">Parameter</span></span>    | <span data-ttu-id="6d71d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6d71d-131">Type</span></span>   |<span data-ttu-id="6d71d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d71d-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6d71d-133">groupIds</span><span class="sxs-lookup"><span data-stu-id="6d71d-133">groupIds</span></span>|<span data-ttu-id="6d71d-134">String</span><span class="sxs-lookup"><span data-stu-id="6d71d-134">String</span></span>|<span data-ttu-id="6d71d-135">Matriz de identificadores de grupo</span><span class="sxs-lookup"><span data-stu-id="6d71d-135">An array of group ids</span></span>|

## <a name="response"></a><span data-ttu-id="6d71d-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d71d-136">Response</span></span>

<span data-ttu-id="6d71d-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d71d-137">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6d71d-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d71d-138">Example</span></span>
<span data-ttu-id="6d71d-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="6d71d-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="6d71d-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6d71d-140">Request</span></span>
<span data-ttu-id="6d71d-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6d71d-141">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="6d71d-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d71d-142">Response</span></span>
<span data-ttu-id="6d71d-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6d71d-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
