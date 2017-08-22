# <a name="chart-setposition"></a><span data-ttu-id="4262e-101">Chart: setPosition</span><span class="sxs-lookup"><span data-stu-id="4262e-101">Chart: setPosition</span></span>

<span data-ttu-id="4262e-102">Coloca el gráfico con respecto a las celdas de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="4262e-102">Positions the chart relative to cells on the worksheet.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4262e-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4262e-103">Prerequisites</span></span>
<span data-ttu-id="4262e-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="4262e-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="4262e-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4262e-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="4262e-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4262e-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/setPosition

```
## <a name="request-headers"></a><span data-ttu-id="4262e-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4262e-107">Request headers</span></span>
| <span data-ttu-id="4262e-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="4262e-108">Name</span></span>       | <span data-ttu-id="4262e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4262e-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="4262e-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="4262e-110">Authorization</span></span>  | <span data-ttu-id="4262e-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4262e-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="4262e-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4262e-113">Request body</span></span>
<span data-ttu-id="4262e-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="4262e-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="4262e-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4262e-115">Parameter</span></span>    | <span data-ttu-id="4262e-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="4262e-116">Type</span></span>   |<span data-ttu-id="4262e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4262e-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4262e-118">startCell</span><span class="sxs-lookup"><span data-stu-id="4262e-118">startCell</span></span>|<span data-ttu-id="4262e-119">string</span><span class="sxs-lookup"><span data-stu-id="4262e-119">string</span></span>|<span data-ttu-id="4262e-p102">Celda de inicio. Aquí es adonde se moverá el gráfico. La celda de inicio es la celda superior izquierda o superior derecha, en función de la configuración del usuario de la presentación de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="4262e-p102">The start cell. This is where the chart will be moved to. The start cell is the top-left or top-right cell, depending on the user's right-to-left display settings.</span></span>|
|<span data-ttu-id="4262e-123">endCell</span><span class="sxs-lookup"><span data-stu-id="4262e-123">endCell</span></span>|<span data-ttu-id="4262e-124">string</span><span class="sxs-lookup"><span data-stu-id="4262e-124">string</span></span>|<span data-ttu-id="4262e-p103">Opcional. Última celda. Si se especifica, el ancho y el alto del gráfico se establecerán de modo que cubran totalmente esta celda o rango.</span><span class="sxs-lookup"><span data-stu-id="4262e-p103">Optional. The end cell. If specified, the chart's width and height will be set to fully cover up this cell/range.</span></span>|

## <a name="response"></a><span data-ttu-id="4262e-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4262e-128">Response</span></span>

<span data-ttu-id="4262e-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4262e-p104">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4262e-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4262e-131">Example</span></span>
<span data-ttu-id="4262e-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="4262e-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="4262e-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4262e-133">Request</span></span>
<span data-ttu-id="4262e-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4262e-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chart_setposition"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/setPosition
Content-type: application/json
Content-length: 66

{
  "startCell": "startCell-value",
  "endCell": "endCell-value"
}
```

##### <a name="response"></a><span data-ttu-id="4262e-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4262e-135">Response</span></span>
<span data-ttu-id="4262e-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4262e-136">Here is an example of the response.</span></span> 
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
  "description": "Chart: setPosition",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->