---
title: Actualizar charttitle
description: Actualizar las propiedades del objeto charttitle.
author: lumine2008
ms.openlocfilehash: 2a3dd005b7932325685e9efa23acf1accd9320f8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353371"
---
# <a name="update-charttitle"></a><span data-ttu-id="b5ea7-103">Actualizar charttitle</span><span class="sxs-lookup"><span data-stu-id="b5ea7-103">Update charttitle</span></span>

> <span data-ttu-id="b5ea7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b5ea7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b5ea7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b5ea7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b5ea7-106">Actualizar las propiedades del objeto charttitle.</span><span class="sxs-lookup"><span data-stu-id="b5ea7-106">Update the properties of charttitle object.</span></span>
## <a name="permissions"></a><span data-ttu-id="b5ea7-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b5ea7-107">Permissions</span></span>
<span data-ttu-id="b5ea7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b5ea7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b5ea7-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b5ea7-110">Permission type</span></span>      | <span data-ttu-id="b5ea7-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b5ea7-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b5ea7-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b5ea7-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b5ea7-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b5ea7-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b5ea7-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b5ea7-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b5ea7-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b5ea7-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b5ea7-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b5ea7-116">Application</span></span> | <span data-ttu-id="b5ea7-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b5ea7-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b5ea7-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b5ea7-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/title
```
## <a name="optional-request-headers"></a><span data-ttu-id="b5ea7-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="b5ea7-119">Optional request headers</span></span>
| <span data-ttu-id="b5ea7-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="b5ea7-120">Name</span></span>       | <span data-ttu-id="b5ea7-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5ea7-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="b5ea7-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="b5ea7-122">Authorization</span></span>  | <span data-ttu-id="b5ea7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b5ea7-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b5ea7-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="b5ea7-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="b5ea7-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="b5ea7-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="b5ea7-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b5ea7-128">Request body</span></span>
<span data-ttu-id="b5ea7-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="b5ea7-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="b5ea7-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b5ea7-132">Property</span></span>     | <span data-ttu-id="b5ea7-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="b5ea7-133">Type</span></span>   |<span data-ttu-id="b5ea7-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5ea7-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b5ea7-135">overlay</span><span class="sxs-lookup"><span data-stu-id="b5ea7-135">overlay</span></span>|<span data-ttu-id="b5ea7-136">boolean</span><span class="sxs-lookup"><span data-stu-id="b5ea7-136">boolean</span></span>|<span data-ttu-id="b5ea7-137">Valor booleano que representa si el título del gráfico se superpondrá al gráfico o no.</span><span class="sxs-lookup"><span data-stu-id="b5ea7-137">Boolean value representing if the chart title will overlay the chart or not.</span></span>|
|<span data-ttu-id="b5ea7-138">text</span><span class="sxs-lookup"><span data-stu-id="b5ea7-138">text</span></span>|<span data-ttu-id="b5ea7-139">string</span><span class="sxs-lookup"><span data-stu-id="b5ea7-139">string</span></span>|<span data-ttu-id="b5ea7-140">Representa el texto del título de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="b5ea7-140">Represents the title text of a chart.</span></span>|
|<span data-ttu-id="b5ea7-141">visible</span><span class="sxs-lookup"><span data-stu-id="b5ea7-141">visible</span></span>|<span data-ttu-id="b5ea7-142">boolean</span><span class="sxs-lookup"><span data-stu-id="b5ea7-142">boolean</span></span>|<span data-ttu-id="b5ea7-143">Valor booleano que representa la visibilidad de un objeto de título del gráfico.</span><span class="sxs-lookup"><span data-stu-id="b5ea7-143">A boolean value the represents the visibility of a chart title object.</span></span>|

## <a name="response"></a><span data-ttu-id="b5ea7-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b5ea7-144">Response</span></span>

<span data-ttu-id="b5ea7-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartTitle](../resources/charttitle.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b5ea7-145">If successful, this method returns a `200 OK` response code and updated [ChartTitle](../resources/charttitle.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b5ea7-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b5ea7-146">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b5ea7-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b5ea7-147">Request</span></span>
<span data-ttu-id="b5ea7-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b5ea7-148">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="b5ea7-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b5ea7-149">Response</span></span>
<span data-ttu-id="b5ea7-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b5ea7-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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