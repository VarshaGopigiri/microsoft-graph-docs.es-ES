---
title: 'ChartCollection: ItemAt'
description: Obtiene un gráfico en función de su posición en la colección.
author: lumine2008
ms.openlocfilehash: 0c32068abe2ccbea0a093d2a973bfd6dbf05e938
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27341695"
---
# <a name="chartcollection-itemat"></a><span data-ttu-id="437a9-103">ChartCollection: ItemAt</span><span class="sxs-lookup"><span data-stu-id="437a9-103">ChartCollection: ItemAt</span></span>

<span data-ttu-id="437a9-104">Obtiene un gráfico en función de su posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="437a9-104">Gets a chart based on its position in the collection.</span></span>
## <a name="permissions"></a><span data-ttu-id="437a9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="437a9-105">Permissions</span></span>
<span data-ttu-id="437a9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="437a9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="437a9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="437a9-108">Permission type</span></span>      | <span data-ttu-id="437a9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="437a9-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="437a9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="437a9-110">Delegated (work or school account)</span></span> | <span data-ttu-id="437a9-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="437a9-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="437a9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="437a9-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="437a9-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="437a9-113">Not supported.</span></span>    |
|<span data-ttu-id="437a9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="437a9-114">Application</span></span> | <span data-ttu-id="437a9-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="437a9-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="437a9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="437a9-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/itemAt

```
## <a name="request-headers"></a><span data-ttu-id="437a9-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="437a9-117">Request headers</span></span>
| <span data-ttu-id="437a9-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="437a9-118">Name</span></span>       | <span data-ttu-id="437a9-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="437a9-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="437a9-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="437a9-120">Authorization</span></span>  | <span data-ttu-id="437a9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="437a9-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="437a9-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="437a9-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="437a9-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="437a9-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="437a9-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="437a9-126">Request body</span></span>
<span data-ttu-id="437a9-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="437a9-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="437a9-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="437a9-128">Parameter</span></span>    | <span data-ttu-id="437a9-129">Type</span><span class="sxs-lookup"><span data-stu-id="437a9-129">Type</span></span>   |<span data-ttu-id="437a9-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="437a9-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="437a9-131">index</span><span class="sxs-lookup"><span data-stu-id="437a9-131">index</span></span>|<span data-ttu-id="437a9-132">Int32</span><span class="sxs-lookup"><span data-stu-id="437a9-132">Int32</span></span>|<span data-ttu-id="437a9-p104">Valor de índice del objeto que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="437a9-p104">Index value of the object to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="437a9-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="437a9-135">Response</span></span>

<span data-ttu-id="437a9-136">Si tiene éxito, este método devuelve `200 OK` código de respuesta y [WorkbookChart](../resources/chart.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="437a9-136">If successful, this method returns `200 OK` response code and [WorkbookChart](../resources/chart.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="437a9-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="437a9-137">Example</span></span>
<span data-ttu-id="437a9-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="437a9-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="437a9-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="437a9-139">Request</span></span>
<span data-ttu-id="437a9-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="437a9-140">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "chartcollection_itemat",
  "idempotent": true,
  "@type": "requestBodyResourceFor.chartcollection_itemat"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/itemAt
Content-type: application/json
Content-length: 20

{
  "index": 8
}
```

##### <a name="response"></a><span data-ttu-id="437a9-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="437a9-141">Response</span></span>
<span data-ttu-id="437a9-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="437a9-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChart"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 52

{
  "id": "id-value",
  "height": 99,
  "left": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartCollection: ItemAt",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->