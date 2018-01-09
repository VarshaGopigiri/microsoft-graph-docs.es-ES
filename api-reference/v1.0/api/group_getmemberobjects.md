# <a name="group-getmemberobjects"></a><span data-ttu-id="9469f-101">group: getMemberObjects</span><span class="sxs-lookup"><span data-stu-id="9469f-101">group: getMemberObjects</span></span>
<span data-ttu-id="9469f-p101">Devuelve todos los grupos de los que el grupo es miembro. La comprobación es transitiva. Nota: Los grupos no pueden ser miembros de roles de directorio, por lo que no se devolverá ningún rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="9469f-p101">Return all of the groups that this group is a member of. The check is transitive. Note: Groups cannot be members of directory roles, so no directory roles will be returned.</span></span>

## <a name="permissions"></a><span data-ttu-id="9469f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="9469f-105">Permissions</span></span>
<span data-ttu-id="9469f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9469f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9469f-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9469f-108">Permission type</span></span>      | <span data-ttu-id="9469f-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9469f-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9469f-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9469f-110">Delegated (work or school account)</span></span> | <span data-ttu-id="9469f-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="9469f-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="9469f-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9469f-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9469f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9469f-113">Not supported.</span></span>    |
|<span data-ttu-id="9469f-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9469f-114">Application</span></span> | <span data-ttu-id="9469f-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9469f-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9469f-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9469f-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/getMemberObjects
```

## <a name="request-headers"></a><span data-ttu-id="9469f-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9469f-117">Request headers</span></span>
| <span data-ttu-id="9469f-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="9469f-118">Name</span></span>       | <span data-ttu-id="9469f-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="9469f-119">Type</span></span> | <span data-ttu-id="9469f-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="9469f-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="9469f-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="9469f-121">Authorization</span></span>  | <span data-ttu-id="9469f-122">string</span><span class="sxs-lookup"><span data-stu-id="9469f-122">string</span></span>  | <span data-ttu-id="9469f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9469f-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9469f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9469f-125">Request body</span></span>
<span data-ttu-id="9469f-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="9469f-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="9469f-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9469f-127">Parameter</span></span>    | <span data-ttu-id="9469f-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="9469f-128">Type</span></span>   |<span data-ttu-id="9469f-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="9469f-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9469f-130">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="9469f-130">securityEnabledOnly</span></span>|<span data-ttu-id="9469f-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="9469f-131">Boolean</span></span>| <span data-ttu-id="9469f-p104">Establecer en **false**. La devolución solo de grupos con la seguridad activada solo es compatible para usuarios.</span><span class="sxs-lookup"><span data-stu-id="9469f-p104">Set to **false**. Returning only security-enabled groups is supported for users only.</span></span>|

## <a name="response"></a><span data-ttu-id="9469f-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9469f-134">Response</span></span>
<span data-ttu-id="9469f-135">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la colección String en el cuerpo de la respuesta que contiene los identificadores de los grupos de los que el grupo sea miembro.</span><span class="sxs-lookup"><span data-stu-id="9469f-135">If successful, this method returns `200 OK` response code and String collection in the response body that contains the IDs of the groups that the group is a member of.</span></span>

## <a name="example"></a><span data-ttu-id="9469f-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9469f-136">Example</span></span>
#### <a name="request"></a><span data-ttu-id="9469f-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9469f-137">Request</span></span>
<span data-ttu-id="9469f-138">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9469f-138">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>
<!-- {
  "blockType": "request",
  "name": "group_getmemberobjects"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/getMemberObjects
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": false
}
```

#### <a name="response"></a><span data-ttu-id="9469f-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9469f-139">Response</span></span>
<span data-ttu-id="9469f-140">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9469f-140">Here is an example of the response.</span></span>
><span data-ttu-id="9469f-141">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="9469f-141">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="9469f-142">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9469f-142">All the properties will be returned from an actual call.</span></span>
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
  "description": "group: getMemberObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
