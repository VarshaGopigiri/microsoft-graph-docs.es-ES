# <a name="tablecolumn-databodyrange"></a><span data-ttu-id="4d609-101">TableColumn: DataBodyRange</span><span class="sxs-lookup"><span data-stu-id="4d609-101">TableColumn: DataBodyRange</span></span>

<span data-ttu-id="4d609-102">Obtiene el objeto de rango asociado al cuerpo de datos de la columna.</span><span class="sxs-lookup"><span data-stu-id="4d609-102">Gets the range object associated with the data body of the column.</span></span>
## <a name="permissions"></a><span data-ttu-id="4d609-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="4d609-103">Permissions</span></span>
<span data-ttu-id="4d609-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4d609-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4d609-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4d609-106">Permission type</span></span>      | <span data-ttu-id="4d609-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4d609-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4d609-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4d609-108">Delegated (work or school account)</span></span> | <span data-ttu-id="4d609-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4d609-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="4d609-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4d609-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4d609-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4d609-111">Not supported.</span></span>    |
|<span data-ttu-id="4d609-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4d609-112">Application</span></span> | <span data-ttu-id="4d609-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4d609-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4d609-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4d609-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/{id|name}/dataBodyRange
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/{id|name}/dataBodyRange

```
## <a name="request-headers"></a><span data-ttu-id="4d609-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4d609-115">Request headers</span></span>
| <span data-ttu-id="4d609-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="4d609-116">Name</span></span>       | <span data-ttu-id="4d609-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d609-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="4d609-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="4d609-118">Authorization</span></span>  | <span data-ttu-id="4d609-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4d609-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4d609-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="4d609-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="4d609-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="4d609-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="4d609-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4d609-124">Request body</span></span>

## <a name="response"></a><span data-ttu-id="4d609-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d609-125">Response</span></span>

<span data-ttu-id="4d609-126">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d609-126">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4d609-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d609-127">Example</span></span>
<span data-ttu-id="4d609-128">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="4d609-128">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="4d609-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4d609-129">Request</span></span>
<span data-ttu-id="4d609-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4d609-130">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "tablecolumn_databodyrange",
  "idempotent": true
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}/dataBodyRange
```

##### <a name="response"></a><span data-ttu-id="4d609-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d609-131">Response</span></span>
<span data-ttu-id="4d609-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4d609-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "TableColumn: DataBodyRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->