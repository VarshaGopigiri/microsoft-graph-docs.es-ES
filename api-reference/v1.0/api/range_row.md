# <a name="range-row"></a><span data-ttu-id="de684-101">Range: Row</span><span class="sxs-lookup"><span data-stu-id="de684-101">Range: Row</span></span>

<span data-ttu-id="de684-102">Obtiene una fila contenida en el rango.</span><span class="sxs-lookup"><span data-stu-id="de684-102">Gets a row contained in the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="de684-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="de684-103">Permissions</span></span>
<span data-ttu-id="de684-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="de684-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="de684-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="de684-106">Permission type</span></span>      | <span data-ttu-id="de684-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="de684-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="de684-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="de684-108">Delegated (work or school account)</span></span> | <span data-ttu-id="de684-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="de684-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="de684-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="de684-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="de684-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="de684-111">Not supported.</span></span>    |
|<span data-ttu-id="de684-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="de684-112">Application</span></span> | <span data-ttu-id="de684-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="de684-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="de684-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="de684-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/Row
POST /workbook/worksheets/{id|name}/range(address='<address>')/Row
POST /workbook/tables/{id|name}/columns/{id|name}/range/Row

```
## <a name="request-headers"></a><span data-ttu-id="de684-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="de684-115">Request headers</span></span>
| <span data-ttu-id="de684-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="de684-116">Name</span></span>       | <span data-ttu-id="de684-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="de684-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="de684-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="de684-118">Authorization</span></span>  | <span data-ttu-id="de684-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="de684-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="de684-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="de684-121">Request body</span></span>
<span data-ttu-id="de684-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="de684-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="de684-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="de684-123">Parameter</span></span>    | <span data-ttu-id="de684-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="de684-124">Type</span></span>   |<span data-ttu-id="de684-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="de684-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="de684-126">row</span><span class="sxs-lookup"><span data-stu-id="de684-126">row</span></span>|<span data-ttu-id="de684-127">number</span><span class="sxs-lookup"><span data-stu-id="de684-127">number</span></span>|<span data-ttu-id="de684-p103">Número de fila del intervalo que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="de684-p103">Row number of the range to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="de684-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de684-130">Response</span></span>

<span data-ttu-id="de684-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="de684-131">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="de684-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="de684-132">Example</span></span>
<span data-ttu-id="de684-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="de684-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="de684-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="de684-134">Request</span></span>
<span data-ttu-id="de684-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="de684-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_row"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/Row
Content-type: application/json
Content-length: 18

{
  "row": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="de684-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de684-136">Response</span></span>
<span data-ttu-id="de684-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="de684-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: Row",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->