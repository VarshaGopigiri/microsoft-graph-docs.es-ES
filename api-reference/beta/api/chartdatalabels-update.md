---
title: Actualizar chartdatalabels
description: Actualizar las propiedades del objeto chartdatalabels.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: f61113f8cd0617d6d8eb3f3191112d74e55f27cb
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27985441"
---
# <a name="update-chartdatalabels"></a><span data-ttu-id="ec9b9-103">Actualizar chartdatalabels</span><span class="sxs-lookup"><span data-stu-id="ec9b9-103">Update chartdatalabels</span></span>

> <span data-ttu-id="ec9b9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ec9b9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ec9b9-106">Actualizar las propiedades del objeto chartdatalabels.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-106">Update the properties of chartdatalabels object.</span></span>
## <a name="permissions"></a><span data-ttu-id="ec9b9-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ec9b9-107">Permissions</span></span>
<span data-ttu-id="ec9b9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ec9b9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ec9b9-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ec9b9-110">Permission type</span></span>      | <span data-ttu-id="ec9b9-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ec9b9-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ec9b9-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ec9b9-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ec9b9-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ec9b9-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="ec9b9-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ec9b9-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ec9b9-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ec9b9-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="ec9b9-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ec9b9-116">Application</span></span> | <span data-ttu-id="ec9b9-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ec9b9-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ec9b9-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/datalabels
```
## <a name="optional-request-headers"></a><span data-ttu-id="ec9b9-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="ec9b9-119">Optional request headers</span></span>
| <span data-ttu-id="ec9b9-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="ec9b9-120">Name</span></span>       | <span data-ttu-id="ec9b9-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec9b9-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="ec9b9-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="ec9b9-122">Authorization</span></span>  | <span data-ttu-id="ec9b9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ec9b9-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="ec9b9-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="ec9b9-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="ec9b9-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ec9b9-128">Request body</span></span>
<span data-ttu-id="ec9b9-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="ec9b9-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ec9b9-132">Property</span></span>     | <span data-ttu-id="ec9b9-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="ec9b9-133">Type</span></span>   |<span data-ttu-id="ec9b9-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec9b9-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ec9b9-135">position</span><span class="sxs-lookup"><span data-stu-id="ec9b9-135">position</span></span>|<span data-ttu-id="ec9b9-136">string</span><span class="sxs-lookup"><span data-stu-id="ec9b9-136">string</span></span>|<span data-ttu-id="ec9b9-p106">Valor DataLabelPosition que representa la posición de la etiqueta de datos. Valores posibles: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-p106">DataLabelPosition value that represents the position of the data label. Possible values are: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span></span>|
|<span data-ttu-id="ec9b9-139">separator</span><span class="sxs-lookup"><span data-stu-id="ec9b9-139">separator</span></span>|<span data-ttu-id="ec9b9-140">string</span><span class="sxs-lookup"><span data-stu-id="ec9b9-140">string</span></span>|<span data-ttu-id="ec9b9-141">Cadena que representa el separador empleado para las etiquetas de datos de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-141">String representing the separator used for the data labels on a chart.</span></span>|
|<span data-ttu-id="ec9b9-142">showBubbleSize</span><span class="sxs-lookup"><span data-stu-id="ec9b9-142">showBubbleSize</span></span>|<span data-ttu-id="ec9b9-143">boolean</span><span class="sxs-lookup"><span data-stu-id="ec9b9-143">boolean</span></span>|<span data-ttu-id="ec9b9-144">Valor booleano que representa si el tamaño de la burbuja de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-144">Boolean value representing if the data label bubble size is visible or not.</span></span>|
|<span data-ttu-id="ec9b9-145">showCategoryName</span><span class="sxs-lookup"><span data-stu-id="ec9b9-145">showCategoryName</span></span>|<span data-ttu-id="ec9b9-146">boolean</span><span class="sxs-lookup"><span data-stu-id="ec9b9-146">boolean</span></span>|<span data-ttu-id="ec9b9-147">Valor booleano que representa si el nombre de categoría de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-147">Boolean value representing if the data label category name is visible or not.</span></span>|
|<span data-ttu-id="ec9b9-148">showLegendKey</span><span class="sxs-lookup"><span data-stu-id="ec9b9-148">showLegendKey</span></span>|<span data-ttu-id="ec9b9-149">boolean</span><span class="sxs-lookup"><span data-stu-id="ec9b9-149">boolean</span></span>|<span data-ttu-id="ec9b9-150">Valor booleano que representa si la clave de leyenda de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-150">Boolean value representing if the data label legend key is visible or not.</span></span>|
|<span data-ttu-id="ec9b9-151">showPercentage</span><span class="sxs-lookup"><span data-stu-id="ec9b9-151">showPercentage</span></span>|<span data-ttu-id="ec9b9-152">boolean</span><span class="sxs-lookup"><span data-stu-id="ec9b9-152">boolean</span></span>|<span data-ttu-id="ec9b9-153">Valor booleano que representa si el porcentaje de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-153">Boolean value representing if the data label percentage is visible or not.</span></span>|
|<span data-ttu-id="ec9b9-154">showSeriesName</span><span class="sxs-lookup"><span data-stu-id="ec9b9-154">showSeriesName</span></span>|<span data-ttu-id="ec9b9-155">boolean</span><span class="sxs-lookup"><span data-stu-id="ec9b9-155">boolean</span></span>|<span data-ttu-id="ec9b9-156">Valor booleano que representa si el nombre de serie de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-156">Boolean value representing if the data label series name is visible or not.</span></span>|
|<span data-ttu-id="ec9b9-157">showValue</span><span class="sxs-lookup"><span data-stu-id="ec9b9-157">showValue</span></span>|<span data-ttu-id="ec9b9-158">boolean</span><span class="sxs-lookup"><span data-stu-id="ec9b9-158">boolean</span></span>|<span data-ttu-id="ec9b9-159">Valor booleano que representa si el valor de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-159">Boolean value representing if the data label value is visible or not.</span></span>|

## <a name="response"></a><span data-ttu-id="ec9b9-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec9b9-160">Response</span></span>

<span data-ttu-id="ec9b9-161">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartDataLabels](../resources/chartdatalabels.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-161">If successful, this method returns a `200 OK` response code and updated [ChartDataLabels](../resources/chartdatalabels.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ec9b9-162">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec9b9-162">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ec9b9-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ec9b9-163">Request</span></span>
<span data-ttu-id="ec9b9-164">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-164">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartdatalabels"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/datalabels
Content-type: application/json
Content-length: 134

{
  "position": "position-value",
  "showValue": true,
  "showSeriesName": true,
  "showCategoryName": true,
  "showLegendKey": true
}
```
##### <a name="response"></a><span data-ttu-id="ec9b9-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec9b9-165">Response</span></span>
<span data-ttu-id="ec9b9-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ec9b9-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartDataLabels"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 134

{
  "position": "position-value",
  "showValue": true,
  "showSeriesName": true,
  "showCategoryName": true,
  "showLegendKey": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartdatalabels",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
