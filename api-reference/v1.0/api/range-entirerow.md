---
title: 'Range: EntireRow'
description: Obtiene un objeto que representa toda la fila del rango.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 4e07b3da46d30e3163c62b182d55d9f3fea3a9df
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27928034"
---
# <a name="range-entirerow"></a><span data-ttu-id="11eef-103">Range: EntireRow</span><span class="sxs-lookup"><span data-stu-id="11eef-103">Range: EntireRow</span></span>

<span data-ttu-id="11eef-104">Obtiene un objeto que representa toda la fila del rango.</span><span class="sxs-lookup"><span data-stu-id="11eef-104">Gets an object that represents the entire row of the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="11eef-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="11eef-105">Permissions</span></span>
<span data-ttu-id="11eef-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="11eef-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="11eef-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="11eef-108">Permission type</span></span>      | <span data-ttu-id="11eef-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="11eef-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="11eef-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="11eef-110">Delegated (work or school account)</span></span> | <span data-ttu-id="11eef-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="11eef-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="11eef-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="11eef-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="11eef-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="11eef-113">Not supported.</span></span>    |
|<span data-ttu-id="11eef-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="11eef-114">Application</span></span> | <span data-ttu-id="11eef-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="11eef-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="11eef-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="11eef-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/entireRow
GET /workbook/worksheets/{id|name}/range(address='<address>'/entireRow
GET /workbook/tables/{id|name}/columns/{id|name}/range/entireRow

```
## <a name="request-headers"></a><span data-ttu-id="11eef-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="11eef-117">Request headers</span></span>
| <span data-ttu-id="11eef-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="11eef-118">Name</span></span>       | <span data-ttu-id="11eef-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="11eef-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="11eef-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="11eef-120">Authorization</span></span>  | <span data-ttu-id="11eef-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="11eef-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="11eef-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="11eef-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="11eef-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="11eef-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="11eef-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="11eef-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="11eef-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11eef-127">Response</span></span>

<span data-ttu-id="11eef-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="11eef-128">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="11eef-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11eef-129">Example</span></span>
<span data-ttu-id="11eef-130">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="11eef-130">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="11eef-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="11eef-131">Request</span></span>
<span data-ttu-id="11eef-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="11eef-132">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "range_entirerow"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/entireRow
```

##### <a name="response"></a><span data-ttu-id="11eef-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="11eef-133">Response</span></span>
<span data-ttu-id="11eef-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="11eef-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: EntireRow",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
