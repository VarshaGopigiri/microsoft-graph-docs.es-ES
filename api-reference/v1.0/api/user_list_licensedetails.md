# <a name="list-licensedetails"></a><span data-ttu-id="c1e92-101">Enumerar licenseDetails</span><span class="sxs-lookup"><span data-stu-id="c1e92-101">List licenseDetails</span></span>

<span data-ttu-id="c1e92-102">Recupere una lista de objetos licenseDetails.</span><span class="sxs-lookup"><span data-stu-id="c1e92-102">Retrieve a list of licenseDetails objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c1e92-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c1e92-103">Prerequisites</span></span>
<span data-ttu-id="c1e92-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *User.Read*; *User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="c1e92-104">One of the following **scopes** is required to execute this API: *User.Read*; *User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="c1e92-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c1e92-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/licenseDetails
GET /users/{id}/licenseDetails
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c1e92-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c1e92-106">Optional query parameters</span></span>
<span data-ttu-id="c1e92-107">Este método **no** admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters).</span><span class="sxs-lookup"><span data-stu-id="c1e92-107">This method does **not** support [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters).</span></span>

## <a name="request-headers"></a><span data-ttu-id="c1e92-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c1e92-108">Request headers</span></span>
| <span data-ttu-id="c1e92-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="c1e92-109">Name</span></span>      |<span data-ttu-id="c1e92-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1e92-110">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="c1e92-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="c1e92-111">Authorization</span></span>  | <span data-ttu-id="c1e92-112">&lt;código&gt; de portador</span><span class="sxs-lookup"><span data-stu-id="c1e92-112">Bearer &lt;code&gt;</span></span>|

## <a name="request-body"></a><span data-ttu-id="c1e92-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c1e92-113">Request body</span></span>
<span data-ttu-id="c1e92-114">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c1e92-114">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c1e92-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c1e92-115">Response</span></span>

<span data-ttu-id="c1e92-116">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [licenseDetails](../resources/licensedetails.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c1e92-116">If successful, this method returns a `200 OK` response code and collection of [licenseDetails](../resources/licensedetails.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c1e92-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c1e92-117">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c1e92-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c1e92-118">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_licensedetails"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/licenseDetails
```
##### <a name="response"></a><span data-ttu-id="c1e92-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c1e92-119">Response</span></span>
<span data-ttu-id="c1e92-p101">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c1e92-p101">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.licenseDetails",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 389

{
  "value": [
    {
      "servicePlans": [
        {
          "servicePlanId": "servicePlanId-value",
          "servicePlanName": "servicePlanName-value",
          "provisioningStatus": "provisioningStatus-value",
          "appliesTo": "appliesTo-value"
        }
      ],
      "skuId": "skuId-value",
      "skuPartNumber": "skuPartNumber-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List licenseDetails",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->