---
title: 'Table: convertToRange'
description: Convierte la tabla en un rango de celdas normal. Se conservan todos los datos.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 4528daab7cfde480e93d75cdcb5f9a969f583144
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825378"
---
# <a name="table-converttorange"></a><span data-ttu-id="225e8-104">Table: convertToRange</span><span class="sxs-lookup"><span data-stu-id="225e8-104">Table: convertToRange</span></span>

<span data-ttu-id="225e8-p102">Convierte la tabla en un rango de celdas normal. Se conservan todos los datos.</span><span class="sxs-lookup"><span data-stu-id="225e8-p102">Converts the table into a normal range of cells. All data is preserved.</span></span>
## <a name="permissions"></a><span data-ttu-id="225e8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="225e8-107">Permissions</span></span>
<span data-ttu-id="225e8-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="225e8-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="225e8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="225e8-110">Permission type</span></span>      | <span data-ttu-id="225e8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="225e8-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="225e8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="225e8-112">Delegated (work or school account)</span></span> | <span data-ttu-id="225e8-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="225e8-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="225e8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="225e8-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="225e8-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="225e8-115">Not supported.</span></span>    |
|<span data-ttu-id="225e8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="225e8-116">Application</span></span> | <span data-ttu-id="225e8-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="225e8-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="225e8-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="225e8-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/convertToRange
POST /workbook/worksheets/{id|name}/tables/{id|name}/convertToRange

```
## <a name="request-headers"></a><span data-ttu-id="225e8-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="225e8-119">Request headers</span></span>
| <span data-ttu-id="225e8-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="225e8-120">Name</span></span>       | <span data-ttu-id="225e8-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="225e8-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="225e8-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="225e8-122">Authorization</span></span>  | <span data-ttu-id="225e8-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="225e8-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="225e8-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="225e8-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="225e8-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="225e8-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="225e8-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="225e8-128">Request body</span></span>

## <a name="response"></a><span data-ttu-id="225e8-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="225e8-129">Response</span></span>

<span data-ttu-id="225e8-130">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="225e8-130">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="225e8-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="225e8-131">Example</span></span>
<span data-ttu-id="225e8-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="225e8-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="225e8-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="225e8-133">Request</span></span>
<span data-ttu-id="225e8-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="225e8-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "table_converttorange"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/convertToRange
```

##### <a name="response"></a><span data-ttu-id="225e8-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="225e8-135">Response</span></span>
<span data-ttu-id="225e8-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="225e8-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Table: convertToRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
