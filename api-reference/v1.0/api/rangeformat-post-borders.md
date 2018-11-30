---
title: Create RangeBorder
description: Use esta API para crear un objeto RangeBorder.
ms.openlocfilehash: 22a0e85a0e4e2ca6ad0a4fb2bdf503a01c892452
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029466"
---
# <a name="create-rangeborder"></a><span data-ttu-id="e0688-103">Create RangeBorder</span><span class="sxs-lookup"><span data-stu-id="e0688-103">Create RangeBorder</span></span>

<span data-ttu-id="e0688-104">Use esta API para crear un objeto RangeBorder.</span><span class="sxs-lookup"><span data-stu-id="e0688-104">Use this API to create a new RangeBorder.</span></span>
## <a name="permissions"></a><span data-ttu-id="e0688-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="e0688-105">Permissions</span></span>
<span data-ttu-id="e0688-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e0688-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e0688-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e0688-108">Permission type</span></span>      | <span data-ttu-id="e0688-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e0688-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e0688-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e0688-110">Delegated (work or school account)</span></span> | <span data-ttu-id="e0688-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e0688-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="e0688-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e0688-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e0688-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e0688-113">Not supported.</span></span>    |
|<span data-ttu-id="e0688-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e0688-114">Application</span></span> | <span data-ttu-id="e0688-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e0688-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e0688-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e0688-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/format/borders
POST /workbook/worksheets/{id|name}/range(address='<address>')/format/borders
POST /workbook/tables/{id|name}/columns/{id|name}/range/format/borders

```
## <a name="request-headers"></a><span data-ttu-id="e0688-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e0688-117">Request headers</span></span>
| <span data-ttu-id="e0688-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="e0688-118">Name</span></span>       | <span data-ttu-id="e0688-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0688-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e0688-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="e0688-120">Authorization</span></span>  | <span data-ttu-id="e0688-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e0688-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e0688-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="e0688-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="e0688-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="e0688-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="e0688-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e0688-126">Request body</span></span>
<span data-ttu-id="e0688-127">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [WorkbookRangeBorder](../resources/rangeborder.md) .</span><span class="sxs-lookup"><span data-stu-id="e0688-127">In the request body, supply a JSON representation of [WorkbookRangeBorder](../resources/rangeborder.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="e0688-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e0688-128">Response</span></span>

<span data-ttu-id="e0688-129">Si tiene éxito, este método devuelve `201 Created` código de respuesta y [WorkbookRangeBorder](../resources/rangeborder.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e0688-129">If successful, this method returns `201 Created` response code and [WorkbookRangeBorder](../resources/rangeborder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e0688-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e0688-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e0688-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e0688-131">Request</span></span>
<span data-ttu-id="e0688-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0688-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_rangeborder_from_rangeformat"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/format/borders
Content-type: application/json
Content-length: 136

{
  "id": "id-value",
  "color": "color-value",
  "style": "style-value",
  "sideIndex": "sideIndex-value",
  "weight": "weight-value"
}
```
<span data-ttu-id="e0688-133">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [WorkbookRangeBorder](../resources/rangeborder.md) .</span><span class="sxs-lookup"><span data-stu-id="e0688-133">In the request body, supply a JSON representation of [WorkbookRangeBorder](../resources/rangeborder.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="e0688-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e0688-134">Response</span></span>
<span data-ttu-id="e0688-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e0688-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeBorder"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 136

{
  "id": "id-value",
  "color": "color-value",
  "style": "style-value",
  "sideIndex": "sideIndex-value",
  "weight": "weight-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create RangeBorder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->