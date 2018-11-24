# <a name="list-grouplifecyclepolicies"></a><span data-ttu-id="f0d0d-101">Mostrar groupLifecyclePolicies</span><span class="sxs-lookup"><span data-stu-id="f0d0d-101">List groupLifecyclePolicies</span></span>

<span data-ttu-id="f0d0d-102">Muestra todos los objetos [groupLifecyclePolicies](../resources/grouplifecyclepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="f0d0d-102">List all the [groupLifecyclePolicies](../resources/grouplifecyclepolicy.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="f0d0d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="f0d0d-103">Permissions</span></span>

<span data-ttu-id="f0d0d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f0d0d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="f0d0d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f0d0d-106">Permission type</span></span>      | <span data-ttu-id="f0d0d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f0d0d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f0d0d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f0d0d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="f0d0d-109">Directory.Read.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f0d0d-109">Directory.Read.All or Directory.ReadWrite.All</span></span> |
|<span data-ttu-id="f0d0d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f0d0d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f0d0d-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f0d0d-111">Not supported.</span></span>    |
|<span data-ttu-id="f0d0d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f0d0d-112">Application</span></span> | <span data-ttu-id="f0d0d-113">Directory.Read.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f0d0d-113">Directory.Read.All or Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f0d0d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f0d0d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groupLifecyclePolicies
```
## <a name="optional-query-parameters"></a><span data-ttu-id="f0d0d-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f0d0d-115">Optional query parameters</span></span>
<span data-ttu-id="f0d0d-116">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f0d0d-116">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f0d0d-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f0d0d-117">Request headers</span></span>
| <span data-ttu-id="f0d0d-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="f0d0d-118">Name</span></span> | <span data-ttu-id="f0d0d-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0d0d-119">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="f0d0d-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="f0d0d-120">Authorization</span></span> | <span data-ttu-id="f0d0d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f0d0d-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f0d0d-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f0d0d-123">Request body</span></span>
<span data-ttu-id="f0d0d-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f0d0d-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f0d0d-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f0d0d-125">Response</span></span>

<span data-ttu-id="f0d0d-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f0d0d-126">If successful, this method returns a `200 OK` response code and a collection of [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f0d0d-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f0d0d-127">Example</span></span>

##### <a name="request"></a><span data-ttu-id="f0d0d-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f0d0d-128">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_grouplifecyclepolicy"
}-->
```http
GET https://graph.microsoft.com/v1.0/groupLifecyclePolicies
```
##### <a name="response"></a><span data-ttu-id="f0d0d-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f0d0d-129">Response</span></span>

<span data-ttu-id="f0d0d-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f0d0d-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupLifecyclePolicy",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 223

{
  "value": [
    {
      "id": "ffffffff-ffff-ffff-ffff-ffffffffffff",
      "groupLifetimeInDays": 100,
      "managedGroupTypes": "Selected",
      "alternateNotificationEmails": "admin@contoso.com"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List groupLifecyclePolicies",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->