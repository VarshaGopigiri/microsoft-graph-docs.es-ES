---
title: Actualizar chartaxis
description: Actualizar las propiedades del objeto chartaxis.
ms.openlocfilehash: 665c20683c2a2f54d4f5e73a66993707bc5f6539
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030215"
---
# <a name="update-chartaxis"></a><span data-ttu-id="abd5e-103">Actualizar chartaxis</span><span class="sxs-lookup"><span data-stu-id="abd5e-103">Update chartaxis</span></span>

<span data-ttu-id="abd5e-104">Actualizar las propiedades del objeto chartaxis.</span><span class="sxs-lookup"><span data-stu-id="abd5e-104">Update the properties of chartaxis object.</span></span>
## <a name="permissions"></a><span data-ttu-id="abd5e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="abd5e-105">Permissions</span></span>
<span data-ttu-id="abd5e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="abd5e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="abd5e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="abd5e-108">Permission type</span></span>      | <span data-ttu-id="abd5e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="abd5e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="abd5e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="abd5e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="abd5e-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="abd5e-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="abd5e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="abd5e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="abd5e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="abd5e-113">Not supported.</span></span>    |
|<span data-ttu-id="abd5e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="abd5e-114">Application</span></span> | <span data-ttu-id="abd5e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="abd5e-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="abd5e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="abd5e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/seriesAxis
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/categoryaxis
```
## <a name="optional-request-headers"></a><span data-ttu-id="abd5e-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="abd5e-117">Optional request headers</span></span>
| <span data-ttu-id="abd5e-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="abd5e-118">Name</span></span>       | <span data-ttu-id="abd5e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="abd5e-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="abd5e-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="abd5e-120">Authorization</span></span>  | <span data-ttu-id="abd5e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="abd5e-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="abd5e-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="abd5e-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="abd5e-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="abd5e-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="abd5e-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="abd5e-126">Request body</span></span>
<span data-ttu-id="abd5e-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="abd5e-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="abd5e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="abd5e-130">Property</span></span>     | <span data-ttu-id="abd5e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="abd5e-131">Type</span></span>   |<span data-ttu-id="abd5e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="abd5e-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="abd5e-133">majorUnit</span><span class="sxs-lookup"><span data-stu-id="abd5e-133">majorUnit</span></span>|<span data-ttu-id="abd5e-134">Json</span><span class="sxs-lookup"><span data-stu-id="abd5e-134">Json</span></span>|<span data-ttu-id="abd5e-p105">Representa el intervalo entre dos marcas de graduación principales. Puede establecerse en un valor numérico o en una cadena vacía.  El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="abd5e-p105">Represents the interval between two major tick marks. Can be set to a numeric value or an empty string.  The returned value is always a number.</span></span>|
|<span data-ttu-id="abd5e-138">maximum</span><span class="sxs-lookup"><span data-stu-id="abd5e-138">maximum</span></span>|<span data-ttu-id="abd5e-139">Json</span><span class="sxs-lookup"><span data-stu-id="abd5e-139">Json</span></span>|<span data-ttu-id="abd5e-p106">Representa el valor máximo del eje de valores.  Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos).  El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="abd5e-p106">Represents the maximum value on the value axis.  Can be set to a numeric value or an empty string (for automatic axis values).  The returned value is always a number.</span></span>|
|<span data-ttu-id="abd5e-143">minimum</span><span class="sxs-lookup"><span data-stu-id="abd5e-143">minimum</span></span>|<span data-ttu-id="abd5e-144">Json</span><span class="sxs-lookup"><span data-stu-id="abd5e-144">Json</span></span>|<span data-ttu-id="abd5e-p107">Representa el valor mínimo del eje de valores. Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos). El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="abd5e-p107">Represents the minimum value on the value axis. Can be set to a numeric value or an empty string (for automatic axis values).  The returned value is always a number.</span></span>|
|<span data-ttu-id="abd5e-148">minorUnit</span><span class="sxs-lookup"><span data-stu-id="abd5e-148">minorUnit</span></span>|<span data-ttu-id="abd5e-149">Json</span><span class="sxs-lookup"><span data-stu-id="abd5e-149">Json</span></span>|<span data-ttu-id="abd5e-p108">Representa el intervalo entre dos marcas de graduación secundarias. Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos). El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="abd5e-p108">Represents the interval between two minor tick marks. "Can be set to a numeric value or an empty string (for automatic axis values). The returned value is always a number.</span></span>|

## <a name="response"></a><span data-ttu-id="abd5e-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="abd5e-153">Response</span></span>

<span data-ttu-id="abd5e-154">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookChartAxis](../resources/chartaxis.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="abd5e-154">If successful, this method returns a `200 OK` response code and updated [WorkbookChartAxis](../resources/chartaxis.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="abd5e-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="abd5e-155">Example</span></span>
##### <a name="request"></a><span data-ttu-id="abd5e-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="abd5e-156">Request</span></span>
<span data-ttu-id="abd5e-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="abd5e-157">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartaxis"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis
Content-type: application/json
Content-length: 64

{
  "majorUnit": {
  },
  "maximum": {
  },
  "minimum": {
  }
}
```
##### <a name="response"></a><span data-ttu-id="abd5e-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="abd5e-158">Response</span></span>
<span data-ttu-id="abd5e-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="abd5e-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartAxis"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 64

{
  "majorUnit": {
  },
  "maximum": {
  },
  "minimum": {
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartaxis",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->