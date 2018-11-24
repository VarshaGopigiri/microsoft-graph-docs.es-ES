# <a name="get-directoryroletemplate"></a><span data-ttu-id="035e0-101">Get directoryRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="035e0-101">Get directoryRoleTemplate</span></span>

<span data-ttu-id="035e0-102">Recupera las propiedades y relaciones de un objeto directoryroletemplate.</span><span class="sxs-lookup"><span data-stu-id="035e0-102">Retrieve the properties and relationships of a directoryroletemplate object.</span></span>
## <a name="permissions"></a><span data-ttu-id="035e0-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="035e0-103">Permissions</span></span>
<span data-ttu-id="035e0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="035e0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="035e0-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="035e0-106">Permission type</span></span>      | <span data-ttu-id="035e0-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="035e0-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="035e0-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="035e0-108">Delegated (work or school account)</span></span> | <span data-ttu-id="035e0-109">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="035e0-109">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="035e0-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="035e0-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="035e0-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="035e0-111">Not supported.</span></span>    |
|<span data-ttu-id="035e0-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="035e0-112">Application</span></span> | <span data-ttu-id="035e0-113">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="035e0-113">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="035e0-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="035e0-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoleTemplates/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="035e0-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="035e0-115">Optional query parameters</span></span>
<span data-ttu-id="035e0-116">Este método **no** es compatible con los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="035e0-116">This method does **not** support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="035e0-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="035e0-117">Request headers</span></span>
| <span data-ttu-id="035e0-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="035e0-118">Name</span></span>       | <span data-ttu-id="035e0-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="035e0-119">Type</span></span> | <span data-ttu-id="035e0-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="035e0-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="035e0-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="035e0-121">Authorization</span></span>  | <span data-ttu-id="035e0-122">string</span><span class="sxs-lookup"><span data-stu-id="035e0-122">string</span></span>  | <span data-ttu-id="035e0-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="035e0-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="035e0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="035e0-125">Request body</span></span>
<span data-ttu-id="035e0-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="035e0-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="035e0-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="035e0-127">Response</span></span>

<span data-ttu-id="035e0-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryRoleTemplate](../resources/directoryroletemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="035e0-128">If successful, this method returns a `200 OK` response code and [directoryRoleTemplate](../resources/directoryroletemplate.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="035e0-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="035e0-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="035e0-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="035e0-130">Request</span></span>
<span data-ttu-id="035e0-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="035e0-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_directoryroletemplate"
}-->
```http
GET https://graph.microsoft.com/v1.0/directoryRoleTemplates/{id}
```
##### <a name="response"></a><span data-ttu-id="035e0-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="035e0-132">Response</span></span>
<span data-ttu-id="035e0-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="035e0-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryRoleTemplate"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 98

{
  "description": "description-value",
  "displayName": "displayName-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get directoryRoleTemplate",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
