# <a name="range-entirecolumn"></a><span data-ttu-id="84910-101">Range: EntireColumn</span><span class="sxs-lookup"><span data-stu-id="84910-101">Range: EntireColumn</span></span>

<span data-ttu-id="84910-102">Obtiene un objeto que representa toda la columna del rango.</span><span class="sxs-lookup"><span data-stu-id="84910-102">Gets an object that represents the entire column of the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="84910-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="84910-103">Permissions</span></span>
<span data-ttu-id="84910-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="84910-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="84910-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="84910-106">Permission type</span></span>      | <span data-ttu-id="84910-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="84910-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="84910-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="84910-108">Delegated (work or school account)</span></span> | <span data-ttu-id="84910-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="84910-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="84910-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="84910-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="84910-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="84910-111">Not supported.</span></span>    |
|<span data-ttu-id="84910-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="84910-112">Application</span></span> | <span data-ttu-id="84910-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="84910-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="84910-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="84910-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/EntireColumn
GET /workbook/worksheets/{id|name}/range(address='<address>')/EntireColumn
GET /workbook/tables/{id|name}/columns/{id|name}/range/EntireColumn

```
## <a name="request-headers"></a><span data-ttu-id="84910-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="84910-115">Request headers</span></span>
| <span data-ttu-id="84910-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="84910-116">Name</span></span>       | <span data-ttu-id="84910-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="84910-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="84910-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="84910-118">Authorization</span></span>  | <span data-ttu-id="84910-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="84910-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="84910-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="84910-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="84910-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="84910-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="84910-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="84910-124">Request body</span></span>

## <a name="response"></a><span data-ttu-id="84910-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="84910-125">Response</span></span>

<span data-ttu-id="84910-126">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="84910-126">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="84910-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84910-127">Example</span></span>
<span data-ttu-id="84910-128">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="84910-128">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="84910-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="84910-129">Request</span></span>
<span data-ttu-id="84910-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="84910-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_entirecolumn"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/EntireColumn
```

##### <a name="response"></a><span data-ttu-id="84910-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="84910-131">Response</span></span>
<span data-ttu-id="84910-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="84910-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: EntireColumn",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->