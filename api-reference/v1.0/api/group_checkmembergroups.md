# <a name="group-checkmembergroups"></a><span data-ttu-id="7b27d-101">group: checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="7b27d-101">group: checkMemberGroups</span></span>

<span data-ttu-id="7b27d-p101">Comprueba la pertenencia en la lista especificada de grupos. Devuelve de la lista los grupos en los que el grupo especificado tenga una pertenencia directa o transitiva.</span><span class="sxs-lookup"><span data-stu-id="7b27d-p101">Check for membership in the specified list of groups. Returns from the list those groups of which the specified group has a direct or transitive membership.</span></span>

<span data-ttu-id="7b27d-p102">Puede comprobarse un máximo de 20 grupos por solicitud. Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="7b27d-p102">You can check up to a maximum of 20 groups per request. This function supports Office 365 and other types of groups provisioned in Azure AD. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span>

## <a name="permissions"></a><span data-ttu-id="7b27d-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="7b27d-108">Permissions</span></span>

<span data-ttu-id="7b27d-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7b27d-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="7b27d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7b27d-111">Permission type</span></span>                        | <span data-ttu-id="7b27d-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7b27d-112">Permissions (from least to most privileged)</span></span>                                                 |
| :------------------------------------- | :------------------------------------------------------------------------------------------ |
| <span data-ttu-id="7b27d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7b27d-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="7b27d-114">~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="7b27d-114">~~Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="7b27d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7b27d-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7b27d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7b27d-116">Not supported.</span></span>                                                                              |
| <span data-ttu-id="7b27d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7b27d-117">Application</span></span>                            | <span data-ttu-id="7b27d-118">_Group.Read.All_, Directory.Read.All.</span><span class="sxs-lookup"><span data-stu-id="7b27d-118">_Group.Read.All_, Directory.Read.All, Directory.ReadWrite.All</span></span> <span data-ttu-id="7b27d-119">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7b27d-119">Directory.ReadWrite.All</span></span>                               |

> <span data-ttu-id="7b27d-120">**Nota:** En este momento, esta API requiere el permiso `Directory.Read.All` o superior.</span><span class="sxs-lookup"><span data-stu-id="7b27d-120">Note: This API currently requires the Directory.Read.All permission or higher.</span></span> <span data-ttu-id="7b27d-121">El uso del permiso `Gorup.Read.All` devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="7b27d-121">Using the Group.Read.All permission will return an error.</span></span> <span data-ttu-id="7b27d-122">Se trata de un problema conocido.</span><span class="sxs-lookup"><span data-stu-id="7b27d-122">This is a known bug.</span></span>

## <a name="http-request"></a><span data-ttu-id="7b27d-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7b27d-123">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /groups/{id}/checkMemberGroups
```

## <a name="request-headers"></a><span data-ttu-id="7b27d-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7b27d-124">Request headers</span></span>

| <span data-ttu-id="7b27d-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="7b27d-125">Name</span></span>          | <span data-ttu-id="7b27d-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b27d-126">Type</span></span>   | <span data-ttu-id="7b27d-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b27d-127">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="7b27d-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="7b27d-128">Authorization</span></span> | <span data-ttu-id="7b27d-129">cadena</span><span class="sxs-lookup"><span data-stu-id="7b27d-129">string</span></span> | <span data-ttu-id="7b27d-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7b27d-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7b27d-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7b27d-132">Request body</span></span>

<span data-ttu-id="7b27d-133">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="7b27d-133">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="7b27d-134">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7b27d-134">Parameter</span></span> | <span data-ttu-id="7b27d-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b27d-135">Type</span></span>              | <span data-ttu-id="7b27d-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b27d-136">Description</span></span>           |
| :-------- | :---------------- | :-------------------- |
| <span data-ttu-id="7b27d-137">groupIds</span><span class="sxs-lookup"><span data-stu-id="7b27d-137">groupIds</span></span>  | <span data-ttu-id="7b27d-138">Colección String</span><span class="sxs-lookup"><span data-stu-id="7b27d-138">String collection</span></span> | <span data-ttu-id="7b27d-139">Matriz de identificadores de grupo</span><span class="sxs-lookup"><span data-stu-id="7b27d-139">An array of group ids</span></span> |

## <a name="response"></a><span data-ttu-id="7b27d-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b27d-140">Response</span></span>

<span data-ttu-id="7b27d-141">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b27d-141">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7b27d-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b27d-142">Example</span></span>

<span data-ttu-id="7b27d-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="7b27d-143">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="7b27d-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7b27d-144">Request</span></span>

<span data-ttu-id="7b27d-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7b27d-145">Here is an example of the request.</span></span>

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

##### <a name="response"></a><span data-ttu-id="7b27d-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b27d-146">Response</span></span>

<span data-ttu-id="7b27d-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7b27d-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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
