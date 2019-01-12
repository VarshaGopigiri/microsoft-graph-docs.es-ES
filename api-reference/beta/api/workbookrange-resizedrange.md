---
title: 'workbookRange: resizedRange'
description: Obtiene un objeto de rango similar al objeto actual, pero con su esquina inferior derecha expandida (o contraída) mediante un número de filas y columnas.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 4068da86c1653a01a478d385c5c854c700e50ae9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931338"
---
# <a name="workbookrange-resizedrange"></a><span data-ttu-id="49faf-103">workbookRange: resizedRange</span><span class="sxs-lookup"><span data-stu-id="49faf-103">workbookRange: resizedRange</span></span>

> <span data-ttu-id="49faf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="49faf-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="49faf-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="49faf-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="49faf-106">Obtiene un objeto de rango similar al objeto actual, pero con su esquina inferior derecha expandida (o contraída) mediante un número de filas y columnas.</span><span class="sxs-lookup"><span data-stu-id="49faf-106">Gets a range object similar to the current range object, but with its bottom-right corner expanded (or contracted) by some number of rows and columns.</span></span>

## <a name="permissions"></a><span data-ttu-id="49faf-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="49faf-107">Permissions</span></span>
<span data-ttu-id="49faf-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="49faf-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="49faf-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="49faf-110">Permission type</span></span>      | <span data-ttu-id="49faf-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="49faf-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="49faf-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="49faf-112">Delegated (work or school account)</span></span> | <span data-ttu-id="49faf-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="49faf-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="49faf-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="49faf-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="49faf-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="49faf-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="49faf-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="49faf-116">Application</span></span> | <span data-ttu-id="49faf-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="49faf-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="49faf-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="49faf-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/range/resizedRange(deltaRows={n}, deltaColumns={n})

```

## <a name="function-parameters"></a><span data-ttu-id="49faf-119">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="49faf-119">Function parameters</span></span>

| <span data-ttu-id="49faf-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="49faf-120">Parameter</span></span>    | <span data-ttu-id="49faf-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="49faf-121">Type</span></span>   |<span data-ttu-id="49faf-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="49faf-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="49faf-123">deltarows</span><span class="sxs-lookup"><span data-stu-id="49faf-123">deltarows</span></span>|<span data-ttu-id="49faf-124">Int32</span><span class="sxs-lookup"><span data-stu-id="49faf-124">Int32</span></span>|<span data-ttu-id="49faf-p103">El número de filas en el que se va a expandir la esquina inferior derecha, con respecto al intervalo actual. Use un número positivo para expandir el intervalo, o un número negativo para reducirlo.</span><span class="sxs-lookup"><span data-stu-id="49faf-p103">The number of rows by which to expand the bottom-right corner, relative to the current range. Use a positive number to expand the range, or a negative number to decrease it</span></span>|
|<span data-ttu-id="49faf-127">deltaColumns</span><span class="sxs-lookup"><span data-stu-id="49faf-127">deltaColumns</span></span>|<span data-ttu-id="49faf-128">Int32</span><span class="sxs-lookup"><span data-stu-id="49faf-128">Int32</span></span>|<span data-ttu-id="49faf-p104">El número de columnas en el que se va a expandir la esquina inferior derecha, con respecto al intervalo actual. Use un número positivo para expandir el intervalo, o un número negativo para reducirlo.</span><span class="sxs-lookup"><span data-stu-id="49faf-p104">The number of columnsby which to expand the bottom-right corner, relative to the current range. Use a positive number to expand the range, or a negative number to decrease it.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="49faf-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="49faf-131">Request headers</span></span>
| <span data-ttu-id="49faf-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="49faf-132">Name</span></span>       | <span data-ttu-id="49faf-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="49faf-133">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="49faf-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="49faf-134">Authorization</span></span>  | <span data-ttu-id="49faf-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="49faf-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="49faf-137">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="49faf-137">Workbook-Session-Id</span></span>  | <span data-ttu-id="49faf-p106">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="49faf-p106">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="49faf-140">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="49faf-140">Request body</span></span>
<span data-ttu-id="49faf-141">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="49faf-141">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="49faf-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49faf-142">Response</span></span>

<span data-ttu-id="49faf-143">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="49faf-143">If successful, this method returns `200 OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="49faf-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="49faf-144">Example</span></span>
<span data-ttu-id="49faf-145">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="49faf-145">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="49faf-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="49faf-146">Request</span></span>
<span data-ttu-id="49faf-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49faf-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookrange_resizedrange"
}-->
```http
POST https://graph.microsoft.com/beta/drive/root/workbook/worksheets/{id}/range/resizedRange(deltarows={n}, deltaColumns={n})
```

##### <a name="response"></a><span data-ttu-id="49faf-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49faf-148">Response</span></span>
<span data-ttu-id="49faf-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="49faf-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
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
