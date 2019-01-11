---
title: 'Table: convertToRange'
description: Convierte la tabla en un rango de celdas normal. Se conservan todos los datos.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 27f4e406f7021c7fa2e61b39b376d61ab8b36784
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866461"
---
# <a name="table-converttorange"></a><span data-ttu-id="9a7a5-104">Table: convertToRange</span><span class="sxs-lookup"><span data-stu-id="9a7a5-104">Table: convertToRange</span></span>

> <span data-ttu-id="9a7a5-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9a7a5-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9a7a5-p103">Convierte la tabla en un rango de celdas normal. Se conservan todos los datos.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-p103">Converts the table into a normal range of cells. All data is preserved.</span></span>
## <a name="permissions"></a><span data-ttu-id="9a7a5-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="9a7a5-109">Permissions</span></span>
<span data-ttu-id="9a7a5-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9a7a5-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9a7a5-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9a7a5-112">Permission type</span></span>      | <span data-ttu-id="9a7a5-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9a7a5-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9a7a5-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9a7a5-114">Delegated (work or school account)</span></span> | <span data-ttu-id="9a7a5-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9a7a5-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="9a7a5-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9a7a5-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9a7a5-117">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9a7a5-117">Files.ReadWrite</span></span>    |
|<span data-ttu-id="9a7a5-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9a7a5-118">Application</span></span> | <span data-ttu-id="9a7a5-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9a7a5-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9a7a5-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/convertToRange
POST /workbook/worksheets/{id|name}/tables/{id|name}/convertToRange

```
## <a name="request-headers"></a><span data-ttu-id="9a7a5-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9a7a5-121">Request headers</span></span>
| <span data-ttu-id="9a7a5-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="9a7a5-122">Name</span></span>       | <span data-ttu-id="9a7a5-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a7a5-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9a7a5-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="9a7a5-124">Authorization</span></span>  | <span data-ttu-id="9a7a5-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9a7a5-127">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="9a7a5-127">Workbook-Session-Id</span></span>  | <span data-ttu-id="9a7a5-p106">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-p106">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="9a7a5-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9a7a5-130">Request body</span></span>

## <a name="response"></a><span data-ttu-id="9a7a5-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a7a5-131">Response</span></span>

<span data-ttu-id="9a7a5-132">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-132">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9a7a5-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9a7a5-133">Example</span></span>
<span data-ttu-id="9a7a5-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-134">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="9a7a5-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9a7a5-135">Request</span></span>
<span data-ttu-id="9a7a5-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "table_converttorange"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/convertToRange
```

##### <a name="response"></a><span data-ttu-id="9a7a5-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a7a5-137">Response</span></span>
<span data-ttu-id="9a7a5-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9a7a5-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Table: convertToRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
