# <a name="range-column"></a><span data-ttu-id="d5b63-101">Range: Column</span><span class="sxs-lookup"><span data-stu-id="d5b63-101">Range: Column</span></span>

<span data-ttu-id="d5b63-102">Obtiene una columna contenida en el rango.</span><span class="sxs-lookup"><span data-stu-id="d5b63-102">Gets a column contained in the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="d5b63-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="d5b63-103">Permissions</span></span>
<span data-ttu-id="d5b63-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d5b63-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d5b63-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d5b63-106">Permission type</span></span>      | <span data-ttu-id="d5b63-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d5b63-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d5b63-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d5b63-108">Delegated (work or school account)</span></span> | <span data-ttu-id="d5b63-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d5b63-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d5b63-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d5b63-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d5b63-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d5b63-111">Not supported.</span></span>    |
|<span data-ttu-id="d5b63-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d5b63-112">Application</span></span> | <span data-ttu-id="d5b63-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d5b63-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d5b63-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d5b63-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/Column
GET /workbook/worksheets/{id|name}/range(address='<address>')/Column
GET /workbook/tables/{id|name}/columns/{id|name}/range/Column

```
## <a name="request-headers"></a><span data-ttu-id="d5b63-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d5b63-115">Request headers</span></span>
| <span data-ttu-id="d5b63-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="d5b63-116">Name</span></span>       | <span data-ttu-id="d5b63-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5b63-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d5b63-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="d5b63-118">Authorization</span></span>  | <span data-ttu-id="d5b63-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d5b63-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d5b63-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="d5b63-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="d5b63-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="d5b63-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d5b63-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d5b63-124">Request body</span></span>
<span data-ttu-id="d5b63-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="d5b63-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d5b63-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d5b63-126">Parameter</span></span>    | <span data-ttu-id="d5b63-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="d5b63-127">Type</span></span>   |<span data-ttu-id="d5b63-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5b63-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d5b63-129">column</span><span class="sxs-lookup"><span data-stu-id="d5b63-129">column</span></span>|<span data-ttu-id="d5b63-130">number</span><span class="sxs-lookup"><span data-stu-id="d5b63-130">number</span></span>|<span data-ttu-id="d5b63-p104">Número de columna del intervalo que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="d5b63-p104">Column number of the range to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="d5b63-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d5b63-133">Response</span></span>

<span data-ttu-id="d5b63-134">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d5b63-134">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d5b63-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d5b63-135">Example</span></span>
<span data-ttu-id="d5b63-136">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d5b63-136">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="d5b63-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d5b63-137">Request</span></span>
<span data-ttu-id="d5b63-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d5b63-138">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="d5b63-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d5b63-139">Response</span></span>
<span data-ttu-id="d5b63-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d5b63-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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