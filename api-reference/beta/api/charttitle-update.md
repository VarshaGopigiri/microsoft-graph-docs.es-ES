---
title: Actualizar charttitle
description: Actualizar las propiedades del objeto charttitle.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 4d0beb65acb208d6f04d495a98b3c48a046b29ba
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980807"
---
# <a name="update-charttitle"></a><span data-ttu-id="531a1-103">Actualizar charttitle</span><span class="sxs-lookup"><span data-stu-id="531a1-103">Update charttitle</span></span>

> <span data-ttu-id="531a1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="531a1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="531a1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="531a1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="531a1-106">Actualizar las propiedades del objeto charttitle.</span><span class="sxs-lookup"><span data-stu-id="531a1-106">Update the properties of charttitle object.</span></span>
## <a name="permissions"></a><span data-ttu-id="531a1-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="531a1-107">Permissions</span></span>
<span data-ttu-id="531a1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="531a1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="531a1-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="531a1-110">Permission type</span></span>      | <span data-ttu-id="531a1-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="531a1-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="531a1-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="531a1-112">Delegated (work or school account)</span></span> | <span data-ttu-id="531a1-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="531a1-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="531a1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="531a1-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="531a1-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="531a1-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="531a1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="531a1-116">Application</span></span> | <span data-ttu-id="531a1-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="531a1-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="531a1-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="531a1-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/title
```
## <a name="optional-request-headers"></a><span data-ttu-id="531a1-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="531a1-119">Optional request headers</span></span>
| <span data-ttu-id="531a1-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="531a1-120">Name</span></span>       | <span data-ttu-id="531a1-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="531a1-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="531a1-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="531a1-122">Authorization</span></span>  | <span data-ttu-id="531a1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="531a1-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="531a1-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="531a1-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="531a1-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="531a1-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="531a1-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="531a1-128">Request body</span></span>
<span data-ttu-id="531a1-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="531a1-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="531a1-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="531a1-132">Property</span></span>     | <span data-ttu-id="531a1-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="531a1-133">Type</span></span>   |<span data-ttu-id="531a1-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="531a1-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="531a1-135">overlay</span><span class="sxs-lookup"><span data-stu-id="531a1-135">overlay</span></span>|<span data-ttu-id="531a1-136">boolean</span><span class="sxs-lookup"><span data-stu-id="531a1-136">boolean</span></span>|<span data-ttu-id="531a1-137">Valor booleano que representa si el título del gráfico se superpondrá al gráfico o no.</span><span class="sxs-lookup"><span data-stu-id="531a1-137">Boolean value representing if the chart title will overlay the chart or not.</span></span>|
|<span data-ttu-id="531a1-138">text</span><span class="sxs-lookup"><span data-stu-id="531a1-138">text</span></span>|<span data-ttu-id="531a1-139">string</span><span class="sxs-lookup"><span data-stu-id="531a1-139">string</span></span>|<span data-ttu-id="531a1-140">Representa el texto del título de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="531a1-140">Represents the title text of a chart.</span></span>|
|<span data-ttu-id="531a1-141">visible</span><span class="sxs-lookup"><span data-stu-id="531a1-141">visible</span></span>|<span data-ttu-id="531a1-142">boolean</span><span class="sxs-lookup"><span data-stu-id="531a1-142">boolean</span></span>|<span data-ttu-id="531a1-143">Valor booleano que representa la visibilidad de un objeto de título del gráfico.</span><span class="sxs-lookup"><span data-stu-id="531a1-143">A boolean value the represents the visibility of a chart title object.</span></span>|

## <a name="response"></a><span data-ttu-id="531a1-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="531a1-144">Response</span></span>

<span data-ttu-id="531a1-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartTitle](../resources/charttitle.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="531a1-145">If successful, this method returns a `200 OK` response code and updated [ChartTitle](../resources/charttitle.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="531a1-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="531a1-146">Example</span></span>
##### <a name="request"></a><span data-ttu-id="531a1-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="531a1-147">Request</span></span>
<span data-ttu-id="531a1-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="531a1-148">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_charttitle"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/title
Content-type: application/json
Content-length: 64

{
  "overlay": true,
  "text": "text-value",
  "visible": true
}
```
##### <a name="response"></a><span data-ttu-id="531a1-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="531a1-149">Response</span></span>
<span data-ttu-id="531a1-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="531a1-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartTitle"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 64

{
  "overlay": true,
  "text": "text-value",
  "visible": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update charttitle",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
