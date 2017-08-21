# <a name="worksheet-usedrange"></a><span data-ttu-id="158ad-101">Worksheet: UsedRange</span><span class="sxs-lookup"><span data-stu-id="158ad-101">Worksheet: UsedRange</span></span>

<span data-ttu-id="158ad-p101">El rango usado es el rango más pequeño que abarque las celdas que tienen asignado un valor o un formato. Si la hoja de cálculo está en blanco, esta función devolverá la celda superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="158ad-p101">The used range is the smallest range that encompasses any cells that have a value or formatting assigned to them. If the worksheet is blank, this function will return the top left cell.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="158ad-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="158ad-104">Prerequisites</span></span>
<span data-ttu-id="158ad-105">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="158ad-105">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="158ad-106">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="158ad-106">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="158ad-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="158ad-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/UsedRange

```

## <a name="optional-request-parameter"></a><span data-ttu-id="158ad-108">Parámetro de solicitud opcional</span><span class="sxs-lookup"><span data-stu-id="158ad-108">Optional request parameter</span></span>
<span data-ttu-id="158ad-109">En la URL de solicitud, proporcione un parámetro de consulta opcional.</span><span class="sxs-lookup"><span data-stu-id="158ad-109">In the request URL, provide an optional query parameter.</span></span>

| <span data-ttu-id="158ad-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="158ad-110">Parameter</span></span>    | <span data-ttu-id="158ad-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="158ad-111">Type</span></span>   |<span data-ttu-id="158ad-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="158ad-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="158ad-113">valuesOnly</span><span class="sxs-lookup"><span data-stu-id="158ad-113">valuesOnly</span></span>|<span data-ttu-id="158ad-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="158ad-114">Boolean</span></span>|<span data-ttu-id="158ad-p102">Opcional. Solo tiene en cuenta las celdas con valores como celdas usadas (ignora el formato).</span><span class="sxs-lookup"><span data-stu-id="158ad-p102">Optional. Considers only cells with values as used cells (ignores formatting).</span></span>|


## <a name="request-headers"></a><span data-ttu-id="158ad-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="158ad-117">Request headers</span></span>
| <span data-ttu-id="158ad-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="158ad-118">Name</span></span>       | <span data-ttu-id="158ad-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="158ad-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="158ad-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="158ad-120">Authorization</span></span>  | <span data-ttu-id="158ad-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="158ad-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="158ad-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="158ad-123">Response</span></span>

<span data-ttu-id="158ad-124">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="158ad-124">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="158ad-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="158ad-125">Example</span></span>
<span data-ttu-id="158ad-126">Aquí tiene un ejemplo que muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="158ad-126">Here is an example that shows how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="158ad-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="158ad-127">Request</span></span>
<span data-ttu-id="158ad-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="158ad-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheet_usedrange"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/UsedRange(valuesOnly=true)
Content-type: application/json

```

##### <a name="response"></a><span data-ttu-id="158ad-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="158ad-129">Response</span></span>
<span data-ttu-id="158ad-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="158ad-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Worksheet: UsedRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
