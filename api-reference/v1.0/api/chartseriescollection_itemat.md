# <a name="chartseriescollection-itemat"></a><span data-ttu-id="d4b94-101">ChartSeriesCollection: ItemAt</span><span class="sxs-lookup"><span data-stu-id="d4b94-101">ChartSeriesCollection: ItemAt</span></span>

<span data-ttu-id="d4b94-102">Recupera una serie en función de su posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="d4b94-102">Retrieves a series based on its position in the collection</span></span>
## <a name="permissions"></a><span data-ttu-id="d4b94-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="d4b94-103">Permissions</span></span>
<span data-ttu-id="d4b94-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d4b94-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d4b94-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d4b94-106">Permission type</span></span>      | <span data-ttu-id="d4b94-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d4b94-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d4b94-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d4b94-108">Delegated (work or school account)</span></span> | <span data-ttu-id="d4b94-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d4b94-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d4b94-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d4b94-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d4b94-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d4b94-111">Not supported.</span></span>    |
|<span data-ttu-id="d4b94-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d4b94-112">Application</span></span> | <span data-ttu-id="d4b94-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d4b94-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d4b94-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d4b94-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/series/ItemAt

```
## <a name="request-headers"></a><span data-ttu-id="d4b94-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d4b94-115">Request headers</span></span>
| <span data-ttu-id="d4b94-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="d4b94-116">Name</span></span>       | <span data-ttu-id="d4b94-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4b94-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d4b94-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="d4b94-118">Authorization</span></span>  | <span data-ttu-id="d4b94-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d4b94-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d4b94-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d4b94-121">Request body</span></span>
<span data-ttu-id="d4b94-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="d4b94-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d4b94-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d4b94-123">Parameter</span></span>    | <span data-ttu-id="d4b94-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4b94-124">Type</span></span>   |<span data-ttu-id="d4b94-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4b94-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d4b94-126">index</span><span class="sxs-lookup"><span data-stu-id="d4b94-126">index</span></span>|<span data-ttu-id="d4b94-127">number</span><span class="sxs-lookup"><span data-stu-id="d4b94-127">number</span></span>|<span data-ttu-id="d4b94-p103">Valor de índice del objeto que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="d4b94-p103">Index value of the object to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="d4b94-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d4b94-130">Response</span></span>

<span data-ttu-id="d4b94-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [ChartSeries](../resources/chartseries.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d4b94-131">If successful, this method returns `200 OK` response code and [ChartSeries](../resources/chartseries.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d4b94-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d4b94-132">Example</span></span>
<span data-ttu-id="d4b94-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d4b94-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="d4b94-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d4b94-134">Request</span></span>
<span data-ttu-id="d4b94-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d4b94-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartseriescollection_itemat"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/series/ItemAt
Content-type: application/json
Content-length: 20

{
  "index": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="d4b94-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d4b94-136">Response</span></span>
<span data-ttu-id="d4b94-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d4b94-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartSeries"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartSeriesCollection: ItemAt",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->