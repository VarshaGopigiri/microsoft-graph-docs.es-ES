---
title: 'Range: insert'
description: Inserta una celda o un intervalo de celdas en la hoja de cálculo en lugar de este intervalo y desplaza las demás celdas para crear espacio. Devuelve un objeto Range en el espacio que queda en blanco.
ms.openlocfilehash: 242db28474965493ceb8a584e8d9fb01679f13d2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028671"
---
# <a name="range-insert"></a><span data-ttu-id="5d07f-104">Range: insert</span><span class="sxs-lookup"><span data-stu-id="5d07f-104">Range: insert</span></span>

<span data-ttu-id="5d07f-p102">Inserta una celda o un intervalo de celdas en la hoja de cálculo en lugar de este intervalo y desplaza las demás celdas para crear espacio. Devuelve un objeto Range en el espacio que queda en blanco.</span><span class="sxs-lookup"><span data-stu-id="5d07f-p102">Inserts a cell or a range of cells into the worksheet in place of this range, and shifts the other cells to make space. Returns a new Range object at the now blank space.</span></span>
## <a name="permissions"></a><span data-ttu-id="5d07f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5d07f-107">Permissions</span></span>
<span data-ttu-id="5d07f-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5d07f-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5d07f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5d07f-110">Permission type</span></span>      | <span data-ttu-id="5d07f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5d07f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5d07f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5d07f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5d07f-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5d07f-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="5d07f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5d07f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5d07f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d07f-115">Not supported.</span></span>    |
|<span data-ttu-id="5d07f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5d07f-116">Application</span></span> | <span data-ttu-id="5d07f-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d07f-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5d07f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5d07f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/insert
POST /workbook/worksheets/{id|name}/range(address='<address>')/insert
POST /workbook/tables/{id|name}/columns/{id|name}/range/insert

```
## <a name="request-headers"></a><span data-ttu-id="5d07f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5d07f-119">Request headers</span></span>
| <span data-ttu-id="5d07f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="5d07f-120">Name</span></span>       | <span data-ttu-id="5d07f-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d07f-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="5d07f-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="5d07f-122">Authorization</span></span>  | <span data-ttu-id="5d07f-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5d07f-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5d07f-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="5d07f-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="5d07f-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="5d07f-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="5d07f-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5d07f-128">Request body</span></span>
<span data-ttu-id="5d07f-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="5d07f-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="5d07f-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5d07f-130">Parameter</span></span>    | <span data-ttu-id="5d07f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="5d07f-131">Type</span></span>   |<span data-ttu-id="5d07f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d07f-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5d07f-133">Shift</span><span class="sxs-lookup"><span data-stu-id="5d07f-133">shift</span></span>|<span data-ttu-id="5d07f-134">string</span><span class="sxs-lookup"><span data-stu-id="5d07f-134">string</span></span>|<span data-ttu-id="5d07f-135">Especifica el modo de desplazar las celdas.</span><span class="sxs-lookup"><span data-stu-id="5d07f-135">Specifies which way to shift the cells.</span></span>  <span data-ttu-id="5d07f-136">Los valores posibles son: `Down`, `Right`.</span><span class="sxs-lookup"><span data-stu-id="5d07f-136">The possible values are: `Down`, `Right`.</span></span>|

## <a name="response"></a><span data-ttu-id="5d07f-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d07f-137">Response</span></span>

<span data-ttu-id="5d07f-138">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5d07f-138">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5d07f-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5d07f-139">Example</span></span>
<span data-ttu-id="5d07f-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="5d07f-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="5d07f-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5d07f-141">Request</span></span>
<span data-ttu-id="5d07f-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5d07f-142">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="5d07f-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d07f-143">Response</span></span>
<span data-ttu-id="5d07f-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5d07f-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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