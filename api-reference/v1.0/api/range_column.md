# <a name="range-column"></a><span data-ttu-id="eefc2-101">Range: Column</span><span class="sxs-lookup"><span data-stu-id="eefc2-101">Range: Column</span></span>

<span data-ttu-id="eefc2-102">Obtiene una columna contenida en el rango.</span><span class="sxs-lookup"><span data-stu-id="eefc2-102">Gets a column contained in the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="eefc2-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="eefc2-103">Permissions</span></span>
<span data-ttu-id="eefc2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="eefc2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="eefc2-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eefc2-106">Permission type</span></span>      | <span data-ttu-id="eefc2-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eefc2-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eefc2-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eefc2-108">Delegated (work or school account)</span></span> | <span data-ttu-id="eefc2-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="eefc2-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="eefc2-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eefc2-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eefc2-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eefc2-111">Not supported.</span></span>    |
|<span data-ttu-id="eefc2-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eefc2-112">Application</span></span> | <span data-ttu-id="eefc2-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eefc2-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="eefc2-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eefc2-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/column
GET /workbook/worksheets/{id|name}/range(address='<address>')/column
GET /workbook/tables/{id|name}/columns/{id|name}/range/column

```
## <a name="request-headers"></a><span data-ttu-id="eefc2-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eefc2-115">Request headers</span></span>
| <span data-ttu-id="eefc2-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="eefc2-116">Name</span></span>       | <span data-ttu-id="eefc2-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="eefc2-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="eefc2-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="eefc2-118">Authorization</span></span>  | <span data-ttu-id="eefc2-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eefc2-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="eefc2-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="eefc2-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="eefc2-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="eefc2-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="path-parameters"></a><span data-ttu-id="eefc2-124">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="eefc2-124">Path parameters</span></span>
<span data-ttu-id="eefc2-125">En la ruta de acceso de la solicitud, proporcione los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="eefc2-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="eefc2-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="eefc2-126">Parameter</span></span>    | <span data-ttu-id="eefc2-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="eefc2-127">Type</span></span>   |<span data-ttu-id="eefc2-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="eefc2-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="eefc2-129">column</span><span class="sxs-lookup"><span data-stu-id="eefc2-129">column</span></span>|<span data-ttu-id="eefc2-130">Int32</span><span class="sxs-lookup"><span data-stu-id="eefc2-130">Int32</span></span>|<span data-ttu-id="eefc2-p104">Número de columna del intervalo que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="eefc2-p104">Column number of the range to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="eefc2-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eefc2-133">Response</span></span>

<span data-ttu-id="eefc2-134">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eefc2-134">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eefc2-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eefc2-135">Example</span></span>
<span data-ttu-id="eefc2-136">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="eefc2-136">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="eefc2-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eefc2-137">Request</span></span>
<span data-ttu-id="eefc2-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eefc2-138">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "range_column"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/column(column=5)
```

##### <a name="response"></a><span data-ttu-id="eefc2-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eefc2-139">Response</span></span>
<span data-ttu-id="eefc2-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eefc2-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRange"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 169

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnIndex": 99,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: Column",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->