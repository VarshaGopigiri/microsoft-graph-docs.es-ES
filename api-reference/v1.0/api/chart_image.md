# <a name="chart-image"></a><span data-ttu-id="c407d-101">Chart: Image</span><span class="sxs-lookup"><span data-stu-id="c407d-101">Chart: Image</span></span>

<span data-ttu-id="c407d-102">Representa el gráfico como una imagen con codificación Base64 al escalar el gráfico a las dimensiones especificadas.</span><span class="sxs-lookup"><span data-stu-id="c407d-102">Renders the chart as a base64-encoded image by scaling the chart to fit the specified dimensions.</span></span>
## <a name="permissions"></a><span data-ttu-id="c407d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="c407d-103">Permissions</span></span>
<span data-ttu-id="c407d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c407d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c407d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c407d-106">Permission type</span></span>      | <span data-ttu-id="c407d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c407d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c407d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c407d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="c407d-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c407d-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c407d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c407d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c407d-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c407d-111">Not supported.</span></span>    |
|<span data-ttu-id="c407d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c407d-112">Application</span></span> | <span data-ttu-id="c407d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c407d-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c407d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c407d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts(<name>)/Image(width=0,height=0,fittingMode='fit')

```
## <a name="request-headers"></a><span data-ttu-id="c407d-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c407d-115">Request headers</span></span>
| <span data-ttu-id="c407d-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="c407d-116">Name</span></span>       | <span data-ttu-id="c407d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c407d-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="c407d-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="c407d-118">Authorization</span></span>  | <span data-ttu-id="c407d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c407d-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c407d-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c407d-121">Request body</span></span>
<span data-ttu-id="c407d-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="c407d-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c407d-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c407d-123">Parameter</span></span>    | <span data-ttu-id="c407d-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="c407d-124">Type</span></span>   |<span data-ttu-id="c407d-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="c407d-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c407d-126">height</span><span class="sxs-lookup"><span data-stu-id="c407d-126">height</span></span>|<span data-ttu-id="c407d-127">número</span><span class="sxs-lookup"><span data-stu-id="c407d-127">number</span></span>|<span data-ttu-id="c407d-p103">Opcional. Alto deseado de la imagen resultante.</span><span class="sxs-lookup"><span data-stu-id="c407d-p103">Optional. The desired height of the resulting image.</span></span>|
|<span data-ttu-id="c407d-130">width</span><span class="sxs-lookup"><span data-stu-id="c407d-130">width</span></span>|<span data-ttu-id="c407d-131">número</span><span class="sxs-lookup"><span data-stu-id="c407d-131">number</span></span>|<span data-ttu-id="c407d-p104">Opcional. Ancho deseado de la imagen resultante.</span><span class="sxs-lookup"><span data-stu-id="c407d-p104">Optional. The desired width of the resulting image.</span></span>|
|<span data-ttu-id="c407d-134">fittingMode</span><span class="sxs-lookup"><span data-stu-id="c407d-134">fittingMode</span></span>|<span data-ttu-id="c407d-135">string</span><span class="sxs-lookup"><span data-stu-id="c407d-135">string</span></span>|<span data-ttu-id="c407d-p105">Opcional. Método usado para escalar el gráfico a las dimensiones especificadas (si se han establecido el alto y el ancho)".  Valores posibles: `Fit`, `FitAndCenter`, `Fill`.</span><span class="sxs-lookup"><span data-stu-id="c407d-p105">Optional. The method used to scale the chart to the specified to the specified dimensions (if both height and width are set)."  Possible values are: `Fit`, `FitAndCenter`, `Fill`.</span></span>|

## <a name="response"></a><span data-ttu-id="c407d-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c407d-139">Response</span></span>

<span data-ttu-id="c407d-140">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la cadena de imagen en base 64 en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c407d-140">If successful, this method returns `200 OK` response code and base-64 image string in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c407d-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c407d-141">Example</span></span>
<span data-ttu-id="c407d-142">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c407d-142">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c407d-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c407d-143">Request</span></span>
<span data-ttu-id="c407d-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c407d-144">Here is an example of the request.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/Image(width=0,height=0,fittingMode='fit')
```

##### <a name="response"></a><span data-ttu-id="c407d-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c407d-145">Response</span></span>
<span data-ttu-id="c407d-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c407d-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
Content-type: application/json;odata.metadata=minimal;odata.streaming=true

{
"value" : "base-64 chart image string"
}
```

## <a name="usage"></a><span data-ttu-id="c407d-149">Uso</span><span class="sxs-lookup"><span data-stu-id="c407d-149">Usage</span></span>

<span data-ttu-id="c407d-150">Puede mostrar la cadena en base 64 en una etiqueta de imagen HTML: `<img src="data:image/png;base64,{base-64 chart image string}/>`.</span><span class="sxs-lookup"><span data-stu-id="c407d-150">You can display the base-64 string inside an HTML image tag: `<img src="data:image/png;base64,{base-64 chart image string}/>`.</span></span>

<span data-ttu-id="c407d-151">Para usar el comportamiento predeterminado, utilice `Image(width=0,height=0,fittingMode='fit')`.</span><span class="sxs-lookup"><span data-stu-id="c407d-151">For default behavior, use `Image(width=0,height=0,fittingMode='fit')`.</span></span> <span data-ttu-id="c407d-152">Este es un ejemplo de una imagen de gráfico devuelta con los parámetros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="c407d-152">Here is an example of a chart image returned with the default parameters.</span></span>

![Imagen de gráfico de Excel con alto y ancho predeterminados.](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/GetChart-default.png)

<span data-ttu-id="c407d-154">Si quiere personalizar la visualización de la imagen, especifique un alto, un ancho y un modo de ajuste.</span><span class="sxs-lookup"><span data-stu-id="c407d-154">If you want to customize the display of the image, specify a height, width, and a fitting mode.</span></span> <span data-ttu-id="c407d-155">Esta es la misma imagen de gráfico si la recupera con estos parámetros: `Image(width=500,height=500,fittingMode='Fill')`.</span><span class="sxs-lookup"><span data-stu-id="c407d-155">Here is what the same chart image looks like if you retrieve it with these parameters: `Image(width=500,height=500,fittingMode='Fill')`.</span></span>

![Imagen de gráfico de Excel con alto y ancho predeterminados.](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/GetChart-fill.png)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Chart: Image",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
