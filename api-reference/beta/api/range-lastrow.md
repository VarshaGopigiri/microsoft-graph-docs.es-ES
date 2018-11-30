---
title: 'Range: LastRow'
description: .
ms.openlocfilehash: 4e41fa16ebf58ce33f2301861b843d677f3d0fdf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084731"
---
# <a name="range-lastrow"></a><span data-ttu-id="c6cfa-103">Range: LastRow</span><span class="sxs-lookup"><span data-stu-id="c6cfa-103">Range: LastRow</span></span>

> <span data-ttu-id="c6cfa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c6cfa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c6cfa-p102">Obtiene la última fila del intervalo. Por ejemplo, la última fila de "B2:D5" es "B5:D5".</span><span class="sxs-lookup"><span data-stu-id="c6cfa-p102">Gets the last row within the range. For example, the last row of "B2:D5" is "B5:D5".</span></span>
## <a name="permissions"></a><span data-ttu-id="c6cfa-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="c6cfa-108">Permissions</span></span>
<span data-ttu-id="c6cfa-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c6cfa-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c6cfa-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c6cfa-111">Permission type</span></span>      | <span data-ttu-id="c6cfa-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c6cfa-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c6cfa-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c6cfa-113">Delegated (work or school account)</span></span> | <span data-ttu-id="c6cfa-114">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c6cfa-114">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c6cfa-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c6cfa-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c6cfa-116">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c6cfa-116">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c6cfa-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c6cfa-117">Application</span></span> | <span data-ttu-id="c6cfa-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c6cfa-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c6cfa-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/LastRow
GET /workbook/worksheets/{id|name}/range(address='<address>')/LastRow
GET /workbook/tables/{id|name}/columns/{id|name}/range/LastRow

```
## <a name="request-headers"></a><span data-ttu-id="c6cfa-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c6cfa-120">Request headers</span></span>
| <span data-ttu-id="c6cfa-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="c6cfa-121">Name</span></span>       | <span data-ttu-id="c6cfa-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6cfa-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="c6cfa-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="c6cfa-123">Authorization</span></span>  | <span data-ttu-id="c6cfa-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c6cfa-126">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="c6cfa-126">Workbook-Session-Id</span></span>  | <span data-ttu-id="c6cfa-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c6cfa-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c6cfa-129">Request body</span></span>

## <a name="response"></a><span data-ttu-id="c6cfa-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6cfa-130">Response</span></span>

<span data-ttu-id="c6cfa-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-131">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c6cfa-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6cfa-132">Example</span></span>
<span data-ttu-id="c6cfa-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c6cfa-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6cfa-134">Request</span></span>
<span data-ttu-id="c6cfa-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_lastrow"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/LastRow
```

##### <a name="response"></a><span data-ttu-id="c6cfa-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6cfa-136">Response</span></span>
<span data-ttu-id="c6cfa-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: LastRow",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->