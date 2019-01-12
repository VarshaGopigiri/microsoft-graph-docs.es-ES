---
title: Actualizar chartseries
description: Actualizar las propiedades del objeto chartserie.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 5c0d2e802b082be1578cbe4a56185681fd06156b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932199"
---
# <a name="update-chartseries"></a><span data-ttu-id="4a137-103">Actualizar chartseries</span><span class="sxs-lookup"><span data-stu-id="4a137-103">Update chartseries</span></span>

<span data-ttu-id="4a137-104">Actualizar las propiedades del objeto chartserie.</span><span class="sxs-lookup"><span data-stu-id="4a137-104">Update the properties of chartseries object.</span></span>
## <a name="permissions"></a><span data-ttu-id="4a137-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="4a137-105">Permissions</span></span>
<span data-ttu-id="4a137-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4a137-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4a137-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4a137-108">Permission type</span></span>      | <span data-ttu-id="4a137-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4a137-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4a137-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4a137-110">Delegated (work or school account)</span></span> | <span data-ttu-id="4a137-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4a137-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="4a137-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4a137-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4a137-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4a137-113">Not supported.</span></span>    |
|<span data-ttu-id="4a137-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4a137-114">Application</span></span> | <span data-ttu-id="4a137-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4a137-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4a137-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4a137-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts/{name}/series/{series-id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="4a137-117">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="4a137-117">Optional request headers</span></span>
| <span data-ttu-id="4a137-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="4a137-118">Name</span></span>       | <span data-ttu-id="4a137-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a137-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="4a137-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="4a137-120">Authorization</span></span>  | <span data-ttu-id="4a137-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4a137-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4a137-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="4a137-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="4a137-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="4a137-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="4a137-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4a137-126">Request body</span></span>
<span data-ttu-id="4a137-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="4a137-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="4a137-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4a137-130">Property</span></span>     | <span data-ttu-id="4a137-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a137-131">Type</span></span>   |<span data-ttu-id="4a137-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a137-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4a137-133">name</span><span class="sxs-lookup"><span data-stu-id="4a137-133">name</span></span>|<span data-ttu-id="4a137-134">string</span><span class="sxs-lookup"><span data-stu-id="4a137-134">string</span></span>|<span data-ttu-id="4a137-135">Representa el nombre de una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="4a137-135">Represents the name of a series in a chart.</span></span>|

## <a name="response"></a><span data-ttu-id="4a137-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a137-136">Response</span></span>

<span data-ttu-id="4a137-137">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y el objeto [WorkbookChartSeries](../resources/chartseries.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a137-137">If successful, this method returns a `200 OK` response code and updated [WorkbookChartSeries](../resources/chartseries.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4a137-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4a137-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4a137-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4a137-139">Request</span></span>
<span data-ttu-id="4a137-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4a137-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartseries"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/series/{series-id}
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```
##### <a name="response"></a><span data-ttu-id="4a137-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a137-141">Response</span></span>
<span data-ttu-id="4a137-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4a137-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookChartSeries"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartseries",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
