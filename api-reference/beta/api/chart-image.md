---
title: 'Chart: Image'
description: Representa el gráfico como una imagen con codificación Base64 al escalar el gráfico a las dimensiones especificadas.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: d7d3b0bc33be46301a4abffa90d37c53c553e37d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854239"
---
# <a name="chart-image"></a><span data-ttu-id="3f7ef-103">Chart: Image</span><span class="sxs-lookup"><span data-stu-id="3f7ef-103">Chart: Image</span></span>

> <span data-ttu-id="3f7ef-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3f7ef-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3f7ef-106">Representa el gráfico como una imagen con codificación Base64 al escalar el gráfico a las dimensiones especificadas.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-106">Renders the chart as a base64-encoded image by scaling the chart to fit the specified dimensions.</span></span>
## <a name="permissions"></a><span data-ttu-id="3f7ef-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3f7ef-107">Permissions</span></span>
<span data-ttu-id="3f7ef-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3f7ef-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3f7ef-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3f7ef-110">Permission type</span></span>      | <span data-ttu-id="3f7ef-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3f7ef-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3f7ef-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3f7ef-112">Delegated (work or school account)</span></span> | <span data-ttu-id="3f7ef-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3f7ef-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="3f7ef-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3f7ef-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3f7ef-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3f7ef-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="3f7ef-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3f7ef-116">Application</span></span> | <span data-ttu-id="3f7ef-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="3f7ef-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3f7ef-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/charts(<name>)/Image(width=0,height=0,fittingMode='fit')

```
## <a name="request-headers"></a><span data-ttu-id="3f7ef-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3f7ef-119">Request headers</span></span>
| <span data-ttu-id="3f7ef-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="3f7ef-120">Name</span></span>       | <span data-ttu-id="3f7ef-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f7ef-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="3f7ef-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="3f7ef-122">Authorization</span></span>  | <span data-ttu-id="3f7ef-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="3f7ef-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="3f7ef-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="3f7ef-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="3f7ef-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3f7ef-128">Request body</span></span>
<span data-ttu-id="3f7ef-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="3f7ef-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3f7ef-130">Parameter</span></span>    | <span data-ttu-id="3f7ef-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f7ef-131">Type</span></span>   |<span data-ttu-id="3f7ef-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f7ef-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3f7ef-133">height</span><span class="sxs-lookup"><span data-stu-id="3f7ef-133">height</span></span>|<span data-ttu-id="3f7ef-134">number</span><span class="sxs-lookup"><span data-stu-id="3f7ef-134">number</span></span>|<span data-ttu-id="3f7ef-p105">Opcional. Alto deseado de la imagen resultante.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-p105">Optional. The desired height of the resulting image.</span></span>|
|<span data-ttu-id="3f7ef-137">width</span><span class="sxs-lookup"><span data-stu-id="3f7ef-137">width</span></span>|<span data-ttu-id="3f7ef-138">number</span><span class="sxs-lookup"><span data-stu-id="3f7ef-138">number</span></span>|<span data-ttu-id="3f7ef-p106">Opcional. Ancho deseado de la imagen resultante.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-p106">Optional. The desired width of the resulting image.</span></span>|
|<span data-ttu-id="3f7ef-141">fittingMode</span><span class="sxs-lookup"><span data-stu-id="3f7ef-141">fittingMode</span></span>|<span data-ttu-id="3f7ef-142">string</span><span class="sxs-lookup"><span data-stu-id="3f7ef-142">string</span></span>|<span data-ttu-id="3f7ef-p107">Opcional. Método usado para escalar el gráfico a las dimensiones especificadas (si se han establecido el alto y el ancho)".  Valores posibles: `Fit`, `FitAndCenter`, `Fill`.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-p107">Optional. The method used to scale the chart to the specified to the specified dimensions (if both height and width are set)."  Possible values are: `Fit`, `FitAndCenter`, `Fill`.</span></span>|

## <a name="response"></a><span data-ttu-id="3f7ef-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f7ef-146">Response</span></span>

<span data-ttu-id="3f7ef-147">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la cadena de imagen en base 64 en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-147">If successful, this method returns `200 OK` response code and base-64 image string in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3f7ef-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3f7ef-148">Example</span></span>
<span data-ttu-id="3f7ef-149">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-149">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="3f7ef-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3f7ef-150">Request</span></span>
<span data-ttu-id="3f7ef-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-151">Here is an example of the request.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/Image(width=0,height=0,fittingMode='fit')
```

##### <a name="response"></a><span data-ttu-id="3f7ef-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f7ef-152">Response</span></span>
<span data-ttu-id="3f7ef-153">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-153">Here is an example of the response.</span></span> <span data-ttu-id="3f7ef-154">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-154">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="3f7ef-155">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-155">All of the properties will be returned from an actual call.</span></span>
<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 3

{
"value" : "base-64 chart image string"
}
```

##### <a name="usage"></a><span data-ttu-id="3f7ef-156">Uso</span><span class="sxs-lookup"><span data-stu-id="3f7ef-156">Usage</span></span>

<span data-ttu-id="3f7ef-157">Puede mostrar la cadena en base 64 en una etiqueta de imagen HTML: `<img src="data:image/png;base64,{base-64 chart image string}/>`.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-157">You can display the base-64 string inside an HTML image tag: `<img src="data:image/png;base64,{base-64 chart image string}/>`.</span></span>

<span data-ttu-id="3f7ef-158">Para usar el comportamiento predeterminado, utilice `Image(width=0,height=0,fittingMode='fit')`.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-158">For default behavior, use `Image(width=0,height=0,fittingMode='fit')`.</span></span> <span data-ttu-id="3f7ef-159">Este es un ejemplo de una imagen de gráfico devuelta con los parámetros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-159">Here is an example of a chart image returned with the default parameters.</span></span>

![Imagen de gráfico de Excel con alto y ancho predeterminados.](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/GetChart-default.png)

<span data-ttu-id="3f7ef-161">Si quiere personalizar la visualización de la imagen, especifique un alto, un ancho y un modo de ajuste.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-161">If you want to customize the display of the image, specify a height, width, and a fitting mode.</span></span> <span data-ttu-id="3f7ef-162">Esta es la misma imagen de gráfico si la recupera con estos parámetros: `Image(width=500,height=500,fittingMode='Fill')`.</span><span class="sxs-lookup"><span data-stu-id="3f7ef-162">Here is what the same chart image looks like if you retrieve it with these parameters: `Image(width=500,height=500,fittingMode='Fill')`.</span></span>

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
