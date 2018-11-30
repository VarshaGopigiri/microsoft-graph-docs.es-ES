---
title: 'Chart: Image'
description: Representa el gráfico como una imagen con codificación Base64 al escalar el gráfico a las dimensiones especificadas.
ms.openlocfilehash: 33a28f5b5033f9e123fede12eacfbaa78215f313
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032337"
---
# <a name="chart-image"></a><span data-ttu-id="fb07b-103">Chart: Image</span><span class="sxs-lookup"><span data-stu-id="fb07b-103">Chart: Image</span></span>

<span data-ttu-id="fb07b-104">Representa el gráfico como una imagen con codificación Base64 al escalar el gráfico a las dimensiones especificadas.</span><span class="sxs-lookup"><span data-stu-id="fb07b-104">Renders the chart as a base64-encoded image by scaling the chart to fit the specified dimensions.</span></span>
## <a name="permissions"></a><span data-ttu-id="fb07b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="fb07b-105">Permissions</span></span>
<span data-ttu-id="fb07b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fb07b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fb07b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fb07b-108">Permission type</span></span>      | <span data-ttu-id="fb07b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fb07b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fb07b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fb07b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="fb07b-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb07b-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="fb07b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fb07b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fb07b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fb07b-113">Not supported.</span></span>    |
|<span data-ttu-id="fb07b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fb07b-114">Application</span></span> | <span data-ttu-id="fb07b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fb07b-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fb07b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fb07b-116">HTTP request</span></span>
<!-- { "blockType": "samples" } -->
```http
GET /workbook/worksheets/{id|name}/charts/{name}/image
GET /workbook/worksheets/{id|name}/charts/{name}/image(width=640)
GET /workbook/worksheets/{id|name}/charts/{name}/image(width=640,height=480)
GET /workbook/worksheets/{id|name}/charts/{name}/image(width=640,height=480,fittingMode='fit')
```
## <a name="request-headers"></a><span data-ttu-id="fb07b-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fb07b-117">Request headers</span></span>
| <span data-ttu-id="fb07b-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="fb07b-118">Name</span></span>       | <span data-ttu-id="fb07b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb07b-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="fb07b-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="fb07b-120">Authorization</span></span>  | <span data-ttu-id="fb07b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fb07b-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="fb07b-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="fb07b-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="fb07b-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="fb07b-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="path-parameters"></a><span data-ttu-id="fb07b-126">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="fb07b-126">Path parameters</span></span>
<span data-ttu-id="fb07b-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="fb07b-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="fb07b-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fb07b-128">Parameter</span></span>    | <span data-ttu-id="fb07b-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb07b-129">Type</span></span>   |<span data-ttu-id="fb07b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb07b-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fb07b-131">height</span><span class="sxs-lookup"><span data-stu-id="fb07b-131">height</span></span>|<span data-ttu-id="fb07b-132">Int32</span><span class="sxs-lookup"><span data-stu-id="fb07b-132">Int32</span></span>|<span data-ttu-id="fb07b-133">La altura deseada de la imagen resultante.</span><span class="sxs-lookup"><span data-stu-id="fb07b-133">The desired height of the resulting image.</span></span> <span data-ttu-id="fb07b-134">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fb07b-134">Optional.</span></span>|
|<span data-ttu-id="fb07b-135">width</span><span class="sxs-lookup"><span data-stu-id="fb07b-135">width</span></span>|<span data-ttu-id="fb07b-136">Int32</span><span class="sxs-lookup"><span data-stu-id="fb07b-136">Int32</span></span>|<span data-ttu-id="fb07b-137">El ancho deseado de la imagen resultante.</span><span class="sxs-lookup"><span data-stu-id="fb07b-137">The desired width of the resulting image.</span></span> <span data-ttu-id="fb07b-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fb07b-138">Optional.</span></span>|
|<span data-ttu-id="fb07b-139">fittingMode</span><span class="sxs-lookup"><span data-stu-id="fb07b-139">fittingMode</span></span>|<span data-ttu-id="fb07b-140">string</span><span class="sxs-lookup"><span data-stu-id="fb07b-140">string</span></span>|<span data-ttu-id="fb07b-141">El método utilizado para escalar el gráfico a las dimensiones especificadas (si se establecen el alto y ancho)."</span><span class="sxs-lookup"><span data-stu-id="fb07b-141">The method used to scale the chart to the specified dimensions (if both height and width are set)."</span></span>  <span data-ttu-id="fb07b-142">Los valores posibles son: `Fit`, `FitAndCenter`, `Fill`.</span><span class="sxs-lookup"><span data-stu-id="fb07b-142">The possible values are: `Fit`, `FitAndCenter`, `Fill`.</span></span>|

