# <a name="chartpointscollection-itemat"></a><span data-ttu-id="0a0e3-101">ChartPointsCollection: ItemAt</span><span class="sxs-lookup"><span data-stu-id="0a0e3-101">ChartPointsCollection: ItemAt</span></span>

<span data-ttu-id="0a0e3-102">Recupera un punto en función de su posición dentro de la serie.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-102">Retrieve a point based on its position within the series.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0a0e3-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0a0e3-103">Prerequisites</span></span>
<span data-ttu-id="0a0e3-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="0a0e3-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="0a0e3-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0a0e3-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="0a0e3-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0a0e3-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)/points/ItemAt

```
## <a name="request-headers"></a><span data-ttu-id="0a0e3-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0a0e3-107">Request headers</span></span>
| <span data-ttu-id="0a0e3-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="0a0e3-108">Name</span></span>       | <span data-ttu-id="0a0e3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a0e3-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0a0e3-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="0a0e3-110">Authorization</span></span>  | <span data-ttu-id="0a0e3-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="0a0e3-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0a0e3-113">Request body</span></span>
<span data-ttu-id="0a0e3-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="0a0e3-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0a0e3-115">Parameter</span></span>    | <span data-ttu-id="0a0e3-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a0e3-116">Type</span></span>   |<span data-ttu-id="0a0e3-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a0e3-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0a0e3-118">index</span><span class="sxs-lookup"><span data-stu-id="0a0e3-118">index</span></span>|<span data-ttu-id="0a0e3-119">number</span><span class="sxs-lookup"><span data-stu-id="0a0e3-119">number</span></span>|<span data-ttu-id="0a0e3-p102">Valor de índice del objeto que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-p102">Index value of the object to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="0a0e3-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a0e3-122">Response</span></span>

<span data-ttu-id="0a0e3-123">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [ChartPoint](../resources/chartpoint.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-123">If successful, this method returns `200, OK` response code and [ChartPoint](../resources/chartpoint.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0a0e3-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a0e3-124">Example</span></span>
<span data-ttu-id="0a0e3-125">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-125">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="0a0e3-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0a0e3-126">Request</span></span>
<span data-ttu-id="0a0e3-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-127">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="0a0e3-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a0e3-128">Response</span></span>
<span data-ttu-id="0a0e3-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0a0e3-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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