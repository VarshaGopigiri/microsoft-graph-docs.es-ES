---
title: Create TableColumn
description: Use esta API para crear un objeto TableColumn.
ms.openlocfilehash: 44a3bc0c3f33af7ffdca3c35778b6aafb5fd626b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029012"
---
# <a name="create-tablecolumn"></a><span data-ttu-id="94b39-103">Create TableColumn</span><span class="sxs-lookup"><span data-stu-id="94b39-103">Create TableColumn</span></span>

<span data-ttu-id="94b39-104">Use esta API para crear un objeto TableColumn.</span><span class="sxs-lookup"><span data-stu-id="94b39-104">Use this API to create a new TableColumn.</span></span>
## <a name="permissions"></a><span data-ttu-id="94b39-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="94b39-105">Permissions</span></span>
<span data-ttu-id="94b39-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="94b39-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="94b39-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="94b39-108">Permission type</span></span>      | <span data-ttu-id="94b39-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="94b39-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="94b39-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="94b39-110">Delegated (work or school account)</span></span> | <span data-ttu-id="94b39-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="94b39-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="94b39-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="94b39-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="94b39-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="94b39-113">Not supported.</span></span>    |
|<span data-ttu-id="94b39-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="94b39-114">Application</span></span> | <span data-ttu-id="94b39-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="94b39-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="94b39-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="94b39-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns

```
## <a name="request-headers"></a><span data-ttu-id="94b39-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="94b39-117">Request headers</span></span>
| <span data-ttu-id="94b39-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="94b39-118">Name</span></span>       | <span data-ttu-id="94b39-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="94b39-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="94b39-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="94b39-120">Authorization</span></span>  | <span data-ttu-id="94b39-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="94b39-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="94b39-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="94b39-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="94b39-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="94b39-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="94b39-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="94b39-126">Request body</span></span>
<span data-ttu-id="94b39-127">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [WorkbookTableColumn](../resources/tablecolumn.md) .</span><span class="sxs-lookup"><span data-stu-id="94b39-127">In the request body, supply a JSON representation of [WorkbookTableColumn](../resources/tablecolumn.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="94b39-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="94b39-128">Response</span></span>

<span data-ttu-id="94b39-129">Si tiene éxito, este método devuelve `201 Created` código de respuesta y [WorkbookTableColumn](../resources/tablecolumn.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="94b39-129">If successful, this method returns `201 Created` response code and [WorkbookTableColumn](../resources/tablecolumn.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="94b39-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="94b39-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="94b39-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="94b39-131">Request</span></span>
<span data-ttu-id="94b39-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="94b39-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_tablecolumn_from_table"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns
Content-type: application/json
Content-length: 81

{
  "id": 99,
  "name": "name-value",
  "index": 99,
  "values": "values-value"
}
```
<span data-ttu-id="94b39-133">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [WorkbookTableColumn](../resources/tablecolumn.md) .</span><span class="sxs-lookup"><span data-stu-id="94b39-133">In the request body, supply a JSON representation of [WorkbookTableColumn](../resources/tablecolumn.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="94b39-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="94b39-134">Response</span></span>
<span data-ttu-id="94b39-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="94b39-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTableColumn"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 81

{
  "id": 99,
  "name": "name-value",
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create TableColumn",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->