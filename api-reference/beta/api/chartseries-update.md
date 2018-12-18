---
title: Actualizar chartseries
description: Actualizar las propiedades del objeto chartserie.
author: lumine2008
ms.openlocfilehash: 69e6de2e6d332a63f4ea7b1cc23ca48032cbbaba
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358957"
---
# <a name="update-chartseries"></a><span data-ttu-id="34140-103">Actualizar chartseries</span><span class="sxs-lookup"><span data-stu-id="34140-103">Update chartseries</span></span>

> <span data-ttu-id="34140-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="34140-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="34140-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="34140-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="34140-106">Actualizar las propiedades del objeto chartserie.</span><span class="sxs-lookup"><span data-stu-id="34140-106">Update the properties of chartseries object.</span></span>
## <a name="permissions"></a><span data-ttu-id="34140-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="34140-107">Permissions</span></span>
<span data-ttu-id="34140-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="34140-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="34140-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="34140-110">Permission type</span></span>      | <span data-ttu-id="34140-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="34140-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="34140-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="34140-112">Delegated (work or school account)</span></span> | <span data-ttu-id="34140-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34140-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="34140-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="34140-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="34140-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34140-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="34140-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="34140-116">Application</span></span> | <span data-ttu-id="34140-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="34140-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="34140-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="34140-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)
```
## <a name="optional-request-headers"></a><span data-ttu-id="34140-119">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="34140-119">Optional request headers</span></span>
| <span data-ttu-id="34140-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="34140-120">Name</span></span>       | <span data-ttu-id="34140-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="34140-121">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="34140-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="34140-122">Authorization</span></span>  | <span data-ttu-id="34140-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="34140-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="34140-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="34140-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="34140-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="34140-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="34140-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="34140-128">Request body</span></span>
<span data-ttu-id="34140-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="34140-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="34140-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="34140-132">Property</span></span>     | <span data-ttu-id="34140-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="34140-133">Type</span></span>   |<span data-ttu-id="34140-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="34140-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="34140-135">name</span><span class="sxs-lookup"><span data-stu-id="34140-135">name</span></span>|<span data-ttu-id="34140-136">string</span><span class="sxs-lookup"><span data-stu-id="34140-136">string</span></span>|<span data-ttu-id="34140-137">Representa el nombre de una serie de un gráfico.</span><span class="sxs-lookup"><span data-stu-id="34140-137">Represents the name of a series in a chart.</span></span>|

## <a name="response"></a><span data-ttu-id="34140-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34140-138">Response</span></span>

<span data-ttu-id="34140-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [ChartSeries](../resources/chartseries.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="34140-139">If successful, this method returns a `200 OK` response code and updated [ChartSeries](../resources/chartseries.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="34140-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="34140-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="34140-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="34140-141">Request</span></span>
<span data-ttu-id="34140-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="34140-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_chartseries"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/series(<undefined>)
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```
##### <a name="response"></a><span data-ttu-id="34140-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34140-143">Response</span></span>
<span data-ttu-id="34140-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="34140-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chartSeries"
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