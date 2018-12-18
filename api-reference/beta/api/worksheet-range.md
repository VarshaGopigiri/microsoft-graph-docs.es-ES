---
title: 'Worksheet: Range'
description: Obtiene el objeto de rango especificado por la dirección o el nombre.
author: lumine2008
ms.openlocfilehash: 449851fca7d6f5f57193bf456f7358b76e68e3b0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308277"
---
# <a name="worksheet-range"></a><span data-ttu-id="28680-103">Worksheet: Range</span><span class="sxs-lookup"><span data-stu-id="28680-103">Worksheet: Range</span></span>

> <span data-ttu-id="28680-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="28680-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="28680-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="28680-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="28680-106">Obtiene el objeto de rango especificado por la dirección o el nombre.</span><span class="sxs-lookup"><span data-stu-id="28680-106">Gets the range object specified by the address or name.</span></span>
## <a name="permissions"></a><span data-ttu-id="28680-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="28680-107">Permissions</span></span>
<span data-ttu-id="28680-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="28680-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="28680-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="28680-110">Permission type</span></span>      | <span data-ttu-id="28680-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="28680-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="28680-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="28680-112">Delegated (work or school account)</span></span> | <span data-ttu-id="28680-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="28680-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="28680-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="28680-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="28680-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="28680-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="28680-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="28680-116">Application</span></span> | <span data-ttu-id="28680-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="28680-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="28680-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="28680-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/Range

```
## <a name="request-headers"></a><span data-ttu-id="28680-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="28680-119">Request headers</span></span>
| <span data-ttu-id="28680-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="28680-120">Name</span></span>       | <span data-ttu-id="28680-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="28680-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="28680-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="28680-122">Authorization</span></span>  | <span data-ttu-id="28680-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="28680-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="28680-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="28680-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="28680-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="28680-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="28680-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="28680-128">Request body</span></span>
<span data-ttu-id="28680-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="28680-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="28680-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="28680-130">Parameter</span></span>    | <span data-ttu-id="28680-131">Type</span><span class="sxs-lookup"><span data-stu-id="28680-131">Type</span></span>   |<span data-ttu-id="28680-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="28680-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="28680-133">address</span><span class="sxs-lookup"><span data-stu-id="28680-133">address</span></span>|<span data-ttu-id="28680-134">string</span><span class="sxs-lookup"><span data-stu-id="28680-134">string</span></span>|<span data-ttu-id="28680-p105">Opcional. Dirección o nombre del intervalo. Si no se especifica, se devuelve todo el intervalo de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="28680-p105">Optional. The address or the name of the range. If not specified, the entire worksheet range is returned.</span></span>|

## <a name="response"></a><span data-ttu-id="28680-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28680-138">Response</span></span>

<span data-ttu-id="28680-139">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="28680-139">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="28680-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="28680-140">Example</span></span>
<span data-ttu-id="28680-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="28680-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="28680-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="28680-142">Request</span></span>
<span data-ttu-id="28680-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="28680-143">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="28680-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28680-144">Response</span></span>
<span data-ttu-id="28680-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="28680-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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