# <a name="list-contracts"></a><span data-ttu-id="ba69d-101">Enumerar contratos</span><span class="sxs-lookup"><span data-stu-id="ba69d-101">List contracts</span></span>

<span data-ttu-id="ba69d-102">Recupere una lista de objetos [contract](../resources/contract.md) asociados a un inquilino de partner.</span><span class="sxs-lookup"><span data-stu-id="ba69d-102">Retrieve a list of [contract](../resources/contract.md) objects associated to a partner tenant.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ba69d-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ba69d-103">Prerequisites</span></span>

<span data-ttu-id="ba69d-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All*, *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="ba69d-104">One of the following **scopes** are required to execute this API: *Directory.Read.All*, *Directory.ReadWrite.All*, or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="ba69d-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ba69d-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

```http
GET /contracts
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ba69d-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ba69d-106">Optional query parameters</span></span>

<span data-ttu-id="ba69d-107">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba69d-107">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span> 

> <span data-ttu-id="ba69d-108">El filtrado es compatible con customerId, defaultDomainName y displayName.</span><span class="sxs-lookup"><span data-stu-id="ba69d-108">Filtering is supported for customerId, defaultDomainName, and displayName.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ba69d-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ba69d-109">Request headers</span></span>

| <span data-ttu-id="ba69d-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="ba69d-110">Name</span></span>      |<span data-ttu-id="ba69d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba69d-111">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="ba69d-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="ba69d-112">Authorization</span></span>  | <span data-ttu-id="ba69d-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ba69d-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ba69d-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ba69d-115">Request body</span></span>

<span data-ttu-id="ba69d-116">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ba69d-116">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ba69d-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba69d-117">Response</span></span>

<span data-ttu-id="ba69d-118">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Contract](../resources/contract.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba69d-118">If successful, this method returns a `200 OK` response code and a collection of [Contract](../resources/contract.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ba69d-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ba69d-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ba69d-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ba69d-120">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_contract"
}-->
```http
GET https://graph.microsoft.com/v1.0/contracts
```

##### <a name="response"></a><span data-ttu-id="ba69d-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba69d-121">Response</span></span>

<span data-ttu-id="ba69d-p102">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ba69d-p102">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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