---
title: 'Table: HeaderRowRange'
description: Obtiene el objeto de rango asociado a la fila de encabezado de la tabla.
ms.openlocfilehash: 99f94847cb82a78a885aebb0ec3035dfdc50fbce
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028806"
---
# <a name="table-headerrowrange"></a><span data-ttu-id="9cd67-103">Table: HeaderRowRange</span><span class="sxs-lookup"><span data-stu-id="9cd67-103">Table: HeaderRowRange</span></span>

<span data-ttu-id="9cd67-104">Obtiene el objeto de rango asociado a la fila de encabezado de la tabla.</span><span class="sxs-lookup"><span data-stu-id="9cd67-104">Gets the range object associated with header row of the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="9cd67-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="9cd67-105">Permissions</span></span>
<span data-ttu-id="9cd67-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9cd67-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9cd67-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9cd67-108">Permission type</span></span>      | <span data-ttu-id="9cd67-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9cd67-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9cd67-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9cd67-110">Delegated (work or school account)</span></span> | <span data-ttu-id="9cd67-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9cd67-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="9cd67-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9cd67-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9cd67-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9cd67-113">Not supported.</span></span>    |
|<span data-ttu-id="9cd67-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9cd67-114">Application</span></span> | <span data-ttu-id="9cd67-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9cd67-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9cd67-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9cd67-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/headerRowRange
POST /workbook/worksheets/{id|name}/tables/{id|name}/headerRowRange

```
## <a name="request-headers"></a><span data-ttu-id="9cd67-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9cd67-117">Request headers</span></span>
| <span data-ttu-id="9cd67-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="9cd67-118">Name</span></span>       | <span data-ttu-id="9cd67-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="9cd67-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9cd67-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="9cd67-120">Authorization</span></span>  | <span data-ttu-id="9cd67-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9cd67-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9cd67-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="9cd67-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="9cd67-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="9cd67-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="9cd67-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9cd67-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="9cd67-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9cd67-127">Response</span></span>

<span data-ttu-id="9cd67-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9cd67-128">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9cd67-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9cd67-129">Example</span></span>
<span data-ttu-id="9cd67-130">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9cd67-130">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="9cd67-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9cd67-131">Request</span></span>
<span data-ttu-id="9cd67-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9cd67-132">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "table_headerrowrange",
  "idempotent": true
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/headerRowRange
```

##### <a name="response"></a><span data-ttu-id="9cd67-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9cd67-133">Response</span></span>
<span data-ttu-id="9cd67-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9cd67-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Table: HeaderRowRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->