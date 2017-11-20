# <a name="chart-setdata"></a><span data-ttu-id="4fc04-101">Chart: setData</span><span class="sxs-lookup"><span data-stu-id="4fc04-101">Chart: setData</span></span>

<span data-ttu-id="4fc04-102">Restablece los datos de origen del gráfico.</span><span class="sxs-lookup"><span data-stu-id="4fc04-102">Resets the source data for the chart.</span></span>
## <a name="permissions"></a><span data-ttu-id="4fc04-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="4fc04-103">Permissions</span></span>
<span data-ttu-id="4fc04-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4fc04-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4fc04-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4fc04-106">Permission type</span></span>      | <span data-ttu-id="4fc04-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4fc04-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4fc04-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4fc04-108">Delegated (work or school account)</span></span> | <span data-ttu-id="4fc04-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4fc04-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="4fc04-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4fc04-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4fc04-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4fc04-111">Not supported.</span></span>    |
|<span data-ttu-id="4fc04-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4fc04-112">Application</span></span> | <span data-ttu-id="4fc04-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4fc04-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4fc04-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4fc04-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/setData

```
## <a name="request-headers"></a><span data-ttu-id="4fc04-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4fc04-115">Request headers</span></span>
| <span data-ttu-id="4fc04-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="4fc04-116">Name</span></span>       | <span data-ttu-id="4fc04-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4fc04-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="4fc04-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="4fc04-118">Authorization</span></span>  | <span data-ttu-id="4fc04-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4fc04-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4fc04-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="4fc04-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="4fc04-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="4fc04-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="4fc04-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4fc04-124">Request body</span></span>
<span data-ttu-id="4fc04-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="4fc04-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="4fc04-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4fc04-126">Parameter</span></span>    | <span data-ttu-id="4fc04-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="4fc04-127">Type</span></span>   |<span data-ttu-id="4fc04-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="4fc04-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4fc04-129">sourceData</span><span class="sxs-lookup"><span data-stu-id="4fc04-129">sourceData</span></span>|<span data-ttu-id="4fc04-130">string</span><span class="sxs-lookup"><span data-stu-id="4fc04-130">string</span></span>|<span data-ttu-id="4fc04-131">Objeto Range correspondiente a los datos de origen.</span><span class="sxs-lookup"><span data-stu-id="4fc04-131">The Range object corresponding to the source data.</span></span>|
|<span data-ttu-id="4fc04-132">seriesBy</span><span class="sxs-lookup"><span data-stu-id="4fc04-132">seriesBy</span></span>|<span data-ttu-id="4fc04-133">string</span><span class="sxs-lookup"><span data-stu-id="4fc04-133">string</span></span>|<span data-ttu-id="4fc04-p104">Opcional. Especifica la manera en que las columnas o las filas se usan como series de datos en el gráfico. Puede ser de una de las siguientes: Auto (valor predeterminado), Rows, Columns.  Valores posibles: `Auto`, `Columns`, `Rows`.</span><span class="sxs-lookup"><span data-stu-id="4fc04-p104">Optional. Specifies the way columns or rows are used as data series on the chart. Can be one of the following: Auto (default), Rows, Columns.  Possible values are: `Auto`, `Columns`, `Rows`.</span></span>|

## <a name="response"></a><span data-ttu-id="4fc04-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4fc04-138">Response</span></span>

<span data-ttu-id="4fc04-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4fc04-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4fc04-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4fc04-141">Example</span></span>
<span data-ttu-id="4fc04-142">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="4fc04-142">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="4fc04-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4fc04-143">Request</span></span>
<span data-ttu-id="4fc04-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4fc04-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chart_setdata"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/setData
Content-type: application/json
Content-length: 70

{
  "sourceData": "sourceData-value",
  "seriesBy": "seriesBy-value"
}
```

##### <a name="response"></a><span data-ttu-id="4fc04-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4fc04-145">Response</span></span>
<span data-ttu-id="4fc04-146">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4fc04-146">Here is an example of the response.</span></span> 
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
  "description": "Chart: setData",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->