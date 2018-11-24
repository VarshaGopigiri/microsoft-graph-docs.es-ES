# <a name="list-directoryroles"></a><span data-ttu-id="27c86-101">List directoryRoles</span><span class="sxs-lookup"><span data-stu-id="27c86-101">List directoryRoles</span></span>

<span data-ttu-id="27c86-102">Enumera los roles de directorio que están activados en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="27c86-102">List the directory roles that are activated in the tenant.</span></span>
## <a name="permissions"></a><span data-ttu-id="27c86-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="27c86-103">Permissions</span></span>
<span data-ttu-id="27c86-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="27c86-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="27c86-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="27c86-106">Permission type</span></span>      | <span data-ttu-id="27c86-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="27c86-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="27c86-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="27c86-108">Delegated (work or school account)</span></span> | <span data-ttu-id="27c86-109">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="27c86-109">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="27c86-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="27c86-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="27c86-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="27c86-111">Not supported.</span></span>    |
|<span data-ttu-id="27c86-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="27c86-112">Application</span></span> | <span data-ttu-id="27c86-113">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="27c86-113">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="27c86-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="27c86-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoles
```
## <a name="optional-query-parameters"></a><span data-ttu-id="27c86-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="27c86-115">Optional query parameters</span></span>
<span data-ttu-id="27c86-116">Este método **no** es compatible con los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para facilitar la personalización de la respuesta (por ejemplo, aquí no se admite $filter).</span><span class="sxs-lookup"><span data-stu-id="27c86-116">This method does **not** support the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response (e.g. $filter is not supported here).</span></span>

## <a name="request-headers"></a><span data-ttu-id="27c86-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="27c86-117">Request headers</span></span>
| <span data-ttu-id="27c86-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="27c86-118">Name</span></span>       | <span data-ttu-id="27c86-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="27c86-119">Type</span></span> | <span data-ttu-id="27c86-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="27c86-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="27c86-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="27c86-121">Authorization</span></span>  | <span data-ttu-id="27c86-122">string</span><span class="sxs-lookup"><span data-stu-id="27c86-122">string</span></span>  | <span data-ttu-id="27c86-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="27c86-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="27c86-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="27c86-125">Request body</span></span>
<span data-ttu-id="27c86-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="27c86-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="27c86-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27c86-127">Response</span></span>

<span data-ttu-id="27c86-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryRole](../resources/directoryrole.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27c86-128">If successful, this method returns a `200 OK` response code and collection of [directoryRole](../resources/directoryrole.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="27c86-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="27c86-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="27c86-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="27c86-130">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_directoryroles"
}-->
```http
GET https://graph.microsoft.com/v1.0/directoryRoles
```
##### <a name="response"></a><span data-ttu-id="27c86-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27c86-131">Response</span></span>
<span data-ttu-id="27c86-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="27c86-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryRole",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "description": "description-value",
      "displayName": "displayName-value",
      "roleTemplateId": "roleTemplateId-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List directoryRoles",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
