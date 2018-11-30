---
title: Actualizar chartdatalabels
description: Actualizar las propiedades del objeto chartdatalabels.
ms.openlocfilehash: d0e7628bc342d83dfd349104105428bb81c4c8f5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029677"
---
# <a name="update-chartdatalabels"></a><span data-ttu-id="ac0ac-103">Actualizar chartdatalabels</span><span class="sxs-lookup"><span data-stu-id="ac0ac-103">Update chartdatalabels</span></span>

<span data-ttu-id="ac0ac-104">Actualizar las propiedades del objeto chartdatalabels.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-104">Update the properties of chartdatalabels object.</span></span>
## <a name="permissions"></a><span data-ttu-id="ac0ac-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ac0ac-105">Permissions</span></span>
<span data-ttu-id="ac0ac-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ac0ac-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ac0ac-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ac0ac-108">Permission type</span></span>      | <span data-ttu-id="ac0ac-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ac0ac-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ac0ac-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ac0ac-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ac0ac-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ac0ac-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="ac0ac-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ac0ac-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ac0ac-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-113">Not supported.</span></span>    |
|<span data-ttu-id="ac0ac-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ac0ac-114">Application</span></span> | <span data-ttu-id="ac0ac-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ac0ac-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ac0ac-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts/{name}/dataLabels
```
## <a name="optional-request-headers"></a><span data-ttu-id="ac0ac-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="ac0ac-117">Optional request headers</span></span>
| <span data-ttu-id="ac0ac-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac0ac-118">Name</span></span>       | <span data-ttu-id="ac0ac-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac0ac-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="ac0ac-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="ac0ac-120">Authorization</span></span>  | <span data-ttu-id="ac0ac-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ac0ac-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="ac0ac-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="ac0ac-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="ac0ac-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ac0ac-126">Request body</span></span>
<span data-ttu-id="ac0ac-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="ac0ac-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac0ac-130">Property</span></span>     | <span data-ttu-id="ac0ac-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac0ac-131">Type</span></span>   |<span data-ttu-id="ac0ac-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac0ac-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ac0ac-133">position</span><span class="sxs-lookup"><span data-stu-id="ac0ac-133">position</span></span>|<span data-ttu-id="ac0ac-134">string</span><span class="sxs-lookup"><span data-stu-id="ac0ac-134">string</span></span>|<span data-ttu-id="ac0ac-135">Valor de DataLabelPosition que representa la posición de la etiqueta de datos.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-135">DataLabelPosition value that represents the position of the data label.</span></span> <span data-ttu-id="ac0ac-136">Los valores posibles son: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-136">The possible values are: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.</span></span>|
|<span data-ttu-id="ac0ac-137">separator</span><span class="sxs-lookup"><span data-stu-id="ac0ac-137">separator</span></span>|<span data-ttu-id="ac0ac-138">string</span><span class="sxs-lookup"><span data-stu-id="ac0ac-138">string</span></span>|<span data-ttu-id="ac0ac-139">Cadena que representa el separador empleado para las etiquetas de datos de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-139">String representing the separator used for the data labels on a chart.</span></span>|
|<span data-ttu-id="ac0ac-140">showBubbleSize</span><span class="sxs-lookup"><span data-stu-id="ac0ac-140">showBubbleSize</span></span>|<span data-ttu-id="ac0ac-141">boolean</span><span class="sxs-lookup"><span data-stu-id="ac0ac-141">boolean</span></span>|<span data-ttu-id="ac0ac-142">Valor booleano que representa si el tamaño de la burbuja de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-142">Boolean value representing if the data label bubble size is visible or not.</span></span>|
|<span data-ttu-id="ac0ac-143">showCategoryName</span><span class="sxs-lookup"><span data-stu-id="ac0ac-143">showCategoryName</span></span>|<span data-ttu-id="ac0ac-144">boolean</span><span class="sxs-lookup"><span data-stu-id="ac0ac-144">boolean</span></span>|<span data-ttu-id="ac0ac-145">Valor booleano que representa si el nombre de categoría de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-145">Boolean value representing if the data label category name is visible or not.</span></span>|
|<span data-ttu-id="ac0ac-146">showLegendKey</span><span class="sxs-lookup"><span data-stu-id="ac0ac-146">showLegendKey</span></span>|<span data-ttu-id="ac0ac-147">boolean</span><span class="sxs-lookup"><span data-stu-id="ac0ac-147">boolean</span></span>|<span data-ttu-id="ac0ac-148">Valor booleano que representa si la clave de leyenda de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-148">Boolean value representing if the data label legend key is visible or not.</span></span>|
|<span data-ttu-id="ac0ac-149">showPercentage</span><span class="sxs-lookup"><span data-stu-id="ac0ac-149">showPercentage</span></span>|<span data-ttu-id="ac0ac-150">boolean</span><span class="sxs-lookup"><span data-stu-id="ac0ac-150">boolean</span></span>|<span data-ttu-id="ac0ac-151">Valor booleano que representa si el porcentaje de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-151">Boolean value representing if the data label percentage is visible or not.</span></span>|
|<span data-ttu-id="ac0ac-152">showSeriesName</span><span class="sxs-lookup"><span data-stu-id="ac0ac-152">showSeriesName</span></span>|<span data-ttu-id="ac0ac-153">boolean</span><span class="sxs-lookup"><span data-stu-id="ac0ac-153">boolean</span></span>|<span data-ttu-id="ac0ac-154">Valor booleano que representa si el nombre de serie de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-154">Boolean value representing if the data label series name is visible or not.</span></span>|
|<span data-ttu-id="ac0ac-155">showValue</span><span class="sxs-lookup"><span data-stu-id="ac0ac-155">showValue</span></span>|<span data-ttu-id="ac0ac-156">boolean</span><span class="sxs-lookup"><span data-stu-id="ac0ac-156">boolean</span></span>|<span data-ttu-id="ac0ac-157">Valor booleano que representa si el valor de la etiqueta de datos es visible o no.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-157">Boolean value representing if the data label value is visible or not.</span></span>|

## <a name="response"></a><span data-ttu-id="ac0ac-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac0ac-158">Response</span></span>

<span data-ttu-id="ac0ac-159">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookChartDataLabels](../resources/chartdatalabels.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-159">If successful, this method returns a `200 OK` response code and updated [WorkbookChartDataLabels](../resources/chartdatalabels.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ac0ac-160">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac0ac-160">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ac0ac-161">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ac0ac-161">Request</span></span>
<span data-ttu-id="ac0ac-162">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-162">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartdatalabels"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/dataLabels
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
##### <a name="response"></a><span data-ttu-id="ac0ac-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac0ac-163">Response</span></span>
<span data-ttu-id="ac0ac-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ac0ac-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartDataLabels"
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