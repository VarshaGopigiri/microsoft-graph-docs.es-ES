# <a name="chartcollection-itemat"></a><span data-ttu-id="9cb54-101">ChartCollection: ItemAt</span><span class="sxs-lookup"><span data-stu-id="9cb54-101">ChartCollection: ItemAt</span></span>

<span data-ttu-id="9cb54-102">Obtiene un gráfico en función de su posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="9cb54-102">Gets a chart based on its position in the collection.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9cb54-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9cb54-103">Prerequisites</span></span>
<span data-ttu-id="9cb54-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="9cb54-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="9cb54-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9cb54-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="9cb54-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9cb54-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/ItemAt

```
## <a name="request-headers"></a><span data-ttu-id="9cb54-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9cb54-107">Request headers</span></span>
| <span data-ttu-id="9cb54-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="9cb54-108">Name</span></span>       | <span data-ttu-id="9cb54-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9cb54-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9cb54-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="9cb54-110">Authorization</span></span>  | <span data-ttu-id="9cb54-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9cb54-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="9cb54-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9cb54-113">Request body</span></span>
<span data-ttu-id="9cb54-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="9cb54-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="9cb54-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9cb54-115">Parameter</span></span>    | <span data-ttu-id="9cb54-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="9cb54-116">Type</span></span>   |<span data-ttu-id="9cb54-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9cb54-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9cb54-118">index</span><span class="sxs-lookup"><span data-stu-id="9cb54-118">index</span></span>|<span data-ttu-id="9cb54-119">number</span><span class="sxs-lookup"><span data-stu-id="9cb54-119">number</span></span>|<span data-ttu-id="9cb54-p102">Valor de índice del objeto que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="9cb54-p102">Index value of the object to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="9cb54-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9cb54-122">Response</span></span>

<span data-ttu-id="9cb54-123">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Chart](../resources/chart.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9cb54-123">If successful, this method returns `200, OK` response code and [Chart](../resources/chart.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9cb54-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9cb54-124">Example</span></span>
<span data-ttu-id="9cb54-125">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9cb54-125">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="9cb54-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9cb54-126">Request</span></span>
<span data-ttu-id="9cb54-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9cb54-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartcollection_itemat"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/ItemAt
Content-type: application/json
Content-length: 20

{
  "index": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="9cb54-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9cb54-128">Response</span></span>
<span data-ttu-id="9cb54-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9cb54-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chart"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 52

{
  "id": "id-value",
  "height": 99,
  "left": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartCollection: ItemAt",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->