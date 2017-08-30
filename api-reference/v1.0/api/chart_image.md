# <a name="chart-image"></a><span data-ttu-id="9ee99-101">Chart: Image</span><span class="sxs-lookup"><span data-stu-id="9ee99-101">Chart: Image</span></span>

<span data-ttu-id="9ee99-102">Representa el gráfico como una imagen con codificación Base64 al escalar el gráfico a las dimensiones especificadas.</span><span class="sxs-lookup"><span data-stu-id="9ee99-102">Renders the chart as a base64-encoded image by scaling the chart to fit the specified dimensions.</span></span>
## <a name="permissions"></a><span data-ttu-id="9ee99-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="9ee99-103">Permissions</span></span>
<span data-ttu-id="9ee99-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9ee99-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9ee99-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9ee99-106">Permission type</span></span>      | <span data-ttu-id="9ee99-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9ee99-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9ee99-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9ee99-108">Delegated (work or school account)</span></span> | <span data-ttu-id="9ee99-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9ee99-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="9ee99-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9ee99-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9ee99-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ee99-111">Not supported.</span></span>    |
|<span data-ttu-id="9ee99-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9ee99-112">Application</span></span> | <span data-ttu-id="9ee99-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ee99-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9ee99-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9ee99-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts(<name>)/Image(width=0,height=0,fittingMode='fit')

```
## <a name="request-headers"></a><span data-ttu-id="9ee99-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9ee99-115">Request headers</span></span>
| <span data-ttu-id="9ee99-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="9ee99-116">Name</span></span>       | <span data-ttu-id="9ee99-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ee99-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9ee99-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="9ee99-118">Authorization</span></span>  | <span data-ttu-id="9ee99-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9ee99-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9ee99-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9ee99-121">Request body</span></span>
<span data-ttu-id="9ee99-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="9ee99-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="9ee99-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9ee99-123">Parameter</span></span>    | <span data-ttu-id="9ee99-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="9ee99-124">Type</span></span>   |<span data-ttu-id="9ee99-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ee99-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9ee99-126">height</span><span class="sxs-lookup"><span data-stu-id="9ee99-126">height</span></span>|<span data-ttu-id="9ee99-127">número</span><span class="sxs-lookup"><span data-stu-id="9ee99-127">number</span></span>|<span data-ttu-id="9ee99-p103">Opcional. Alto deseado de la imagen resultante.</span><span class="sxs-lookup"><span data-stu-id="9ee99-p103">Optional. The desired height of the resulting image.</span></span>|
|<span data-ttu-id="9ee99-130">width</span><span class="sxs-lookup"><span data-stu-id="9ee99-130">width</span></span>|<span data-ttu-id="9ee99-131">número</span><span class="sxs-lookup"><span data-stu-id="9ee99-131">number</span></span>|<span data-ttu-id="9ee99-p104">Opcional. Ancho deseado de la imagen resultante.</span><span class="sxs-lookup"><span data-stu-id="9ee99-p104">Optional. The desired width of the resulting image.</span></span>|
|<span data-ttu-id="9ee99-134">fittingMode</span><span class="sxs-lookup"><span data-stu-id="9ee99-134">fittingMode</span></span>|<span data-ttu-id="9ee99-135">string</span><span class="sxs-lookup"><span data-stu-id="9ee99-135">string</span></span>|<span data-ttu-id="9ee99-p105">Opcional. Método usado para escalar el gráfico a las dimensiones especificadas (si se han establecido el alto y el ancho)".  Valores posibles: `Fit`, `FitAndCenter`, `Fill`.</span><span class="sxs-lookup"><span data-stu-id="9ee99-p105">Optional. The method used to scale the chart to the specified to the specified dimensions (if both height and width are set)."  Possible values are: `Fit`, `FitAndCenter`, `Fill`.</span></span>|

## <a name="response"></a><span data-ttu-id="9ee99-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ee99-139">Response</span></span>

<span data-ttu-id="9ee99-140">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y la cadena de imagen en base 64 en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ee99-140">If successful, this method returns `200, OK` response code and base-64 image string in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9ee99-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ee99-141">Example</span></span>
<span data-ttu-id="9ee99-142">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9ee99-142">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="9ee99-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9ee99-143">Request</span></span>
<span data-ttu-id="9ee99-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9ee99-144">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="9ee99-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ee99-145">Response</span></span>
<span data-ttu-id="9ee99-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9ee99-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
