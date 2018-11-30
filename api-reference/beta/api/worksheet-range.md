---
title: 'Worksheet: Range'
description: Obtiene el objeto de rango especificado por la dirección o el nombre.
ms.openlocfilehash: defe05f953d5fe7cd5fafda6ae16f04bb9f91e86
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087744"
---
# <a name="worksheet-range"></a><span data-ttu-id="c0efc-103">Worksheet: Range</span><span class="sxs-lookup"><span data-stu-id="c0efc-103">Worksheet: Range</span></span>

> <span data-ttu-id="c0efc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c0efc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c0efc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c0efc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c0efc-106">Obtiene el objeto de rango especificado por la dirección o el nombre.</span><span class="sxs-lookup"><span data-stu-id="c0efc-106">Gets the range object specified by the address or name.</span></span>
## <a name="permissions"></a><span data-ttu-id="c0efc-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c0efc-107">Permissions</span></span>
<span data-ttu-id="c0efc-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c0efc-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c0efc-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c0efc-110">Permission type</span></span>      | <span data-ttu-id="c0efc-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c0efc-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c0efc-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c0efc-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c0efc-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c0efc-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c0efc-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c0efc-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c0efc-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c0efc-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c0efc-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c0efc-116">Application</span></span> | <span data-ttu-id="c0efc-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c0efc-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c0efc-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c0efc-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/Range

```
## <a name="request-headers"></a><span data-ttu-id="c0efc-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c0efc-119">Request headers</span></span>
| <span data-ttu-id="c0efc-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c0efc-120">Name</span></span>       | <span data-ttu-id="c0efc-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0efc-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="c0efc-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c0efc-122">Authorization</span></span>  | <span data-ttu-id="c0efc-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c0efc-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c0efc-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="c0efc-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="c0efc-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="c0efc-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c0efc-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c0efc-128">Request body</span></span>
<span data-ttu-id="c0efc-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="c0efc-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c0efc-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c0efc-130">Parameter</span></span>    | <span data-ttu-id="c0efc-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c0efc-131">Type</span></span>   |<span data-ttu-id="c0efc-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0efc-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c0efc-133">address</span><span class="sxs-lookup"><span data-stu-id="c0efc-133">address</span></span>|<span data-ttu-id="c0efc-134">string</span><span class="sxs-lookup"><span data-stu-id="c0efc-134">string</span></span>|<span data-ttu-id="c0efc-p105">Opcional. Dirección o nombre del intervalo. Si no se especifica, se devuelve todo el intervalo de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="c0efc-p105">Optional. The address or the name of the range. If not specified, the entire worksheet range is returned.</span></span>|

## <a name="response"></a><span data-ttu-id="c0efc-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0efc-138">Response</span></span>

<span data-ttu-id="c0efc-139">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0efc-139">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c0efc-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0efc-140">Example</span></span>
<span data-ttu-id="c0efc-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c0efc-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c0efc-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c0efc-142">Request</span></span>
<span data-ttu-id="c0efc-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c0efc-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheet_range"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/Range
Content-type: application/json
Content-length: 32

{
  "address": "address-value"
}
```

##### <a name="response"></a><span data-ttu-id="c0efc-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0efc-144">Response</span></span>
<span data-ttu-id="c0efc-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c0efc-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Worksheet: Range",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->