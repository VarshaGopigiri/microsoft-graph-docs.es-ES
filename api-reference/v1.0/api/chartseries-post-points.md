---
title: Create ChartPoints
description: Use esta API para crear un objeto ChartPoints.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 0b9d5597bd57bc97f60e6e90101b42401b067635
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27985945"
---
# <a name="create-chartpoints"></a><span data-ttu-id="f1ad4-103">Create ChartPoints</span><span class="sxs-lookup"><span data-stu-id="f1ad4-103">Create ChartPoints</span></span>

<span data-ttu-id="f1ad4-104">Use esta API para crear un objeto ChartPoints.</span><span class="sxs-lookup"><span data-stu-id="f1ad4-104">Use this API to create a new ChartPoints.</span></span>
## <a name="permissions"></a><span data-ttu-id="f1ad4-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f1ad4-105">Permissions</span></span>
<span data-ttu-id="f1ad4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f1ad4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f1ad4-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f1ad4-108">Permission type</span></span>      | <span data-ttu-id="f1ad4-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f1ad4-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f1ad4-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f1ad4-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f1ad4-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f1ad4-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f1ad4-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f1ad4-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f1ad4-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f1ad4-113">Not supported.</span></span>    |
|<span data-ttu-id="f1ad4-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f1ad4-114">Application</span></span> | <span data-ttu-id="f1ad4-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f1ad4-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f1ad4-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f1ad4-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/{name}/series/{series-id}/points

```
## <a name="request-headers"></a><span data-ttu-id="f1ad4-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f1ad4-117">Request headers</span></span>
| <span data-ttu-id="f1ad4-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="f1ad4-118">Name</span></span>       | <span data-ttu-id="f1ad4-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1ad4-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f1ad4-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="f1ad4-120">Authorization</span></span>  | <span data-ttu-id="f1ad4-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f1ad4-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f1ad4-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="f1ad4-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="f1ad4-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="f1ad4-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="f1ad4-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f1ad4-126">Request body</span></span>
<span data-ttu-id="f1ad4-127">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ChartPoints](../resources/chartpoint.md).</span><span class="sxs-lookup"><span data-stu-id="f1ad4-127">In the request body, supply a JSON representation of [ChartPoints](../resources/chartpoint.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="f1ad4-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f1ad4-128">Response</span></span>

<span data-ttu-id="f1ad4-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [ChartPoints](../resources/chartpoint.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1ad4-129">If successful, this method returns `201 Created` response code and [ChartPoints](../resources/chartpoint.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f1ad4-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f1ad4-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f1ad4-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f1ad4-131">Request</span></span>
<span data-ttu-id="f1ad4-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f1ad4-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_chartpoints_from_chartseries"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/series/{series-id}/points
Content-type: application/json
Content-length: 3

{
}
```
<span data-ttu-id="f1ad4-133">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ChartPoints](../resources/chartpoint.md).</span><span class="sxs-lookup"><span data-stu-id="f1ad4-133">In the request body, supply a JSON representation of [ChartPoints](../resources/chartpoint.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="f1ad4-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f1ad4-134">Response</span></span>
<span data-ttu-id="f1ad4-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f1ad4-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartPoint"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 3

{
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create ChartPoints",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
