---
title: 'Range: LastCell'
description: .
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 5156554c5e094556415a03a7651fd0ffee1bcf33
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860280"
---
# <a name="range-lastcell"></a><span data-ttu-id="48d24-103">Range: LastCell</span><span class="sxs-lookup"><span data-stu-id="48d24-103">Range: LastCell</span></span>

<span data-ttu-id="48d24-p101">Obtiene la última celda del intervalo. Por ejemplo, la última celda de "B2:D5" es "D5".</span><span class="sxs-lookup"><span data-stu-id="48d24-p101">Gets the last cell within the range. For example, the last cell of "B2:D5" is "D5".</span></span>
## <a name="permissions"></a><span data-ttu-id="48d24-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="48d24-106">Permissions</span></span>
<span data-ttu-id="48d24-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="48d24-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="48d24-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="48d24-109">Permission type</span></span>      | <span data-ttu-id="48d24-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="48d24-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="48d24-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="48d24-111">Delegated (work or school account)</span></span> | <span data-ttu-id="48d24-112">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="48d24-112">Files.ReadWrite</span></span>    |
|<span data-ttu-id="48d24-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="48d24-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="48d24-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="48d24-114">Not supported.</span></span>    |
|<span data-ttu-id="48d24-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="48d24-115">Application</span></span> | <span data-ttu-id="48d24-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="48d24-116">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="48d24-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="48d24-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/lastCell
GET /workbook/worksheets/{id|name}/range(address='<address>')/lastCell
GET /workbook/tables/{id|name}/columns/{id|name}/range/lastCell

```
## <a name="request-headers"></a><span data-ttu-id="48d24-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="48d24-118">Request headers</span></span>
| <span data-ttu-id="48d24-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="48d24-119">Name</span></span>       | <span data-ttu-id="48d24-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="48d24-120">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="48d24-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="48d24-121">Authorization</span></span>  | <span data-ttu-id="48d24-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="48d24-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="48d24-124">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="48d24-124">Workbook-Session-Id</span></span>  | <span data-ttu-id="48d24-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="48d24-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="48d24-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="48d24-127">Request body</span></span>

## <a name="response"></a><span data-ttu-id="48d24-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48d24-128">Response</span></span>

<span data-ttu-id="48d24-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="48d24-129">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="48d24-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="48d24-130">Example</span></span>
<span data-ttu-id="48d24-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="48d24-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="48d24-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48d24-132">Request</span></span>
<span data-ttu-id="48d24-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="48d24-133">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "range_lastcell"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/lastCell
```

##### <a name="response"></a><span data-ttu-id="48d24-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48d24-134">Response</span></span>
<span data-ttu-id="48d24-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="48d24-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: LastCell",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
