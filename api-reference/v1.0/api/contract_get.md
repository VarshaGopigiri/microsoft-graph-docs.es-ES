# <a name="get-contract"></a><span data-ttu-id="3095c-101">Obtener contrato</span><span class="sxs-lookup"><span data-stu-id="3095c-101">Get Contract</span></span>

<span data-ttu-id="3095c-102">Recupera las propiedades y las relaciones del objeto [contract](../resources/contract.md).</span><span class="sxs-lookup"><span data-stu-id="3095c-102">Retrieve the properties and relationships of [contract](../resources/contract.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="3095c-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="3095c-103">Permissions</span></span>

<span data-ttu-id="3095c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3095c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="3095c-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3095c-106">Permission type</span></span>      | <span data-ttu-id="3095c-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3095c-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3095c-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3095c-108">Delegated (work or school account)</span></span> | <span data-ttu-id="3095c-109">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="3095c-109">One of the following scopes is required to execute this API: Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="3095c-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3095c-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3095c-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3095c-111">Not supported.</span></span>    |
|<span data-ttu-id="3095c-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3095c-112">Application</span></span> | <span data-ttu-id="3095c-113">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3095c-113">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="3095c-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3095c-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /contracts/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="3095c-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3095c-115">Optional query parameters</span></span>

<span data-ttu-id="3095c-116">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3095c-116">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="3095c-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3095c-117">Request headers</span></span>

| <span data-ttu-id="3095c-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="3095c-118">Name</span></span>      |<span data-ttu-id="3095c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="3095c-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="3095c-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="3095c-120">Authorization</span></span>  | <span data-ttu-id="3095c-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3095c-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3095c-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3095c-123">Request body</span></span>

<span data-ttu-id="3095c-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3095c-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3095c-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3095c-125">Response</span></span>

<span data-ttu-id="3095c-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Contract](../resources/contract.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3095c-126">If successful, this method returns a `200 OK` response code and [Contract](../resources/contract.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3095c-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3095c-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3095c-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3095c-128">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_contract"
}-->
```http
GET https://graph.microsoft.com/v1.0/contracts/{id}
```

##### <a name="response"></a><span data-ttu-id="3095c-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3095c-129">Response</span></span>
<span data-ttu-id="3095c-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3095c-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.Contract"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 186

{
  "contractType": "contractType-value",
  "customerId": "customerId-value",
  "defaultDomainName": "defaultDomainName-value",
  "displayName": "displayName-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get Contract",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->