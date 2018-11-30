---
title: 'Range: OffsetRange'
description: Obtiene un objeto que representa un intervalo desplazado con respecto al intervalo especificado. La dimensión del intervalo devuelto coincidirá con este intervalo. Si el intervalo resultante se fuerza fuera de los límites de la cuadrícula de la hoja de cálculo, se producirá una excepción.
ms.openlocfilehash: fcbc13fa17e0df97eceb4705e7775d733d1728dd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032205"
---
# <a name="range-offsetrange"></a><span data-ttu-id="fdaa0-105">Range: OffsetRange</span><span class="sxs-lookup"><span data-stu-id="fdaa0-105">Range: OffsetRange</span></span>

<span data-ttu-id="fdaa0-p102">Obtiene un objeto que representa un intervalo desplazado con respecto al intervalo especificado. La dimensión del intervalo devuelto coincidirá con este intervalo. Si el intervalo resultante se fuerza fuera de los límites de la cuadrícula de la hoja de cálculo, se producirá una excepción.</span><span class="sxs-lookup"><span data-stu-id="fdaa0-p102">Gets an object which represents a range that's offset from the specified range. The dimension of the returned range will match this range. If the resulting range is forced outside the bounds of the worksheet grid, an exception will be thrown.</span></span>
## <a name="permissions"></a><span data-ttu-id="fdaa0-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="fdaa0-109">Permissions</span></span>
<span data-ttu-id="fdaa0-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fdaa0-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fdaa0-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fdaa0-112">Permission type</span></span>      | <span data-ttu-id="fdaa0-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fdaa0-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fdaa0-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fdaa0-114">Delegated (work or school account)</span></span> | <span data-ttu-id="fdaa0-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fdaa0-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="fdaa0-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fdaa0-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fdaa0-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fdaa0-117">Not supported.</span></span>    |
|<span data-ttu-id="fdaa0-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fdaa0-118">Application</span></span> | <span data-ttu-id="fdaa0-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fdaa0-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fdaa0-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fdaa0-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/offsetRange
GET /workbook/worksheets/{id|name}/range(address='<address>')/offsetRange
GET /workbook/tables/{id|name}/columns/{id|name}/range/offsetRange

```
## <a name="request-headers"></a><span data-ttu-id="fdaa0-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fdaa0-121">Request headers</span></span>
| <span data-ttu-id="fdaa0-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="fdaa0-122">Name</span></span>       | <span data-ttu-id="fdaa0-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdaa0-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="fdaa0-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="fdaa0-124">Authorization</span></span>  | <span data-ttu-id="fdaa0-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fdaa0-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="fdaa0-127">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="fdaa0-127">Workbook-Session-Id</span></span>  | <span data-ttu-id="fdaa0-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="fdaa0-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="fdaa0-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fdaa0-130">Request body</span></span>
<span data-ttu-id="fdaa0-131">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="fdaa0-131">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="fdaa0-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fdaa0-132">Parameter</span></span>    | <span data-ttu-id="fdaa0-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="fdaa0-133">Type</span></span>   |<span data-ttu-id="fdaa0-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdaa0-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fdaa0-135">rowOffset</span><span class="sxs-lookup"><span data-stu-id="fdaa0-135">rowOffset</span></span>|<span data-ttu-id="fdaa0-136">Int32</span><span class="sxs-lookup"><span data-stu-id="fdaa0-136">Int32</span></span>|<span data-ttu-id="fdaa0-p106">Número de filas (número positivo, negativo o 0) que debe desplazarse el intervalo. Los valores positivos desplazan hacia abajo, mientras que los negativos lo hacen hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="fdaa0-p106">The number of rows (positive, negative, or 0) by which the range is to be offset. Positive values are offset downward, and negative values are offset upward.</span></span>|
|<span data-ttu-id="fdaa0-139">columnOffset</span><span class="sxs-lookup"><span data-stu-id="fdaa0-139">columnOffset</span></span>|<span data-ttu-id="fdaa0-140">Int32</span><span class="sxs-lookup"><span data-stu-id="fdaa0-140">Int32</span></span>|<span data-ttu-id="fdaa0-p107">Número de columnas (número positivo, negativo o 0) que debe desplazarse el rango. Los valores positivos desplazan hacia la derecha, mientras que los negativos lo hacen hacia la izquierda.</span><span class="sxs-lookup"><span data-stu-id="fdaa0-p107">The number of columns (positive, negative, or 0) by which the range is to be offset. Positive values are offset to the right, and negative values are offset to the left.</span></span>|

## <a name="response"></a><span data-ttu-id="fdaa0-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fdaa0-143">Response</span></span>

<span data-ttu-id="fdaa0-144">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fdaa0-144">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fdaa0-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fdaa0-145">Example</span></span>
<span data-ttu-id="fdaa0-146">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="fdaa0-146">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="fdaa0-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fdaa0-147">Request</span></span>
<span data-ttu-id="fdaa0-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fdaa0-148">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "isComposable": true,
  "name": "range_offsetrange"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/offsetRange
Content-type: application/json
Content-length: 49

{
  "rowOffset": 3,
  "columnOffset": 5
}
```

##### <a name="response"></a><span data-ttu-id="fdaa0-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fdaa0-149">Response</span></span>
<span data-ttu-id="fdaa0-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fdaa0-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRange"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 169

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnIndex": 99,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: OffsetRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->