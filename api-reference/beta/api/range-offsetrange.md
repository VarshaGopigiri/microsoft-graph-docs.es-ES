---
title: 'Range: OffsetRange'
description: Obtiene un objeto que representa un intervalo desplazado con respecto al intervalo especificado. La dimensión del intervalo devuelto coincidirá con este intervalo. Si el intervalo resultante se fuerza fuera de los límites de la cuadrícula de la hoja de cálculo, se producirá una excepción.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 4f1a513a33185dba976398e31caf4996005feb67
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27925801"
---
# <a name="range-offsetrange"></a><span data-ttu-id="e94ec-105">Range: OffsetRange</span><span class="sxs-lookup"><span data-stu-id="e94ec-105">Range: OffsetRange</span></span>

> <span data-ttu-id="e94ec-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e94ec-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e94ec-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e94ec-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e94ec-p103">Obtiene un objeto que representa un intervalo desplazado con respecto al intervalo especificado. La dimensión del intervalo devuelto coincidirá con este intervalo. Si el intervalo resultante se fuerza fuera de los límites de la cuadrícula de la hoja de cálculo, se producirá una excepción.</span><span class="sxs-lookup"><span data-stu-id="e94ec-p103">Gets an object which represents a range that's offset from the specified range. The dimension of the returned range will match this range. If the resulting range is forced outside the bounds of the worksheet grid, an exception will be thrown.</span></span>
## <a name="permissions"></a><span data-ttu-id="e94ec-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="e94ec-111">Permissions</span></span>
<span data-ttu-id="e94ec-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e94ec-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e94ec-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e94ec-114">Permission type</span></span>      | <span data-ttu-id="e94ec-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e94ec-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e94ec-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e94ec-116">Delegated (work or school account)</span></span> | <span data-ttu-id="e94ec-117">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e94ec-117">Files.ReadWrite</span></span>    |
|<span data-ttu-id="e94ec-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e94ec-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e94ec-119">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e94ec-119">Files.ReadWrite</span></span>    |
|<span data-ttu-id="e94ec-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e94ec-120">Application</span></span> | <span data-ttu-id="e94ec-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e94ec-121">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e94ec-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e94ec-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/OffsetRange
GET /workbook/worksheets/{id|name}/range(address='<address>')/OffsetRange
GET /workbook/tables/{id|name}/columns/{id|name}/range/OffsetRange

```
## <a name="request-headers"></a><span data-ttu-id="e94ec-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e94ec-123">Request headers</span></span>
| <span data-ttu-id="e94ec-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="e94ec-124">Name</span></span>       | <span data-ttu-id="e94ec-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="e94ec-125">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e94ec-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="e94ec-126">Authorization</span></span>  | <span data-ttu-id="e94ec-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e94ec-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e94ec-129">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="e94ec-129">Workbook-Session-Id</span></span>  | <span data-ttu-id="e94ec-p106">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="e94ec-p106">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="e94ec-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e94ec-132">Request body</span></span>
<span data-ttu-id="e94ec-133">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="e94ec-133">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="e94ec-134">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e94ec-134">Parameter</span></span>    | <span data-ttu-id="e94ec-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="e94ec-135">Type</span></span>   |<span data-ttu-id="e94ec-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="e94ec-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e94ec-137">rowOffset</span><span class="sxs-lookup"><span data-stu-id="e94ec-137">rowOffset</span></span>|<span data-ttu-id="e94ec-138">number</span><span class="sxs-lookup"><span data-stu-id="e94ec-138">number</span></span>|<span data-ttu-id="e94ec-p107">Número de filas (número positivo, negativo o 0) que debe desplazarse el intervalo. Los valores positivos desplazan hacia abajo, mientras que los negativos lo hacen hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="e94ec-p107">The number of rows (positive, negative, or 0) by which the range is to be offset. Positive values are offset downward, and negative values are offset upward.</span></span>|
|<span data-ttu-id="e94ec-141">columnOffset</span><span class="sxs-lookup"><span data-stu-id="e94ec-141">columnOffset</span></span>|<span data-ttu-id="e94ec-142">number</span><span class="sxs-lookup"><span data-stu-id="e94ec-142">number</span></span>|<span data-ttu-id="e94ec-p108">Número de columnas (número positivo, negativo o 0) que debe desplazarse el rango. Los valores positivos desplazan hacia la derecha, mientras que los negativos lo hacen hacia la izquierda.</span><span class="sxs-lookup"><span data-stu-id="e94ec-p108">The number of columns (positive, negative, or 0) by which the range is to be offset. Positive values are offset to the right, and negative values are offset to the left.</span></span>|

## <a name="response"></a><span data-ttu-id="e94ec-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e94ec-145">Response</span></span>

<span data-ttu-id="e94ec-146">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e94ec-146">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e94ec-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e94ec-147">Example</span></span>
<span data-ttu-id="e94ec-148">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="e94ec-148">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="e94ec-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e94ec-149">Request</span></span>
<span data-ttu-id="e94ec-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e94ec-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_offsetrange"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/OffsetRange
Content-type: application/json
Content-length: 49

{
  "rowOffset": {
  },
  "columnOffset": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="e94ec-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e94ec-151">Response</span></span>
<span data-ttu-id="e94ec-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e94ec-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
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
