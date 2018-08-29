# <a name="worksheet-range"></a><span data-ttu-id="bb6cf-101">Worksheet: Range</span><span class="sxs-lookup"><span data-stu-id="bb6cf-101">Worksheet: Range</span></span>

<span data-ttu-id="bb6cf-102">Obtiene el objeto de rango especificado por la dirección o el nombre.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-102">Gets the range object specified by the address or name.</span></span>
## <a name="permissions"></a><span data-ttu-id="bb6cf-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="bb6cf-103">Permissions</span></span>
<span data-ttu-id="bb6cf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bb6cf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="bb6cf-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bb6cf-106">Permission type</span></span>      | <span data-ttu-id="bb6cf-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bb6cf-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bb6cf-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bb6cf-108">Delegated (work or school account)</span></span> | <span data-ttu-id="bb6cf-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bb6cf-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="bb6cf-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bb6cf-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bb6cf-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-111">Not supported.</span></span>    |
|<span data-ttu-id="bb6cf-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bb6cf-112">Application</span></span> | <span data-ttu-id="bb6cf-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="bb6cf-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bb6cf-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/range

```
## <a name="request-headers"></a><span data-ttu-id="bb6cf-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bb6cf-115">Request headers</span></span>
| <span data-ttu-id="bb6cf-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="bb6cf-116">Name</span></span>       | <span data-ttu-id="bb6cf-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb6cf-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="bb6cf-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="bb6cf-118">Authorization</span></span>  | <span data-ttu-id="bb6cf-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bb6cf-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="bb6cf-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="bb6cf-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="function-parameters"></a><span data-ttu-id="bb6cf-124">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="bb6cf-124">Function parameters</span></span>

| <span data-ttu-id="bb6cf-125">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bb6cf-125">Parameter</span></span>    | <span data-ttu-id="bb6cf-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb6cf-126">Type</span></span>   |<span data-ttu-id="bb6cf-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb6cf-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bb6cf-128">address</span><span class="sxs-lookup"><span data-stu-id="bb6cf-128">address</span></span>|<span data-ttu-id="bb6cf-129">cadena</span><span class="sxs-lookup"><span data-stu-id="bb6cf-129">string</span></span>|<span data-ttu-id="bb6cf-p104">Opcional. Dirección o nombre del intervalo. Si no se especifica, se devuelve todo el intervalo de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-p104">Optional. The address or the name of the range. If not specified, the entire worksheet range is returned.</span></span>|

## <a name="response"></a><span data-ttu-id="bb6cf-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb6cf-133">Response</span></span>

<span data-ttu-id="bb6cf-134">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-134">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bb6cf-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bb6cf-135">Example</span></span>
<span data-ttu-id="bb6cf-136">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-136">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="bb6cf-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bb6cf-137">Request</span></span>
<span data-ttu-id="bb6cf-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheet_range"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/range(address='A1:B2')
```

##### <a name="response"></a><span data-ttu-id="bb6cf-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb6cf-139">Response</span></span>
<span data-ttu-id="bb6cf-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

<span data-ttu-id="bb6cf-143">Si el parámetro opcional `address` no se especifica, esta función devuelve el intervalo de hoja de cálculo completa.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-143">If the optional `address` parameter is not specified, this function returns the entire worksheet range.</span></span>

##### <a name="request"></a><span data-ttu-id="bb6cf-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bb6cf-144">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "worksheet_range_noaddress"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/range
```

##### <a name="response"></a><span data-ttu-id="bb6cf-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb6cf-145">Response</span></span>

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
  "description": "Worksheet: Range",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->