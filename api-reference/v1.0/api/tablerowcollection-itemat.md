---
title: 'TableRowCollection: ItemAt'
description: Obtiene una fila en función de su posición en la colección.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 402f096473b6fbffac7e5653e0d2be1f01897c75
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27974878"
---
# <a name="tablerowcollection-itemat"></a><span data-ttu-id="aa26c-103">TableRowCollection: ItemAt</span><span class="sxs-lookup"><span data-stu-id="aa26c-103">TableRowCollection: ItemAt</span></span>

<span data-ttu-id="aa26c-104">Obtiene una fila en función de su posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="aa26c-104">Gets a row based on its position in the collection.</span></span>
## <a name="permissions"></a><span data-ttu-id="aa26c-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="aa26c-105">Permissions</span></span>
<span data-ttu-id="aa26c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="aa26c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="aa26c-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="aa26c-108">Permission type</span></span>      | <span data-ttu-id="aa26c-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="aa26c-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="aa26c-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="aa26c-110">Delegated (work or school account)</span></span> | <span data-ttu-id="aa26c-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="aa26c-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="aa26c-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="aa26c-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="aa26c-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aa26c-113">Not supported.</span></span>    |
|<span data-ttu-id="aa26c-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="aa26c-114">Application</span></span> | <span data-ttu-id="aa26c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aa26c-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="aa26c-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aa26c-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/rows/itemAt
POST /workbook/worksheets/{id|name}/tables/{id|name}/rows/itemAt

```
## <a name="request-headers"></a><span data-ttu-id="aa26c-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="aa26c-117">Request headers</span></span>
| <span data-ttu-id="aa26c-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="aa26c-118">Name</span></span>       | <span data-ttu-id="aa26c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa26c-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="aa26c-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="aa26c-120">Authorization</span></span>  | <span data-ttu-id="aa26c-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aa26c-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="aa26c-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="aa26c-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="aa26c-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="aa26c-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="aa26c-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aa26c-126">Request body</span></span>
<span data-ttu-id="aa26c-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="aa26c-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="aa26c-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="aa26c-128">Parameter</span></span>    | <span data-ttu-id="aa26c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa26c-129">Type</span></span>   |<span data-ttu-id="aa26c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa26c-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="aa26c-131">index</span><span class="sxs-lookup"><span data-stu-id="aa26c-131">index</span></span>|<span data-ttu-id="aa26c-132">Int32</span><span class="sxs-lookup"><span data-stu-id="aa26c-132">Int32</span></span>|<span data-ttu-id="aa26c-p104">Valor de índice del objeto que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="aa26c-p104">Index value of the object to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="aa26c-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa26c-135">Response</span></span>

<span data-ttu-id="aa26c-136">Si tiene éxito, este método devuelve `200 OK` código de respuesta y [WorkbookTableRow](../resources/tablerow.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aa26c-136">If successful, this method returns `200 OK` response code and [WorkbookTableRow](../resources/tablerow.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="aa26c-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa26c-137">Example</span></span>
<span data-ttu-id="aa26c-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="aa26c-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="aa26c-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aa26c-139">Request</span></span>
<span data-ttu-id="aa26c-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aa26c-140">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "tablerowcollection_itemat",
  "idempotent": true,
  "@type": "requestBodyResourceFor.tablerowcollection_itemat"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/rows/itemAt
Content-type: application/json
Content-length: 20

{
  "index": 4
}
```

##### <a name="response"></a><span data-ttu-id="aa26c-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa26c-141">Response</span></span>
<span data-ttu-id="aa26c-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aa26c-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTableRow"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 45

{
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableRowCollection: ItemAt",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
