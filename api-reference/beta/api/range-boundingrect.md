---
title: 'Range: BoundingRect'
description: .
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 54a8fea095909d199f2cd2b74e2512f6c2f05a6f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876618"
---
# <a name="range-boundingrect"></a><span data-ttu-id="4c8f4-103">Range: BoundingRect</span><span class="sxs-lookup"><span data-stu-id="4c8f4-103">Range: BoundingRect</span></span>

> <span data-ttu-id="4c8f4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4c8f4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4c8f4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4c8f4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4c8f4-p102">Obtiene el objeto de intervalo más pequeño que abarca los intervalos especificados. Por ejemplo, el valor GetBoundingRect de "B2:C5" y "D10:E15" es "B2:E16".</span><span class="sxs-lookup"><span data-stu-id="4c8f4-p102">Gets the smallest range object that encompasses the given ranges. For example, the GetBoundingRect of "B2:C5" and "D10:E15" is "B2:E16".</span></span>
## <a name="permissions"></a><span data-ttu-id="4c8f4-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="4c8f4-108">Permissions</span></span>
<span data-ttu-id="4c8f4-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4c8f4-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4c8f4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4c8f4-111">Permission type</span></span>      | <span data-ttu-id="4c8f4-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4c8f4-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4c8f4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4c8f4-113">Delegated (work or school account)</span></span> | <span data-ttu-id="4c8f4-114">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4c8f4-114">Files.ReadWrite</span></span>    |
|<span data-ttu-id="4c8f4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4c8f4-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4c8f4-116">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4c8f4-116">Files.ReadWrite</span></span>    |
|<span data-ttu-id="4c8f4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4c8f4-117">Application</span></span> | <span data-ttu-id="4c8f4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4c8f4-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4c8f4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4c8f4-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/BoundingRect
GET /workbook/worksheets/{id|name}/range(address='<address>')/BoundingRect
GET /workbook/tables/{id|name}/columns/{id|name}/range/BoundingRect

```
## <a name="request-headers"></a><span data-ttu-id="4c8f4-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4c8f4-120">Request headers</span></span>
| <span data-ttu-id="4c8f4-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="4c8f4-121">Name</span></span>       | <span data-ttu-id="4c8f4-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c8f4-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="4c8f4-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="4c8f4-123">Authorization</span></span>  | <span data-ttu-id="4c8f4-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4c8f4-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4c8f4-126">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="4c8f4-126">Workbook-Session-Id</span></span>  | <span data-ttu-id="4c8f4-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="4c8f4-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="4c8f4-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4c8f4-129">Request body</span></span>
<span data-ttu-id="4c8f4-130">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="4c8f4-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="4c8f4-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4c8f4-131">Parameter</span></span>    | <span data-ttu-id="4c8f4-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c8f4-132">Type</span></span>   |<span data-ttu-id="4c8f4-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c8f4-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4c8f4-134">anotherRange</span><span class="sxs-lookup"><span data-stu-id="4c8f4-134">anotherRange</span></span>|<span data-ttu-id="4c8f4-135">string</span><span class="sxs-lookup"><span data-stu-id="4c8f4-135">string</span></span>|<span data-ttu-id="4c8f4-136">Objeto o dirección de intervalo o nombre de intervalo.</span><span class="sxs-lookup"><span data-stu-id="4c8f4-136">The range object or address or range name.</span></span>|

## <a name="response"></a><span data-ttu-id="4c8f4-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4c8f4-137">Response</span></span>

<span data-ttu-id="4c8f4-138">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4c8f4-138">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4c8f4-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4c8f4-139">Example</span></span>
<span data-ttu-id="4c8f4-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="4c8f4-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="4c8f4-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4c8f4-141">Request</span></span>
<span data-ttu-id="4c8f4-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4c8f4-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_boundingrect"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/BoundingRect
Content-type: application/json
Content-length: 42

{
  "anotherRange": "anotherRange-value"
}
```

##### <a name="response"></a><span data-ttu-id="4c8f4-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4c8f4-143">Response</span></span>
<span data-ttu-id="4c8f4-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4c8f4-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: BoundingRect",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
