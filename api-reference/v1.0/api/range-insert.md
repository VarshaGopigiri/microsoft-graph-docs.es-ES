---
title: 'Range: insert'
description: Inserta una celda o un intervalo de celdas en la hoja de cálculo en lugar de este intervalo y desplaza las demás celdas para crear espacio. Devuelve un objeto Range en el espacio que queda en blanco.
localization_priority: Normal
ms.openlocfilehash: 78cd2d4018a96428b7e5336d00ca20bada4abd36
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27804875"
---
# <a name="range-insert"></a><span data-ttu-id="15794-104">Range: insert</span><span class="sxs-lookup"><span data-stu-id="15794-104">Range: insert</span></span>

<span data-ttu-id="15794-p102">Inserta una celda o un intervalo de celdas en la hoja de cálculo en lugar de este intervalo y desplaza las demás celdas para crear espacio. Devuelve un objeto Range en el espacio que queda en blanco.</span><span class="sxs-lookup"><span data-stu-id="15794-p102">Inserts a cell or a range of cells into the worksheet in place of this range, and shifts the other cells to make space. Returns a new Range object at the now blank space.</span></span>
## <a name="permissions"></a><span data-ttu-id="15794-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="15794-107">Permissions</span></span>
<span data-ttu-id="15794-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="15794-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="15794-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="15794-110">Permission type</span></span>      | <span data-ttu-id="15794-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="15794-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="15794-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="15794-112">Delegated (work or school account)</span></span> | <span data-ttu-id="15794-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="15794-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="15794-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="15794-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="15794-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="15794-115">Not supported.</span></span>    |
|<span data-ttu-id="15794-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="15794-116">Application</span></span> | <span data-ttu-id="15794-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="15794-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="15794-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="15794-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/insert
POST /workbook/worksheets/{id|name}/range(address='<address>')/insert
POST /workbook/tables/{id|name}/columns/{id|name}/range/insert

```
## <a name="request-headers"></a><span data-ttu-id="15794-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="15794-119">Request headers</span></span>
| <span data-ttu-id="15794-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="15794-120">Name</span></span>       | <span data-ttu-id="15794-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="15794-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="15794-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="15794-122">Authorization</span></span>  | <span data-ttu-id="15794-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="15794-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="15794-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="15794-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="15794-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="15794-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="15794-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="15794-128">Request body</span></span>
<span data-ttu-id="15794-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="15794-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="15794-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="15794-130">Parameter</span></span>    | <span data-ttu-id="15794-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="15794-131">Type</span></span>   |<span data-ttu-id="15794-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="15794-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="15794-133">Shift</span><span class="sxs-lookup"><span data-stu-id="15794-133">shift</span></span>|<span data-ttu-id="15794-134">string</span><span class="sxs-lookup"><span data-stu-id="15794-134">string</span></span>|<span data-ttu-id="15794-135">Especifica el modo de desplazar las celdas.</span><span class="sxs-lookup"><span data-stu-id="15794-135">Specifies which way to shift the cells.</span></span>  <span data-ttu-id="15794-136">Los valores posibles son: `Down`, `Right`.</span><span class="sxs-lookup"><span data-stu-id="15794-136">The possible values are: `Down`, `Right`.</span></span>|

## <a name="response"></a><span data-ttu-id="15794-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15794-137">Response</span></span>

<span data-ttu-id="15794-138">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15794-138">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="15794-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="15794-139">Example</span></span>
<span data-ttu-id="15794-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="15794-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="15794-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="15794-141">Request</span></span>
<span data-ttu-id="15794-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="15794-142">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="15794-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15794-143">Response</span></span>
<span data-ttu-id="15794-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="15794-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
