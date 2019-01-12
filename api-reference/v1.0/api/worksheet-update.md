---
title: Update worksheet
description: Actualizar las propiedades del objeto worksheet.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 651900f00e842640b292deef7569efde1701939b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27915553"
---
# <a name="update-worksheet"></a><span data-ttu-id="38885-103">Update worksheet</span><span class="sxs-lookup"><span data-stu-id="38885-103">Update worksheet</span></span>

<span data-ttu-id="38885-104">Actualizar las propiedades del objeto worksheet.</span><span class="sxs-lookup"><span data-stu-id="38885-104">Update the properties of worksheet object.</span></span>
## <a name="permissions"></a><span data-ttu-id="38885-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="38885-105">Permissions</span></span>
<span data-ttu-id="38885-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="38885-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="38885-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="38885-108">Permission type</span></span>      | <span data-ttu-id="38885-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="38885-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="38885-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="38885-110">Delegated (work or school account)</span></span> | <span data-ttu-id="38885-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="38885-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="38885-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="38885-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="38885-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38885-113">Not supported.</span></span>    |
|<span data-ttu-id="38885-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="38885-114">Application</span></span> | <span data-ttu-id="38885-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38885-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="38885-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="38885-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}
```
## <a name="optional-request-headers"></a><span data-ttu-id="38885-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="38885-117">Optional request headers</span></span>
| <span data-ttu-id="38885-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="38885-118">Name</span></span>       | <span data-ttu-id="38885-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="38885-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="38885-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="38885-120">Authorization</span></span>  | <span data-ttu-id="38885-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="38885-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="38885-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="38885-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="38885-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="38885-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="38885-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="38885-126">Request body</span></span>
<span data-ttu-id="38885-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="38885-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="38885-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="38885-130">Property</span></span>     | <span data-ttu-id="38885-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="38885-131">Type</span></span>   |<span data-ttu-id="38885-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="38885-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="38885-133">name</span><span class="sxs-lookup"><span data-stu-id="38885-133">name</span></span>|<span data-ttu-id="38885-134">string</span><span class="sxs-lookup"><span data-stu-id="38885-134">string</span></span>|<span data-ttu-id="38885-135">Nombre para mostrar de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="38885-135">The display name of the worksheet.</span></span>|
|<span data-ttu-id="38885-136">position</span><span class="sxs-lookup"><span data-stu-id="38885-136">position</span></span>|<span data-ttu-id="38885-137">entero</span><span class="sxs-lookup"><span data-stu-id="38885-137">int</span></span>|<span data-ttu-id="38885-138">Posición de base cero de la hoja de cálculo dentro del libro.</span><span class="sxs-lookup"><span data-stu-id="38885-138">The zero-based position of the worksheet within the workbook.</span></span>|
|<span data-ttu-id="38885-139">visibility</span><span class="sxs-lookup"><span data-stu-id="38885-139">visibility</span></span>|<span data-ttu-id="38885-140">string</span><span class="sxs-lookup"><span data-stu-id="38885-140">string</span></span>|<span data-ttu-id="38885-141">La visibilidad de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="38885-141">The Visibility of the worksheet.</span></span> <span data-ttu-id="38885-142">Los valores posibles son: `Visible`, `Hidden`, `VeryHidden`.</span><span class="sxs-lookup"><span data-stu-id="38885-142">The possible values are: `Visible`, `Hidden`, `VeryHidden`.</span></span>|

## <a name="response"></a><span data-ttu-id="38885-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38885-143">Response</span></span>

<span data-ttu-id="38885-144">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookWorksheet](../resources/worksheet.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38885-144">If successful, this method returns a `200 OK` response code and updated [WorkbookWorksheet](../resources/worksheet.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="38885-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38885-145">Example</span></span>
##### <a name="request"></a><span data-ttu-id="38885-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="38885-146">Request</span></span>
<span data-ttu-id="38885-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="38885-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_worksheet"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}
Content-type: application/json
Content-length: 100

{
  "position": 99,
  "name": "name-value",
  "visibility": "visibility-value"
}
```
##### <a name="response"></a><span data-ttu-id="38885-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38885-148">Response</span></span>
<span data-ttu-id="38885-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="38885-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookWorksheet"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 100

{
  "id": "id-value",
  "position": 99,
  "name": "name-value",
  "visibility": "visibility-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update worksheet",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
