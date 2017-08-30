# <a name="range-insert"></a><span data-ttu-id="8d601-101">Range: insert</span><span class="sxs-lookup"><span data-stu-id="8d601-101">Range: insert</span></span>

<span data-ttu-id="8d601-p101">Inserta una celda o un intervalo de celdas en la hoja de cálculo en lugar de este intervalo y desplaza las demás celdas para crear espacio. Devuelve un objeto Range en el espacio que queda en blanco.</span><span class="sxs-lookup"><span data-stu-id="8d601-p101">Inserts a cell or a range of cells into the worksheet in place of this range, and shifts the other cells to make space. Returns a new Range object at the now blank space.</span></span>
## <a name="permissions"></a><span data-ttu-id="8d601-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="8d601-104">Permissions</span></span>
<span data-ttu-id="8d601-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8d601-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8d601-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8d601-107">Permission type</span></span>      | <span data-ttu-id="8d601-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8d601-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8d601-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8d601-109">Delegated (work or school account)</span></span> | <span data-ttu-id="8d601-110">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8d601-110">Files.ReadWrite</span></span>    |
|<span data-ttu-id="8d601-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8d601-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8d601-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8d601-112">Not supported.</span></span>    |
|<span data-ttu-id="8d601-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8d601-113">Application</span></span> | <span data-ttu-id="8d601-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8d601-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="8d601-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8d601-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/insert
POST /workbook/worksheets/{id|name}/range(<address>)/insert
POST /workbook/tables/{id|name}/columns/{id|name}/range/insert

```
## <a name="request-headers"></a><span data-ttu-id="8d601-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8d601-116">Request headers</span></span>
| <span data-ttu-id="8d601-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="8d601-117">Name</span></span>       | <span data-ttu-id="8d601-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d601-118">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="8d601-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="8d601-119">Authorization</span></span>  | <span data-ttu-id="8d601-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8d601-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8d601-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8d601-122">Request body</span></span>
<span data-ttu-id="8d601-123">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="8d601-123">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="8d601-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="8d601-124">Parameter</span></span>    | <span data-ttu-id="8d601-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d601-125">Type</span></span>   |<span data-ttu-id="8d601-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d601-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8d601-127">Shift</span><span class="sxs-lookup"><span data-stu-id="8d601-127">shift</span></span>|<span data-ttu-id="8d601-128">string</span><span class="sxs-lookup"><span data-stu-id="8d601-128">string</span></span>|<span data-ttu-id="8d601-p104">Especifica hacia dónde se desplazarán las celdas.  Valores posibles: `Down`, `Right`.</span><span class="sxs-lookup"><span data-stu-id="8d601-p104">Specifies which way to shift the cells.  Possible values are: `Down`, `Right`.</span></span>|

## <a name="response"></a><span data-ttu-id="8d601-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8d601-131">Response</span></span>

<span data-ttu-id="8d601-132">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8d601-132">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8d601-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8d601-133">Example</span></span>
<span data-ttu-id="8d601-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="8d601-134">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="8d601-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8d601-135">Request</span></span>
<span data-ttu-id="8d601-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8d601-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_insert"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/insert
Content-type: application/json
Content-length: 28

{
  "shift": "shift-value"
}
```

##### <a name="response"></a><span data-ttu-id="8d601-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8d601-137">Response</span></span>
<span data-ttu-id="8d601-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8d601-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: insert",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->