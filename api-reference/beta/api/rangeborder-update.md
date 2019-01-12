---
title: Update rangeborder
description: Actualizar las propiedades del objeto rangeborder.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: ac989724f0e950a079479c8285cea64e2e24a8fc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933781"
---
# <a name="update-rangeborder"></a><span data-ttu-id="3bee7-103">Update rangeborder</span><span class="sxs-lookup"><span data-stu-id="3bee7-103">Update rangeborder</span></span>

> <span data-ttu-id="3bee7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3bee7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3bee7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3bee7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3bee7-106">Actualizar las propiedades del objeto rangeborder.</span><span class="sxs-lookup"><span data-stu-id="3bee7-106">Update the properties of rangeborder object.</span></span>
## <a name="permissions"></a><span data-ttu-id="3bee7-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3bee7-107">Permissions</span></span>
<span data-ttu-id="3bee7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3bee7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3bee7-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3bee7-110">Permission type</span></span>      | <span data-ttu-id="3bee7-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3bee7-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3bee7-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3bee7-112">Delegated (work or school account)</span></span> | <span data-ttu-id="3bee7-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3bee7-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="3bee7-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3bee7-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3bee7-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3bee7-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="3bee7-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3bee7-116">Application</span></span> | <span data-ttu-id="3bee7-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3bee7-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="3bee7-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3bee7-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names(<name>)/range/format/borders(<sideIndex>)
PATCH /workbook/worksheets/{id|name}/range(address='<address>')/format/borders(<sideIndex>)
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format/borders(<sideIndex>)
```
## <a name="optional-request-headers"></a><span data-ttu-id="3bee7-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="3bee7-119">Optional request headers</span></span>
| <span data-ttu-id="3bee7-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="3bee7-120">Name</span></span>       | <span data-ttu-id="3bee7-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bee7-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="3bee7-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="3bee7-122">Authorization</span></span>  | <span data-ttu-id="3bee7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3bee7-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="3bee7-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="3bee7-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="3bee7-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="3bee7-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="3bee7-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3bee7-128">Request body</span></span>
<span data-ttu-id="3bee7-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="3bee7-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="3bee7-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3bee7-132">Property</span></span>     | <span data-ttu-id="3bee7-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="3bee7-133">Type</span></span>   |<span data-ttu-id="3bee7-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bee7-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3bee7-135">color</span><span class="sxs-lookup"><span data-stu-id="3bee7-135">color</span></span>|<span data-ttu-id="3bee7-136">string</span><span class="sxs-lookup"><span data-stu-id="3bee7-136">string</span></span>|<span data-ttu-id="3bee7-137">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="3bee7-137">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange").</span></span>|
|<span data-ttu-id="3bee7-138">style</span><span class="sxs-lookup"><span data-stu-id="3bee7-138">style</span></span>|<span data-ttu-id="3bee7-139">string</span><span class="sxs-lookup"><span data-stu-id="3bee7-139">string</span></span>|<span data-ttu-id="3bee7-p106">Una de las constantes de estilo de línea que especifica el estilo de línea del borde. Valores posibles: `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double`, `SlantDashDot`.</span><span class="sxs-lookup"><span data-stu-id="3bee7-p106">One of the constants of line style specifying the line style for the border. Possible values are: `None`, `Continuous`, `Dash`, `DashDot`, `DashDotDot`, `Dot`, `Double`, `SlantDashDot`.</span></span>|
|<span data-ttu-id="3bee7-142">weight</span><span class="sxs-lookup"><span data-stu-id="3bee7-142">weight</span></span>|<span data-ttu-id="3bee7-143">string</span><span class="sxs-lookup"><span data-stu-id="3bee7-143">string</span></span>|<span data-ttu-id="3bee7-p107">Especifica el grosor del borde alrededor de un rango. Valores posibles: `Hairline`, `Thin`, `Medium`, `Thick`.</span><span class="sxs-lookup"><span data-stu-id="3bee7-p107">Specifies the weight of the border around a range. Possible values are: `Hairline`, `Thin`, `Medium`, `Thick`.</span></span>|

## <a name="response"></a><span data-ttu-id="3bee7-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3bee7-146">Response</span></span>

<span data-ttu-id="3bee7-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [RangeBorder](../resources/rangeborder.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3bee7-147">If successful, this method returns a `200 OK` response code and updated [RangeBorder](../resources/rangeborder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="3bee7-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3bee7-148">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3bee7-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3bee7-149">Request</span></span>
<span data-ttu-id="3bee7-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3bee7-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_rangeborder"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/format/borders(<sideIndex>)
Content-type: application/json
Content-length: 136

{
  "color": "color-value",
  "style": "style-value",
  "sideIndex": "sideIndex-value",
  "weight": "weight-value"
}
```
##### <a name="response"></a><span data-ttu-id="3bee7-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3bee7-151">Response</span></span>
<span data-ttu-id="3bee7-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3bee7-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeBorder"
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
