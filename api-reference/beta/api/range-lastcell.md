---
title: 'Range: LastCell'
description: .
author: lumine2008
ms.openlocfilehash: 90087ab5e5000b096092e664abe19b7e384e310b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27310125"
---
# <a name="range-lastcell"></a><span data-ttu-id="c8c23-103">Range: LastCell</span><span class="sxs-lookup"><span data-stu-id="c8c23-103">Range: LastCell</span></span>

> <span data-ttu-id="c8c23-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c8c23-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c8c23-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c8c23-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c8c23-p102">Obtiene la última celda del intervalo. Por ejemplo, la última celda de "B2:D5" es "D5".</span><span class="sxs-lookup"><span data-stu-id="c8c23-p102">Gets the last cell within the range. For example, the last cell of "B2:D5" is "D5".</span></span>
## <a name="permissions"></a><span data-ttu-id="c8c23-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="c8c23-108">Permissions</span></span>
<span data-ttu-id="c8c23-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c8c23-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c8c23-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c8c23-111">Permission type</span></span>      | <span data-ttu-id="c8c23-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c8c23-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c8c23-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c8c23-113">Delegated (work or school account)</span></span> | <span data-ttu-id="c8c23-114">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c8c23-114">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c8c23-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c8c23-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c8c23-116">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c8c23-116">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c8c23-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c8c23-117">Application</span></span> | <span data-ttu-id="c8c23-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c8c23-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c8c23-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c8c23-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/LastCell
GET /workbook/worksheets/{id|name}/range(address='<address>')/LastCell
GET /workbook/tables/{id|name}/columns/{id|name}/range/LastCell

```
## <a name="request-headers"></a><span data-ttu-id="c8c23-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c8c23-120">Request headers</span></span>
| <span data-ttu-id="c8c23-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="c8c23-121">Name</span></span>       | <span data-ttu-id="c8c23-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8c23-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="c8c23-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="c8c23-123">Authorization</span></span>  | <span data-ttu-id="c8c23-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c8c23-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c8c23-126">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="c8c23-126">Workbook-Session-Id</span></span>  | <span data-ttu-id="c8c23-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="c8c23-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c8c23-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c8c23-129">Request body</span></span>

## <a name="response"></a><span data-ttu-id="c8c23-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c8c23-130">Response</span></span>

<span data-ttu-id="c8c23-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c8c23-131">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c8c23-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c8c23-132">Example</span></span>
<span data-ttu-id="c8c23-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c8c23-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c8c23-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c8c23-134">Request</span></span>
<span data-ttu-id="c8c23-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c8c23-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_lastcell"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/LastCell
```

##### <a name="response"></a><span data-ttu-id="c8c23-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c8c23-136">Response</span></span>
<span data-ttu-id="c8c23-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c8c23-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
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