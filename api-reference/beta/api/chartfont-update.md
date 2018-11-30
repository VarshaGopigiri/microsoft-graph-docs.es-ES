---
title: Actualizar chartfont
description: Actualizar las propiedades del objeto chartfont.
ms.openlocfilehash: 61ed9a6d8c9fc2507defcfe744825e9a0684c6e8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086269"
---
# <a name="update-chartfont"></a><span data-ttu-id="a5e5c-103">Actualizar chartfont</span><span class="sxs-lookup"><span data-stu-id="a5e5c-103">Update chartfont</span></span>

> <span data-ttu-id="a5e5c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a5e5c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a5e5c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a5e5c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a5e5c-106">Actualizar las propiedades del objeto chartfont.</span><span class="sxs-lookup"><span data-stu-id="a5e5c-106">Update the properties of chartfont object.</span></span>
## <a name="permissions"></a><span data-ttu-id="a5e5c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a5e5c-107">Permissions</span></span>
<span data-ttu-id="a5e5c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a5e5c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a5e5c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a5e5c-110">Permission type</span></span>      | <span data-ttu-id="a5e5c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a5e5c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a5e5c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a5e5c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="a5e5c-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a5e5c-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="a5e5c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a5e5c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a5e5c-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a5e5c-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="a5e5c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a5e5c-116">Application</span></span> | <span data-ttu-id="a5e5c-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5e5c-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a5e5c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a5e5c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/format/font
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/seriesaxis/format/font
PATCH /workbook/worksheets/{id|name}/charts(<name>)/axes/categoryaxis/format/font
```
## <a name="optional-request-headers"></a><span data-ttu-id="a5e5c-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="a5e5c-119">Optional request headers</span></span>
| <span data-ttu-id="a5e5c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="a5e5c-120">Name</span></span>       | <span data-ttu-id="a5e5c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5e5c-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="a5e5c-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="a5e5c-122">Authorization</span></span>  | <span data-ttu-id="a5e5c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a5e5c-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a5e5c-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="a5e5c-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="a5e5c-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="a5e5c-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="a5e5c-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a5e5c-128">Request body</span></span>
<span data-ttu-id="a5e5c-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="a5e5c-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="a5e5c-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a5e5c-132">Property</span></span>     | <span data-ttu-id="a5e5c-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5e5c-133">Type</span></span>   |<span data-ttu-id="a5e5c-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5e5c-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a5e5c-135">bold</span><span class="sxs-lookup"><span data-stu-id="a5e5c-135">bold</span></span>|<span data-ttu-id="a5e5c-136">boolean</span><span class="sxs-lookup"><span data-stu-id="a5e5c-136">boolean</span></span>|<span data-ttu-id="a5e5c-137">Representa el estado de negrita de la fuente.</span><span class="sxs-lookup"><span data-stu-id="a5e5c-137">Represents the bold status of font.</span></span>|
|<span data-ttu-id="a5e5c-138">color</span><span class="sxs-lookup"><span data-stu-id="a5e5c-138">color</span></span>|<span data-ttu-id="a5e5c-139">string</span><span class="sxs-lookup"><span data-stu-id="a5e5c-139">string</span></span>|<span data-ttu-id="a5e5c-p106">Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.</span><span class="sxs-lookup"><span data-stu-id="a5e5c-p106">HTML color code representation of the text color. E.g. #FF0000 represents Red.</span></span>|
|<span data-ttu-id="a5e5c-143">italic</span><span class="sxs-lookup"><span data-stu-id="a5e5c-143">italic</span></span>|<span data-ttu-id="a5e5c-144">boolean</span><span class="sxs-lookup"><span data-stu-id="a5e5c-144">boolean</span></span>|<span data-ttu-id="a5e5c-145">Representa el estado de cursiva de la fuente.</span><span class="sxs-lookup"><span data-stu-id="a5e5c-145">Represents the italic status of the font.</span></span>|
|<span data-ttu-id="a5e5c-146">name</span><span class="sxs-lookup"><span data-stu-id="a5e5c-146">name</span></span>|<span data-ttu-id="a5e5c-147">string</span><span class="sxs-lookup"><span data-stu-id="a5e5c-147">string</span></span>|<span data-ttu-id="a5e5c-148">Nombre de fuente (por ejemplo, "Calibri")</span><span class="sxs-lookup"><span data-stu-id="a5e5c-148">Font name (e.g. "Calibri")</span></span>|
|<span data-ttu-id="a5e5c-149">Tamaño</span><span class="sxs-lookup"><span data-stu-id="a5e5c-149">size</span></span>|<span data-ttu-id="a5e5c-150">Double</span><span class="sxs-lookup"><span data-stu-id="a5e5c-150">double</span></span>|<span data-ttu-id="a5e5c-151">Tamaño de la fuente (por ejemplo, 11).</span><span class="sxs-lookup"><span data-stu-id="a5e5c-151">Size of the font (e.g. 11)</span></span>|
|<span data-ttu-id="a5e5c-152">underline</span><span class="sxs-lookup"><span data-stu-id="a5e5c-152">underline</span></span>|<span data-ttu-id="a5e5c-153">string</span><span class="sxs-lookup"><span data-stu-id="a5e5c-153">string</span></span>|<span data-ttu-id="a5e5c-p107">Tipo de subrayado aplicado a la fuente. Valores posibles: `None`, `Single`.</span><span class="sxs-lookup"><span data-stu-id="a5e5c-p107">Type of underline applied to the font. Possible values are: `None`, `Single`.</span></span>|

## <a name="response"></a><span data-ttu-id="a5e5c-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5e5c-156">Response</span></span>

<span data-ttu-id="a5e5c-157">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartFont](../resources/chartfont.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5e5c-157">If successful, this method returns a `200 OK` response code and updated [ChartFont](../resources/chartfont.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a5e5c-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5e5c-158">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a5e5c-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a5e5c-159">Request</span></span>
<span data-ttu-id="a5e5c-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5e5c-160">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartfont"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/axes/valueaxis/format/font
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
##### <a name="response"></a><span data-ttu-id="a5e5c-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5e5c-161">Response</span></span>
<span data-ttu-id="a5e5c-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a5e5c-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartFont"
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