---
title: Actualizar chartlegend
description: Actualizar las propiedades del objeto chartlegend.
ms.openlocfilehash: 7eb89f40e0f691e597d519070997f90729d8a2f0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083327"
---
# <a name="update-chartlegend"></a><span data-ttu-id="1e86d-103">Actualizar chartlegend</span><span class="sxs-lookup"><span data-stu-id="1e86d-103">Update chartlegend</span></span>

> <span data-ttu-id="1e86d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1e86d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1e86d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1e86d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1e86d-106">Actualizar las propiedades del objeto chartlegend.</span><span class="sxs-lookup"><span data-stu-id="1e86d-106">Update the properties of chartlegend object.</span></span>
## <a name="permissions"></a><span data-ttu-id="1e86d-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1e86d-107">Permissions</span></span>
<span data-ttu-id="1e86d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1e86d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1e86d-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1e86d-110">Permission type</span></span>      | <span data-ttu-id="1e86d-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1e86d-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1e86d-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1e86d-112">Delegated (work or school account)</span></span> | <span data-ttu-id="1e86d-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1e86d-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="1e86d-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1e86d-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1e86d-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1e86d-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="1e86d-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1e86d-116">Application</span></span> | <span data-ttu-id="1e86d-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1e86d-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1e86d-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1e86d-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/legend
```
## <a name="optional-request-headers"></a><span data-ttu-id="1e86d-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="1e86d-119">Optional request headers</span></span>
| <span data-ttu-id="1e86d-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="1e86d-120">Name</span></span>       | <span data-ttu-id="1e86d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e86d-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="1e86d-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="1e86d-122">Authorization</span></span>  | <span data-ttu-id="1e86d-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1e86d-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1e86d-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="1e86d-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="1e86d-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="1e86d-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="1e86d-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1e86d-128">Request body</span></span>
<span data-ttu-id="1e86d-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="1e86d-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="1e86d-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1e86d-132">Property</span></span>     | <span data-ttu-id="1e86d-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="1e86d-133">Type</span></span>   |<span data-ttu-id="1e86d-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e86d-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1e86d-135">overlay</span><span class="sxs-lookup"><span data-stu-id="1e86d-135">overlay</span></span>|<span data-ttu-id="1e86d-136">boolean</span><span class="sxs-lookup"><span data-stu-id="1e86d-136">boolean</span></span>|<span data-ttu-id="1e86d-137">Valor booleano que indica si la leyenda del gráfico debe superponerse al cuerpo principal del gráfico.</span><span class="sxs-lookup"><span data-stu-id="1e86d-137">Boolean value for whether the chart legend should overlap with the main body of the chart.</span></span>|
|<span data-ttu-id="1e86d-138">position</span><span class="sxs-lookup"><span data-stu-id="1e86d-138">position</span></span>|<span data-ttu-id="1e86d-139">string</span><span class="sxs-lookup"><span data-stu-id="1e86d-139">string</span></span>|<span data-ttu-id="1e86d-p106">Representa la posición de la leyenda del gráfico. Valores posibles: `Top`, `Bottom`, `Left`, `Right`, `Corner`, `Custom`.</span><span class="sxs-lookup"><span data-stu-id="1e86d-p106">Represents the position of the legend on the chart. Possible values are: `Top`, `Bottom`, `Left`, `Right`, `Corner`, `Custom`.</span></span>|
|<span data-ttu-id="1e86d-142">visible</span><span class="sxs-lookup"><span data-stu-id="1e86d-142">visible</span></span>|<span data-ttu-id="1e86d-143">boolean</span><span class="sxs-lookup"><span data-stu-id="1e86d-143">boolean</span></span>|<span data-ttu-id="1e86d-144">Valor booleano que representa la visibilidad de un objeto ChartLegend.</span><span class="sxs-lookup"><span data-stu-id="1e86d-144">A boolean value the represents the visibility of a ChartLegend object.</span></span>|

## <a name="response"></a><span data-ttu-id="1e86d-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e86d-145">Response</span></span>

<span data-ttu-id="1e86d-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartLegend](../resources/chartlegend.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1e86d-146">If successful, this method returns a `200 OK` response code and updated [ChartLegend](../resources/chartlegend.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1e86d-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1e86d-147">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1e86d-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1e86d-148">Request</span></span>
<span data-ttu-id="1e86d-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1e86d-149">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartlegend"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/legend
Content-type: application/json
Content-length: 72

{
  "visible": true,
  "position": "position-value",
  "overlay": true
}
```
##### <a name="response"></a><span data-ttu-id="1e86d-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e86d-150">Response</span></span>
<span data-ttu-id="1e86d-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1e86d-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartLegend"
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