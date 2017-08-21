# <a name="create-chartseries"></a><span data-ttu-id="9effd-101">Create ChartSeries</span><span class="sxs-lookup"><span data-stu-id="9effd-101">Create ChartSeries</span></span>

<span data-ttu-id="9effd-102">Use esta API para crear un objeto ChartSeries.</span><span class="sxs-lookup"><span data-stu-id="9effd-102">Use this API to create a new ChartSeries.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9effd-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9effd-103">Prerequisites</span></span>
<span data-ttu-id="9effd-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="9effd-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="9effd-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9effd-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="9effd-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9effd-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/series

```
## <a name="request-headers"></a><span data-ttu-id="9effd-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9effd-107">Request headers</span></span>
| <span data-ttu-id="9effd-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="9effd-108">Name</span></span>       | <span data-ttu-id="9effd-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9effd-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9effd-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="9effd-110">Authorization</span></span>  | <span data-ttu-id="9effd-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9effd-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="9effd-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9effd-113">Request body</span></span>
<span data-ttu-id="9effd-114">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ChartSeries](../resources/chartseries.md).</span><span class="sxs-lookup"><span data-stu-id="9effd-114">In the request body, supply a JSON representation of [ChartSeries](../resources/chartseries.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="9effd-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9effd-115">Response</span></span>

<span data-ttu-id="9effd-116">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [ChartSeries](../resources/chartseries.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9effd-116">If successful, this method returns `201, Created` response code and [ChartSeries](../resources/chartseries.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9effd-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9effd-117">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9effd-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9effd-118">Request</span></span>
<span data-ttu-id="9effd-119">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9effd-119">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_chartseries_from_chart"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/series
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```
<span data-ttu-id="9effd-120">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ChartSeries](../resources/chartseries.md).</span><span class="sxs-lookup"><span data-stu-id="9effd-120">In the request body, supply a JSON representation of [ChartSeries](../resources/chartseries.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="9effd-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9effd-121">Response</span></span>
<span data-ttu-id="9effd-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9effd-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartSeries"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create ChartSeries",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->