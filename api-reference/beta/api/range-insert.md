---
title: 'Range: insert'
description: Inserta una celda o un intervalo de celdas en la hoja de cálculo en lugar de este intervalo y desplaza las demás celdas para crear espacio. Devuelve un objeto Range en el espacio que queda en blanco.
localization_priority: Normal
ms.openlocfilehash: 0e7ab0d729dad4eec7fb455774cfed19bf4f5013
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831517"
---
# <a name="range-insert"></a><span data-ttu-id="01630-104">Range: insert</span><span class="sxs-lookup"><span data-stu-id="01630-104">Range: insert</span></span>

> <span data-ttu-id="01630-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="01630-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="01630-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="01630-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="01630-p103">Inserta una celda o un intervalo de celdas en la hoja de cálculo en lugar de este intervalo y desplaza las demás celdas para crear espacio. Devuelve un objeto Range en el espacio que queda en blanco.</span><span class="sxs-lookup"><span data-stu-id="01630-p103">Inserts a cell or a range of cells into the worksheet in place of this range, and shifts the other cells to make space. Returns a new Range object at the now blank space.</span></span>
## <a name="permissions"></a><span data-ttu-id="01630-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="01630-109">Permissions</span></span>
<span data-ttu-id="01630-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="01630-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="01630-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="01630-112">Permission type</span></span>      | <span data-ttu-id="01630-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="01630-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="01630-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="01630-114">Delegated (work or school account)</span></span> | <span data-ttu-id="01630-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="01630-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="01630-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="01630-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="01630-117">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="01630-117">Files.ReadWrite</span></span>    |
|<span data-ttu-id="01630-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="01630-118">Application</span></span> | <span data-ttu-id="01630-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01630-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="01630-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01630-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/insert
POST /workbook/worksheets/{id|name}/range(address='<address>')/insert
POST /workbook/tables/{id|name}/columns/{id|name}/range/insert

```
## <a name="request-headers"></a><span data-ttu-id="01630-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="01630-121">Request headers</span></span>
| <span data-ttu-id="01630-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="01630-122">Name</span></span>       | <span data-ttu-id="01630-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="01630-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="01630-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="01630-124">Authorization</span></span>  | <span data-ttu-id="01630-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="01630-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="01630-127">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="01630-127">Workbook-Session-Id</span></span>  | <span data-ttu-id="01630-p106">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="01630-p106">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="01630-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="01630-130">Request body</span></span>
<span data-ttu-id="01630-131">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="01630-131">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="01630-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="01630-132">Parameter</span></span>    | <span data-ttu-id="01630-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="01630-133">Type</span></span>   |<span data-ttu-id="01630-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="01630-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="01630-135">Shift</span><span class="sxs-lookup"><span data-stu-id="01630-135">shift</span></span>|<span data-ttu-id="01630-136">string</span><span class="sxs-lookup"><span data-stu-id="01630-136">string</span></span>|<span data-ttu-id="01630-p107">Especifica hacia dónde se desplazarán las celdas.  Valores posibles: `Down`, `Right`.</span><span class="sxs-lookup"><span data-stu-id="01630-p107">Specifies which way to shift the cells.  Possible values are: `Down`, `Right`.</span></span>|

## <a name="response"></a><span data-ttu-id="01630-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01630-139">Response</span></span>

<span data-ttu-id="01630-140">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01630-140">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="01630-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01630-141">Example</span></span>
<span data-ttu-id="01630-142">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="01630-142">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="01630-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01630-143">Request</span></span>
<span data-ttu-id="01630-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="01630-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_insert"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/insert
Content-type: application/json
Content-length: 28

{
  "shift": "shift-value"
}
```

##### <a name="response"></a><span data-ttu-id="01630-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01630-145">Response</span></span>
<span data-ttu-id="01630-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="01630-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: insert",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
