---
title: Actualizar chartaxis
description: Actualizar las propiedades del objeto chartaxis.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 843aad2b3d6ea822078834439a085ba4bb10bf8b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27813702"
---
# <a name="update-chartaxis"></a><span data-ttu-id="76fae-103">Actualizar chartaxis</span><span class="sxs-lookup"><span data-stu-id="76fae-103">Update chartaxis</span></span>

> <span data-ttu-id="76fae-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="76fae-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="76fae-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="76fae-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="76fae-106">Actualizar las propiedades del objeto chartaxis.</span><span class="sxs-lookup"><span data-stu-id="76fae-106">Update the properties of chartaxis object.</span></span>
## <a name="permissions"></a><span data-ttu-id="76fae-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="76fae-107">Permissions</span></span>
<span data-ttu-id="76fae-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="76fae-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="76fae-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="76fae-110">Permission type</span></span>      | <span data-ttu-id="76fae-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="76fae-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="76fae-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="76fae-112">Delegated (work or school account)</span></span> | <span data-ttu-id="76fae-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="76fae-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="76fae-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="76fae-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="76fae-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="76fae-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="76fae-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="76fae-116">Application</span></span> | <span data-ttu-id="76fae-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="76fae-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="76fae-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="76fae-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/seriesaxis
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/categoryaxis
```
## <a name="optional-request-headers"></a><span data-ttu-id="76fae-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="76fae-119">Optional request headers</span></span>
| <span data-ttu-id="76fae-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="76fae-120">Name</span></span>       | <span data-ttu-id="76fae-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="76fae-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="76fae-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="76fae-122">Authorization</span></span>  | <span data-ttu-id="76fae-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="76fae-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="76fae-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="76fae-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="76fae-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="76fae-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="76fae-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="76fae-128">Request body</span></span>
<span data-ttu-id="76fae-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="76fae-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="76fae-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="76fae-132">Property</span></span>     | <span data-ttu-id="76fae-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="76fae-133">Type</span></span>   |<span data-ttu-id="76fae-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="76fae-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="76fae-135">majorUnit</span><span class="sxs-lookup"><span data-stu-id="76fae-135">majorUnit</span></span>|<span data-ttu-id="76fae-136">object</span><span class="sxs-lookup"><span data-stu-id="76fae-136">object</span></span>|<span data-ttu-id="76fae-p106">Representa el intervalo entre dos marcas de graduación principales. Puede establecerse en un valor numérico o en una cadena vacía.  El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="76fae-p106">Represents the interval between two major tick marks. Can be set to a numeric value or an empty string.  The returned value is always a number.</span></span>|
|<span data-ttu-id="76fae-140">maximum</span><span class="sxs-lookup"><span data-stu-id="76fae-140">maximum</span></span>|<span data-ttu-id="76fae-141">object</span><span class="sxs-lookup"><span data-stu-id="76fae-141">object</span></span>|<span data-ttu-id="76fae-p107">Representa el valor máximo del eje de valores.  Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos).  El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="76fae-p107">Represents the maximum value on the value axis.  Can be set to a numeric value or an empty string (for automatic axis values).  The returned value is always a number.</span></span>|
|<span data-ttu-id="76fae-145">minimum</span><span class="sxs-lookup"><span data-stu-id="76fae-145">minimum</span></span>|<span data-ttu-id="76fae-146">object</span><span class="sxs-lookup"><span data-stu-id="76fae-146">object</span></span>|<span data-ttu-id="76fae-p108">Representa el valor mínimo del eje de valores. Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos). El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="76fae-p108">Represents the minimum value on the value axis. Can be set to a numeric value or an empty string (for automatic axis values).  The returned value is always a number.</span></span>|
|<span data-ttu-id="76fae-150">minorUnit</span><span class="sxs-lookup"><span data-stu-id="76fae-150">minorUnit</span></span>|<span data-ttu-id="76fae-151">object</span><span class="sxs-lookup"><span data-stu-id="76fae-151">object</span></span>|<span data-ttu-id="76fae-p109">Representa el intervalo entre dos marcas de graduación secundarias. Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos). El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="76fae-p109">Represents the interval between two minor tick marks. "Can be set to a numeric value or an empty string (for automatic axis values). The returned value is always a number.</span></span>|

## <a name="response"></a><span data-ttu-id="76fae-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76fae-155">Response</span></span>

<span data-ttu-id="76fae-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartAxis](../resources/chartaxis.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="76fae-156">If successful, this method returns a `200 OK` response code and updated [ChartAxis](../resources/chartaxis.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="76fae-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="76fae-157">Example</span></span>
##### <a name="request"></a><span data-ttu-id="76fae-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="76fae-158">Request</span></span>
<span data-ttu-id="76fae-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="76fae-159">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartaxis"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis
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
##### <a name="response"></a><span data-ttu-id="76fae-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76fae-160">Response</span></span>
<span data-ttu-id="76fae-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="76fae-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartaxis"
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
