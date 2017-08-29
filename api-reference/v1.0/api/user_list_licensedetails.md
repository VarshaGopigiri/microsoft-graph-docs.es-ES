# <a name="list-licensedetails"></a><span data-ttu-id="562f4-101">Enumerar licenseDetails</span><span class="sxs-lookup"><span data-stu-id="562f4-101">List licenseDetails</span></span>

<span data-ttu-id="562f4-102">Recupera una lista de objetos licenseDetails.</span><span class="sxs-lookup"><span data-stu-id="562f4-102">Retrieve a list of licenseDetails objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="562f4-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="562f4-103">Permissions</span></span>
<span data-ttu-id="562f4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="562f4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="562f4-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="562f4-106">Permission type</span></span>      | <span data-ttu-id="562f4-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="562f4-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="562f4-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="562f4-108">Delegated (work or school account)</span></span> | <span data-ttu-id="562f4-109">User.Read, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="562f4-109">One of the following scopes is required to execute this API: User.Read; User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All</span></span>    | 
|<span data-ttu-id="562f4-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="562f4-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="562f4-111">User.Read</span><span class="sxs-lookup"><span data-stu-id="562f4-111">User.Read</span></span>    | 
|<span data-ttu-id="562f4-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="562f4-112">Application</span></span> | <span data-ttu-id="562f4-113">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="562f4-113">One of the following scopes is required to execute this API: User.Read.All; User.ReadWrite.All; Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="562f4-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="562f4-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/licenseDetails
GET /users/{id}/licenseDetails
```
## <a name="optional-query-parameters"></a><span data-ttu-id="562f4-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="562f4-115">Optional query parameters</span></span>
<span data-ttu-id="562f4-116">Este método **no** admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters).</span><span class="sxs-lookup"><span data-stu-id="562f4-116">This method does **not** support [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters).</span></span>

## <a name="request-headers"></a><span data-ttu-id="562f4-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="562f4-117">Request headers</span></span>
| <span data-ttu-id="562f4-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="562f4-118">Name</span></span>      |<span data-ttu-id="562f4-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="562f4-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="562f4-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="562f4-120">Authorization</span></span>  | <span data-ttu-id="562f4-121">&lt;código&gt; de portador</span><span class="sxs-lookup"><span data-stu-id="562f4-121">Bearer &lt;code&gt;</span></span>|

## <a name="request-body"></a><span data-ttu-id="562f4-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="562f4-122">Request body</span></span>
<span data-ttu-id="562f4-123">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="562f4-123">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="562f4-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="562f4-124">Response</span></span>

<span data-ttu-id="562f4-125">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [licenseDetails](../resources/licensedetails.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="562f4-125">If successful, this method returns a `200 OK` response code and collection of [licenseDetails](../resources/licensedetails.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="562f4-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="562f4-126">Example</span></span>
##### <a name="request"></a><span data-ttu-id="562f4-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="562f4-127">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_licensedetails"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/licenseDetails
```
##### <a name="response"></a><span data-ttu-id="562f4-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="562f4-128">Response</span></span>
<span data-ttu-id="562f4-p102">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="562f4-p102">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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