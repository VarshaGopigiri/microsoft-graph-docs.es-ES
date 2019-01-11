---
title: Actualizar gráfico
description: Actualizar las propiedades del objeto chart.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 7d4189ac4f009059ae83ba50fc0ad8f0236786a5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858054"
---
# <a name="update-chart"></a><span data-ttu-id="ceb94-103">Actualizar gráfico</span><span class="sxs-lookup"><span data-stu-id="ceb94-103">Update chart</span></span>

<span data-ttu-id="ceb94-104">Actualizar las propiedades del objeto chart.</span><span class="sxs-lookup"><span data-stu-id="ceb94-104">Update the properties of chart object.</span></span>
## <a name="permissions"></a><span data-ttu-id="ceb94-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ceb94-105">Permissions</span></span>
<span data-ttu-id="ceb94-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ceb94-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ceb94-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ceb94-108">Permission type</span></span>      | <span data-ttu-id="ceb94-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ceb94-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ceb94-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ceb94-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ceb94-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ceb94-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="ceb94-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ceb94-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ceb94-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ceb94-113">Not supported.</span></span>    |
|<span data-ttu-id="ceb94-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ceb94-114">Application</span></span> | <span data-ttu-id="ceb94-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ceb94-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ceb94-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ceb94-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts/{name}
```
## <a name="optional-request-headers"></a><span data-ttu-id="ceb94-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="ceb94-117">Optional request headers</span></span>
| <span data-ttu-id="ceb94-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="ceb94-118">Name</span></span>       | <span data-ttu-id="ceb94-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ceb94-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="ceb94-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="ceb94-120">Authorization</span></span>  | <span data-ttu-id="ceb94-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ceb94-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ceb94-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="ceb94-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="ceb94-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="ceb94-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="ceb94-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ceb94-126">Request body</span></span>
<span data-ttu-id="ceb94-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="ceb94-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="ceb94-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ceb94-130">Property</span></span>     | <span data-ttu-id="ceb94-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ceb94-131">Type</span></span>   |<span data-ttu-id="ceb94-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ceb94-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ceb94-133">height</span><span class="sxs-lookup"><span data-stu-id="ceb94-133">height</span></span>|<span data-ttu-id="ceb94-134">Double</span><span class="sxs-lookup"><span data-stu-id="ceb94-134">double</span></span>|<span data-ttu-id="ceb94-135">Representa el alto, en puntos, del objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="ceb94-135">Represents the height, in points, of the chart object.</span></span>|
|<span data-ttu-id="ceb94-136">left</span><span class="sxs-lookup"><span data-stu-id="ceb94-136">left</span></span>|<span data-ttu-id="ceb94-137">Double</span><span class="sxs-lookup"><span data-stu-id="ceb94-137">double</span></span>|<span data-ttu-id="ceb94-138">Distancia, en puntos, desde el lado izquierdo del gráfico hasta el origen de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="ceb94-138">The distance, in points, from the left side of the chart to the worksheet origin.</span></span>|
|<span data-ttu-id="ceb94-139">name</span><span class="sxs-lookup"><span data-stu-id="ceb94-139">name</span></span>|<span data-ttu-id="ceb94-140">string</span><span class="sxs-lookup"><span data-stu-id="ceb94-140">string</span></span>|<span data-ttu-id="ceb94-141">Representa el nombre de un objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="ceb94-141">Represents the name of a chart object.</span></span>|
|<span data-ttu-id="ceb94-142">top</span><span class="sxs-lookup"><span data-stu-id="ceb94-142">top</span></span>|<span data-ttu-id="ceb94-143">Double</span><span class="sxs-lookup"><span data-stu-id="ceb94-143">double</span></span>|<span data-ttu-id="ceb94-144">Representa la distancia, en puntos, desde el borde superior del objeto hasta la parte superior de la fila 1 (en una hoja de cálculo) o la parte superior del área del gráfico (en un gráfico).</span><span class="sxs-lookup"><span data-stu-id="ceb94-144">Represents the distance, in points, from the top edge of the object to the top of row 1 (on a worksheet) or the top of the chart area (on a chart).</span></span>|
|<span data-ttu-id="ceb94-145">width</span><span class="sxs-lookup"><span data-stu-id="ceb94-145">width</span></span>|<span data-ttu-id="ceb94-146">double</span><span class="sxs-lookup"><span data-stu-id="ceb94-146">double</span></span>|<span data-ttu-id="ceb94-147">Representa el ancho, en puntos, del objeto graph.</span><span class="sxs-lookup"><span data-stu-id="ceb94-147">Represents the width, in points, of the chart object.</span></span>|

## <a name="response"></a><span data-ttu-id="ceb94-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ceb94-148">Response</span></span>

<span data-ttu-id="ceb94-149">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookChart](../resources/chart.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ceb94-149">If successful, this method returns a `200 OK` response code and updated [WorkbookChart](../resources/chart.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ceb94-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ceb94-150">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ceb94-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ceb94-151">Request</span></span>
<span data-ttu-id="ceb94-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ceb94-152">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="ceb94-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ceb94-153">Response</span></span>
<span data-ttu-id="ceb94-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ceb94-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
