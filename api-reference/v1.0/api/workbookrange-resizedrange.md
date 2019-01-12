---
title: 'workbookRange: resizedRange'
description: Obtiene un objeto de rango similar al objeto actual, pero con su esquina inferior derecha expandida (o contraída) mediante un número de filas y columnas.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 4eb5aad208ecd7c60e45b2419b61570915bb7338
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931296"
---
# <a name="workbookrange-resizedrange"></a><span data-ttu-id="569ef-103">workbookRange: resizedRange</span><span class="sxs-lookup"><span data-stu-id="569ef-103">workbookRange: resizedRange</span></span>
<span data-ttu-id="569ef-104">Obtiene un objeto de rango similar al objeto actual, pero con su esquina inferior derecha expandida (o contraída) mediante un número de filas y columnas.</span><span class="sxs-lookup"><span data-stu-id="569ef-104">Gets a range object similar to the current range object, but with its bottom-right corner expanded (or contracted) by some number of rows and columns.</span></span>

## <a name="permissions"></a><span data-ttu-id="569ef-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="569ef-105">Permissions</span></span>
<span data-ttu-id="569ef-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="569ef-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="569ef-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="569ef-108">Permission type</span></span>      | <span data-ttu-id="569ef-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="569ef-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="569ef-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="569ef-110">Delegated (work or school account)</span></span> | <span data-ttu-id="569ef-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="569ef-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="569ef-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="569ef-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="569ef-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="569ef-113">Not supported.</span></span>    |
|<span data-ttu-id="569ef-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="569ef-114">Application</span></span> | <span data-ttu-id="569ef-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="569ef-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="569ef-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="569ef-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/range/resizedRange(deltaRows={n}, deltaColumns={n})

```

## <a name="function-parameters"></a><span data-ttu-id="569ef-117">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="569ef-117">Function parameters</span></span>

| <span data-ttu-id="569ef-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="569ef-118">Parameter</span></span>    | <span data-ttu-id="569ef-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="569ef-119">Type</span></span>   |<span data-ttu-id="569ef-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="569ef-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="569ef-121">deltaRows</span><span class="sxs-lookup"><span data-stu-id="569ef-121">deltaRows</span></span>|<span data-ttu-id="569ef-122">Int32</span><span class="sxs-lookup"><span data-stu-id="569ef-122">Int32</span></span>|<span data-ttu-id="569ef-p102">El número de filas en el que se va a expandir la esquina inferior derecha, con respecto al intervalo actual. Use un número positivo para expandir el intervalo, o un número negativo para reducirlo.</span><span class="sxs-lookup"><span data-stu-id="569ef-p102">The number of rows by which to expand the bottom-right corner, relative to the current range. Use a positive number to expand the range, or a negative number to decrease it</span></span>|
|<span data-ttu-id="569ef-125">deltaColumns</span><span class="sxs-lookup"><span data-stu-id="569ef-125">deltaColumns</span></span>|<span data-ttu-id="569ef-126">Int32</span><span class="sxs-lookup"><span data-stu-id="569ef-126">Int32</span></span>|<span data-ttu-id="569ef-127">El número de columnas que se usará expandir la esquina inferior derecha, en relación con el intervalo actual.</span><span class="sxs-lookup"><span data-stu-id="569ef-127">The number of columns by which to expand the bottom-right corner, relative to the current range.</span></span> <span data-ttu-id="569ef-128">Use un número positivo para expandir el intervalo o un número negativo para reducirlo.</span><span class="sxs-lookup"><span data-stu-id="569ef-128">Use a positive number to expand the range, or a negative number to decrease it.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="569ef-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="569ef-129">Request headers</span></span>
| <span data-ttu-id="569ef-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="569ef-130">Name</span></span>       | <span data-ttu-id="569ef-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="569ef-131">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="569ef-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="569ef-132">Authorization</span></span>  | <span data-ttu-id="569ef-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="569ef-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="569ef-135">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="569ef-135">Workbook-Session-Id</span></span>  | <span data-ttu-id="569ef-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="569ef-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="569ef-138">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="569ef-138">Request body</span></span>
<span data-ttu-id="569ef-139">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="569ef-139">Do not supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="569ef-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="569ef-140">Response</span></span>
<span data-ttu-id="569ef-141">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="569ef-141">If successful, this method returns `200 OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="569ef-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="569ef-142">Example</span></span>
<span data-ttu-id="569ef-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="569ef-143">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="569ef-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="569ef-144">Request</span></span>
<span data-ttu-id="569ef-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="569ef-145">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "workbookrange_resizedrange",
  "idempotent": true
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/range/resizedRange(deltaRows={n}, deltaColumns={n})
```

##### <a name="response"></a><span data-ttu-id="569ef-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="569ef-146">Response</span></span>
<span data-ttu-id="569ef-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="569ef-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRange"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 157

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnHidden": true,
  "columnIndex": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "workbookRange: resizedRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
