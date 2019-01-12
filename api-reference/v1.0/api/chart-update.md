---
title: Actualizar gráfico
description: Actualizar las propiedades del objeto chart.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 03a375e874a06914f5da9039dad58079df1199a8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27986323"
---
# <a name="update-chart"></a><span data-ttu-id="791da-103">Actualizar gráfico</span><span class="sxs-lookup"><span data-stu-id="791da-103">Update chart</span></span>

<span data-ttu-id="791da-104">Actualizar las propiedades del objeto chart.</span><span class="sxs-lookup"><span data-stu-id="791da-104">Update the properties of chart object.</span></span>
## <a name="permissions"></a><span data-ttu-id="791da-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="791da-105">Permissions</span></span>
<span data-ttu-id="791da-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="791da-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="791da-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="791da-108">Permission type</span></span>      | <span data-ttu-id="791da-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="791da-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="791da-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="791da-110">Delegated (work or school account)</span></span> | <span data-ttu-id="791da-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="791da-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="791da-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="791da-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="791da-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="791da-113">Not supported.</span></span>    |
|<span data-ttu-id="791da-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="791da-114">Application</span></span> | <span data-ttu-id="791da-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="791da-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="791da-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="791da-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts/{name}
```
## <a name="optional-request-headers"></a><span data-ttu-id="791da-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="791da-117">Optional request headers</span></span>
| <span data-ttu-id="791da-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="791da-118">Name</span></span>       | <span data-ttu-id="791da-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="791da-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="791da-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="791da-120">Authorization</span></span>  | <span data-ttu-id="791da-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="791da-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="791da-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="791da-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="791da-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="791da-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="791da-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="791da-126">Request body</span></span>
<span data-ttu-id="791da-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="791da-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="791da-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="791da-130">Property</span></span>     | <span data-ttu-id="791da-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="791da-131">Type</span></span>   |<span data-ttu-id="791da-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="791da-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="791da-133">height</span><span class="sxs-lookup"><span data-stu-id="791da-133">height</span></span>|<span data-ttu-id="791da-134">Double</span><span class="sxs-lookup"><span data-stu-id="791da-134">double</span></span>|<span data-ttu-id="791da-135">Representa el alto, en puntos, del objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="791da-135">Represents the height, in points, of the chart object.</span></span>|
|<span data-ttu-id="791da-136">left</span><span class="sxs-lookup"><span data-stu-id="791da-136">left</span></span>|<span data-ttu-id="791da-137">Double</span><span class="sxs-lookup"><span data-stu-id="791da-137">double</span></span>|<span data-ttu-id="791da-138">Distancia, en puntos, desde el lado izquierdo del gráfico hasta el origen de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="791da-138">The distance, in points, from the left side of the chart to the worksheet origin.</span></span>|
|<span data-ttu-id="791da-139">name</span><span class="sxs-lookup"><span data-stu-id="791da-139">name</span></span>|<span data-ttu-id="791da-140">string</span><span class="sxs-lookup"><span data-stu-id="791da-140">string</span></span>|<span data-ttu-id="791da-141">Representa el nombre de un objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="791da-141">Represents the name of a chart object.</span></span>|
|<span data-ttu-id="791da-142">top</span><span class="sxs-lookup"><span data-stu-id="791da-142">top</span></span>|<span data-ttu-id="791da-143">Double</span><span class="sxs-lookup"><span data-stu-id="791da-143">double</span></span>|<span data-ttu-id="791da-144">Representa la distancia, en puntos, desde el borde superior del objeto hasta la parte superior de la fila 1 (en una hoja de cálculo) o la parte superior del área del gráfico (en un gráfico).</span><span class="sxs-lookup"><span data-stu-id="791da-144">Represents the distance, in points, from the top edge of the object to the top of row 1 (on a worksheet) or the top of the chart area (on a chart).</span></span>|
|<span data-ttu-id="791da-145">width</span><span class="sxs-lookup"><span data-stu-id="791da-145">width</span></span>|<span data-ttu-id="791da-146">double</span><span class="sxs-lookup"><span data-stu-id="791da-146">double</span></span>|<span data-ttu-id="791da-147">Representa el ancho, en puntos, del objeto graph.</span><span class="sxs-lookup"><span data-stu-id="791da-147">Represents the width, in points, of the chart object.</span></span>|

## <a name="response"></a><span data-ttu-id="791da-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="791da-148">Response</span></span>

<span data-ttu-id="791da-149">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookChart](../resources/chart.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="791da-149">If successful, this method returns a `200 OK` response code and updated [WorkbookChart](../resources/chart.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="791da-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="791da-150">Example</span></span>
##### <a name="request"></a><span data-ttu-id="791da-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="791da-151">Request</span></span>
<span data-ttu-id="791da-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="791da-152">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chart"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}
Content-type: application/json
Content-length: 52

{
  "height": 99,
  "left": 99
}
```
##### <a name="response"></a><span data-ttu-id="791da-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="791da-153">Response</span></span>
<span data-ttu-id="791da-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="791da-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChart"
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
  "description": "Update chart",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
