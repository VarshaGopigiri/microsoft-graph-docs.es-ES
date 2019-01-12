---
title: Actualizar chartaxistitle
description: Actualizar las propiedades del objeto chartaxistitle.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: a38e768904539c011a44ebc8b242a86f22ce43fb
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932689"
---
# <a name="update-chartaxistitle"></a><span data-ttu-id="2b0d9-103">Actualizar chartaxistitle</span><span class="sxs-lookup"><span data-stu-id="2b0d9-103">Update chartaxistitle</span></span>

<span data-ttu-id="2b0d9-104">Actualizar las propiedades del objeto chartaxistitle.</span><span class="sxs-lookup"><span data-stu-id="2b0d9-104">Update the properties of chartaxistitle object.</span></span>
## <a name="permissions"></a><span data-ttu-id="2b0d9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="2b0d9-105">Permissions</span></span>
<span data-ttu-id="2b0d9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2b0d9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2b0d9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2b0d9-108">Permission type</span></span>      | <span data-ttu-id="2b0d9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2b0d9-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2b0d9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2b0d9-110">Delegated (work or school account)</span></span> | <span data-ttu-id="2b0d9-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2b0d9-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="2b0d9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2b0d9-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2b0d9-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2b0d9-113">Not supported.</span></span>    |
|<span data-ttu-id="2b0d9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2b0d9-114">Application</span></span> | <span data-ttu-id="2b0d9-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2b0d9-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2b0d9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2b0d9-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis/title
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/seriesAxis/title
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/categoryaxis/title
```
## <a name="optional-request-headers"></a><span data-ttu-id="2b0d9-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="2b0d9-117">Optional request headers</span></span>
| <span data-ttu-id="2b0d9-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="2b0d9-118">Name</span></span>       | <span data-ttu-id="2b0d9-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b0d9-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="2b0d9-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="2b0d9-120">Authorization</span></span>  | <span data-ttu-id="2b0d9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b0d9-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2b0d9-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="2b0d9-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="2b0d9-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="2b0d9-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="2b0d9-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2b0d9-126">Request body</span></span>
<span data-ttu-id="2b0d9-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="2b0d9-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="2b0d9-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2b0d9-130">Property</span></span>     | <span data-ttu-id="2b0d9-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b0d9-131">Type</span></span>   |<span data-ttu-id="2b0d9-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b0d9-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2b0d9-133">text</span><span class="sxs-lookup"><span data-stu-id="2b0d9-133">text</span></span>|<span data-ttu-id="2b0d9-134">string</span><span class="sxs-lookup"><span data-stu-id="2b0d9-134">string</span></span>|<span data-ttu-id="2b0d9-135">Representa el título del eje.</span><span class="sxs-lookup"><span data-stu-id="2b0d9-135">Represents the axis title.</span></span>|
|<span data-ttu-id="2b0d9-136">visible</span><span class="sxs-lookup"><span data-stu-id="2b0d9-136">visible</span></span>|<span data-ttu-id="2b0d9-137">boolean</span><span class="sxs-lookup"><span data-stu-id="2b0d9-137">boolean</span></span>|<span data-ttu-id="2b0d9-138">Valor booleano que especifica la visibilidad del título de un eje.</span><span class="sxs-lookup"><span data-stu-id="2b0d9-138">A boolean that specifies the visibility of an axis title.</span></span>|

## <a name="response"></a><span data-ttu-id="2b0d9-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b0d9-139">Response</span></span>

<span data-ttu-id="2b0d9-140">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookChartAxisTitle](../resources/chartaxistitle.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2b0d9-140">If successful, this method returns a `200 OK` response code and updated [WorkbookChartAxisTitle](../resources/chartaxistitle.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2b0d9-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2b0d9-141">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2b0d9-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b0d9-142">Request</span></span>
<span data-ttu-id="2b0d9-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2b0d9-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartaxistitle"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis/title
Content-type: application/json
Content-length: 45

{
  "text": "text-value",
  "visible": true
}
```
##### <a name="response"></a><span data-ttu-id="2b0d9-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b0d9-144">Response</span></span>
<span data-ttu-id="2b0d9-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b0d9-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartAxisTitle"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 45

{
  "text": "text-value",
  "visible": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartaxistitle",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
