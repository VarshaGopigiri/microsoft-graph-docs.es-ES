# <a name="display-a-chart-image-in-excel-with-microsoft-graph"></a><span data-ttu-id="c29ee-101">Mostrar una imagen de gráfico de Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="c29ee-101">Display a chart image in Excel with Microsoft Graph</span></span>

<span data-ttu-id="c29ee-102">Al realizar una [operación GET para recuperar una imagen de gráfico](/api-reference/v1.0/api/chart_image.md), la API de Excel devuelve una imagen como una cadena Base 64.</span><span class="sxs-lookup"><span data-stu-id="c29ee-102">When you perform a [GET operation to retrieve a chart image](/api-reference/v1.0/api/chart_image.md), the Excel API returns the image as a base-64 string.</span></span>

<span data-ttu-id="c29ee-103">Puede mostrar la cadena Base 64 en una etiqueta de imagen HTML: `<img src="data:image/png;base64,{base-64 chart image string}/>`.</span><span class="sxs-lookup"><span data-stu-id="c29ee-103">You can display the base-64 string inside an HTML image tag: `<img src="data:image/png;base64,{base-64 chart image string}/>`.</span></span>

<span data-ttu-id="c29ee-104">Para usar el comportamiento predeterminado, utilice `Image(width=0,height=0,fittingMode='fit')`.</span><span class="sxs-lookup"><span data-stu-id="c29ee-104">For default behavior, use `Image(width=0,height=0,fittingMode='fit')`.</span></span> <span data-ttu-id="c29ee-105">Este es un ejemplo de una imagen de gráfico devuelta con los parámetros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="c29ee-105">Here is an example of a chart image returned with the default parameters.</span></span>

![Imagen de gráfico de Excel con alto y ancho predeterminados.](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/GetChart-default.png)

<span data-ttu-id="c29ee-107">Si quiere personalizar la visualización de la imagen, especifique un alto, un ancho y un modo de ajuste.</span><span class="sxs-lookup"><span data-stu-id="c29ee-107">If you want to customize the display of the image, specify a height, width, and a fitting mode.</span></span> <span data-ttu-id="c29ee-108">Esta es la apariencia de la misma imagen de gráfico si la recupera con estos parámetros: `Image(width=500,height=500,fittingMode='Fill')`.</span><span class="sxs-lookup"><span data-stu-id="c29ee-108">Here is what the same chart image looks like if you retrieve it with these parameters: `Image(width=500,height=500,fittingMode='Fill')`.</span></span>

## <a name="see-also"></a><span data-ttu-id="c29ee-109">Vea también</span><span class="sxs-lookup"><span data-stu-id="c29ee-109">See also</span></span>

* [<span data-ttu-id="c29ee-110">Administrar sesiones en Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="c29ee-110">Manage sessions in Excel with Microsoft Graph</span></span>](excel-manage-sessions.md)
* [<span data-ttu-id="c29ee-111">Escribir en un libro de Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="c29ee-111">Write to an Excel workbook using Microsoft Graph</span></span>](excel-write-to-workbook.md)
* [<span data-ttu-id="c29ee-112">Usar funciones de libro en Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="c29ee-112">Use workbook functions in Excel with Microsoft Graph</span></span>](excel-use-functions.md)
* [<span data-ttu-id="c29ee-113">Actualizar el formato de un rango en Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="c29ee-113">Update a range’s format in Excel with Microsoft Graph</span></span>](excel-update-range-format.md)
* [<span data-ttu-id="c29ee-114">Usar la API de REST de Excel</span><span class="sxs-lookup"><span data-stu-id="c29ee-114">Use the Excel REST API</span></span>](../api-reference/v1.0/resources/excel.md)
