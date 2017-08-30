# <a name="chartpointscollection-itemat"></a><span data-ttu-id="bcddd-101">ChartPointsCollection: ItemAt</span><span class="sxs-lookup"><span data-stu-id="bcddd-101">ChartPointsCollection: ItemAt</span></span>

<span data-ttu-id="bcddd-102">Recuperar un punto en función de su posición dentro de la serie.</span><span class="sxs-lookup"><span data-stu-id="bcddd-102">Retrieve a point based on its position within the series.</span></span>
## <a name="permissions"></a><span data-ttu-id="bcddd-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="bcddd-103">Permissions</span></span>
<span data-ttu-id="bcddd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bcddd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="bcddd-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bcddd-106">Permission type</span></span>      | <span data-ttu-id="bcddd-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bcddd-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bcddd-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bcddd-108">Delegated (work or school account)</span></span> | <span data-ttu-id="bcddd-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bcddd-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="bcddd-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bcddd-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bcddd-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bcddd-111">Not supported.</span></span>    |
|<span data-ttu-id="bcddd-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bcddd-112">Application</span></span> | <span data-ttu-id="bcddd-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bcddd-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="bcddd-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bcddd-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)/points/ItemAt

```
## <a name="request-headers"></a><span data-ttu-id="bcddd-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bcddd-115">Request headers</span></span>
| <span data-ttu-id="bcddd-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="bcddd-116">Name</span></span>       | <span data-ttu-id="bcddd-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcddd-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="bcddd-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="bcddd-118">Authorization</span></span>  | <span data-ttu-id="bcddd-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bcddd-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bcddd-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bcddd-121">Request body</span></span>
<span data-ttu-id="bcddd-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="bcddd-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="bcddd-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bcddd-123">Parameter</span></span>    | <span data-ttu-id="bcddd-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="bcddd-124">Type</span></span>   |<span data-ttu-id="bcddd-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcddd-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bcddd-126">index</span><span class="sxs-lookup"><span data-stu-id="bcddd-126">index</span></span>|<span data-ttu-id="bcddd-127">number</span><span class="sxs-lookup"><span data-stu-id="bcddd-127">number</span></span>|<span data-ttu-id="bcddd-p103">Valor de índice del objeto que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="bcddd-p103">Index value of the object to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="bcddd-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bcddd-130">Response</span></span>

<span data-ttu-id="bcddd-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [ChartPoint](../resources/chartpoint.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bcddd-131">If successful, this method returns `200, OK` response code and [ChartPoint](../resources/chartpoint.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bcddd-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bcddd-132">Example</span></span>
<span data-ttu-id="bcddd-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="bcddd-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="bcddd-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bcddd-134">Request</span></span>
<span data-ttu-id="bcddd-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bcddd-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartpointscollection_itemat"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)/points/ItemAt
Content-type: application/json
Content-length: 20

{
  "index": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="bcddd-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bcddd-136">Response</span></span>
<span data-ttu-id="bcddd-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bcddd-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartPoint"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 20

{
  "value": {
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartPointsCollection: ItemAt",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->