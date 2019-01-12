---
title: Update rangeborder
description: Actualizar las propiedades del objeto rangeborder.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 2d8a3bbd24f83dd635c6254b852a2ecd00660fe9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912165"
---
# <a name="update-rangeborder"></a><span data-ttu-id="7fca7-103">Update rangeborder</span><span class="sxs-lookup"><span data-stu-id="7fca7-103">Update rangeborder</span></span>

<span data-ttu-id="7fca7-104">Actualizar las propiedades del objeto rangeborder.</span><span class="sxs-lookup"><span data-stu-id="7fca7-104">Update the properties of rangeborder object.</span></span>
## <a name="permissions"></a><span data-ttu-id="7fca7-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="7fca7-105">Permissions</span></span>
<span data-ttu-id="7fca7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7fca7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7fca7-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7fca7-108">Permission type</span></span>      | <span data-ttu-id="7fca7-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7fca7-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7fca7-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7fca7-110">Delegated (work or school account)</span></span> | <span data-ttu-id="7fca7-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7fca7-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="7fca7-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7fca7-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7fca7-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7fca7-113">Not supported.</span></span>    |
|<span data-ttu-id="7fca7-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7fca7-114">Application</span></span> | <span data-ttu-id="7fca7-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7fca7-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7fca7-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7fca7-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names/{name}/range/format/borders/{sideIndex}
PATCH /workbook/worksheets/{id|name}/range(address='<address>')/format/borders/{sideIndex}
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format/borders/{sideIndex}
```
## <a name="optional-request-headers"></a><span data-ttu-id="7fca7-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="7fca7-117">Optional request headers</span></span>
| <span data-ttu-id="7fca7-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="7fca7-118">Name</span></span>       | <span data-ttu-id="7fca7-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="7fca7-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="7fca7-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="7fca7-120">Authorization</span></span>  | <span data-ttu-id="7fca7-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7fca7-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7fca7-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="7fca7-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="7fca7-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="7fca7-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="7fca7-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7fca7-126">Request body</span></span>
<span data-ttu-id="7fca7-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="7fca7-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="7fca7-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7fca7-130">Property</span></span>     | <span data-ttu-id="7fca7-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="7fca7-131">Type</span></span>   |<span data-ttu-id="7fca7-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="7fca7-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7fca7-133">color</span><span class="sxs-lookup"><span data-stu-id="7fca7-133">color</span></span>|<span data-ttu-id="7fca7-134">string</span><span class="sxs-lookup"><span data-stu-id="7fca7-134">string</span></span>|<span data-ttu-id="7fca7-135">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="7fca7-135">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange").</span></span>|
|<span data-ttu-id="7fca7-136">style</span><span class="sxs-lookup"><span data-stu-id="7fca7-136">style</span></span>|<span data-ttu-id="7fca7-137">string</span><span class="sxs-lookup"><span data-stu-id="7fca7-137">string</span></span>|<span data-ttu-id="7fca7-138">Una de las constantes de estilo de línea que especifica el estilo de línea para el borde.</span><span class="sxs-lookup"><span data-stu-id="7fca7-138">One of the constants of line style specifying the line style for the border.</span></span> <span data-ttu-id="7fca7-139">Los valores posibles son: `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double`, `SlantDashDot`.</span><span class="sxs-lookup"><span data-stu-id="7fca7-139">The possible values are: `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double`, `SlantDashDot`.</span></span>|
|<span data-ttu-id="7fca7-140">weight</span><span class="sxs-lookup"><span data-stu-id="7fca7-140">weight</span></span>|<span data-ttu-id="7fca7-141">string</span><span class="sxs-lookup"><span data-stu-id="7fca7-141">string</span></span>|<span data-ttu-id="7fca7-142">Especifica el grosor del borde que rodea un rango.</span><span class="sxs-lookup"><span data-stu-id="7fca7-142">Specifies the weight of the border around a range.</span></span> <span data-ttu-id="7fca7-143">Los valores posibles son: `Hairline`, `Thin`, `Medium`, `Thick`.</span><span class="sxs-lookup"><span data-stu-id="7fca7-143">The possible values are: `Hairline`, `Thin`, `Medium`, `Thick`.</span></span>|

## <a name="response"></a><span data-ttu-id="7fca7-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7fca7-144">Response</span></span>

<span data-ttu-id="7fca7-145">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookRangeBorder](../resources/rangeborder.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7fca7-145">If successful, this method returns a `200 OK` response code and updated [WorkbookRangeBorder](../resources/rangeborder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7fca7-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7fca7-146">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7fca7-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7fca7-147">Request</span></span>
<span data-ttu-id="7fca7-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7fca7-148">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_rangeborder"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/format/borders/{sideIndex}
Content-type: application/json
Content-length: 136

{
  "color": "color-value",
  "style": "style-value",
  "sideIndex": "sideIndex-value",
  "weight": "weight-value"
}
```
##### <a name="response"></a><span data-ttu-id="7fca7-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7fca7-149">Response</span></span>
<span data-ttu-id="7fca7-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7fca7-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeBorder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 136

{
  "id": "id-value",
  "color": "color-value",
  "style": "style-value",
  "sideIndex": "sideIndex-value",
  "weight": "weight-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update rangeborder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
