# <a name="chartcollection-add"></a><span data-ttu-id="15a82-101">ChartCollection: add</span><span class="sxs-lookup"><span data-stu-id="15a82-101">ChartCollection: add</span></span>

<span data-ttu-id="15a82-102">Crea un nuevo gráfico.</span><span class="sxs-lookup"><span data-stu-id="15a82-102">Creates a new chart.</span></span>
## <a name="permissions"></a><span data-ttu-id="15a82-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="15a82-103">Permissions</span></span>
<span data-ttu-id="15a82-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="15a82-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="15a82-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="15a82-106">Permission type</span></span>      | <span data-ttu-id="15a82-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="15a82-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="15a82-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="15a82-108">Delegated (work or school account)</span></span> | <span data-ttu-id="15a82-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="15a82-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="15a82-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="15a82-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="15a82-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="15a82-111">Not supported.</span></span>    |
|<span data-ttu-id="15a82-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="15a82-112">Application</span></span> | <span data-ttu-id="15a82-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="15a82-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="15a82-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="15a82-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/add

```
## <a name="request-headers"></a><span data-ttu-id="15a82-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="15a82-115">Request headers</span></span>
| <span data-ttu-id="15a82-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="15a82-116">Name</span></span>       | <span data-ttu-id="15a82-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="15a82-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="15a82-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="15a82-118">Authorization</span></span>  | <span data-ttu-id="15a82-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="15a82-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="15a82-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="15a82-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="15a82-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="15a82-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="15a82-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="15a82-124">Request body</span></span>
<span data-ttu-id="15a82-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="15a82-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="15a82-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="15a82-126">Parameter</span></span>    | <span data-ttu-id="15a82-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="15a82-127">Type</span></span>   |<span data-ttu-id="15a82-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="15a82-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="15a82-129">type</span><span class="sxs-lookup"><span data-stu-id="15a82-129">type</span></span>|<span data-ttu-id="15a82-130">cadena</span><span class="sxs-lookup"><span data-stu-id="15a82-130">string</span></span>|<span data-ttu-id="15a82-131">Representa el tipo de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="15a82-131">Represents the name of a chart object.</span></span>  <span data-ttu-id="15a82-132">Los valores posibles son: `ColumnClustered`, `ColumnStacked`, `ColumnStacked100`, `BarClustered`, `BarStacked`, `BarStacked100`, `LineStacked`, `LineStacked100`, `LineMarkers`, `LineMarkersStacked`, `LineMarkersStacked100`, `PieOfPie`, `etc.`.</span><span class="sxs-lookup"><span data-stu-id="15a82-132">The possible values are `ColumnClustered`, `ColumnStacked`, `ColumnStacked100`, `BarClustered`, `BarStacked`, `BarStacked100`, `LineStacked`, `LineStacked100`, `LineMarkers`, `LineMarkersStacked`, `LineMarkersStacked100`, or `PieOfPie`.</span></span>|
|<span data-ttu-id="15a82-133">sourceData</span><span class="sxs-lookup"><span data-stu-id="15a82-133">sourceData</span></span>|<span data-ttu-id="15a82-134">Json</span><span class="sxs-lookup"><span data-stu-id="15a82-134">Json</span></span>|<span data-ttu-id="15a82-135">Objeto Range correspondiente a los datos de origen.</span><span class="sxs-lookup"><span data-stu-id="15a82-135">The Range object corresponding to the source data.</span></span>|
|<span data-ttu-id="15a82-136">seriesBy</span><span class="sxs-lookup"><span data-stu-id="15a82-136">seriesBy</span></span>|<span data-ttu-id="15a82-137">cadena</span><span class="sxs-lookup"><span data-stu-id="15a82-137">string</span></span>|<span data-ttu-id="15a82-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="15a82-138">Optional.</span></span> <span data-ttu-id="15a82-139">Especifica las filas o columnas de forma que se usan como series de datos en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="15a82-139">Returns or sets the way columns or rows are used as data series on the chart.</span></span>  <span data-ttu-id="15a82-140">Los valores posibles son: `Auto`, `Columns` y `Rows`.</span><span class="sxs-lookup"><span data-stu-id="15a82-140">The possible values are `Auto`, `Columns`, `Rows`, , , , , , , , , or .</span></span>|

## <a name="response"></a><span data-ttu-id="15a82-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15a82-141">Response</span></span>

<span data-ttu-id="15a82-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [WorbookChart](../resources/chart.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15a82-142">If successful, this method returns `200 OK` response code and [groupSetting](../resources/chart.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="15a82-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="15a82-143">Example</span></span>
<span data-ttu-id="15a82-144">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="15a82-144">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="15a82-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="15a82-145">Request</span></span>
<span data-ttu-id="15a82-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="15a82-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartcollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/add
Content-type: application/json
Content-length: 94

{
  "type": "ColumnStacked",
  "sourceData": "A1:B1",
  "seriesBy": "Auto"
}
```

##### <a name="response"></a><span data-ttu-id="15a82-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15a82-147">Response</span></span>
<span data-ttu-id="15a82-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="15a82-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChart"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 52

{
  "id": "id-value",
  "height": 99,
  "left": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartCollection: add",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
