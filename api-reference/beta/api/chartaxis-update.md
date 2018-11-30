---
title: Actualizar chartaxis
description: Actualizar las propiedades del objeto chartaxis.
ms.openlocfilehash: aebb499bd6aaa601fc63eb15c7cd7ab9fc3fe7ed
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086274"
---
# <a name="update-chartaxis"></a><span data-ttu-id="05f5c-103">Actualizar chartaxis</span><span class="sxs-lookup"><span data-stu-id="05f5c-103">Update chartaxis</span></span>

> <span data-ttu-id="05f5c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="05f5c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="05f5c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="05f5c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="05f5c-106">Actualizar las propiedades del objeto chartaxis.</span><span class="sxs-lookup"><span data-stu-id="05f5c-106">Update the properties of chartaxis object.</span></span>
## <a name="permissions"></a><span data-ttu-id="05f5c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="05f5c-107">Permissions</span></span>
<span data-ttu-id="05f5c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="05f5c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="05f5c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="05f5c-110">Permission type</span></span>      | <span data-ttu-id="05f5c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="05f5c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="05f5c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="05f5c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="05f5c-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="05f5c-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="05f5c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="05f5c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="05f5c-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="05f5c-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="05f5c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="05f5c-116">Application</span></span> | <span data-ttu-id="05f5c-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="05f5c-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="05f5c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="05f5c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/seriesaxis
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/categoryaxis
```
## <a name="optional-request-headers"></a><span data-ttu-id="05f5c-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="05f5c-119">Optional request headers</span></span>
| <span data-ttu-id="05f5c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="05f5c-120">Name</span></span>       | <span data-ttu-id="05f5c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="05f5c-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="05f5c-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="05f5c-122">Authorization</span></span>  | <span data-ttu-id="05f5c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="05f5c-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="05f5c-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="05f5c-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="05f5c-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="05f5c-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="05f5c-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="05f5c-128">Request body</span></span>
<span data-ttu-id="05f5c-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="05f5c-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="05f5c-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="05f5c-132">Property</span></span>     | <span data-ttu-id="05f5c-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="05f5c-133">Type</span></span>   |<span data-ttu-id="05f5c-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="05f5c-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="05f5c-135">majorUnit</span><span class="sxs-lookup"><span data-stu-id="05f5c-135">majorUnit</span></span>|<span data-ttu-id="05f5c-136">object</span><span class="sxs-lookup"><span data-stu-id="05f5c-136">object</span></span>|<span data-ttu-id="05f5c-p106">Representa el intervalo entre dos marcas de graduación principales. Puede establecerse en un valor numérico o en una cadena vacía.  El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="05f5c-p106">Represents the interval between two major tick marks. Can be set to a numeric value or an empty string.  The returned value is always a number.</span></span>|
|<span data-ttu-id="05f5c-140">maximum</span><span class="sxs-lookup"><span data-stu-id="05f5c-140">maximum</span></span>|<span data-ttu-id="05f5c-141">object</span><span class="sxs-lookup"><span data-stu-id="05f5c-141">object</span></span>|<span data-ttu-id="05f5c-p107">Representa el valor máximo del eje de valores.  Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos).  El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="05f5c-p107">Represents the maximum value on the value axis.  Can be set to a numeric value or an empty string (for automatic axis values).  The returned value is always a number.</span></span>|
|<span data-ttu-id="05f5c-145">minimum</span><span class="sxs-lookup"><span data-stu-id="05f5c-145">minimum</span></span>|<span data-ttu-id="05f5c-146">object</span><span class="sxs-lookup"><span data-stu-id="05f5c-146">object</span></span>|<span data-ttu-id="05f5c-p108">Representa el valor mínimo del eje de valores. Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos). El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="05f5c-p108">Represents the minimum value on the value axis. Can be set to a numeric value or an empty string (for automatic axis values).  The returned value is always a number.</span></span>|
|<span data-ttu-id="05f5c-150">minorUnit</span><span class="sxs-lookup"><span data-stu-id="05f5c-150">minorUnit</span></span>|<span data-ttu-id="05f5c-151">object</span><span class="sxs-lookup"><span data-stu-id="05f5c-151">object</span></span>|<span data-ttu-id="05f5c-p109">Representa el intervalo entre dos marcas de graduación secundarias. Puede establecerse en un valor numérico o en una cadena vacía (para valores de eje automáticos). El valor devuelto siempre es un número.</span><span class="sxs-lookup"><span data-stu-id="05f5c-p109">Represents the interval between two minor tick marks. "Can be set to a numeric value or an empty string (for automatic axis values). The returned value is always a number.</span></span>|

## <a name="response"></a><span data-ttu-id="05f5c-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05f5c-155">Response</span></span>

<span data-ttu-id="05f5c-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartAxis](../resources/chartaxis.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="05f5c-156">If successful, this method returns a `200 OK` response code and updated [ChartAxis](../resources/chartaxis.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="05f5c-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="05f5c-157">Example</span></span>
##### <a name="request"></a><span data-ttu-id="05f5c-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="05f5c-158">Request</span></span>
<span data-ttu-id="05f5c-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="05f5c-159">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="05f5c-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05f5c-160">Response</span></span>
<span data-ttu-id="05f5c-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="05f5c-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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