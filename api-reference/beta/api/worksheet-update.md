---
title: Update worksheet
description: Actualizar las propiedades del objeto worksheet.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: e2139e1e350ab4c0f416e48181398011666274b8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27942034"
---
# <a name="update-worksheet"></a><span data-ttu-id="199b1-103">Update worksheet</span><span class="sxs-lookup"><span data-stu-id="199b1-103">Update worksheet</span></span>

> <span data-ttu-id="199b1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="199b1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="199b1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="199b1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="199b1-106">Actualizar las propiedades del objeto worksheet.</span><span class="sxs-lookup"><span data-stu-id="199b1-106">Update the properties of worksheet object.</span></span>
## <a name="permissions"></a><span data-ttu-id="199b1-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="199b1-107">Permissions</span></span>
<span data-ttu-id="199b1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="199b1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="199b1-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="199b1-110">Permission type</span></span>      | <span data-ttu-id="199b1-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="199b1-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="199b1-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="199b1-112">Delegated (work or school account)</span></span> | <span data-ttu-id="199b1-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="199b1-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="199b1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="199b1-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="199b1-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="199b1-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="199b1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="199b1-116">Application</span></span> | <span data-ttu-id="199b1-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="199b1-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="199b1-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="199b1-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}
```
## <a name="optional-request-headers"></a><span data-ttu-id="199b1-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="199b1-119">Optional request headers</span></span>
| <span data-ttu-id="199b1-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="199b1-120">Name</span></span>       | <span data-ttu-id="199b1-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="199b1-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="199b1-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="199b1-122">Authorization</span></span>  | <span data-ttu-id="199b1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="199b1-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="199b1-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="199b1-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="199b1-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="199b1-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="199b1-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="199b1-128">Request body</span></span>
<span data-ttu-id="199b1-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="199b1-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="199b1-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="199b1-132">Property</span></span>     | <span data-ttu-id="199b1-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="199b1-133">Type</span></span>   |<span data-ttu-id="199b1-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="199b1-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="199b1-135">name</span><span class="sxs-lookup"><span data-stu-id="199b1-135">name</span></span>|<span data-ttu-id="199b1-136">string</span><span class="sxs-lookup"><span data-stu-id="199b1-136">string</span></span>|<span data-ttu-id="199b1-137">Nombre para mostrar de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="199b1-137">The display name of the worksheet.</span></span>|
|<span data-ttu-id="199b1-138">position</span><span class="sxs-lookup"><span data-stu-id="199b1-138">position</span></span>|<span data-ttu-id="199b1-139">entero</span><span class="sxs-lookup"><span data-stu-id="199b1-139">int</span></span>|<span data-ttu-id="199b1-140">Posición de base cero de la hoja de cálculo dentro del libro.</span><span class="sxs-lookup"><span data-stu-id="199b1-140">The zero-based position of the worksheet within the workbook.</span></span>|
|<span data-ttu-id="199b1-141">visibility</span><span class="sxs-lookup"><span data-stu-id="199b1-141">visibility</span></span>|<span data-ttu-id="199b1-142">string</span><span class="sxs-lookup"><span data-stu-id="199b1-142">string</span></span>|<span data-ttu-id="199b1-p106">Visibilidad de la hoja de cálculo. Valores posibles: `Visible`, `Hidden`, `VeryHidden`.</span><span class="sxs-lookup"><span data-stu-id="199b1-p106">The Visibility of the worksheet. Possible values are: `Visible`, `Hidden`, `VeryHidden`.</span></span>|

## <a name="response"></a><span data-ttu-id="199b1-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="199b1-145">Response</span></span>

<span data-ttu-id="199b1-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [Worksheet](../resources/worksheet.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="199b1-146">If successful, this method returns a `200 OK` response code and updated [Worksheet](../resources/worksheet.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="199b1-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="199b1-147">Example</span></span>
##### <a name="request"></a><span data-ttu-id="199b1-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="199b1-148">Request</span></span>
<span data-ttu-id="199b1-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="199b1-149">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_worksheet"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}
Content-type: application/json
Content-length: 100

{
  "position": 99,
  "name": "name-value",
  "visibility": "visibility-value"
}
```
##### <a name="response"></a><span data-ttu-id="199b1-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="199b1-150">Response</span></span>
<span data-ttu-id="199b1-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="199b1-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.worksheet"
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
