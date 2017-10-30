# <a name="range-column"></a><span data-ttu-id="9ccfa-101">Range: Column</span><span class="sxs-lookup"><span data-stu-id="9ccfa-101">Range: Column</span></span>

<span data-ttu-id="9ccfa-102">Obtiene una columna contenida en el rango.</span><span class="sxs-lookup"><span data-stu-id="9ccfa-102">Gets a column contained in the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="9ccfa-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="9ccfa-103">Permissions</span></span>
<span data-ttu-id="9ccfa-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9ccfa-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9ccfa-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9ccfa-106">Permission type</span></span>      | <span data-ttu-id="9ccfa-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9ccfa-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9ccfa-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9ccfa-108">Delegated (work or school account)</span></span> | <span data-ttu-id="9ccfa-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9ccfa-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="9ccfa-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9ccfa-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9ccfa-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ccfa-111">Not supported.</span></span>    |
|<span data-ttu-id="9ccfa-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9ccfa-112">Application</span></span> | <span data-ttu-id="9ccfa-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ccfa-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9ccfa-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9ccfa-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/Column
GET /workbook/worksheets/{id|name}/range(address='<address>')/Column
GET /workbook/tables/{id|name}/columns/{id|name}/range/Column

```
## <a name="request-headers"></a><span data-ttu-id="9ccfa-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9ccfa-115">Request headers</span></span>
| <span data-ttu-id="9ccfa-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="9ccfa-116">Name</span></span>       | <span data-ttu-id="9ccfa-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ccfa-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9ccfa-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="9ccfa-118">Authorization</span></span>  | <span data-ttu-id="9ccfa-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9ccfa-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9ccfa-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9ccfa-121">Request body</span></span>
<span data-ttu-id="9ccfa-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="9ccfa-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="9ccfa-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9ccfa-123">Parameter</span></span>    | <span data-ttu-id="9ccfa-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="9ccfa-124">Type</span></span>   |<span data-ttu-id="9ccfa-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ccfa-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9ccfa-126">column</span><span class="sxs-lookup"><span data-stu-id="9ccfa-126">column</span></span>|<span data-ttu-id="9ccfa-127">number</span><span class="sxs-lookup"><span data-stu-id="9ccfa-127">number</span></span>|<span data-ttu-id="9ccfa-p103">Número de columna del intervalo que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="9ccfa-p103">Column number of the range to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="9ccfa-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ccfa-130">Response</span></span>

<span data-ttu-id="9ccfa-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ccfa-131">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9ccfa-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ccfa-132">Example</span></span>
<span data-ttu-id="9ccfa-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9ccfa-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="9ccfa-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9ccfa-134">Request</span></span>
<span data-ttu-id="9ccfa-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9ccfa-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_column"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/Column
Content-type: application/json
Content-length: 21

{
  "column": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="9ccfa-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ccfa-136">Response</span></span>
<span data-ttu-id="9ccfa-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9ccfa-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: Column",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->