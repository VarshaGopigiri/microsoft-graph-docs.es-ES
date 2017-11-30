# <a name="worksheet-cell"></a><span data-ttu-id="dd6f4-101">Worksheet: Cell</span><span class="sxs-lookup"><span data-stu-id="dd6f4-101">Worksheet: Cell</span></span>

<span data-ttu-id="dd6f4-p101">Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="dd6f4-p101">Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid.</span></span>
## <a name="permissions"></a><span data-ttu-id="dd6f4-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="dd6f4-104">Permissions</span></span>
<span data-ttu-id="dd6f4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="dd6f4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="dd6f4-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dd6f4-107">Permission type</span></span>      | <span data-ttu-id="dd6f4-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dd6f4-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dd6f4-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dd6f4-109">Delegated (work or school account)</span></span> | <span data-ttu-id="dd6f4-110">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="dd6f4-110">Files.ReadWrite</span></span>    |
|<span data-ttu-id="dd6f4-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dd6f4-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dd6f4-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dd6f4-112">Not supported.</span></span>    |
|<span data-ttu-id="dd6f4-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dd6f4-113">Application</span></span> | <span data-ttu-id="dd6f4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dd6f4-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="dd6f4-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dd6f4-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/Cell(row=<row>,column=<column>)

```
## <a name="request-headers"></a><span data-ttu-id="dd6f4-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dd6f4-116">Request headers</span></span>
| <span data-ttu-id="dd6f4-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="dd6f4-117">Name</span></span>       | <span data-ttu-id="dd6f4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd6f4-118">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="dd6f4-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="dd6f4-119">Authorization</span></span>  | <span data-ttu-id="dd6f4-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dd6f4-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="dd6f4-122">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="dd6f4-122">Workbook-Session-Id</span></span>  | <span data-ttu-id="dd6f4-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="dd6f4-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="response"></a><span data-ttu-id="dd6f4-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd6f4-125">Response</span></span>

<span data-ttu-id="dd6f4-126">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dd6f4-126">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dd6f4-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dd6f4-127">Example</span></span>
<span data-ttu-id="dd6f4-128">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="dd6f4-128">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="dd6f4-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dd6f4-129">Request</span></span>
<span data-ttu-id="dd6f4-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dd6f4-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheet_cell"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/Cell(row=<row>,column=<column>)
```

##### <a name="response"></a><span data-ttu-id="dd6f4-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd6f4-131">Response</span></span>
<span data-ttu-id="dd6f4-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dd6f4-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 169

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 1,
  "columnCount": 1,
  "columnIndex": 3,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Worksheet: Cell",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
