# <a name="range-intersection"></a><span data-ttu-id="104a9-101">Range: Intersection</span><span class="sxs-lookup"><span data-stu-id="104a9-101">Range: Intersection</span></span>

<span data-ttu-id="104a9-102">Obtiene el objeto de intervalo que representa la intersección rectangular de los intervalos especificados.</span><span class="sxs-lookup"><span data-stu-id="104a9-102">Gets the range object that represents the rectangular intersection of the given ranges.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="104a9-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="104a9-103">Prerequisites</span></span>
<span data-ttu-id="104a9-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="104a9-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="104a9-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="104a9-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="104a9-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="104a9-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/Intersection
GET /workbook/worksheets/{id|name}/range(<address>)/Intersection
GET /workbook/tables/{id|name}/columns/{id|name}/range/Intersection

```
## <a name="request-headers"></a><span data-ttu-id="104a9-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="104a9-107">Request headers</span></span>
| <span data-ttu-id="104a9-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="104a9-108">Name</span></span>       | <span data-ttu-id="104a9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="104a9-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="104a9-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="104a9-110">Authorization</span></span>  | <span data-ttu-id="104a9-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="104a9-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="104a9-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="104a9-113">Request body</span></span>
<span data-ttu-id="104a9-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="104a9-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="104a9-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="104a9-115">Parameter</span></span>    | <span data-ttu-id="104a9-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="104a9-116">Type</span></span>   |<span data-ttu-id="104a9-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="104a9-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="104a9-118">anotherRange</span><span class="sxs-lookup"><span data-stu-id="104a9-118">anotherRange</span></span>|<span data-ttu-id="104a9-119">string</span><span class="sxs-lookup"><span data-stu-id="104a9-119">string</span></span>|<span data-ttu-id="104a9-120">Objeto de intervalo o dirección de intervalo que se usará para determinar la intersección de los intervalos.</span><span class="sxs-lookup"><span data-stu-id="104a9-120">The range object or range address that will be used to determine the intersection of ranges.</span></span>|

## <a name="response"></a><span data-ttu-id="104a9-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="104a9-121">Response</span></span>

<span data-ttu-id="104a9-122">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="104a9-122">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="104a9-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="104a9-123">Example</span></span>
<span data-ttu-id="104a9-124">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="104a9-124">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="104a9-125">Solicitud</span><span class="sxs-lookup"><span data-stu-id="104a9-125">Request</span></span>
<span data-ttu-id="104a9-126">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="104a9-126">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_intersection"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/Intersection
Content-type: application/json
Content-length: 42

{
  "anotherRange": "anotherRange-value"
}
```

##### <a name="response"></a><span data-ttu-id="104a9-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="104a9-127">Response</span></span>
<span data-ttu-id="104a9-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="104a9-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 169

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnIndex": 99,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: Intersection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->