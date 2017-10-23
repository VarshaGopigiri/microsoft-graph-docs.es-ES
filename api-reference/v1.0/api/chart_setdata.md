# <a name="chart-setdata"></a><span data-ttu-id="4d342-101">Chart: setData</span><span class="sxs-lookup"><span data-stu-id="4d342-101">Chart: setData</span></span>

<span data-ttu-id="4d342-102">Restablece los datos de origen del gráfico.</span><span class="sxs-lookup"><span data-stu-id="4d342-102">Resets the source data for the chart.</span></span>
## <a name="permissions"></a><span data-ttu-id="4d342-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="4d342-103">Permissions</span></span>
<span data-ttu-id="4d342-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4d342-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4d342-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4d342-106">Permission type</span></span>      | <span data-ttu-id="4d342-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4d342-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4d342-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4d342-108">Delegated (work or school account)</span></span> | <span data-ttu-id="4d342-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4d342-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="4d342-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4d342-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4d342-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4d342-111">Not supported.</span></span>    |
|<span data-ttu-id="4d342-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4d342-112">Application</span></span> | <span data-ttu-id="4d342-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4d342-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4d342-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4d342-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/setData

```
## <a name="request-headers"></a><span data-ttu-id="4d342-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4d342-115">Request headers</span></span>
| <span data-ttu-id="4d342-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="4d342-116">Name</span></span>       | <span data-ttu-id="4d342-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d342-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="4d342-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="4d342-118">Authorization</span></span>  | <span data-ttu-id="4d342-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4d342-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4d342-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4d342-121">Request body</span></span>
<span data-ttu-id="4d342-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="4d342-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="4d342-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4d342-123">Parameter</span></span>    | <span data-ttu-id="4d342-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="4d342-124">Type</span></span>   |<span data-ttu-id="4d342-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d342-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4d342-126">sourceData</span><span class="sxs-lookup"><span data-stu-id="4d342-126">sourceData</span></span>|<span data-ttu-id="4d342-127">string</span><span class="sxs-lookup"><span data-stu-id="4d342-127">string</span></span>|<span data-ttu-id="4d342-128">Objeto Range correspondiente a los datos de origen.</span><span class="sxs-lookup"><span data-stu-id="4d342-128">The Range object corresponding to the source data.</span></span>|
|<span data-ttu-id="4d342-129">seriesBy</span><span class="sxs-lookup"><span data-stu-id="4d342-129">seriesBy</span></span>|<span data-ttu-id="4d342-130">string</span><span class="sxs-lookup"><span data-stu-id="4d342-130">string</span></span>|<span data-ttu-id="4d342-p103">Opcional. Especifica la manera en que las columnas o las filas se usan como series de datos en el gráfico. Puede ser de una de las siguientes: Auto (valor predeterminado), Rows, Columns.  Valores posibles: `Auto`, `Columns`, `Rows`.</span><span class="sxs-lookup"><span data-stu-id="4d342-p103">Optional. Specifies the way columns or rows are used as data series on the chart. Can be one of the following: Auto (default), Rows, Columns.  Possible values are: `Auto`, `Columns`, `Rows`.</span></span>|

## <a name="response"></a><span data-ttu-id="4d342-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d342-135">Response</span></span>

<span data-ttu-id="4d342-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d342-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4d342-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d342-138">Example</span></span>
<span data-ttu-id="4d342-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="4d342-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="4d342-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4d342-140">Request</span></span>
<span data-ttu-id="4d342-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4d342-141">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="4d342-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d342-142">Response</span></span>
<span data-ttu-id="4d342-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d342-143">Here is an example of the response.</span></span> 
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