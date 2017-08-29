# <a name="list-contracts"></a><span data-ttu-id="0e957-101">Enumerar contratos</span><span class="sxs-lookup"><span data-stu-id="0e957-101">List contracts</span></span>

<span data-ttu-id="0e957-102">Recupera una lista de objetos [contract](../resources/contract.md) asociados a un inquilino de partner.</span><span class="sxs-lookup"><span data-stu-id="0e957-102">Retrieve a list of [contract](../resources/contract.md) objects associated to a partner tenant.</span></span>

## <a name="permissions"></a><span data-ttu-id="0e957-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="0e957-103">Permissions</span></span>

<span data-ttu-id="0e957-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0e957-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="0e957-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0e957-106">Permission type</span></span>      | <span data-ttu-id="0e957-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0e957-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="0e957-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0e957-108">Delegated (work or school account)</span></span> | <span data-ttu-id="0e957-109">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="0e957-109">One of the following scopes is required to execute this API: Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All</span></span>    | 
|<span data-ttu-id="0e957-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0e957-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0e957-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e957-111">Not supported.</span></span>    | 
|<span data-ttu-id="0e957-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0e957-112">Application</span></span> | <span data-ttu-id="0e957-113">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0e957-113">Directory.Read.All, Directory.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="0e957-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0e957-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

```http
GET /contracts
```

## <a name="optional-query-parameters"></a><span data-ttu-id="0e957-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0e957-115">Optional query parameters</span></span>

<span data-ttu-id="0e957-116">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e957-116">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span> 

> <span data-ttu-id="0e957-117">El filtrado es compatible con customerId, defaultDomainName y displayName.</span><span class="sxs-lookup"><span data-stu-id="0e957-117">Filtering is supported for customerId, defaultDomainName, and displayName.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0e957-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0e957-118">Request headers</span></span>

| <span data-ttu-id="0e957-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="0e957-119">Name</span></span>      |<span data-ttu-id="0e957-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e957-120">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="0e957-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="0e957-121">Authorization</span></span>  | <span data-ttu-id="0e957-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0e957-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0e957-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0e957-124">Request body</span></span>

<span data-ttu-id="0e957-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0e957-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0e957-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e957-126">Response</span></span>

<span data-ttu-id="0e957-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Contract](../resources/contract.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e957-127">If successful, this method returns a `200 OK` response code and a collection of [Contract](../resources/contract.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0e957-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e957-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0e957-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0e957-129">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_contract"
}-->
```http
GET https://graph.microsoft.com/v1.0/contracts
```

##### <a name="response"></a><span data-ttu-id="0e957-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e957-130">Response</span></span>

<span data-ttu-id="0e957-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0e957-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.Contract",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
    {
      "contractType": "contractType-value",
      "customerId": "customerId-value",
      "defaultDomainName": "defaultDomainName-value",
      "displayName": "displayName-value",
      "id": "id-value"
    }
  ]
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