---
title: 'TableColumn: Range'
description: Obtiene el objeto de rango asociado a toda la columna.
ms.openlocfilehash: 29f387366b4b8711cabc237a9548ea14dc27efd9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031929"
---
# <a name="tablecolumn-range"></a><span data-ttu-id="8a44e-103">TableColumn: Range</span><span class="sxs-lookup"><span data-stu-id="8a44e-103">TableColumn: Range</span></span>

<span data-ttu-id="8a44e-104">Obtiene el objeto de rango asociado a toda la columna.</span><span class="sxs-lookup"><span data-stu-id="8a44e-104">Gets the range object associated with the entire column.</span></span>
## <a name="permissions"></a><span data-ttu-id="8a44e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="8a44e-105">Permissions</span></span>
<span data-ttu-id="8a44e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8a44e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8a44e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8a44e-108">Permission type</span></span>      | <span data-ttu-id="8a44e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8a44e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8a44e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8a44e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="8a44e-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8a44e-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="8a44e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8a44e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8a44e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8a44e-113">Not supported.</span></span>    |
|<span data-ttu-id="8a44e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8a44e-114">Application</span></span> | <span data-ttu-id="8a44e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8a44e-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="8a44e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8a44e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/{id|name}/range
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/{id|name}/range

```
## <a name="request-headers"></a><span data-ttu-id="8a44e-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8a44e-117">Request headers</span></span>
| <span data-ttu-id="8a44e-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="8a44e-118">Name</span></span>       | <span data-ttu-id="8a44e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a44e-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="8a44e-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="8a44e-120">Authorization</span></span>  | <span data-ttu-id="8a44e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8a44e-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="8a44e-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="8a44e-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="8a44e-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="8a44e-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="8a44e-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8a44e-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="8a44e-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a44e-127">Response</span></span>

<span data-ttu-id="8a44e-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a44e-128">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8a44e-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a44e-129">Example</span></span>
<span data-ttu-id="8a44e-130">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="8a44e-130">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="8a44e-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8a44e-131">Request</span></span>
<span data-ttu-id="8a44e-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8a44e-132">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "tablecolumn_range",
  "idempotent": true
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}/range
```

##### <a name="response"></a><span data-ttu-id="8a44e-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a44e-133">Response</span></span>
<span data-ttu-id="8a44e-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8a44e-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "TableColumn: Range",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->