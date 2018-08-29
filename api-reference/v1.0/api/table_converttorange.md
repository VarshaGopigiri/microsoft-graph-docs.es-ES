# <a name="table-converttorange"></a><span data-ttu-id="509d8-101">Table: convertToRange</span><span class="sxs-lookup"><span data-stu-id="509d8-101">Table: convertToRange</span></span>

<span data-ttu-id="509d8-p101">Convierte la tabla en un rango de celdas normal. Se conservan todos los datos.</span><span class="sxs-lookup"><span data-stu-id="509d8-p101">Converts the table into a normal range of cells. All data is preserved.</span></span>
## <a name="permissions"></a><span data-ttu-id="509d8-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="509d8-104">Permissions</span></span>
<span data-ttu-id="509d8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="509d8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="509d8-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="509d8-107">Permission type</span></span>      | <span data-ttu-id="509d8-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="509d8-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="509d8-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="509d8-109">Delegated (work or school account)</span></span> | <span data-ttu-id="509d8-110">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="509d8-110">Files.ReadWrite</span></span>    |
|<span data-ttu-id="509d8-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="509d8-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="509d8-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="509d8-112">Not supported.</span></span>    |
|<span data-ttu-id="509d8-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="509d8-113">Application</span></span> | <span data-ttu-id="509d8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="509d8-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="509d8-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="509d8-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/convertToRange
POST /workbook/worksheets/{id|name}/tables/{id|name}/convertToRange

```
## <a name="request-headers"></a><span data-ttu-id="509d8-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="509d8-116">Request headers</span></span>
| <span data-ttu-id="509d8-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="509d8-117">Name</span></span>       | <span data-ttu-id="509d8-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="509d8-118">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="509d8-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="509d8-119">Authorization</span></span>  | <span data-ttu-id="509d8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="509d8-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="509d8-122">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="509d8-122">Workbook-Session-Id</span></span>  | <span data-ttu-id="509d8-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="509d8-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="509d8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="509d8-125">Request body</span></span>

## <a name="response"></a><span data-ttu-id="509d8-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="509d8-126">Response</span></span>

<span data-ttu-id="509d8-127">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="509d8-127">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="509d8-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="509d8-128">Example</span></span>
<span data-ttu-id="509d8-129">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="509d8-129">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="509d8-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="509d8-130">Request</span></span>
<span data-ttu-id="509d8-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="509d8-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "table_converttorange"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/convertToRange
```

##### <a name="response"></a><span data-ttu-id="509d8-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="509d8-132">Response</span></span>
<span data-ttu-id="509d8-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="509d8-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Table: convertToRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->