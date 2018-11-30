---
title: Actualizar chartfont
description: Actualizar las propiedades del objeto chartfont.
ms.openlocfilehash: 271f30c71953156bb74fa587057aab9cc32a1dc6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028943"
---
# <a name="update-chartfont"></a><span data-ttu-id="f688d-103">Actualizar chartfont</span><span class="sxs-lookup"><span data-stu-id="f688d-103">Update chartfont</span></span>

<span data-ttu-id="f688d-104">Actualizar las propiedades del objeto chartfont.</span><span class="sxs-lookup"><span data-stu-id="f688d-104">Update the properties of chartfont object.</span></span>
## <a name="permissions"></a><span data-ttu-id="f688d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f688d-105">Permissions</span></span>
<span data-ttu-id="f688d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f688d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f688d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f688d-108">Permission type</span></span>      | <span data-ttu-id="f688d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f688d-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f688d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f688d-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f688d-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f688d-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f688d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f688d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f688d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f688d-113">Not supported.</span></span>    |
|<span data-ttu-id="f688d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f688d-114">Application</span></span> | <span data-ttu-id="f688d-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f688d-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f688d-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f688d-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis/format/font
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/seriesAxis/format/font
PATCH /workbook/worksheets/{id|name}/charts/{name}/axes/categoryaxis/format/font
```
## <a name="optional-request-headers"></a><span data-ttu-id="f688d-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="f688d-117">Optional request headers</span></span>
| <span data-ttu-id="f688d-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="f688d-118">Name</span></span>       | <span data-ttu-id="f688d-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f688d-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="f688d-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="f688d-120">Authorization</span></span>  | <span data-ttu-id="f688d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f688d-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f688d-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="f688d-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="f688d-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="f688d-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="f688d-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f688d-126">Request body</span></span>
<span data-ttu-id="f688d-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="f688d-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="f688d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f688d-130">Property</span></span>     | <span data-ttu-id="f688d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f688d-131">Type</span></span>   |<span data-ttu-id="f688d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f688d-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f688d-133">bold</span><span class="sxs-lookup"><span data-stu-id="f688d-133">bold</span></span>|<span data-ttu-id="f688d-134">boolean</span><span class="sxs-lookup"><span data-stu-id="f688d-134">boolean</span></span>|<span data-ttu-id="f688d-135">Representa el estado de negrita de la fuente.</span><span class="sxs-lookup"><span data-stu-id="f688d-135">Represents the bold status of font.</span></span>|
|<span data-ttu-id="f688d-136">color</span><span class="sxs-lookup"><span data-stu-id="f688d-136">color</span></span>|<span data-ttu-id="f688d-137">string</span><span class="sxs-lookup"><span data-stu-id="f688d-137">string</span></span>|<span data-ttu-id="f688d-p105">Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.</span><span class="sxs-lookup"><span data-stu-id="f688d-p105">HTML color code representation of the text color. E.g. #FF0000 represents Red.</span></span>|
|<span data-ttu-id="f688d-141">italic</span><span class="sxs-lookup"><span data-stu-id="f688d-141">italic</span></span>|<span data-ttu-id="f688d-142">boolean</span><span class="sxs-lookup"><span data-stu-id="f688d-142">boolean</span></span>|<span data-ttu-id="f688d-143">Representa el estado de cursiva de la fuente.</span><span class="sxs-lookup"><span data-stu-id="f688d-143">Represents the italic status of the font.</span></span>|
|<span data-ttu-id="f688d-144">name</span><span class="sxs-lookup"><span data-stu-id="f688d-144">name</span></span>|<span data-ttu-id="f688d-145">string</span><span class="sxs-lookup"><span data-stu-id="f688d-145">string</span></span>|<span data-ttu-id="f688d-146">Nombre de fuente (por ejemplo, "Calibri")</span><span class="sxs-lookup"><span data-stu-id="f688d-146">Font name (e.g. "Calibri")</span></span>|
|<span data-ttu-id="f688d-147">Tamaño</span><span class="sxs-lookup"><span data-stu-id="f688d-147">size</span></span>|<span data-ttu-id="f688d-148">Double</span><span class="sxs-lookup"><span data-stu-id="f688d-148">double</span></span>|<span data-ttu-id="f688d-149">Tamaño de la fuente (por ejemplo, 11).</span><span class="sxs-lookup"><span data-stu-id="f688d-149">Size of the font (e.g. 11)</span></span>|
|<span data-ttu-id="f688d-150">underline</span><span class="sxs-lookup"><span data-stu-id="f688d-150">underline</span></span>|<span data-ttu-id="f688d-151">string</span><span class="sxs-lookup"><span data-stu-id="f688d-151">string</span></span>|<span data-ttu-id="f688d-152">Tipo de subrayado aplicado a la fuente.</span><span class="sxs-lookup"><span data-stu-id="f688d-152">Type of underline applied to the font.</span></span> <span data-ttu-id="f688d-153">Los valores posibles son: `None`, `Single`.</span><span class="sxs-lookup"><span data-stu-id="f688d-153">The possible values are: `None`, `Single`.</span></span>|

## <a name="response"></a><span data-ttu-id="f688d-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f688d-154">Response</span></span>

<span data-ttu-id="f688d-155">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookChartFont](../resources/chartfont.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f688d-155">If successful, this method returns a `200 OK` response code and updated [WorkbookChartFont](../resources/chartfont.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="f688d-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f688d-156">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f688d-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f688d-157">Request</span></span>
<span data-ttu-id="f688d-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f688d-158">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartfont"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/valueAxis/format/font
Content-type: application/json
Content-length: 134

{
  "bold": true,
  "color": "color-value",
  "italic": true,
  "name": "name-value",
  "size": 99,
  "underline": "underline-value"
}
```
##### <a name="response"></a><span data-ttu-id="f688d-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f688d-159">Response</span></span>
<span data-ttu-id="f688d-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f688d-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartFont"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 134

{
  "bold": true,
  "color": "color-value",
  "italic": true,
  "name": "name-value",
  "size": 99,
  "underline": "underline-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartfont",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->