---
title: 'Range: Intersection'
description: Obtiene el objeto de rango que representa la intersección rectangular de los rangos especificados.
author: lumine2008
ms.openlocfilehash: 0ba9767c3c7d30ee5746b5a6723fd8103c1b8533
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344558"
---
# <a name="range-intersection"></a><span data-ttu-id="e780c-103">Range: Intersection</span><span class="sxs-lookup"><span data-stu-id="e780c-103">Range: Intersection</span></span>

> <span data-ttu-id="e780c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e780c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e780c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e780c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e780c-106">Obtiene el objeto de rango que representa la intersección rectangular de los rangos especificados.</span><span class="sxs-lookup"><span data-stu-id="e780c-106">Gets the range object that represents the rectangular intersection of the given ranges.</span></span>
## <a name="permissions"></a><span data-ttu-id="e780c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e780c-107">Permissions</span></span>
<span data-ttu-id="e780c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e780c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e780c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e780c-110">Permission type</span></span>      | <span data-ttu-id="e780c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e780c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e780c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e780c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e780c-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e780c-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="e780c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e780c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e780c-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e780c-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="e780c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e780c-116">Application</span></span> | <span data-ttu-id="e780c-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e780c-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e780c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e780c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/Intersection
GET /workbook/worksheets/{id|name}/range(address='<address>')/Intersection
GET /workbook/tables/{id|name}/columns/{id|name}/range/Intersection

```
## <a name="request-headers"></a><span data-ttu-id="e780c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e780c-119">Request headers</span></span>
| <span data-ttu-id="e780c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="e780c-120">Name</span></span>       | <span data-ttu-id="e780c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e780c-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e780c-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="e780c-122">Authorization</span></span>  | <span data-ttu-id="e780c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e780c-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e780c-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="e780c-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="e780c-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="e780c-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="e780c-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e780c-128">Request body</span></span>
<span data-ttu-id="e780c-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="e780c-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="e780c-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e780c-130">Parameter</span></span>    | <span data-ttu-id="e780c-131">Type</span><span class="sxs-lookup"><span data-stu-id="e780c-131">Type</span></span>   |<span data-ttu-id="e780c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e780c-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e780c-133">anotherRange</span><span class="sxs-lookup"><span data-stu-id="e780c-133">anotherRange</span></span>|<span data-ttu-id="e780c-134">string</span><span class="sxs-lookup"><span data-stu-id="e780c-134">string</span></span>|<span data-ttu-id="e780c-135">Objeto de intervalo o dirección de intervalo que se usará para determinar la intersección de los intervalos.</span><span class="sxs-lookup"><span data-stu-id="e780c-135">The range object or range address that will be used to determine the intersection of ranges.</span></span>|

## <a name="response"></a><span data-ttu-id="e780c-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e780c-136">Response</span></span>

<span data-ttu-id="e780c-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e780c-137">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e780c-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e780c-138">Example</span></span>
<span data-ttu-id="e780c-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="e780c-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="e780c-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e780c-140">Request</span></span>
<span data-ttu-id="e780c-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e780c-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_intersection"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/Intersection
Content-type: application/json
Content-length: 42

{
  "anotherRange": "anotherRange-value"
}
```

##### <a name="response"></a><span data-ttu-id="e780c-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e780c-142">Response</span></span>
<span data-ttu-id="e780c-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e780c-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: Intersection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->