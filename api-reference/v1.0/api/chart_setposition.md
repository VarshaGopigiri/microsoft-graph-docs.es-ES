# <a name="chart-setposition"></a><span data-ttu-id="460b4-101">Chart: setPosition</span><span class="sxs-lookup"><span data-stu-id="460b4-101">Chart: setPosition</span></span>

<span data-ttu-id="460b4-102">Coloca el gráfico con respecto a las celdas de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="460b4-102">Positions the chart relative to cells on the worksheet.</span></span>
## <a name="permissions"></a><span data-ttu-id="460b4-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="460b4-103">Permissions</span></span>
<span data-ttu-id="460b4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="460b4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="460b4-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="460b4-106">Permission type</span></span>      | <span data-ttu-id="460b4-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="460b4-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="460b4-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="460b4-108">Delegated (work or school account)</span></span> | <span data-ttu-id="460b4-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="460b4-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="460b4-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="460b4-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="460b4-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="460b4-111">Not supported.</span></span>    |
|<span data-ttu-id="460b4-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="460b4-112">Application</span></span> | <span data-ttu-id="460b4-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="460b4-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="460b4-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="460b4-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/{name}/setPosition

```
## <a name="request-headers"></a><span data-ttu-id="460b4-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="460b4-115">Request headers</span></span>
| <span data-ttu-id="460b4-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="460b4-116">Name</span></span>       | <span data-ttu-id="460b4-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="460b4-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="460b4-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="460b4-118">Authorization</span></span>  | <span data-ttu-id="460b4-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="460b4-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="460b4-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="460b4-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="460b4-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="460b4-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="460b4-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="460b4-124">Request body</span></span>
<span data-ttu-id="460b4-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="460b4-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="460b4-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="460b4-126">Parameter</span></span>    | <span data-ttu-id="460b4-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="460b4-127">Type</span></span>   |<span data-ttu-id="460b4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="460b4-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="460b4-129">startCell</span><span class="sxs-lookup"><span data-stu-id="460b4-129">startCell</span></span>|<span data-ttu-id="460b4-130">Json</span><span class="sxs-lookup"><span data-stu-id="460b4-130">Json</span></span>|<span data-ttu-id="460b4-p104">Celda de inicio. Aquí es adonde se moverá el gráfico. La celda de inicio es la celda superior izquierda o superior derecha, en función de la configuración del usuario de la presentación de derecha a izquierda.</span><span class="sxs-lookup"><span data-stu-id="460b4-p104">The start cell. This is where the chart will be moved to. The start cell is the top-left or top-right cell, depending on the user's right-to-left display settings.</span></span>|
|<span data-ttu-id="460b4-134">endCell</span><span class="sxs-lookup"><span data-stu-id="460b4-134">endCell</span></span>|<span data-ttu-id="460b4-135">Json</span><span class="sxs-lookup"><span data-stu-id="460b4-135">Json</span></span>|<span data-ttu-id="460b4-p105">Opcional. Última celda. Si se especifica, el ancho y el alto del gráfico se establecerán de modo que cubran totalmente esta celda o rango.</span><span class="sxs-lookup"><span data-stu-id="460b4-p105">Optional. The end cell. If specified, the chart's width and height will be set to fully cover up this cell/range.</span></span>|

## <a name="response"></a><span data-ttu-id="460b4-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="460b4-139">Response</span></span>

<span data-ttu-id="460b4-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="460b4-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="460b4-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="460b4-142">Example</span></span>
<span data-ttu-id="460b4-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="460b4-143">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="460b4-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="460b4-144">Request</span></span>
<span data-ttu-id="460b4-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="460b4-145">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chart_setposition"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/setPosition
Content-type: application/json
Content-length: 66

{
  "startCell": "startCell-value",
  "endCell": "endCell-value"
}
```

##### <a name="response"></a><span data-ttu-id="460b4-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="460b4-146">Response</span></span>
<span data-ttu-id="460b4-147">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="460b4-147">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response"
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