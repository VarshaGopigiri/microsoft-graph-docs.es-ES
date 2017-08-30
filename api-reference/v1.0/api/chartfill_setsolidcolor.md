# <a name="chartfill-setsolidcolor"></a><span data-ttu-id="a2725-101">ChartFill: setSolidColor</span><span class="sxs-lookup"><span data-stu-id="a2725-101">ChartFill: setSolidColor</span></span>

<span data-ttu-id="a2725-102">Establece el formato de relleno de un elemento de gráfico en un color uniforme.</span><span class="sxs-lookup"><span data-stu-id="a2725-102">Sets the fill formatting of a chart element to a uniform color.</span></span>
## <a name="permissions"></a><span data-ttu-id="a2725-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="a2725-103">Permissions</span></span>
<span data-ttu-id="a2725-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a2725-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a2725-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a2725-106">Permission type</span></span>      | <span data-ttu-id="a2725-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a2725-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a2725-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a2725-108">Delegated (work or school account)</span></span> | <span data-ttu-id="a2725-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a2725-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="a2725-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a2725-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a2725-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2725-111">Not supported.</span></span>    |
|<span data-ttu-id="a2725-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a2725-112">Application</span></span> | <span data-ttu-id="a2725-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2725-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a2725-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a2725-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/format/fill/setSolidColor
POST /workbook/worksheets/{id|name}/charts(<name>)/title/format/fill/setSolidColor
POST /workbook/worksheets/{id|name}/charts(<name>)/legend/format/fill/setSolidColor

```
## <a name="request-headers"></a><span data-ttu-id="a2725-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a2725-115">Request headers</span></span>
| <span data-ttu-id="a2725-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="a2725-116">Name</span></span>       | <span data-ttu-id="a2725-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2725-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="a2725-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="a2725-118">Authorization</span></span>  | <span data-ttu-id="a2725-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a2725-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a2725-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a2725-121">Request body</span></span>
<span data-ttu-id="a2725-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="a2725-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="a2725-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a2725-123">Parameter</span></span>    | <span data-ttu-id="a2725-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2725-124">Type</span></span>   |<span data-ttu-id="a2725-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2725-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a2725-126">color</span><span class="sxs-lookup"><span data-stu-id="a2725-126">color</span></span>|<span data-ttu-id="a2725-127">string</span><span class="sxs-lookup"><span data-stu-id="a2725-127">string</span></span>|<span data-ttu-id="a2725-128">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="a2725-128">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange").</span></span>|

## <a name="response"></a><span data-ttu-id="a2725-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2725-129">Response</span></span>

<span data-ttu-id="a2725-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2725-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a2725-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a2725-132">Example</span></span>
<span data-ttu-id="a2725-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a2725-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="a2725-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a2725-134">Request</span></span>
<span data-ttu-id="a2725-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2725-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartfill_setsolidcolor"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/format/fill/setSolidColor
Content-type: application/json
Content-length: 28

{
  "color": "color-value"
}
```

##### <a name="response"></a><span data-ttu-id="a2725-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2725-136">Response</span></span>
<span data-ttu-id="a2725-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2725-137">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartFill: setSolidColor",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->