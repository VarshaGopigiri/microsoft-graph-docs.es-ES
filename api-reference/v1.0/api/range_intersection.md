# <a name="range-intersection"></a><span data-ttu-id="9a2fc-101">Range: Intersection</span><span class="sxs-lookup"><span data-stu-id="9a2fc-101">Range: Intersection</span></span>

<span data-ttu-id="9a2fc-102">Obtiene el objeto de rango que representa la intersección rectangular de los rangos especificados.</span><span class="sxs-lookup"><span data-stu-id="9a2fc-102">Gets the range object that represents the rectangular intersection of the given ranges.</span></span>
## <a name="permissions"></a><span data-ttu-id="9a2fc-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="9a2fc-103">Permissions</span></span>
<span data-ttu-id="9a2fc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9a2fc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9a2fc-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9a2fc-106">Permission type</span></span>      | <span data-ttu-id="9a2fc-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9a2fc-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9a2fc-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9a2fc-108">Delegated (work or school account)</span></span> | <span data-ttu-id="9a2fc-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9a2fc-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="9a2fc-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9a2fc-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9a2fc-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9a2fc-111">Not supported.</span></span>    |
|<span data-ttu-id="9a2fc-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9a2fc-112">Application</span></span> | <span data-ttu-id="9a2fc-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9a2fc-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9a2fc-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9a2fc-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/Intersection
GET /workbook/worksheets/{id|name}/range(<address>)/Intersection
GET /workbook/tables/{id|name}/columns/{id|name}/range/Intersection

```
## <a name="request-headers"></a><span data-ttu-id="9a2fc-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9a2fc-115">Request headers</span></span>
| <span data-ttu-id="9a2fc-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="9a2fc-116">Name</span></span>       | <span data-ttu-id="9a2fc-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a2fc-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9a2fc-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="9a2fc-118">Authorization</span></span>  | <span data-ttu-id="9a2fc-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9a2fc-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9a2fc-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9a2fc-121">Request body</span></span>
<span data-ttu-id="9a2fc-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="9a2fc-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="9a2fc-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9a2fc-123">Parameter</span></span>    | <span data-ttu-id="9a2fc-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a2fc-124">Type</span></span>   |<span data-ttu-id="9a2fc-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a2fc-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9a2fc-126">anotherRange</span><span class="sxs-lookup"><span data-stu-id="9a2fc-126">anotherRange</span></span>|<span data-ttu-id="9a2fc-127">string</span><span class="sxs-lookup"><span data-stu-id="9a2fc-127">string</span></span>|<span data-ttu-id="9a2fc-128">Objeto de intervalo o dirección de intervalo que se usará para determinar la intersección de los intervalos.</span><span class="sxs-lookup"><span data-stu-id="9a2fc-128">The range object or range address that will be used to determine the intersection of ranges.</span></span>|

## <a name="response"></a><span data-ttu-id="9a2fc-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a2fc-129">Response</span></span>

<span data-ttu-id="9a2fc-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9a2fc-130">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9a2fc-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9a2fc-131">Example</span></span>
<span data-ttu-id="9a2fc-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9a2fc-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="9a2fc-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9a2fc-133">Request</span></span>
<span data-ttu-id="9a2fc-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9a2fc-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_intersection"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/Intersection
Content-type: application/json
Content-length: 42

{
  "anotherRange": "anotherRange-value"
}
```

##### <a name="response"></a><span data-ttu-id="9a2fc-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a2fc-135">Response</span></span>
<span data-ttu-id="9a2fc-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9a2fc-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: Intersection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->