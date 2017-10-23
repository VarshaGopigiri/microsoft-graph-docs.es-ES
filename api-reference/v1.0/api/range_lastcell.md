# <a name="range-lastcell"></a><span data-ttu-id="4f8d0-101">Range: LastCell</span><span class="sxs-lookup"><span data-stu-id="4f8d0-101">Range: LastCell</span></span>

<span data-ttu-id="4f8d0-p101">Obtiene la última celda del intervalo. Por ejemplo, la última celda de "B2:D5" es "D5".</span><span class="sxs-lookup"><span data-stu-id="4f8d0-p101">Gets the last cell within the range. For example, the last cell of "B2:D5" is "D5".</span></span>
## <a name="permissions"></a><span data-ttu-id="4f8d0-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="4f8d0-104">Permissions</span></span>
<span data-ttu-id="4f8d0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4f8d0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4f8d0-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4f8d0-107">Permission type</span></span>      | <span data-ttu-id="4f8d0-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4f8d0-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4f8d0-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4f8d0-109">Delegated (work or school account)</span></span> | <span data-ttu-id="4f8d0-110">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4f8d0-110">Files.ReadWrite</span></span>    |
|<span data-ttu-id="4f8d0-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4f8d0-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4f8d0-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4f8d0-112">Not supported.</span></span>    |
|<span data-ttu-id="4f8d0-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4f8d0-113">Application</span></span> | <span data-ttu-id="4f8d0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4f8d0-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4f8d0-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4f8d0-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/LastCell
GET /workbook/worksheets/{id|name}/range(<address>)/LastCell
GET /workbook/tables/{id|name}/columns/{id|name}/range/LastCell

```
## <a name="request-headers"></a><span data-ttu-id="4f8d0-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4f8d0-116">Request headers</span></span>
| <span data-ttu-id="4f8d0-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="4f8d0-117">Name</span></span>       | <span data-ttu-id="4f8d0-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f8d0-118">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="4f8d0-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="4f8d0-119">Authorization</span></span>  | <span data-ttu-id="4f8d0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4f8d0-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4f8d0-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4f8d0-122">Request body</span></span>

## <a name="response"></a><span data-ttu-id="4f8d0-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f8d0-123">Response</span></span>

<span data-ttu-id="4f8d0-124">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4f8d0-124">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4f8d0-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4f8d0-125">Example</span></span>
<span data-ttu-id="4f8d0-126">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="4f8d0-126">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="4f8d0-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4f8d0-127">Request</span></span>
<span data-ttu-id="4f8d0-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4f8d0-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_lastcell"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/LastCell
```

##### <a name="response"></a><span data-ttu-id="4f8d0-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4f8d0-129">Response</span></span>
<span data-ttu-id="4f8d0-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4f8d0-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: LastCell",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->