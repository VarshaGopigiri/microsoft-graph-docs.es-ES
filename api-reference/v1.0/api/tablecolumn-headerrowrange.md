---
title: 'TableColumn: HeaderRowRange'
description: Obtiene el objeto de rango asociado a la fila de encabezado de la columna.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: e3fdd98598189ee8d0e4d685176dd3ef494d888d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27986407"
---
# <a name="tablecolumn-headerrowrange"></a><span data-ttu-id="cfe78-103">TableColumn: HeaderRowRange</span><span class="sxs-lookup"><span data-stu-id="cfe78-103">TableColumn: HeaderRowRange</span></span>

<span data-ttu-id="cfe78-104">Obtiene el objeto de rango asociado a la fila de encabezado de la columna.</span><span class="sxs-lookup"><span data-stu-id="cfe78-104">Gets the range object associated with the header row of the column.</span></span>
## <a name="permissions"></a><span data-ttu-id="cfe78-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="cfe78-105">Permissions</span></span>
<span data-ttu-id="cfe78-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cfe78-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cfe78-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cfe78-108">Permission type</span></span>      | <span data-ttu-id="cfe78-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cfe78-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cfe78-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cfe78-110">Delegated (work or school account)</span></span> | <span data-ttu-id="cfe78-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cfe78-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="cfe78-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cfe78-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cfe78-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cfe78-113">Not supported.</span></span>    |
|<span data-ttu-id="cfe78-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cfe78-114">Application</span></span> | <span data-ttu-id="cfe78-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cfe78-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="cfe78-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cfe78-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/{id|name}/headerRowRange
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/{id|name}/headerRowRange

```
## <a name="request-headers"></a><span data-ttu-id="cfe78-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cfe78-117">Request headers</span></span>
| <span data-ttu-id="cfe78-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="cfe78-118">Name</span></span>       | <span data-ttu-id="cfe78-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="cfe78-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="cfe78-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="cfe78-120">Authorization</span></span>  | <span data-ttu-id="cfe78-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cfe78-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="cfe78-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="cfe78-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="cfe78-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="cfe78-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="cfe78-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cfe78-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="cfe78-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cfe78-127">Response</span></span>

<span data-ttu-id="cfe78-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cfe78-128">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cfe78-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cfe78-129">Example</span></span>
<span data-ttu-id="cfe78-130">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="cfe78-130">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="cfe78-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cfe78-131">Request</span></span>
<span data-ttu-id="cfe78-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cfe78-132">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "tablecolumn_headerrowrange",
  "idempotent": true
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}/headerRowRange
```

##### <a name="response"></a><span data-ttu-id="cfe78-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cfe78-133">Response</span></span>
<span data-ttu-id="cfe78-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cfe78-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "TableColumn: HeaderRowRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
