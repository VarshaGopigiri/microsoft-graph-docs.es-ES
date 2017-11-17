# <a name="chart-setposition"></a><span data-ttu-id="b5a01-101">Chart: setPosition</span><span class="sxs-lookup"><span data-stu-id="b5a01-101">Chart: setPosition</span></span>

<span data-ttu-id="b5a01-102">Coloca el gráfico con respecto a las celdas de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="b5a01-102">Positions the chart relative to cells on the worksheet.</span></span>
## <a name="permissions"></a><span data-ttu-id="b5a01-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="b5a01-103">Permissions</span></span>
<span data-ttu-id="b5a01-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b5a01-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b5a01-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b5a01-106">Permission type</span></span>      | <span data-ttu-id="b5a01-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b5a01-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b5a01-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b5a01-108">Delegated (work or school account)</span></span> | <span data-ttu-id="b5a01-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b5a01-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b5a01-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b5a01-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b5a01-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b5a01-111">Not supported.</span></span>    |
|<span data-ttu-id="b5a01-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b5a01-112">Application</span></span> | <span data-ttu-id="b5a01-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b5a01-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b5a01-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b5a01-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/setPosition

```
## <a name="request-headers"></a><span data-ttu-id="b5a01-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b5a01-115">Request headers</span></span>
| <span data-ttu-id="b5a01-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="b5a01-116">Name</span></span>       | <span data-ttu-id="b5a01-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5a01-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b5a01-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="b5a01-118">Authorization</span></span>  | <span data-ttu-id="b5a01-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b5a01-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b5a01-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b5a01-121">Request body</span></span>
<span data-ttu-id="b5a01-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="b5a01-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="b5a01-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b5a01-123">Parameter</span></span>    | <span data-ttu-id="b5a01-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="b5a01-124">Type</span></span>   |<span data-ttu-id="b5a01-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5a01-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b5a01-126">startCell</span><span class="sxs-lookup"><span data-stu-id="b5a01-126">startCell</span></span>|<span data-ttu-id="b5a01-127">string</span><span class="sxs-lookup"><span data-stu-id="b5a01-127">string</span></span>|<span data-ttu-id="b5a01-p103">Celda de inicio. Aquí es adonde se moverá el gráfico. La celda de inicio es la celda superior izquierda o superior derecha, en función de la configuración del usuario de la presentación de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="b5a01-p103">The start cell. This is where the chart will be moved to. The start cell is the top-left or top-right cell, depending on the user's right-to-left display settings.</span></span>|
|<span data-ttu-id="b5a01-131">endCell</span><span class="sxs-lookup"><span data-stu-id="b5a01-131">endCell</span></span>|<span data-ttu-id="b5a01-132">string</span><span class="sxs-lookup"><span data-stu-id="b5a01-132">string</span></span>|<span data-ttu-id="b5a01-p104">Opcional. Última celda. Si se especifica, el ancho y el alto del gráfico se establecerán de modo que cubran totalmente esta celda o rango.</span><span class="sxs-lookup"><span data-stu-id="b5a01-p104">Optional. The end cell. If specified, the chart's width and height will be set to fully cover up this cell/range.</span></span>|

## <a name="response"></a><span data-ttu-id="b5a01-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b5a01-136">Response</span></span>

<span data-ttu-id="b5a01-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b5a01-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b5a01-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b5a01-139">Example</span></span>
<span data-ttu-id="b5a01-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b5a01-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b5a01-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b5a01-141">Request</span></span>
<span data-ttu-id="b5a01-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b5a01-142">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="b5a01-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b5a01-143">Response</span></span>
<span data-ttu-id="b5a01-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b5a01-144">Here is an example of the response.</span></span> 
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