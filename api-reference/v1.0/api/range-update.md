---
title: Update range
description: Actualizar las propiedades del objeto de rango.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: fda18c3632874cd60da881ec82ff174c5ede5b7d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987605"
---
# <a name="update-range"></a><span data-ttu-id="6a7b3-103">Update range</span><span class="sxs-lookup"><span data-stu-id="6a7b3-103">Update range</span></span>

<span data-ttu-id="6a7b3-104">Actualizar las propiedades del objeto de rango.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-104">Update the properties of range object.</span></span>
## <a name="permissions"></a><span data-ttu-id="6a7b3-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="6a7b3-105">Permissions</span></span>
<span data-ttu-id="6a7b3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6a7b3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6a7b3-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6a7b3-108">Permission type</span></span>      | <span data-ttu-id="6a7b3-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6a7b3-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6a7b3-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6a7b3-110">Delegated (work or school account)</span></span> | <span data-ttu-id="6a7b3-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6a7b3-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6a7b3-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6a7b3-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6a7b3-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-113">Not supported.</span></span>    |
|<span data-ttu-id="6a7b3-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6a7b3-114">Application</span></span> | <span data-ttu-id="6a7b3-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6a7b3-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6a7b3-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names/{name}/range
PATCH /workbook/worksheets/{id|name}/range(address='<address>')
PATCH /workbook/tables/{id|name}/columns/{id|name}/range
```
## <a name="optional-request-headers"></a><span data-ttu-id="6a7b3-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="6a7b3-117">Optional request headers</span></span>
| <span data-ttu-id="6a7b3-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="6a7b3-118">Name</span></span>       | <span data-ttu-id="6a7b3-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a7b3-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="6a7b3-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="6a7b3-120">Authorization</span></span>  | <span data-ttu-id="6a7b3-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6a7b3-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="6a7b3-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="6a7b3-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="6a7b3-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6a7b3-126">Request body</span></span>
<span data-ttu-id="6a7b3-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="6a7b3-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6a7b3-130">Property</span></span>     | <span data-ttu-id="6a7b3-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a7b3-131">Type</span></span>   |<span data-ttu-id="6a7b3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a7b3-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6a7b3-133">columnHidden</span><span class="sxs-lookup"><span data-stu-id="6a7b3-133">columnHidden</span></span>|<span data-ttu-id="6a7b3-134">boolean</span><span class="sxs-lookup"><span data-stu-id="6a7b3-134">boolean</span></span>|<span data-ttu-id="6a7b3-135">Representa si todas las columnas del rango actual están ocultas.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-135">Represents if all columns of the current range are hidden.</span></span>|
|<span data-ttu-id="6a7b3-136">formulas</span><span class="sxs-lookup"><span data-stu-id="6a7b3-136">formulas</span></span>|<span data-ttu-id="6a7b3-137">Json</span><span class="sxs-lookup"><span data-stu-id="6a7b3-137">Json</span></span>|<span data-ttu-id="6a7b3-138">Representa la fórmula en notación de estilo A1.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-138">Represents the formula in A1-style notation.</span></span>|
|<span data-ttu-id="6a7b3-139">formulasLocal</span><span class="sxs-lookup"><span data-stu-id="6a7b3-139">formulasLocal</span></span>|<span data-ttu-id="6a7b3-140">Json</span><span class="sxs-lookup"><span data-stu-id="6a7b3-140">Json</span></span>|<span data-ttu-id="6a7b3-p105">Representa la fórmula en notación de estilo A1, en el idioma del usuario y en la configuración regional del formato numérico. Por ejemplo, la fórmula "=SUM(A1, 1.5)" en inglés se convertiría en "=SUMME(A1; 1,5)" en alemán.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-p105">Represents the formula in A1-style notation, in the user's language and number-formatting locale.  For example, the English "=SUM(A1, 1.5)" formula would become "=SUMME(A1; 1,5)" in German.</span></span>|
|<span data-ttu-id="6a7b3-143">formulasR1C1</span><span class="sxs-lookup"><span data-stu-id="6a7b3-143">formulasR1C1</span></span>|<span data-ttu-id="6a7b3-144">Json</span><span class="sxs-lookup"><span data-stu-id="6a7b3-144">Json</span></span>|<span data-ttu-id="6a7b3-145">Representa la fórmula en notación de estilo R1C1.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-145">Represents the formula in R1C1-style notation.</span></span>|
|<span data-ttu-id="6a7b3-146">numberFormat</span><span class="sxs-lookup"><span data-stu-id="6a7b3-146">numberFormat</span></span>|<span data-ttu-id="6a7b3-147">Json</span><span class="sxs-lookup"><span data-stu-id="6a7b3-147">Json</span></span>|<span data-ttu-id="6a7b3-148">Representa el código de formato numérico de Excel para la celda especificada.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-148">Represents Excel's number format code for the given cell.</span></span>|
|<span data-ttu-id="6a7b3-149">rowHidden</span><span class="sxs-lookup"><span data-stu-id="6a7b3-149">rowHidden</span></span>|<span data-ttu-id="6a7b3-150">boolean</span><span class="sxs-lookup"><span data-stu-id="6a7b3-150">boolean</span></span>|<span data-ttu-id="6a7b3-151">Representa si todas las filas del rango actual están ocultas.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-151">Represents if all rows of the current range are hidden.</span></span>|
|<span data-ttu-id="6a7b3-152">values</span><span class="sxs-lookup"><span data-stu-id="6a7b3-152">values</span></span>|<span data-ttu-id="6a7b3-153">Json</span><span class="sxs-lookup"><span data-stu-id="6a7b3-153">Json</span></span>|<span data-ttu-id="6a7b3-p106">Representa los valores sin formato del intervalo especificado. Los datos devueltos pueden ser de tipo string, number o boolean. La celda que contenga un error devolverá la cadena de error.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-p106">Represents the raw values of the specified range. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.</span></span>|

## <a name="response"></a><span data-ttu-id="6a7b3-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6a7b3-157">Response</span></span>

<span data-ttu-id="6a7b3-158">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Range](../resources/range.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-158">If successful, this method returns a `200 OK` response code and updated [Range](../resources/range.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6a7b3-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6a7b3-159">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6a7b3-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6a7b3-160">Request</span></span>
<span data-ttu-id="6a7b3-p107">Aquí tiene un ejemplo de la solicitud. Actualiza un rango: valores, formato de número y fórmula. La entrada `null` indica a la API que omita la celda para esa entrada en particular. Los valores, el formato de número y las fórmulas se pueden actualizar por separado o conjuntamente en la misma llamada de API.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-p107">Here is an example of the request. It updates a range - values, number-format and formula. The `null` input is to instruct the API to ignore the cell for that particular input. The values, number-format and formulas can be independently updated or combined together in the same API call.</span></span> 

<!-- {
  "blockType": "request",
  "name": "update_range"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{sheet-id}/range(address='A1:B2')
Content-type: application/json
Content-length: 169

{
"values" : [["Hello", "100"],["1/1/2016", null]],
"formula" : [[null, null], [null, "=B1*2"]],
"numberFormat" : [[null,null], ["m-ddd", null]]
}
```
##### <a name="response"></a><span data-ttu-id="6a7b3-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6a7b3-165">Response</span></span>
<span data-ttu-id="6a7b3-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6a7b3-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Update range",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/api/range-update.md/update_range/numberFormat:
      Inconsistent types between parameter (Collection) and table (None)",
    "Warning: /api-reference/v1.0/api/range-update.md/update_range/values:
      Inconsistent types between parameter (Collection) and table (None)",
    "Error: /api-reference/v1.0/api/range-update.md/update_range/numberFormat:
      Type mismatch between example and table. Parameter name: numberFormat; example type (Collection(Collection)) is a collection, while the table description type (microsoft.graph.Json) is not.",
    "Error: /api-reference/v1.0/api/range-update.md/update_range/values:
      Type mismatch between example and table. Parameter name: values; example type (Collection(Collection)) is a collection, while the table description type (microsoft.graph.Json) is not."
  ],
  "tocPath": ""
}-->
