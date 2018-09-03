# <a name="create-chart"></a><span data-ttu-id="41355-101">Create Chart</span><span class="sxs-lookup"><span data-stu-id="41355-101">Create Chart</span></span>

<span data-ttu-id="41355-102">Use esta API para crear un objeto Chart.</span><span class="sxs-lookup"><span data-stu-id="41355-102">Use this API to create a new Chart.</span></span>
## <a name="permissions"></a><span data-ttu-id="41355-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="41355-103">Permissions</span></span>
<span data-ttu-id="41355-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="41355-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="41355-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="41355-106">Permission type</span></span>      | <span data-ttu-id="41355-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="41355-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="41355-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="41355-108">Delegated (work or school account)</span></span> | <span data-ttu-id="41355-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="41355-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="41355-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="41355-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="41355-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41355-111">Not supported.</span></span>    |
|<span data-ttu-id="41355-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="41355-112">Application</span></span> | <span data-ttu-id="41355-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41355-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="41355-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="41355-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/

```
## <a name="request-headers"></a><span data-ttu-id="41355-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="41355-115">Request headers</span></span>
| <span data-ttu-id="41355-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="41355-116">Name</span></span>       | <span data-ttu-id="41355-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="41355-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="41355-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="41355-118">Authorization</span></span>  | <span data-ttu-id="41355-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="41355-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="41355-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="41355-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="41355-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="41355-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="41355-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="41355-124">Request body</span></span>
<span data-ttu-id="41355-125">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [WorkbookChart](../resources/chart.md).</span><span class="sxs-lookup"><span data-stu-id="41355-125">In the request body, supply a JSON representation of [directoryObject](../resources/chart.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="41355-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41355-126">Response</span></span>

<span data-ttu-id="41355-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [WorbookChart](../resources/chart.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41355-127">If successful, this method returns `201 Created` response code and [groupSetting](../resources/chart.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="41355-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="41355-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="41355-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="41355-129">Request</span></span>
<span data-ttu-id="41355-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="41355-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_chart_from_worksheet"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts
Content-type: application/json
Content-length: 52

{
  "id": "id-value",
  "height": 99,
  "left": 99
}
```
<span data-ttu-id="41355-131">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [WorkbookChart](../resources/chart.md).</span><span class="sxs-lookup"><span data-stu-id="41355-131">In the request body, supply a JSON representation of [plannerPlan](../resources/chart.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="41355-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41355-132">Response</span></span>
<span data-ttu-id="41355-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="41355-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChart"
} -->
```http
HTTP/1.1 201 Created
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
  "description": "Create Chart",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->