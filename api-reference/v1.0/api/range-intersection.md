---
title: 'Range: Intersection'
description: Obtiene el objeto de rango que representa la intersección rectangular de los rangos especificados.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 7f954e377ff051f9063fc210d795b5b6d87981bc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820352"
---
# <a name="range-intersection"></a><span data-ttu-id="99b1e-103">Range: Intersection</span><span class="sxs-lookup"><span data-stu-id="99b1e-103">Range: Intersection</span></span>

<span data-ttu-id="99b1e-104">Obtiene el objeto de rango que representa la intersección rectangular de los rangos especificados.</span><span class="sxs-lookup"><span data-stu-id="99b1e-104">Gets the range object that represents the rectangular intersection of the given ranges.</span></span>
## <a name="permissions"></a><span data-ttu-id="99b1e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="99b1e-105">Permissions</span></span>
<span data-ttu-id="99b1e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="99b1e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="99b1e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="99b1e-108">Permission type</span></span>      | <span data-ttu-id="99b1e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="99b1e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="99b1e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="99b1e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="99b1e-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="99b1e-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="99b1e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="99b1e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="99b1e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="99b1e-113">Not supported.</span></span>    |
|<span data-ttu-id="99b1e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="99b1e-114">Application</span></span> | <span data-ttu-id="99b1e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="99b1e-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="99b1e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="99b1e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/intersection
GET /workbook/worksheets/{id|name}/range(address='<address>')/intersection
GET /workbook/tables/{id|name}/columns/{id|name}/range/intersection

```
## <a name="request-headers"></a><span data-ttu-id="99b1e-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="99b1e-117">Request headers</span></span>
| <span data-ttu-id="99b1e-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="99b1e-118">Name</span></span>       | <span data-ttu-id="99b1e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="99b1e-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="99b1e-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="99b1e-120">Authorization</span></span>  | <span data-ttu-id="99b1e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="99b1e-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="99b1e-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="99b1e-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="99b1e-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="99b1e-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="99b1e-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="99b1e-126">Request body</span></span>
<span data-ttu-id="99b1e-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="99b1e-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="99b1e-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="99b1e-128">Parameter</span></span>    | <span data-ttu-id="99b1e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="99b1e-129">Type</span></span>   |<span data-ttu-id="99b1e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="99b1e-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="99b1e-131">anotherRange</span><span class="sxs-lookup"><span data-stu-id="99b1e-131">anotherRange</span></span>|<span data-ttu-id="99b1e-132">string</span><span class="sxs-lookup"><span data-stu-id="99b1e-132">string</span></span>|<span data-ttu-id="99b1e-133">Objeto de intervalo o dirección de intervalo que se usará para determinar la intersección de los intervalos.</span><span class="sxs-lookup"><span data-stu-id="99b1e-133">The range object or range address that will be used to determine the intersection of ranges.</span></span>|

## <a name="response"></a><span data-ttu-id="99b1e-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99b1e-134">Response</span></span>

<span data-ttu-id="99b1e-135">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="99b1e-135">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="99b1e-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="99b1e-136">Example</span></span>
<span data-ttu-id="99b1e-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="99b1e-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="99b1e-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="99b1e-138">Request</span></span>
<span data-ttu-id="99b1e-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="99b1e-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "isComposable": true,
  "name": "range_intersection"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/intersection
Content-type: application/json
Content-length: 42

{
  "anotherRange": "anotherRange-value"
}
```

##### <a name="response"></a><span data-ttu-id="99b1e-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99b1e-140">Response</span></span>
<span data-ttu-id="99b1e-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="99b1e-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRange"
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
  "description": "Range: Intersection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
