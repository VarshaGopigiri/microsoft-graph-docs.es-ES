# <a name="range-entirerow"></a><span data-ttu-id="50c0c-101">Range: EntireRow</span><span class="sxs-lookup"><span data-stu-id="50c0c-101">Range: EntireRow</span></span>

<span data-ttu-id="50c0c-102">Obtiene un objeto que representa toda la fila del rango.</span><span class="sxs-lookup"><span data-stu-id="50c0c-102">Gets an object that represents the entire row of the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="50c0c-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="50c0c-103">Permissions</span></span>
<span data-ttu-id="50c0c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="50c0c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="50c0c-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="50c0c-106">Permission type</span></span>      | <span data-ttu-id="50c0c-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="50c0c-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="50c0c-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="50c0c-108">Delegated (work or school account)</span></span> | <span data-ttu-id="50c0c-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="50c0c-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="50c0c-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="50c0c-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="50c0c-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="50c0c-111">Not supported.</span></span>    |
|<span data-ttu-id="50c0c-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="50c0c-112">Application</span></span> | <span data-ttu-id="50c0c-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="50c0c-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="50c0c-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="50c0c-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/EntireRow
GET /workbook/worksheets/{id|name}/range(address='<address>'/EntireRow
GET /workbook/tables/{id|name}/columns/{id|name}/range/EntireRow

```
## <a name="request-headers"></a><span data-ttu-id="50c0c-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="50c0c-115">Request headers</span></span>
| <span data-ttu-id="50c0c-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="50c0c-116">Name</span></span>       | <span data-ttu-id="50c0c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="50c0c-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="50c0c-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="50c0c-118">Authorization</span></span>  | <span data-ttu-id="50c0c-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="50c0c-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="50c0c-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="50c0c-121">Request body</span></span>

## <a name="response"></a><span data-ttu-id="50c0c-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50c0c-122">Response</span></span>

<span data-ttu-id="50c0c-123">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="50c0c-123">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="50c0c-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="50c0c-124">Example</span></span>
<span data-ttu-id="50c0c-125">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="50c0c-125">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="50c0c-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="50c0c-126">Request</span></span>
<span data-ttu-id="50c0c-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="50c0c-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_entirerow"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/EntireRow
```

##### <a name="response"></a><span data-ttu-id="50c0c-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50c0c-128">Response</span></span>
<span data-ttu-id="50c0c-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="50c0c-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: EntireRow",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->