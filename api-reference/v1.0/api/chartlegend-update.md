---
title: Actualizar chartlegend
description: Actualizar las propiedades del objeto chartlegend.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: e4408f5a65059fe2b5c79299b712bf465e0bbd7f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27843109"
---
# <a name="update-chartlegend"></a><span data-ttu-id="cc240-103">Actualizar chartlegend</span><span class="sxs-lookup"><span data-stu-id="cc240-103">Update chartlegend</span></span>

<span data-ttu-id="cc240-104">Actualizar las propiedades del objeto chartlegend.</span><span class="sxs-lookup"><span data-stu-id="cc240-104">Update the properties of chartlegend object.</span></span>
## <a name="permissions"></a><span data-ttu-id="cc240-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="cc240-105">Permissions</span></span>
<span data-ttu-id="cc240-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cc240-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cc240-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cc240-108">Permission type</span></span>      | <span data-ttu-id="cc240-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cc240-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cc240-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cc240-110">Delegated (work or school account)</span></span> | <span data-ttu-id="cc240-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cc240-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="cc240-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cc240-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cc240-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc240-113">Not supported.</span></span>    |
|<span data-ttu-id="cc240-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cc240-114">Application</span></span> | <span data-ttu-id="cc240-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc240-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="cc240-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cc240-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts/{name}/legend
```
## <a name="optional-request-headers"></a><span data-ttu-id="cc240-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="cc240-117">Optional request headers</span></span>
| <span data-ttu-id="cc240-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="cc240-118">Name</span></span>       | <span data-ttu-id="cc240-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc240-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="cc240-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="cc240-120">Authorization</span></span>  | <span data-ttu-id="cc240-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cc240-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="cc240-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="cc240-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="cc240-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="cc240-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="cc240-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cc240-126">Request body</span></span>
<span data-ttu-id="cc240-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="cc240-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="cc240-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cc240-130">Property</span></span>     | <span data-ttu-id="cc240-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="cc240-131">Type</span></span>   |<span data-ttu-id="cc240-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc240-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="cc240-133">overlay</span><span class="sxs-lookup"><span data-stu-id="cc240-133">overlay</span></span>|<span data-ttu-id="cc240-134">boolean</span><span class="sxs-lookup"><span data-stu-id="cc240-134">boolean</span></span>|<span data-ttu-id="cc240-135">Valor booleano que indica si la leyenda del gráfico debe superponerse al cuerpo principal del gráfico.</span><span class="sxs-lookup"><span data-stu-id="cc240-135">Boolean value for whether the chart legend should overlap with the main body of the chart.</span></span>|
|<span data-ttu-id="cc240-136">position</span><span class="sxs-lookup"><span data-stu-id="cc240-136">position</span></span>|<span data-ttu-id="cc240-137">string</span><span class="sxs-lookup"><span data-stu-id="cc240-137">string</span></span>|<span data-ttu-id="cc240-138">Representa la posición de la leyenda del gráfico.</span><span class="sxs-lookup"><span data-stu-id="cc240-138">Represents the position of the legend on the chart.</span></span> <span data-ttu-id="cc240-139">Los valores posibles son: `Top`, `Bottom`, `Left`, `Right`, `Corner`, `Custom`.</span><span class="sxs-lookup"><span data-stu-id="cc240-139">The possible values are: `Top`, `Bottom`, `Left`, `Right`, `Corner`, `Custom`.</span></span>|
|<span data-ttu-id="cc240-140">visible</span><span class="sxs-lookup"><span data-stu-id="cc240-140">visible</span></span>|<span data-ttu-id="cc240-141">boolean</span><span class="sxs-lookup"><span data-stu-id="cc240-141">boolean</span></span>|<span data-ttu-id="cc240-142">Valor booleano que representa la visibilidad de un objeto ChartLegend.</span><span class="sxs-lookup"><span data-stu-id="cc240-142">A boolean value the represents the visibility of a ChartLegend object.</span></span>|

## <a name="response"></a><span data-ttu-id="cc240-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc240-143">Response</span></span>

<span data-ttu-id="cc240-144">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookChartLegend](../resources/chartlegend.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc240-144">If successful, this method returns a `200 OK` response code and updated [WorkbookChartLegend](../resources/chartlegend.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="cc240-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cc240-145">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cc240-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cc240-146">Request</span></span>
<span data-ttu-id="cc240-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cc240-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartlegend"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/legend
Content-type: application/json
Content-length: 72

{
  "visible": true,
  "position": "position-value",
  "overlay": true
}
```
##### <a name="response"></a><span data-ttu-id="cc240-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc240-148">Response</span></span>
<span data-ttu-id="cc240-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cc240-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartLegend"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 72

{
  "visible": true,
  "position": "position-value",
  "overlay": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartlegend",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
