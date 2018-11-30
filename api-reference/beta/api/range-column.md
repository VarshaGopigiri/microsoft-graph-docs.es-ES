---
title: 'Range: Column'
description: Obtiene una columna contenida en el rango.
ms.openlocfilehash: dde991dff164f5abab34c0acccc4127ece76b673
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088714"
---
# <a name="range-column"></a><span data-ttu-id="b9c54-103">Range: Column</span><span class="sxs-lookup"><span data-stu-id="b9c54-103">Range: Column</span></span>

> <span data-ttu-id="b9c54-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b9c54-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b9c54-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b9c54-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b9c54-106">Obtiene una columna contenida en el rango.</span><span class="sxs-lookup"><span data-stu-id="b9c54-106">Gets a column contained in the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="b9c54-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="b9c54-107">Permissions</span></span>
<span data-ttu-id="b9c54-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b9c54-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b9c54-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b9c54-110">Permission type</span></span>      | <span data-ttu-id="b9c54-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b9c54-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b9c54-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b9c54-112">Delegated (work or school account)</span></span> | <span data-ttu-id="b9c54-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b9c54-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b9c54-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b9c54-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b9c54-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b9c54-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b9c54-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b9c54-116">Application</span></span> | <span data-ttu-id="b9c54-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b9c54-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b9c54-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b9c54-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/Column
GET /workbook/worksheets/{id|name}/range(address='<address>')/Column
GET /workbook/tables/{id|name}/columns/{id|name}/range/Column

```
## <a name="request-headers"></a><span data-ttu-id="b9c54-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b9c54-119">Request headers</span></span>
| <span data-ttu-id="b9c54-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="b9c54-120">Name</span></span>       | <span data-ttu-id="b9c54-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9c54-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b9c54-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="b9c54-122">Authorization</span></span>  | <span data-ttu-id="b9c54-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9c54-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b9c54-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="b9c54-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="b9c54-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="b9c54-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="b9c54-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b9c54-128">Request body</span></span>
<span data-ttu-id="b9c54-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="b9c54-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="b9c54-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b9c54-130">Parameter</span></span>    | <span data-ttu-id="b9c54-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9c54-131">Type</span></span>   |<span data-ttu-id="b9c54-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9c54-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b9c54-133">column</span><span class="sxs-lookup"><span data-stu-id="b9c54-133">column</span></span>|<span data-ttu-id="b9c54-134">number</span><span class="sxs-lookup"><span data-stu-id="b9c54-134">number</span></span>|<span data-ttu-id="b9c54-p105">Número de columna del intervalo que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="b9c54-p105">Column number of the range to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="b9c54-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9c54-137">Response</span></span>

<span data-ttu-id="b9c54-138">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b9c54-138">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b9c54-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9c54-139">Example</span></span>
<span data-ttu-id="b9c54-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b9c54-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b9c54-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b9c54-141">Request</span></span>
<span data-ttu-id="b9c54-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b9c54-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_column"
}-->
```http
GET https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/Column
Content-type: application/json
Content-length: 21

{
  "column": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="b9c54-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9c54-143">Response</span></span>
<span data-ttu-id="b9c54-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b9c54-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: Column",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->