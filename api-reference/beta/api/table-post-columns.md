---
title: Create TableColumn
description: Use esta API para crear un objeto TableColumn.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 8c315cd4de26dd610a99e7df66b67856e17b3fb0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820730"
---
# <a name="create-tablecolumn"></a><span data-ttu-id="a636f-103">Create TableColumn</span><span class="sxs-lookup"><span data-stu-id="a636f-103">Create TableColumn</span></span>

> <span data-ttu-id="a636f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a636f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a636f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a636f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a636f-106">Use esta API para crear un objeto TableColumn.</span><span class="sxs-lookup"><span data-stu-id="a636f-106">Use this API to create a new TableColumn.</span></span>
## <a name="permissions"></a><span data-ttu-id="a636f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a636f-107">Permissions</span></span>
<span data-ttu-id="a636f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a636f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a636f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a636f-110">Permission type</span></span>      | <span data-ttu-id="a636f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a636f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a636f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a636f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="a636f-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a636f-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="a636f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a636f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a636f-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a636f-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="a636f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a636f-116">Application</span></span> | <span data-ttu-id="a636f-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a636f-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a636f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a636f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns

```
## <a name="request-headers"></a><span data-ttu-id="a636f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a636f-119">Request headers</span></span>
| <span data-ttu-id="a636f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="a636f-120">Name</span></span>       | <span data-ttu-id="a636f-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="a636f-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="a636f-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="a636f-122">Authorization</span></span>  | <span data-ttu-id="a636f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a636f-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a636f-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="a636f-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="a636f-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="a636f-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="a636f-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a636f-128">Request body</span></span>
<span data-ttu-id="a636f-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [TableColumn](../resources/tablecolumn.md).</span><span class="sxs-lookup"><span data-stu-id="a636f-129">In the request body, supply a JSON representation of [TableColumn](../resources/tablecolumn.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="a636f-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a636f-130">Response</span></span>

<span data-ttu-id="a636f-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [TableColumn](../resources/tablecolumn.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a636f-131">If successful, this method returns `201 Created` response code and [TableColumn](../resources/tablecolumn.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a636f-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a636f-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a636f-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a636f-133">Request</span></span>
<span data-ttu-id="a636f-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a636f-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_tablecolumn_from_table"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/columns
Content-type: application/json
Content-length: 81

{
  "id": 99,
  "name": "name-value",
  "index": 99,
  "values": "values-value"
}
```
<span data-ttu-id="a636f-135">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [TableColumn](../resources/tablecolumn.md).</span><span class="sxs-lookup"><span data-stu-id="a636f-135">In the request body, supply a JSON representation of [TableColumn](../resources/tablecolumn.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="a636f-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a636f-136">Response</span></span>
<span data-ttu-id="a636f-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a636f-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.tableColumn"
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