## <a name="response"></a><span data-ttu-id="fb07b-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb07b-143">Response</span></span>

<span data-ttu-id="fb07b-144">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la cadena de imagen en base 64 en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb07b-144">If successful, this method returns `200 OK` response code and base-64 image string in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fb07b-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb07b-145">Example</span></span>
<span data-ttu-id="fb07b-146">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="fb07b-146">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="fb07b-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fb07b-147">Request</span></span>
<span data-ttu-id="fb07b-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fb07b-148">Here is an example of the request.</span></span>

<!-- { "blockType": "request" } -->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/image(width=640,height=480,fittingMode='fit')
```

##### <a name="response"></a><span data-ttu-id="fb07b-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb07b-149">Response</span></span>
<span data-ttu-id="fb07b-150">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb07b-150">Here is an example of the response.</span></span> <span data-ttu-id="fb07b-151">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="fb07b-151">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="fb07b-152">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fb07b-152">All of the properties will be returned from an actual call.</span></span>
<!-- { "blockType": "response", "@odata.type": "Edm.String" } -->
```http
HTTP/1.1 200 OK
Content-type: application/json;odata.metadata=minimal;odata.streaming=true

{
"value" : "base-64 chart image string"
}
```

## <a name="usage"></a><span data-ttu-id="fb07b-153">Uso</span><span class="sxs-lookup"><span data-stu-id="fb07b-153">Usage</span></span>

<span data-ttu-id="fb07b-154">Puede mostrar la cadena en base 64 en una etiqueta de imagen HTML: `<img src="data:image/png;base64,{base-64 chart image string}/>`.</span><span class="sxs-lookup"><span data-stu-id="fb07b-154">You can display the base-64 string inside an HTML image tag: `<img src="data:image/png;base64,{base-64 chart image string}/>`.</span></span>

<span data-ttu-id="fb07b-155">Para usar el comportamiento predeterminado, utilice `Image(width=0,height=0,fittingMode='fit')`.</span><span class="sxs-lookup"><span data-stu-id="fb07b-155">For default behavior, use `Image(width=0,height=0,fittingMode='fit')`.</span></span> <span data-ttu-id="fb07b-156">Este es un ejemplo de una imagen de gráfico devuelta con los parámetros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="fb07b-156">Here is an example of a chart image returned with the default parameters.</span></span>

![Imagen de gráfico de Excel con alto y ancho predeterminados.](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/GetChart-default.png)

<span data-ttu-id="fb07b-158">Si quiere personalizar la visualización de la imagen, especifique un alto, un ancho y un modo de ajuste.</span><span class="sxs-lookup"><span data-stu-id="fb07b-158">If you want to customize the display of the image, specify a height, width, and a fitting mode.</span></span> <span data-ttu-id="fb07b-159">Esta es la misma imagen de gráfico si la recupera con estos parámetros: `Image(width=500,height=500,fittingMode='Fill')`.</span><span class="sxs-lookup"><span data-stu-id="fb07b-159">Here is what the same chart image looks like if you retrieve it with these parameters: `Image(width=500,height=500,fittingMode='Fill')`.</span></span>

![Imagen de gráfico de Excel con alto y ancho predeterminados.](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/GetChart-fill.png)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Chart: Image",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
