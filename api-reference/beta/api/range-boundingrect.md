---
title: 'Range: BoundingRect'
description: .
ms.openlocfilehash: 25a313fca1fe73c0717777b4dabc4c9b6eb9372f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083136"
---
# <a name="range-boundingrect"></a><span data-ttu-id="17809-103">Range: BoundingRect</span><span class="sxs-lookup"><span data-stu-id="17809-103">Range: BoundingRect</span></span>

> <span data-ttu-id="17809-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="17809-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="17809-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="17809-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="17809-p102">Obtiene el objeto de intervalo más pequeño que abarca los intervalos especificados. Por ejemplo, el valor GetBoundingRect de "B2:C5" y "D10:E15" es "B2:E16".</span><span class="sxs-lookup"><span data-stu-id="17809-p102">Gets the smallest range object that encompasses the given ranges. For example, the GetBoundingRect of "B2:C5" and "D10:E15" is "B2:E16".</span></span>
## <a name="permissions"></a><span data-ttu-id="17809-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="17809-108">Permissions</span></span>
<span data-ttu-id="17809-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="17809-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="17809-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="17809-111">Permission type</span></span>      | <span data-ttu-id="17809-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="17809-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="17809-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="17809-113">Delegated (work or school account)</span></span> | <span data-ttu-id="17809-114">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="17809-114">Files.ReadWrite</span></span>    |
|<span data-ttu-id="17809-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="17809-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="17809-116">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="17809-116">Files.ReadWrite</span></span>    |
|<span data-ttu-id="17809-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="17809-117">Application</span></span> | <span data-ttu-id="17809-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="17809-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="17809-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="17809-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/BoundingRect
GET /workbook/worksheets/{id|name}/range(address='<address>')/BoundingRect
GET /workbook/tables/{id|name}/columns/{id|name}/range/BoundingRect

```
## <a name="request-headers"></a><span data-ttu-id="17809-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="17809-120">Request headers</span></span>
| <span data-ttu-id="17809-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="17809-121">Name</span></span>       | <span data-ttu-id="17809-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="17809-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="17809-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="17809-123">Authorization</span></span>  | <span data-ttu-id="17809-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="17809-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="17809-126">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="17809-126">Workbook-Session-Id</span></span>  | <span data-ttu-id="17809-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="17809-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="17809-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="17809-129">Request body</span></span>
<span data-ttu-id="17809-130">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="17809-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="17809-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="17809-131">Parameter</span></span>    | <span data-ttu-id="17809-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="17809-132">Type</span></span>   |<span data-ttu-id="17809-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="17809-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="17809-134">anotherRange</span><span class="sxs-lookup"><span data-stu-id="17809-134">anotherRange</span></span>|<span data-ttu-id="17809-135">string</span><span class="sxs-lookup"><span data-stu-id="17809-135">string</span></span>|<span data-ttu-id="17809-136">Objeto o dirección de intervalo o nombre de intervalo.</span><span class="sxs-lookup"><span data-stu-id="17809-136">The range object or address or range name.</span></span>|

## <a name="response"></a><span data-ttu-id="17809-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17809-137">Response</span></span>

<span data-ttu-id="17809-138">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="17809-138">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="17809-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="17809-139">Example</span></span>
<span data-ttu-id="17809-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="17809-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="17809-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="17809-141">Request</span></span>
<span data-ttu-id="17809-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="17809-142">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="17809-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17809-143">Response</span></span>
<span data-ttu-id="17809-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="17809-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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