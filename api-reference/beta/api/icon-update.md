---
title: Update icon
description: Actualiza las propiedades del objeto icon.
localization_priority: Normal
ms.openlocfilehash: 83e9845e87018a6f7b059a917643c1c51ccd01d5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27859181"
---
# <a name="update-icon"></a><span data-ttu-id="aef44-103">Update icon</span><span class="sxs-lookup"><span data-stu-id="aef44-103">Update icon</span></span>

> <span data-ttu-id="aef44-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="aef44-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="aef44-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="aef44-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="aef44-106">Actualiza las propiedades del objeto icon.</span><span class="sxs-lookup"><span data-stu-id="aef44-106">Update the properties of icon object.</span></span>
## <a name="permissions"></a><span data-ttu-id="aef44-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="aef44-107">Permissions</span></span>
<span data-ttu-id="aef44-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="aef44-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="aef44-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="aef44-110">Permission type</span></span>      | <span data-ttu-id="aef44-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="aef44-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="aef44-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="aef44-112">Delegated (work or school account)</span></span> | <span data-ttu-id="aef44-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aef44-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="aef44-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="aef44-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="aef44-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aef44-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="aef44-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="aef44-116">Application</span></span> | <span data-ttu-id="aef44-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aef44-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="aef44-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aef44-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/tables/{id|name}/sort/fields/icon
PATCH /workbook/worksheets/{id|name}/tables/{id|name}/sort/fields/icon
```
## <a name="optional-request-headers"></a><span data-ttu-id="aef44-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="aef44-119">Optional request headers</span></span>
| <span data-ttu-id="aef44-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="aef44-120">Name</span></span>       | <span data-ttu-id="aef44-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="aef44-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="aef44-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="aef44-122">Authorization</span></span>  | <span data-ttu-id="aef44-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aef44-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="aef44-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aef44-125">Request body</span></span>
<span data-ttu-id="aef44-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="aef44-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="aef44-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aef44-129">Property</span></span>     | <span data-ttu-id="aef44-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="aef44-130">Type</span></span>   |<span data-ttu-id="aef44-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="aef44-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="aef44-132">index</span><span class="sxs-lookup"><span data-stu-id="aef44-132">index</span></span>|<span data-ttu-id="aef44-133">int</span><span class="sxs-lookup"><span data-stu-id="aef44-133">int</span></span>|<span data-ttu-id="aef44-134">Representa el índice del icono en el conjunto concreto.</span><span class="sxs-lookup"><span data-stu-id="aef44-134">Represents the index of the icon in the given set.</span></span>|
|<span data-ttu-id="aef44-135">set</span><span class="sxs-lookup"><span data-stu-id="aef44-135">set</span></span>|<span data-ttu-id="aef44-136">string</span><span class="sxs-lookup"><span data-stu-id="aef44-136">string</span></span>|<span data-ttu-id="aef44-p105">Representa el conjunto al que pertenece el icono. Valores posibles: `Invalid`, `ThreeArrows`, `ThreeArrowsGray`, `ThreeFlags`, `ThreeTrafficLights1`, `ThreeTrafficLights2`, `ThreeSigns`, `ThreeSymbols`, `ThreeSymbols2`, `FourArrows`, `FourArrowsGray`, `FourRedToBlack`, `FourRating`, `FourTrafficLights`, `FiveArrows`, `FiveArrowsGray`, `FiveRating`, `FiveQuarters`, `ThreeStars`, `ThreeTriangles`, `FiveBoxes`.</span><span class="sxs-lookup"><span data-stu-id="aef44-p105">Represents the set that the icon is part of. Possible values are: `Invalid`, `ThreeArrows`, `ThreeArrowsGray`, `ThreeFlags`, `ThreeTrafficLights1`, `ThreeTrafficLights2`, `ThreeSigns`, `ThreeSymbols`, `ThreeSymbols2`, `FourArrows`, `FourArrowsGray`, `FourRedToBlack`, `FourRating`, `FourTrafficLights`, `FiveArrows`, `FiveArrowsGray`, `FiveRating`, `FiveQuarters`, `ThreeStars`, `ThreeTriangles`, `FiveBoxes`.</span></span>|

## <a name="response"></a><span data-ttu-id="aef44-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aef44-139">Response</span></span>

<span data-ttu-id="aef44-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Icon](../resources/icon.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aef44-140">If successful, this method returns a `200 OK` response code and updated [Icon](../resources/icon.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="aef44-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aef44-141">Example</span></span>
##### <a name="request"></a><span data-ttu-id="aef44-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aef44-142">Request</span></span>
<span data-ttu-id="aef44-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aef44-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_icon"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/sort/fields/icon
Content-type: application/json
Content-length: 39

{
  "set": "set-value",
  "index": 99
}
```
##### <a name="response"></a><span data-ttu-id="aef44-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aef44-144">Response</span></span>
<span data-ttu-id="aef44-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aef44-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.icon"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "set": "set-value",
  "index": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update icon",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
