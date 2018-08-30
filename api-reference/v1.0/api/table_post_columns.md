# <a name="create-tablecolumn"></a><span data-ttu-id="eddda-101">Crear un TableColumn</span><span class="sxs-lookup"><span data-stu-id="eddda-101">Create TableColumn</span></span>

<span data-ttu-id="eddda-102">Use esta API para crear un objeto TableColumn.</span><span class="sxs-lookup"><span data-stu-id="eddda-102">Use this API to create a new TableColumn.</span></span>
## <a name="permissions"></a><span data-ttu-id="eddda-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="eddda-103">Permissions</span></span>
<span data-ttu-id="eddda-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="eddda-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="eddda-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eddda-106">Permission type</span></span>      | <span data-ttu-id="eddda-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eddda-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eddda-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eddda-108">Delegated (work or school account)</span></span> | <span data-ttu-id="eddda-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="eddda-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="eddda-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eddda-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eddda-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eddda-111">Not supported.</span></span>    |
|<span data-ttu-id="eddda-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eddda-112">Application</span></span> | <span data-ttu-id="eddda-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eddda-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="eddda-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eddda-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns

```
## <a name="request-headers"></a><span data-ttu-id="eddda-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eddda-115">Request headers</span></span>
| <span data-ttu-id="eddda-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="eddda-116">Name</span></span>       | <span data-ttu-id="eddda-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="eddda-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="eddda-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="eddda-118">Authorization</span></span>  | <span data-ttu-id="eddda-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eddda-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="eddda-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="eddda-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="eddda-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="eddda-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="eddda-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eddda-124">Request body</span></span>
<span data-ttu-id="eddda-125">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [WorkbookTableColumn](../resources/tablecolumn.md).</span><span class="sxs-lookup"><span data-stu-id="eddda-125">In the request body, supply a JSON representation of [directoryObject](../resources/tablecolumn.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="eddda-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eddda-126">Response</span></span>

<span data-ttu-id="eddda-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [WorkbookTableColumn](../resources/tablecolumn.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eddda-127">If successful, this method returns `201 Created` response code and [groupSetting](../resources/tablecolumn.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eddda-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eddda-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="eddda-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eddda-129">Request</span></span>
<span data-ttu-id="eddda-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eddda-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_tablecolumn_from_table"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns
Content-type: application/json
Content-length: 81

{
  "id": 99,
  "name": "name-value",
  "index": 99,
  "values": "values-value"
}
```
<span data-ttu-id="eddda-131">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [WorkbookTableColumn](../resources/tablecolumn.md).</span><span class="sxs-lookup"><span data-stu-id="eddda-131">In the request body, supply a JSON representation of [plannerPlan](../resources/tablecolumn.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="eddda-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eddda-132">Response</span></span>
<span data-ttu-id="eddda-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eddda-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTableColumn"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 81

{
  "id": 99,
  "name": "name-value",
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create TableColumn",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->