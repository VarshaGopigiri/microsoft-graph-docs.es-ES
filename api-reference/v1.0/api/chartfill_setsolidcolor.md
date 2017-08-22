# <a name="chartfill-setsolidcolor"></a><span data-ttu-id="ddfcb-101">ChartFill: setSolidColor</span><span class="sxs-lookup"><span data-stu-id="ddfcb-101">ChartFill: setSolidColor</span></span>

<span data-ttu-id="ddfcb-102">Establece el formato de relleno de un elemento de gráfico en un color uniforme.</span><span class="sxs-lookup"><span data-stu-id="ddfcb-102">Sets the fill formatting of a chart element to a uniform color.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ddfcb-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ddfcb-103">Prerequisites</span></span>
<span data-ttu-id="ddfcb-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="ddfcb-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="ddfcb-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ddfcb-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="ddfcb-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ddfcb-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/format/fill/setSolidColor
POST /workbook/worksheets/{id|name}/charts(<name>)/title/format/fill/setSolidColor
POST /workbook/worksheets/{id|name}/charts(<name>)/legend/format/fill/setSolidColor

```
## <a name="request-headers"></a><span data-ttu-id="ddfcb-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ddfcb-107">Request headers</span></span>
| <span data-ttu-id="ddfcb-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="ddfcb-108">Name</span></span>       | <span data-ttu-id="ddfcb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddfcb-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="ddfcb-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="ddfcb-110">Authorization</span></span>  | <span data-ttu-id="ddfcb-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ddfcb-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="ddfcb-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ddfcb-113">Request body</span></span>
<span data-ttu-id="ddfcb-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="ddfcb-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="ddfcb-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ddfcb-115">Parameter</span></span>    | <span data-ttu-id="ddfcb-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="ddfcb-116">Type</span></span>   |<span data-ttu-id="ddfcb-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddfcb-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ddfcb-118">color</span><span class="sxs-lookup"><span data-stu-id="ddfcb-118">color</span></span>|<span data-ttu-id="ddfcb-119">string</span><span class="sxs-lookup"><span data-stu-id="ddfcb-119">string</span></span>|<span data-ttu-id="ddfcb-120">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="ddfcb-120">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange").</span></span>|

## <a name="response"></a><span data-ttu-id="ddfcb-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ddfcb-121">Response</span></span>

<span data-ttu-id="ddfcb-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ddfcb-p102">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ddfcb-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ddfcb-124">Example</span></span>
<span data-ttu-id="ddfcb-125">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="ddfcb-125">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="ddfcb-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ddfcb-126">Request</span></span>
<span data-ttu-id="ddfcb-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ddfcb-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartfill_setsolidcolor"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/format/fill/setSolidColor
Content-type: application/json
Content-length: 28

{
  "color": "color-value"
}
```

##### <a name="response"></a><span data-ttu-id="ddfcb-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ddfcb-128">Response</span></span>
<span data-ttu-id="ddfcb-129">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ddfcb-129">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartFill: setSolidColor",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->