# <a name="range-boundingrect"></a><span data-ttu-id="2b689-101">Range: BoundingRect</span><span class="sxs-lookup"><span data-stu-id="2b689-101">Range: BoundingRect</span></span>

<span data-ttu-id="2b689-p101">Obtiene el objeto de intervalo más pequeño que abarca los intervalos especificados. Por ejemplo, el valor GetBoundingRect de "B2:C5" y "D10:E15" es "B2:E16".</span><span class="sxs-lookup"><span data-stu-id="2b689-p101">Gets the smallest range object that encompasses the given ranges. For example, the GetBoundingRect of "B2:C5" and "D10:E15" is "B2:E16".</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2b689-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2b689-104">Prerequisites</span></span>
<span data-ttu-id="2b689-105">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="2b689-105">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="2b689-106">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2b689-106">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="2b689-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2b689-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/BoundingRect
GET /workbook/worksheets/{id|name}/range(<address>)/BoundingRect
GET /workbook/tables/{id|name}/columns/{id|name}/range/BoundingRect

```
## <a name="request-headers"></a><span data-ttu-id="2b689-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2b689-108">Request headers</span></span>
| <span data-ttu-id="2b689-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="2b689-109">Name</span></span>       | <span data-ttu-id="2b689-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b689-110">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="2b689-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="2b689-111">Authorization</span></span>  | <span data-ttu-id="2b689-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b689-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="2b689-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2b689-114">Request body</span></span>
<span data-ttu-id="2b689-115">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="2b689-115">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="2b689-116">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2b689-116">Parameter</span></span>    | <span data-ttu-id="2b689-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b689-117">Type</span></span>   |<span data-ttu-id="2b689-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b689-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2b689-119">anotherRange</span><span class="sxs-lookup"><span data-stu-id="2b689-119">anotherRange</span></span>|<span data-ttu-id="2b689-120">string</span><span class="sxs-lookup"><span data-stu-id="2b689-120">string</span></span>|<span data-ttu-id="2b689-121">Objeto o dirección de intervalo o nombre de intervalo.</span><span class="sxs-lookup"><span data-stu-id="2b689-121">The range object or address or range name.</span></span>|

## <a name="response"></a><span data-ttu-id="2b689-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b689-122">Response</span></span>

<span data-ttu-id="2b689-123">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2b689-123">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2b689-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2b689-124">Example</span></span>
<span data-ttu-id="2b689-125">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2b689-125">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="2b689-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b689-126">Request</span></span>
<span data-ttu-id="2b689-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2b689-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_boundingrect"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/BoundingRect
Content-type: application/json
Content-length: 42

{
  "anotherRange": "anotherRange-value"
}
```

##### <a name="response"></a><span data-ttu-id="2b689-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b689-128">Response</span></span>
<span data-ttu-id="2b689-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b689-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: BoundingRect",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->