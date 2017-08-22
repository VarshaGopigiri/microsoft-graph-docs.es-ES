# <a name="get-contract"></a><span data-ttu-id="f86a2-101">Obtener contrato</span><span class="sxs-lookup"><span data-stu-id="f86a2-101">Get Contract</span></span>

<span data-ttu-id="f86a2-102">Recupera las propiedades y las relaciones del objeto [contract](../resources/contract.md).</span><span class="sxs-lookup"><span data-stu-id="f86a2-102">Retrieve the properties and relationships of [contract](../resources/contract.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f86a2-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f86a2-103">Prerequisites</span></span>

<span data-ttu-id="f86a2-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All*, *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="f86a2-104">One of the following **scopes** are required to execute this API: *Directory.Read.All*, *Directory.ReadWrite.All*, or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="f86a2-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f86a2-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /contracts/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f86a2-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f86a2-106">Optional query parameters</span></span>

<span data-ttu-id="f86a2-107">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f86a2-107">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f86a2-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f86a2-108">Request headers</span></span>

| <span data-ttu-id="f86a2-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="f86a2-109">Name</span></span>      |<span data-ttu-id="f86a2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f86a2-110">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="f86a2-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="f86a2-111">Authorization</span></span>  | <span data-ttu-id="f86a2-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f86a2-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f86a2-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f86a2-114">Request body</span></span>

<span data-ttu-id="f86a2-115">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f86a2-115">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f86a2-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f86a2-116">Response</span></span>

<span data-ttu-id="f86a2-117">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Contract](../resources/contract.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f86a2-117">If successful, this method returns a `200 OK` response code and [Contract](../resources/contract.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f86a2-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f86a2-118">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f86a2-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f86a2-119">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_contract"
}-->
```http
GET https://graph.microsoft.com/v1.0/contracts/{id}
```

##### <a name="response"></a><span data-ttu-id="f86a2-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f86a2-120">Response</span></span>
<span data-ttu-id="f86a2-p102">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f86a2-p102">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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