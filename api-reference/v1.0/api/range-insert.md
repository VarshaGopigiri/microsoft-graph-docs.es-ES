---
title: 'Range: insert'
description: Inserta una celda o un intervalo de celdas en la hoja de cálculo en lugar de este intervalo y desplaza las demás celdas para crear espacio. Devuelve un objeto Range en el espacio que queda en blanco.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: aa59abfd2b60454a73472fc5283d3c7212ee48ef
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27929049"
---
# <a name="range-insert"></a><span data-ttu-id="c09df-104">Range: insert</span><span class="sxs-lookup"><span data-stu-id="c09df-104">Range: insert</span></span>

<span data-ttu-id="c09df-p102">Inserta una celda o un intervalo de celdas en la hoja de cálculo en lugar de este intervalo y desplaza las demás celdas para crear espacio. Devuelve un objeto Range en el espacio que queda en blanco.</span><span class="sxs-lookup"><span data-stu-id="c09df-p102">Inserts a cell or a range of cells into the worksheet in place of this range, and shifts the other cells to make space. Returns a new Range object at the now blank space.</span></span>
## <a name="permissions"></a><span data-ttu-id="c09df-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c09df-107">Permissions</span></span>
<span data-ttu-id="c09df-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c09df-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c09df-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c09df-110">Permission type</span></span>      | <span data-ttu-id="c09df-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c09df-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c09df-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c09df-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c09df-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c09df-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c09df-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c09df-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c09df-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c09df-115">Not supported.</span></span>    |
|<span data-ttu-id="c09df-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c09df-116">Application</span></span> | <span data-ttu-id="c09df-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c09df-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c09df-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c09df-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/insert
POST /workbook/worksheets/{id|name}/range(address='<address>')/insert
POST /workbook/tables/{id|name}/columns/{id|name}/range/insert

```
## <a name="request-headers"></a><span data-ttu-id="c09df-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c09df-119">Request headers</span></span>
| <span data-ttu-id="c09df-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c09df-120">Name</span></span>       | <span data-ttu-id="c09df-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c09df-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="c09df-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c09df-122">Authorization</span></span>  | <span data-ttu-id="c09df-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c09df-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c09df-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="c09df-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="c09df-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="c09df-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c09df-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c09df-128">Request body</span></span>
<span data-ttu-id="c09df-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="c09df-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c09df-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c09df-130">Parameter</span></span>    | <span data-ttu-id="c09df-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c09df-131">Type</span></span>   |<span data-ttu-id="c09df-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c09df-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c09df-133">Shift</span><span class="sxs-lookup"><span data-stu-id="c09df-133">shift</span></span>|<span data-ttu-id="c09df-134">string</span><span class="sxs-lookup"><span data-stu-id="c09df-134">string</span></span>|<span data-ttu-id="c09df-135">Especifica el modo de desplazar las celdas.</span><span class="sxs-lookup"><span data-stu-id="c09df-135">Specifies which way to shift the cells.</span></span>  <span data-ttu-id="c09df-136">Los valores posibles son: `Down`, `Right`.</span><span class="sxs-lookup"><span data-stu-id="c09df-136">The possible values are: `Down`, `Right`.</span></span>|

## <a name="response"></a><span data-ttu-id="c09df-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c09df-137">Response</span></span>

<span data-ttu-id="c09df-138">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c09df-138">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c09df-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c09df-139">Example</span></span>
<span data-ttu-id="c09df-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c09df-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c09df-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c09df-141">Request</span></span>
<span data-ttu-id="c09df-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c09df-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_insert"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/insert
Content-type: application/json
Content-length: 28

{
  "shift": "shift-value"
}
```

##### <a name="response"></a><span data-ttu-id="c09df-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c09df-143">Response</span></span>
<span data-ttu-id="c09df-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c09df-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: insert",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
