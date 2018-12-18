---
title: Update rangefont
description: Actualizar las propiedades del objeto rangefont.
author: lumine2008
ms.openlocfilehash: 662bf18fe80ff8942841bad88eb207d1ff569249
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27339959"
---
# <a name="update-rangefont"></a><span data-ttu-id="904c2-103">Update rangefont</span><span class="sxs-lookup"><span data-stu-id="904c2-103">Update rangefont</span></span>

<span data-ttu-id="904c2-104">Actualizar las propiedades del objeto rangefont.</span><span class="sxs-lookup"><span data-stu-id="904c2-104">Update the properties of rangefont object.</span></span>
## <a name="permissions"></a><span data-ttu-id="904c2-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="904c2-105">Permissions</span></span>
<span data-ttu-id="904c2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="904c2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="904c2-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="904c2-108">Permission type</span></span>      | <span data-ttu-id="904c2-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="904c2-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="904c2-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="904c2-110">Delegated (work or school account)</span></span> | <span data-ttu-id="904c2-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="904c2-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="904c2-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="904c2-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="904c2-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="904c2-113">Not supported.</span></span>    |
|<span data-ttu-id="904c2-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="904c2-114">Application</span></span> | <span data-ttu-id="904c2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="904c2-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="904c2-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="904c2-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names/{name}/range/format/font
PATCH /workbook/worksheets/{id|name}/range(address='<address>')/format/font
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format/font
```
## <a name="request-headers"></a><span data-ttu-id="904c2-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="904c2-117">Request headers</span></span>
| <span data-ttu-id="904c2-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="904c2-118">Name</span></span>       | <span data-ttu-id="904c2-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="904c2-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="904c2-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="904c2-120">Authorization</span></span>  | <span data-ttu-id="904c2-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="904c2-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="904c2-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="904c2-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="904c2-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="904c2-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="904c2-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="904c2-126">Request body</span></span>
<span data-ttu-id="904c2-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="904c2-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="904c2-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="904c2-130">Property</span></span>     | <span data-ttu-id="904c2-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="904c2-131">Type</span></span>   |<span data-ttu-id="904c2-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="904c2-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="904c2-133">bold</span><span class="sxs-lookup"><span data-stu-id="904c2-133">bold</span></span>|<span data-ttu-id="904c2-134">boolean</span><span class="sxs-lookup"><span data-stu-id="904c2-134">boolean</span></span>|<span data-ttu-id="904c2-135">Representa el estado de negrita de la fuente.</span><span class="sxs-lookup"><span data-stu-id="904c2-135">Represents the bold status of font.</span></span>|
|<span data-ttu-id="904c2-136">color</span><span class="sxs-lookup"><span data-stu-id="904c2-136">color</span></span>|<span data-ttu-id="904c2-137">string</span><span class="sxs-lookup"><span data-stu-id="904c2-137">string</span></span>|<span data-ttu-id="904c2-p105">Representación del código de color HTML del color del texto. Por ejemplo, #FF0000 representa el rojo.</span><span class="sxs-lookup"><span data-stu-id="904c2-p105">HTML color code representation of the text color. E.g. #FF0000 represents Red.</span></span>|
|<span data-ttu-id="904c2-141">italic</span><span class="sxs-lookup"><span data-stu-id="904c2-141">italic</span></span>|<span data-ttu-id="904c2-142">boolean</span><span class="sxs-lookup"><span data-stu-id="904c2-142">boolean</span></span>|<span data-ttu-id="904c2-143">Representa el estado de cursiva de la fuente.</span><span class="sxs-lookup"><span data-stu-id="904c2-143">Represents the italic status of the font.</span></span>|
|<span data-ttu-id="904c2-144">name</span><span class="sxs-lookup"><span data-stu-id="904c2-144">name</span></span>|<span data-ttu-id="904c2-145">string</span><span class="sxs-lookup"><span data-stu-id="904c2-145">string</span></span>|<span data-ttu-id="904c2-146">Nombre de fuente (por ejemplo, "Calibri")</span><span class="sxs-lookup"><span data-stu-id="904c2-146">Font name (e.g. "Calibri")</span></span>|
|<span data-ttu-id="904c2-147">Tamaño</span><span class="sxs-lookup"><span data-stu-id="904c2-147">size</span></span>|<span data-ttu-id="904c2-148">Double</span><span class="sxs-lookup"><span data-stu-id="904c2-148">double</span></span>|<span data-ttu-id="904c2-149">Tamaño de fuente</span><span class="sxs-lookup"><span data-stu-id="904c2-149">Font size.</span></span>|
|<span data-ttu-id="904c2-150">underline</span><span class="sxs-lookup"><span data-stu-id="904c2-150">underline</span></span>|<span data-ttu-id="904c2-151">string</span><span class="sxs-lookup"><span data-stu-id="904c2-151">string</span></span>|<span data-ttu-id="904c2-152">Tipo de subrayado aplicado a la fuente.</span><span class="sxs-lookup"><span data-stu-id="904c2-152">Type of underline applied to the font.</span></span> <span data-ttu-id="904c2-153">Los valores posibles son: `None`, `Single`, `Double`, `SingleAccountant`, `DoubleAccountant`.</span><span class="sxs-lookup"><span data-stu-id="904c2-153">The possible values are: `None`, `Single`, `Double`, `SingleAccountant`, `DoubleAccountant`.</span></span>|

## <a name="response"></a><span data-ttu-id="904c2-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="904c2-154">Response</span></span>

<span data-ttu-id="904c2-155">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookRangeFont](../resources/rangefont.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="904c2-155">If successful, this method returns a `200 OK` response code and updated [WorkbookRangeFont](../resources/rangefont.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="904c2-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="904c2-156">Example</span></span>
##### <a name="request"></a><span data-ttu-id="904c2-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="904c2-157">Request</span></span>
<span data-ttu-id="904c2-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="904c2-158">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_rangefont"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/format/font
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
##### <a name="response"></a><span data-ttu-id="904c2-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="904c2-159">Response</span></span>
<span data-ttu-id="904c2-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="904c2-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeFont"
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
  "description": "Update rangefont",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->