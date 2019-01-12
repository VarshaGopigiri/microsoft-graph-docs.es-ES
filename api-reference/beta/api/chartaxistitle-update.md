---
title: Actualizar chartaxistitle
description: Actualizar las propiedades del objeto chartaxistitle.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: fd6b38b2ff7b0c65ed58b97326c9bb1e63d34079
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966373"
---
# <a name="update-chartaxistitle"></a><span data-ttu-id="6b7ae-103">Actualizar chartaxistitle</span><span class="sxs-lookup"><span data-stu-id="6b7ae-103">Update chartaxistitle</span></span>

> <span data-ttu-id="6b7ae-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6b7ae-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6b7ae-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6b7ae-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6b7ae-106">Actualizar las propiedades del objeto chartaxistitle.</span><span class="sxs-lookup"><span data-stu-id="6b7ae-106">Update the properties of chartaxistitle object.</span></span>
## <a name="permissions"></a><span data-ttu-id="6b7ae-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6b7ae-107">Permissions</span></span>
<span data-ttu-id="6b7ae-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6b7ae-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6b7ae-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6b7ae-110">Permission type</span></span>      | <span data-ttu-id="6b7ae-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6b7ae-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6b7ae-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6b7ae-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6b7ae-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6b7ae-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6b7ae-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6b7ae-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6b7ae-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6b7ae-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6b7ae-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6b7ae-116">Application</span></span> | <span data-ttu-id="6b7ae-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6b7ae-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6b7ae-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6b7ae-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/title
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/seriesaxis/title
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/categoryaxis/title
```
## <a name="optional-request-headers"></a><span data-ttu-id="6b7ae-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="6b7ae-119">Optional request headers</span></span>
| <span data-ttu-id="6b7ae-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="6b7ae-120">Name</span></span>       | <span data-ttu-id="6b7ae-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b7ae-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="6b7ae-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="6b7ae-122">Authorization</span></span>  | <span data-ttu-id="6b7ae-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6b7ae-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6b7ae-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="6b7ae-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="6b7ae-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="6b7ae-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="6b7ae-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6b7ae-128">Request body</span></span>
<span data-ttu-id="6b7ae-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="6b7ae-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="6b7ae-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6b7ae-132">Property</span></span>     | <span data-ttu-id="6b7ae-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="6b7ae-133">Type</span></span>   |<span data-ttu-id="6b7ae-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b7ae-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6b7ae-135">text</span><span class="sxs-lookup"><span data-stu-id="6b7ae-135">text</span></span>|<span data-ttu-id="6b7ae-136">string</span><span class="sxs-lookup"><span data-stu-id="6b7ae-136">string</span></span>|<span data-ttu-id="6b7ae-137">Representa el título del eje.</span><span class="sxs-lookup"><span data-stu-id="6b7ae-137">Represents the axis title.</span></span>|
|<span data-ttu-id="6b7ae-138">visible</span><span class="sxs-lookup"><span data-stu-id="6b7ae-138">visible</span></span>|<span data-ttu-id="6b7ae-139">boolean</span><span class="sxs-lookup"><span data-stu-id="6b7ae-139">boolean</span></span>|<span data-ttu-id="6b7ae-140">Valor booleano que especifica la visibilidad del título de un eje.</span><span class="sxs-lookup"><span data-stu-id="6b7ae-140">A boolean that specifies the visibility of an axis title.</span></span>|

## <a name="response"></a><span data-ttu-id="6b7ae-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6b7ae-141">Response</span></span>

<span data-ttu-id="6b7ae-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartAxisTitle](../resources/chartaxistitle.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b7ae-142">If successful, this method returns a `200 OK` response code and updated [ChartAxisTitle](../resources/chartaxistitle.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6b7ae-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6b7ae-143">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6b7ae-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6b7ae-144">Request</span></span>
<span data-ttu-id="6b7ae-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6b7ae-145">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartaxistitle"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/title
Content-type: application/json
Content-length: 45

{
  "text": "text-value",
  "visible": true
}
```
##### <a name="response"></a><span data-ttu-id="6b7ae-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6b7ae-146">Response</span></span>
<span data-ttu-id="6b7ae-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6b7ae-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartAxisTitle"
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
