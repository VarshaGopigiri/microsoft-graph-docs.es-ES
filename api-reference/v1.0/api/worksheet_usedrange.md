# <a name="worksheet-usedrange"></a><span data-ttu-id="98594-101">Worksheet: UsedRange</span><span class="sxs-lookup"><span data-stu-id="98594-101">Worksheet: UsedRange</span></span>

<span data-ttu-id="98594-p101">El rango usado es el rango más pequeño que abarque las celdas que tienen asignado un valor o un formato. Si la hoja de cálculo está en blanco, esta función devolverá la celda superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="98594-p101">The used range is the smallest range that encompasses any cells that have a value or formatting assigned to them. If the worksheet is blank, this function will return the top left cell.</span></span>
## <a name="permissions"></a><span data-ttu-id="98594-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="98594-104">Permissions</span></span>
<span data-ttu-id="98594-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="98594-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="98594-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="98594-107">Permission type</span></span>      | <span data-ttu-id="98594-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="98594-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="98594-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="98594-109">Delegated (work or school account)</span></span> | <span data-ttu-id="98594-110">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="98594-110">Files.ReadWrite</span></span>    |
|<span data-ttu-id="98594-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="98594-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="98594-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="98594-112">Not supported.</span></span>    |
|<span data-ttu-id="98594-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="98594-113">Application</span></span> | <span data-ttu-id="98594-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="98594-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="98594-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="98594-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/UsedRange

```

## <a name="optional-request-parameter"></a><span data-ttu-id="98594-116">Parámetro de solicitud opcional</span><span class="sxs-lookup"><span data-stu-id="98594-116">Optional request parameter</span></span>
<span data-ttu-id="98594-117">En la URL de solicitud, proporcione un parámetro de consulta opcional.</span><span class="sxs-lookup"><span data-stu-id="98594-117">In the request URL, provide an optional query parameter.</span></span>

| <span data-ttu-id="98594-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="98594-118">Parameter</span></span>    | <span data-ttu-id="98594-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="98594-119">Type</span></span>   |<span data-ttu-id="98594-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="98594-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="98594-121">valuesOnly</span><span class="sxs-lookup"><span data-stu-id="98594-121">valuesOnly</span></span>|<span data-ttu-id="98594-122">Boolean</span><span class="sxs-lookup"><span data-stu-id="98594-122">Boolean</span></span>|<span data-ttu-id="98594-p103">Opcional. Solo tiene en cuenta las celdas con valores como celdas usadas (ignora el formato).</span><span class="sxs-lookup"><span data-stu-id="98594-p103">Optional. Considers only cells with values as used cells (ignores formatting).</span></span>|

## <a name="request-headers"></a><span data-ttu-id="98594-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="98594-125">Request headers</span></span>
| <span data-ttu-id="98594-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="98594-126">Name</span></span>       | <span data-ttu-id="98594-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="98594-127">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="98594-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="98594-128">Authorization</span></span>  | <span data-ttu-id="98594-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="98594-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="98594-131">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="98594-131">Workbook-Session-Id</span></span>  | <span data-ttu-id="98594-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="98594-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="response"></a><span data-ttu-id="98594-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98594-134">Response</span></span>

<span data-ttu-id="98594-135">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98594-135">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="98594-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="98594-136">Example</span></span>
<span data-ttu-id="98594-137">Aquí tiene un ejemplo que muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="98594-137">Here is an example that shows how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="98594-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="98594-138">Request</span></span>
<span data-ttu-id="98594-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="98594-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheet_usedrange"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/UsedRange(valuesOnly=true)
```

##### <a name="response"></a><span data-ttu-id="98594-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98594-140">Response</span></span>
<span data-ttu-id="98594-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="98594-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "addressLocal": "addressLocal-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Worksheet: UsedRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
