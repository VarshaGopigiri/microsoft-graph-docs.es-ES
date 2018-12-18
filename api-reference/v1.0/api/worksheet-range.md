---
title: 'Worksheet: Range'
description: Obtiene el objeto de rango especificado por la dirección o el nombre.
author: lumine2008
ms.openlocfilehash: fec1ea97be1ca2c094af7e32deac0b6a37f4f086
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27319869"
---
# <a name="worksheet-range"></a><span data-ttu-id="a7c1e-103">Worksheet: Range</span><span class="sxs-lookup"><span data-stu-id="a7c1e-103">Worksheet: Range</span></span>

<span data-ttu-id="a7c1e-104">Obtiene el objeto de rango especificado por la dirección o el nombre.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-104">Gets the range object specified by the address or name.</span></span>
## <a name="permissions"></a><span data-ttu-id="a7c1e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="a7c1e-105">Permissions</span></span>
<span data-ttu-id="a7c1e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a7c1e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a7c1e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a7c1e-108">Permission type</span></span>      | <span data-ttu-id="a7c1e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a7c1e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a7c1e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a7c1e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="a7c1e-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a7c1e-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="a7c1e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a7c1e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a7c1e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-113">Not supported.</span></span>    |
|<span data-ttu-id="a7c1e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a7c1e-114">Application</span></span> | <span data-ttu-id="a7c1e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a7c1e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a7c1e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/range

```
## <a name="request-headers"></a><span data-ttu-id="a7c1e-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a7c1e-117">Request headers</span></span>
| <span data-ttu-id="a7c1e-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="a7c1e-118">Name</span></span>       | <span data-ttu-id="a7c1e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7c1e-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="a7c1e-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="a7c1e-120">Authorization</span></span>  | <span data-ttu-id="a7c1e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a7c1e-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="a7c1e-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="a7c1e-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="function-parameters"></a><span data-ttu-id="a7c1e-126">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="a7c1e-126">Function parameters</span></span>

| <span data-ttu-id="a7c1e-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a7c1e-127">Parameter</span></span>    | <span data-ttu-id="a7c1e-128">Type</span><span class="sxs-lookup"><span data-stu-id="a7c1e-128">Type</span></span>   |<span data-ttu-id="a7c1e-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7c1e-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a7c1e-130">address</span><span class="sxs-lookup"><span data-stu-id="a7c1e-130">address</span></span>|<span data-ttu-id="a7c1e-131">string</span><span class="sxs-lookup"><span data-stu-id="a7c1e-131">string</span></span>|<span data-ttu-id="a7c1e-p104">Opcional. Dirección o nombre del intervalo. Si no se especifica, se devuelve todo el intervalo de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-p104">Optional. The address or the name of the range. If not specified, the entire worksheet range is returned.</span></span>|

## <a name="response"></a><span data-ttu-id="a7c1e-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7c1e-135">Response</span></span>

<span data-ttu-id="a7c1e-136">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-136">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a7c1e-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a7c1e-137">Example</span></span>
<span data-ttu-id="a7c1e-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="a7c1e-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a7c1e-139">Request</span></span>
<span data-ttu-id="a7c1e-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheet_range"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/range(address='A1:B2')
```

##### <a name="response"></a><span data-ttu-id="a7c1e-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7c1e-141">Response</span></span>
<span data-ttu-id="a7c1e-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

<span data-ttu-id="a7c1e-145">Si el opcional `address` parámetro no se especifica, esta función devuelve el rango de hoja de cálculo completa.</span><span class="sxs-lookup"><span data-stu-id="a7c1e-145">If the optional `address` parameter is not specified, this function returns the entire worksheet range.</span></span>

##### <a name="request"></a><span data-ttu-id="a7c1e-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a7c1e-146">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "worksheet_range_noaddress"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/range
```

##### <a name="response"></a><span data-ttu-id="a7c1e-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7c1e-147">Response</span></span>

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
  "description": "Worksheet: Range",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->