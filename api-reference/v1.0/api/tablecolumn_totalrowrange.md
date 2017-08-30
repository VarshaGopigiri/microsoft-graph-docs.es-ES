# <a name="tablecolumn-totalrowrange"></a><span data-ttu-id="98dd9-101">TableColumn: TotalRowRange</span><span class="sxs-lookup"><span data-stu-id="98dd9-101">TableColumn: TotalRowRange</span></span>

<span data-ttu-id="98dd9-102">Obtiene el objeto de rango asociado a la fila de totales de la columna.</span><span class="sxs-lookup"><span data-stu-id="98dd9-102">Gets the range object associated with the totals row of the column.</span></span>
## <a name="permissions"></a><span data-ttu-id="98dd9-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="98dd9-103">Permissions</span></span>
<span data-ttu-id="98dd9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="98dd9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="98dd9-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="98dd9-106">Permission type</span></span>      | <span data-ttu-id="98dd9-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="98dd9-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="98dd9-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="98dd9-108">Delegated (work or school account)</span></span> | <span data-ttu-id="98dd9-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="98dd9-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="98dd9-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="98dd9-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="98dd9-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="98dd9-111">Not supported.</span></span>    |
|<span data-ttu-id="98dd9-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="98dd9-112">Application</span></span> | <span data-ttu-id="98dd9-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="98dd9-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="98dd9-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="98dd9-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/{id|name}/TotalRowRange
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/{id|name}/TotalRowRange

```
## <a name="request-headers"></a><span data-ttu-id="98dd9-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="98dd9-115">Request headers</span></span>
| <span data-ttu-id="98dd9-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="98dd9-116">Name</span></span>       | <span data-ttu-id="98dd9-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="98dd9-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="98dd9-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="98dd9-118">Authorization</span></span>  | <span data-ttu-id="98dd9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="98dd9-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="98dd9-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="98dd9-121">Request body</span></span>

## <a name="response"></a><span data-ttu-id="98dd9-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98dd9-122">Response</span></span>

<span data-ttu-id="98dd9-123">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98dd9-123">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="98dd9-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="98dd9-124">Example</span></span>
<span data-ttu-id="98dd9-125">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="98dd9-125">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="98dd9-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="98dd9-126">Request</span></span>
<span data-ttu-id="98dd9-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="98dd9-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablecolumn_totalrowrange"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}/TotalRowRange
```

##### <a name="response"></a><span data-ttu-id="98dd9-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98dd9-128">Response</span></span>
<span data-ttu-id="98dd9-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="98dd9-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "TableColumn: TotalRowRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->