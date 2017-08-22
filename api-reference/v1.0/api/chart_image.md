# <a name="chart-image"></a><span data-ttu-id="3a9ee-101">Chart: Image</span><span class="sxs-lookup"><span data-stu-id="3a9ee-101">Chart: Image</span></span>

<span data-ttu-id="3a9ee-102">Representa el gráfico como una imagen con codificación Base64 al escalar el gráfico a las dimensiones especificadas.</span><span class="sxs-lookup"><span data-stu-id="3a9ee-102">Renders the chart as a base64-encoded image by scaling the chart to fit the specified dimensions.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3a9ee-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3a9ee-103">Prerequisites</span></span>
<span data-ttu-id="3a9ee-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="3a9ee-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="3a9ee-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3a9ee-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="3a9ee-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3a9ee-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts(<name>)/Image(width=0,height=0,fittingMode='fit')

```
## <a name="request-headers"></a><span data-ttu-id="3a9ee-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3a9ee-107">Request headers</span></span>
| <span data-ttu-id="3a9ee-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="3a9ee-108">Name</span></span>       | <span data-ttu-id="3a9ee-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a9ee-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="3a9ee-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="3a9ee-110">Authorization</span></span>  | <span data-ttu-id="3a9ee-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3a9ee-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="3a9ee-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3a9ee-113">Request body</span></span>
<span data-ttu-id="3a9ee-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="3a9ee-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="3a9ee-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3a9ee-115">Parameter</span></span>    | <span data-ttu-id="3a9ee-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a9ee-116">Type</span></span>   |<span data-ttu-id="3a9ee-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a9ee-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3a9ee-118">height</span><span class="sxs-lookup"><span data-stu-id="3a9ee-118">height</span></span>|<span data-ttu-id="3a9ee-119">número</span><span class="sxs-lookup"><span data-stu-id="3a9ee-119">number</span></span>|<span data-ttu-id="3a9ee-p102">Opcional. Alto deseado de la imagen resultante.</span><span class="sxs-lookup"><span data-stu-id="3a9ee-p102">Optional. The desired height of the resulting image.</span></span>|
|<span data-ttu-id="3a9ee-122">width</span><span class="sxs-lookup"><span data-stu-id="3a9ee-122">width</span></span>|<span data-ttu-id="3a9ee-123">número</span><span class="sxs-lookup"><span data-stu-id="3a9ee-123">number</span></span>|<span data-ttu-id="3a9ee-p103">Opcional. Ancho deseado de la imagen resultante.</span><span class="sxs-lookup"><span data-stu-id="3a9ee-p103">Optional. The desired width of the resulting image.</span></span>|
|<span data-ttu-id="3a9ee-126">fittingMode</span><span class="sxs-lookup"><span data-stu-id="3a9ee-126">fittingMode</span></span>|<span data-ttu-id="3a9ee-127">string</span><span class="sxs-lookup"><span data-stu-id="3a9ee-127">string</span></span>|<span data-ttu-id="3a9ee-p104">Opcional. Método usado para escalar el gráfico a las dimensiones especificadas (si se han establecido el alto y el ancho)".  Valores posibles: `Fit`, `FitAndCenter`, `Fill`.</span><span class="sxs-lookup"><span data-stu-id="3a9ee-p104">Optional. The method used to scale the chart to the specified to the specified dimensions (if both height and width are set)."  Possible values are: `Fit`, `FitAndCenter`, `Fill`.</span></span>|

## <a name="response"></a><span data-ttu-id="3a9ee-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a9ee-131">Response</span></span>

<span data-ttu-id="3a9ee-132">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y la cadena de imagen en base 64 en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a9ee-132">If successful, this method returns `200, OK` response code and base-64 image string in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3a9ee-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a9ee-133">Example</span></span>
<span data-ttu-id="3a9ee-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="3a9ee-134">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="3a9ee-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3a9ee-135">Request</span></span>
<span data-ttu-id="3a9ee-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3a9ee-136">Here is an example of the request.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/Image(width=0,height=0,fittingMode='fit')
Content-type: application/json
Content-length: 77

{
  "height": {
  },
  "width": {
  },
  "fittingMode": "fittingMode-value"
}
```

##### <a name="response"></a><span data-ttu-id="3a9ee-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a9ee-137">Response</span></span>
<span data-ttu-id="3a9ee-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3a9ee-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 3

{
"value" : "base-64 chart image string"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Chart: Image",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
