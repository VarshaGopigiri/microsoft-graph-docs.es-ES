# <a name="worksheet-range"></a><span data-ttu-id="d6667-101">Worksheet: Range</span><span class="sxs-lookup"><span data-stu-id="d6667-101">Worksheet: Range</span></span>

<span data-ttu-id="d6667-102">Obtiene el objeto de intervalo especificado por la dirección o el nombre.</span><span class="sxs-lookup"><span data-stu-id="d6667-102">Gets the range object specified by the address or name.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d6667-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d6667-103">Prerequisites</span></span>
<span data-ttu-id="d6667-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="d6667-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="d6667-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d6667-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="d6667-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d6667-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/Range

```
## <a name="request-headers"></a><span data-ttu-id="d6667-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d6667-107">Request headers</span></span>
| <span data-ttu-id="d6667-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="d6667-108">Name</span></span>       | <span data-ttu-id="d6667-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6667-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d6667-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="d6667-110">Authorization</span></span>  | <span data-ttu-id="d6667-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d6667-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="d6667-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d6667-113">Request body</span></span>
<span data-ttu-id="d6667-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="d6667-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d6667-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d6667-115">Parameter</span></span>    | <span data-ttu-id="d6667-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6667-116">Type</span></span>   |<span data-ttu-id="d6667-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6667-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d6667-118">address</span><span class="sxs-lookup"><span data-stu-id="d6667-118">address</span></span>|<span data-ttu-id="d6667-119">string</span><span class="sxs-lookup"><span data-stu-id="d6667-119">string</span></span>|<span data-ttu-id="d6667-p102">Opcional. Dirección o nombre del intervalo. Si no se especifica, se devuelve todo el intervalo de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="d6667-p102">Optional. The address or the name of the range. If not specified, the entire worksheet range is returned.</span></span>|

## <a name="response"></a><span data-ttu-id="d6667-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6667-123">Response</span></span>

<span data-ttu-id="d6667-124">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6667-124">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d6667-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d6667-125">Example</span></span>
<span data-ttu-id="d6667-126">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d6667-126">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="d6667-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d6667-127">Request</span></span>
<span data-ttu-id="d6667-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d6667-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheet_range"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/Range
Content-type: application/json
Content-length: 32

{
  "address": "address-value"
}
```

##### <a name="response"></a><span data-ttu-id="d6667-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6667-129">Response</span></span>
<span data-ttu-id="d6667-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d6667-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Worksheet: Range",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->