---
title: Actualizar gráfico
description: Actualizar las propiedades del objeto chart.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 3e7a1e2e40ed3aea969683327ba16c022da210d2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27829172"
---
# <a name="update-chart"></a><span data-ttu-id="7b733-103">Actualizar gráfico</span><span class="sxs-lookup"><span data-stu-id="7b733-103">Update chart</span></span>

> <span data-ttu-id="7b733-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7b733-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7b733-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7b733-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7b733-106">Actualizar las propiedades del objeto chart.</span><span class="sxs-lookup"><span data-stu-id="7b733-106">Update the properties of chart object.</span></span>
## <a name="permissions"></a><span data-ttu-id="7b733-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="7b733-107">Permissions</span></span>
<span data-ttu-id="7b733-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7b733-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7b733-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7b733-110">Permission type</span></span>      | <span data-ttu-id="7b733-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7b733-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7b733-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7b733-112">Delegated (work or school account)</span></span> | <span data-ttu-id="7b733-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7b733-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="7b733-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7b733-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7b733-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7b733-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="7b733-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7b733-116">Application</span></span> | <span data-ttu-id="7b733-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7b733-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7b733-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7b733-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)
```
## <a name="optional-request-headers"></a><span data-ttu-id="7b733-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="7b733-119">Optional request headers</span></span>
| <span data-ttu-id="7b733-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="7b733-120">Name</span></span>       | <span data-ttu-id="7b733-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b733-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="7b733-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="7b733-122">Authorization</span></span>  | <span data-ttu-id="7b733-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7b733-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7b733-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="7b733-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="7b733-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="7b733-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="7b733-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7b733-128">Request body</span></span>
<span data-ttu-id="7b733-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="7b733-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="7b733-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7b733-132">Property</span></span>     | <span data-ttu-id="7b733-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b733-133">Type</span></span>   |<span data-ttu-id="7b733-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b733-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7b733-135">height</span><span class="sxs-lookup"><span data-stu-id="7b733-135">height</span></span>|<span data-ttu-id="7b733-136">Double</span><span class="sxs-lookup"><span data-stu-id="7b733-136">double</span></span>|<span data-ttu-id="7b733-137">Representa el alto, en puntos, del objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="7b733-137">Represents the height, in points, of the chart object.</span></span>|
|<span data-ttu-id="7b733-138">left</span><span class="sxs-lookup"><span data-stu-id="7b733-138">left</span></span>|<span data-ttu-id="7b733-139">Double</span><span class="sxs-lookup"><span data-stu-id="7b733-139">double</span></span>|<span data-ttu-id="7b733-140">Distancia, en puntos, desde el lado izquierdo del gráfico hasta el origen de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="7b733-140">The distance, in points, from the left side of the chart to the worksheet origin.</span></span>|
|<span data-ttu-id="7b733-141">name</span><span class="sxs-lookup"><span data-stu-id="7b733-141">name</span></span>|<span data-ttu-id="7b733-142">string</span><span class="sxs-lookup"><span data-stu-id="7b733-142">string</span></span>|<span data-ttu-id="7b733-143">Representa el nombre de un objeto de gráfico.</span><span class="sxs-lookup"><span data-stu-id="7b733-143">Represents the name of a chart object.</span></span>|
|<span data-ttu-id="7b733-144">top</span><span class="sxs-lookup"><span data-stu-id="7b733-144">top</span></span>|<span data-ttu-id="7b733-145">Double</span><span class="sxs-lookup"><span data-stu-id="7b733-145">double</span></span>|<span data-ttu-id="7b733-146">Representa la distancia, en puntos, desde el borde superior del objeto hasta la parte superior de la fila 1 (en una hoja de cálculo) o la parte superior del área del gráfico (en un gráfico).</span><span class="sxs-lookup"><span data-stu-id="7b733-146">Represents the distance, in points, from the top edge of the object to the top of row 1 (on a worksheet) or the top of the chart area (on a chart).</span></span>|
|<span data-ttu-id="7b733-147">width</span><span class="sxs-lookup"><span data-stu-id="7b733-147">width</span></span>|<span data-ttu-id="7b733-148">double</span><span class="sxs-lookup"><span data-stu-id="7b733-148">double</span></span>|<span data-ttu-id="7b733-149">Representa el ancho, en puntos, del objeto graph.</span><span class="sxs-lookup"><span data-stu-id="7b733-149">Represents the width, in points, of the chart object.</span></span>|

## <a name="response"></a><span data-ttu-id="7b733-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b733-150">Response</span></span>

<span data-ttu-id="7b733-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Chart](../resources/chart.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b733-151">If successful, this method returns a `200 OK` response code and updated [Chart](../resources/chart.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7b733-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b733-152">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7b733-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7b733-153">Request</span></span>
<span data-ttu-id="7b733-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7b733-154">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chart"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)
Content-type: application/json
Content-length: 52

{
  "height": 99,
  "left": 99
}
```
##### <a name="response"></a><span data-ttu-id="7b733-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b733-155">Response</span></span>
<span data-ttu-id="7b733-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7b733-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Update chart",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
