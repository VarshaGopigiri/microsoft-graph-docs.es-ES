---
title: 'Worksheet: Range'
description: Obtiene el objeto de rango especificado por la dirección o el nombre.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 3d4241e6aeccd0d400388e03a4ce1254df7d0dc0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27971000"
---
# <a name="worksheet-range"></a><span data-ttu-id="31b0a-103">Worksheet: Range</span><span class="sxs-lookup"><span data-stu-id="31b0a-103">Worksheet: Range</span></span>

> <span data-ttu-id="31b0a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="31b0a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="31b0a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="31b0a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="31b0a-106">Obtiene el objeto de rango especificado por la dirección o el nombre.</span><span class="sxs-lookup"><span data-stu-id="31b0a-106">Gets the range object specified by the address or name.</span></span>
## <a name="permissions"></a><span data-ttu-id="31b0a-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="31b0a-107">Permissions</span></span>
<span data-ttu-id="31b0a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="31b0a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="31b0a-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="31b0a-110">Permission type</span></span>      | <span data-ttu-id="31b0a-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="31b0a-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="31b0a-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="31b0a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="31b0a-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="31b0a-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="31b0a-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="31b0a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="31b0a-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="31b0a-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="31b0a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="31b0a-116">Application</span></span> | <span data-ttu-id="31b0a-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="31b0a-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="31b0a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="31b0a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/Range

```
## <a name="request-headers"></a><span data-ttu-id="31b0a-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="31b0a-119">Request headers</span></span>
| <span data-ttu-id="31b0a-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="31b0a-120">Name</span></span>       | <span data-ttu-id="31b0a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="31b0a-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="31b0a-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="31b0a-122">Authorization</span></span>  | <span data-ttu-id="31b0a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="31b0a-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="31b0a-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="31b0a-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="31b0a-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="31b0a-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="31b0a-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="31b0a-128">Request body</span></span>
<span data-ttu-id="31b0a-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="31b0a-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="31b0a-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="31b0a-130">Parameter</span></span>    | <span data-ttu-id="31b0a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="31b0a-131">Type</span></span>   |<span data-ttu-id="31b0a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="31b0a-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="31b0a-133">address</span><span class="sxs-lookup"><span data-stu-id="31b0a-133">address</span></span>|<span data-ttu-id="31b0a-134">string</span><span class="sxs-lookup"><span data-stu-id="31b0a-134">string</span></span>|<span data-ttu-id="31b0a-p105">Opcional. Dirección o nombre del intervalo. Si no se especifica, se devuelve todo el intervalo de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="31b0a-p105">Optional. The address or the name of the range. If not specified, the entire worksheet range is returned.</span></span>|

## <a name="response"></a><span data-ttu-id="31b0a-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31b0a-138">Response</span></span>

<span data-ttu-id="31b0a-139">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="31b0a-139">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="31b0a-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="31b0a-140">Example</span></span>
<span data-ttu-id="31b0a-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="31b0a-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="31b0a-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="31b0a-142">Request</span></span>
<span data-ttu-id="31b0a-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="31b0a-143">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="31b0a-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31b0a-144">Response</span></span>
<span data-ttu-id="31b0a-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="31b0a-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
