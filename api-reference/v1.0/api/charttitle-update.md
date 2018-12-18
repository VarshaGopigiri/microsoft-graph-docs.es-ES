---
title: Actualizar charttitle
description: Actualizar las propiedades del objeto charttitle.
author: lumine2008
ms.openlocfilehash: c18fcd3f17c0925d2fddc9a69e723ab0cfacb45d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343739"
---
# <a name="update-charttitle"></a><span data-ttu-id="bcd06-103">Actualizar charttitle</span><span class="sxs-lookup"><span data-stu-id="bcd06-103">Update charttitle</span></span>

<span data-ttu-id="bcd06-104">Actualizar las propiedades del objeto charttitle.</span><span class="sxs-lookup"><span data-stu-id="bcd06-104">Update the properties of charttitle object.</span></span>
## <a name="permissions"></a><span data-ttu-id="bcd06-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="bcd06-105">Permissions</span></span>
<span data-ttu-id="bcd06-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bcd06-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bcd06-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bcd06-108">Permission type</span></span>      | <span data-ttu-id="bcd06-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bcd06-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bcd06-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bcd06-110">Delegated (work or school account)</span></span> | <span data-ttu-id="bcd06-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bcd06-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="bcd06-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bcd06-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bcd06-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bcd06-113">Not supported.</span></span>    |
|<span data-ttu-id="bcd06-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bcd06-114">Application</span></span> | <span data-ttu-id="bcd06-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bcd06-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="bcd06-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bcd06-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts/{name}/title
```
## <a name="optional-request-headers"></a><span data-ttu-id="bcd06-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="bcd06-117">Optional request headers</span></span>
| <span data-ttu-id="bcd06-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="bcd06-118">Name</span></span>       | <span data-ttu-id="bcd06-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcd06-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="bcd06-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="bcd06-120">Authorization</span></span>  | <span data-ttu-id="bcd06-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bcd06-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bcd06-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="bcd06-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="bcd06-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="bcd06-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="bcd06-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bcd06-126">Request body</span></span>
<span data-ttu-id="bcd06-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="bcd06-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="bcd06-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bcd06-130">Property</span></span>     | <span data-ttu-id="bcd06-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="bcd06-131">Type</span></span>   |<span data-ttu-id="bcd06-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcd06-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bcd06-133">overlay</span><span class="sxs-lookup"><span data-stu-id="bcd06-133">overlay</span></span>|<span data-ttu-id="bcd06-134">boolean</span><span class="sxs-lookup"><span data-stu-id="bcd06-134">boolean</span></span>|<span data-ttu-id="bcd06-135">Valor booleano que representa si el título del gráfico se superpondrá al gráfico o no.</span><span class="sxs-lookup"><span data-stu-id="bcd06-135">Boolean value representing if the chart title will overlay the chart or not.</span></span>|
|<span data-ttu-id="bcd06-136">text</span><span class="sxs-lookup"><span data-stu-id="bcd06-136">text</span></span>|<span data-ttu-id="bcd06-137">string</span><span class="sxs-lookup"><span data-stu-id="bcd06-137">string</span></span>|<span data-ttu-id="bcd06-138">Representa el texto del título de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="bcd06-138">Represents the title text of a chart.</span></span>|
|<span data-ttu-id="bcd06-139">visible</span><span class="sxs-lookup"><span data-stu-id="bcd06-139">visible</span></span>|<span data-ttu-id="bcd06-140">boolean</span><span class="sxs-lookup"><span data-stu-id="bcd06-140">boolean</span></span>|<span data-ttu-id="bcd06-141">Valor booleano que representa la visibilidad de un objeto de título del gráfico.</span><span class="sxs-lookup"><span data-stu-id="bcd06-141">A boolean value the represents the visibility of a chart title object.</span></span>|

## <a name="response"></a><span data-ttu-id="bcd06-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bcd06-142">Response</span></span>

<span data-ttu-id="bcd06-143">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookChartTitle](../resources/charttitle.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bcd06-143">If successful, this method returns a `200 OK` response code and updated [WorkbookChartTitle](../resources/charttitle.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bcd06-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bcd06-144">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bcd06-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bcd06-145">Request</span></span>
<span data-ttu-id="bcd06-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bcd06-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_charttitle"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/title
Content-type: application/json
Content-length: 64

{
  "overlay": true,
  "text": "text-value",
  "visible": true
}
```
##### <a name="response"></a><span data-ttu-id="bcd06-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bcd06-147">Response</span></span>
<span data-ttu-id="bcd06-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bcd06-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartTitle"
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