# <a name="create-chartseries"></a><span data-ttu-id="5d26a-101">Create ChartSeries</span><span class="sxs-lookup"><span data-stu-id="5d26a-101">Create ChartSeries</span></span>

<span data-ttu-id="5d26a-102">Use esta API para crear un objeto ChartSeries.</span><span class="sxs-lookup"><span data-stu-id="5d26a-102">Use this API to create a new ChartSeries.</span></span>
## <a name="permissions"></a><span data-ttu-id="5d26a-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="5d26a-103">Permissions</span></span>
<span data-ttu-id="5d26a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5d26a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5d26a-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5d26a-106">Permission type</span></span>      | <span data-ttu-id="5d26a-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5d26a-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5d26a-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5d26a-108">Delegated (work or school account)</span></span> | <span data-ttu-id="5d26a-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5d26a-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="5d26a-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5d26a-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5d26a-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d26a-111">Not supported.</span></span>    |
|<span data-ttu-id="5d26a-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5d26a-112">Application</span></span> | <span data-ttu-id="5d26a-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d26a-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5d26a-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5d26a-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/{name}/series

```
## <a name="request-headers"></a><span data-ttu-id="5d26a-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5d26a-115">Request headers</span></span>
| <span data-ttu-id="5d26a-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="5d26a-116">Name</span></span>       | <span data-ttu-id="5d26a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d26a-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="5d26a-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="5d26a-118">Authorization</span></span>  | <span data-ttu-id="5d26a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5d26a-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5d26a-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="5d26a-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="5d26a-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="5d26a-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="5d26a-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5d26a-124">Request body</span></span>
<span data-ttu-id="5d26a-125">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [WorkbookChartSeries](../resources/chartseries.md).</span><span class="sxs-lookup"><span data-stu-id="5d26a-125">In the request body, supply a JSON representation of [directoryObject](../resources/chartseries.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="5d26a-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d26a-126">Response</span></span>

<span data-ttu-id="5d26a-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [WorkbookChartSeries](../resources/chartseries.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5d26a-127">If successful, this method returns `201 Created` response code and [groupSetting](../resources/chartseries.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5d26a-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5d26a-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5d26a-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5d26a-129">Request</span></span>
<span data-ttu-id="5d26a-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5d26a-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_chartseries_from_chart"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/series
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```
<span data-ttu-id="5d26a-131">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [WorkbookChartSeries](../resources/chartseries.md).</span><span class="sxs-lookup"><span data-stu-id="5d26a-131">In the request body, supply a JSON representation of [plannerPlan](../resources/chartseries.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="5d26a-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d26a-132">Response</span></span>
<span data-ttu-id="5d26a-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5d26a-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartSeries"
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