# <a name="worksheet-range"></a><span data-ttu-id="c32cf-101">Worksheet: Range</span><span class="sxs-lookup"><span data-stu-id="c32cf-101">Worksheet: Range</span></span>

<span data-ttu-id="c32cf-102">Obtiene el objeto de rango especificado por la dirección o el nombre.</span><span class="sxs-lookup"><span data-stu-id="c32cf-102">Gets the range object specified by the address or name.</span></span>
## <a name="permissions"></a><span data-ttu-id="c32cf-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="c32cf-103">Permissions</span></span>
<span data-ttu-id="c32cf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c32cf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c32cf-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c32cf-106">Permission type</span></span>      | <span data-ttu-id="c32cf-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c32cf-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c32cf-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c32cf-108">Delegated (work or school account)</span></span> | <span data-ttu-id="c32cf-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c32cf-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c32cf-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c32cf-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c32cf-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c32cf-111">Not supported.</span></span>    |
|<span data-ttu-id="c32cf-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c32cf-112">Application</span></span> | <span data-ttu-id="c32cf-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c32cf-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c32cf-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c32cf-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/Range

```
## <a name="request-headers"></a><span data-ttu-id="c32cf-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c32cf-115">Request headers</span></span>
| <span data-ttu-id="c32cf-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="c32cf-116">Name</span></span>       | <span data-ttu-id="c32cf-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c32cf-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="c32cf-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="c32cf-118">Authorization</span></span>  | <span data-ttu-id="c32cf-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c32cf-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c32cf-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c32cf-121">Request body</span></span>
<span data-ttu-id="c32cf-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="c32cf-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c32cf-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c32cf-123">Parameter</span></span>    | <span data-ttu-id="c32cf-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="c32cf-124">Type</span></span>   |<span data-ttu-id="c32cf-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="c32cf-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c32cf-126">address</span><span class="sxs-lookup"><span data-stu-id="c32cf-126">address</span></span>|<span data-ttu-id="c32cf-127">string</span><span class="sxs-lookup"><span data-stu-id="c32cf-127">string</span></span>|<span data-ttu-id="c32cf-p103">Opcional. Dirección o nombre del intervalo. Si no se especifica, se devuelve todo el intervalo de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="c32cf-p103">Optional. The address or the name of the range. If not specified, the entire worksheet range is returned.</span></span>|

## <a name="response"></a><span data-ttu-id="c32cf-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c32cf-131">Response</span></span>

<span data-ttu-id="c32cf-132">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c32cf-132">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c32cf-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c32cf-133">Example</span></span>
<span data-ttu-id="c32cf-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c32cf-134">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c32cf-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c32cf-135">Request</span></span>
<span data-ttu-id="c32cf-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c32cf-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheet_range"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/Range
Content-type: application/json
Content-length: 32

{
  "address": "address-value"
}
```

##### <a name="response"></a><span data-ttu-id="c32cf-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c32cf-137">Response</span></span>
<span data-ttu-id="c32cf-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c32cf-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Worksheet: Range",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->