---
title: 'Range: Intersection'
description: Obtiene el objeto de rango que representa la intersección rectangular de los rangos especificados.
author: lumine2008
ms.openlocfilehash: e35bf93a07930b34e984df4a84d5ed30b907ea15
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309691"
---
# <a name="range-intersection"></a><span data-ttu-id="5bd34-103">Range: Intersection</span><span class="sxs-lookup"><span data-stu-id="5bd34-103">Range: Intersection</span></span>

<span data-ttu-id="5bd34-104">Obtiene el objeto de rango que representa la intersección rectangular de los rangos especificados.</span><span class="sxs-lookup"><span data-stu-id="5bd34-104">Gets the range object that represents the rectangular intersection of the given ranges.</span></span>
## <a name="permissions"></a><span data-ttu-id="5bd34-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="5bd34-105">Permissions</span></span>
<span data-ttu-id="5bd34-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5bd34-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5bd34-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5bd34-108">Permission type</span></span>      | <span data-ttu-id="5bd34-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5bd34-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5bd34-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5bd34-110">Delegated (work or school account)</span></span> | <span data-ttu-id="5bd34-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5bd34-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="5bd34-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5bd34-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5bd34-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5bd34-113">Not supported.</span></span>    |
|<span data-ttu-id="5bd34-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5bd34-114">Application</span></span> | <span data-ttu-id="5bd34-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5bd34-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5bd34-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5bd34-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/intersection
GET /workbook/worksheets/{id|name}/range(address='<address>')/intersection
GET /workbook/tables/{id|name}/columns/{id|name}/range/intersection

```
## <a name="request-headers"></a><span data-ttu-id="5bd34-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5bd34-117">Request headers</span></span>
| <span data-ttu-id="5bd34-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="5bd34-118">Name</span></span>       | <span data-ttu-id="5bd34-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="5bd34-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="5bd34-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="5bd34-120">Authorization</span></span>  | <span data-ttu-id="5bd34-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5bd34-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5bd34-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="5bd34-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="5bd34-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="5bd34-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="5bd34-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5bd34-126">Request body</span></span>
<span data-ttu-id="5bd34-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="5bd34-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="5bd34-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5bd34-128">Parameter</span></span>    | <span data-ttu-id="5bd34-129">Type</span><span class="sxs-lookup"><span data-stu-id="5bd34-129">Type</span></span>   |<span data-ttu-id="5bd34-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="5bd34-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5bd34-131">anotherRange</span><span class="sxs-lookup"><span data-stu-id="5bd34-131">anotherRange</span></span>|<span data-ttu-id="5bd34-132">string</span><span class="sxs-lookup"><span data-stu-id="5bd34-132">string</span></span>|<span data-ttu-id="5bd34-133">Objeto de intervalo o dirección de intervalo que se usará para determinar la intersección de los intervalos.</span><span class="sxs-lookup"><span data-stu-id="5bd34-133">The range object or range address that will be used to determine the intersection of ranges.</span></span>|

## <a name="response"></a><span data-ttu-id="5bd34-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5bd34-134">Response</span></span>

<span data-ttu-id="5bd34-135">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5bd34-135">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5bd34-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5bd34-136">Example</span></span>
<span data-ttu-id="5bd34-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="5bd34-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="5bd34-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5bd34-138">Request</span></span>
<span data-ttu-id="5bd34-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5bd34-139">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="5bd34-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5bd34-140">Response</span></span>
<span data-ttu-id="5bd34-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5bd34-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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