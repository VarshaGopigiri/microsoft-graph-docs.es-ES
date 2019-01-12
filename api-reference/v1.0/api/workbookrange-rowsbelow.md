---
title: 'workbookRange: rowsBelow'
description: Obtiene un número determinado de filas debajo de un rango dado.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 3b0f4add673d7bf6a8e976b037c39256e69be72d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991695"
---
# <a name="workbookrange-rowsbelow"></a><span data-ttu-id="8816f-103">workbookRange: rowsBelow</span><span class="sxs-lookup"><span data-stu-id="8816f-103">workbookRange: rowsBelow</span></span>

<span data-ttu-id="8816f-104">Obtiene un número determinado de filas debajo de un rango dado.</span><span class="sxs-lookup"><span data-stu-id="8816f-104">Gets certain number of rows below a given range.</span></span>

## <a name="permissions"></a><span data-ttu-id="8816f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="8816f-105">Permissions</span></span>
<span data-ttu-id="8816f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8816f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8816f-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8816f-108">Permission type</span></span>      | <span data-ttu-id="8816f-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8816f-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8816f-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8816f-110">Delegated (work or school account)</span></span> | <span data-ttu-id="8816f-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8816f-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="8816f-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8816f-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8816f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8816f-113">Not supported.</span></span>    |
|<span data-ttu-id="8816f-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8816f-114">Application</span></span> | <span data-ttu-id="8816f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8816f-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="8816f-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8816f-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/range/rowsBelow(count=n)

```

## <a name="function-parameters"></a><span data-ttu-id="8816f-117">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="8816f-117">Function parameters</span></span>

| <span data-ttu-id="8816f-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="8816f-118">Parameter</span></span>    | <span data-ttu-id="8816f-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="8816f-119">Type</span></span>   |<span data-ttu-id="8816f-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="8816f-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8816f-121">count</span><span class="sxs-lookup"><span data-stu-id="8816f-121">count</span></span>|<span data-ttu-id="8816f-122">Int32</span><span class="sxs-lookup"><span data-stu-id="8816f-122">Int32</span></span>| <span data-ttu-id="8816f-p102">Opcional. El número de filas que se va a incluir en el intervalo resultante. En general, use un número positivo para crear un intervalo fuera del intervalo actual. También puede usar un número negativo para crear un intervalo dentro del intervalo actual. El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="8816f-p102">Optional. The number of rows to include in the resulting range. In general, use a positive number to create a range outside the current range. You can also use a negative number to create a range within the current range. The default value is 1.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="8816f-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8816f-128">Request headers</span></span>
| <span data-ttu-id="8816f-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="8816f-129">Name</span></span>       | <span data-ttu-id="8816f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="8816f-130">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="8816f-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="8816f-131">Authorization</span></span>  | <span data-ttu-id="8816f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8816f-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="8816f-134">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="8816f-134">Workbook-Session-Id</span></span>  | <span data-ttu-id="8816f-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="8816f-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="8816f-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8816f-137">Request body</span></span>
<span data-ttu-id="8816f-138">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8816f-138">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8816f-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8816f-139">Response</span></span>
<span data-ttu-id="8816f-140">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8816f-140">If successful, this method returns `200 OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8816f-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8816f-141">Example</span></span>
<span data-ttu-id="8816f-142">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="8816f-142">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="8816f-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8816f-143">Request</span></span>
<span data-ttu-id="8816f-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8816f-144">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "workbookrange_rowsBelow",
  "idempotent": true
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/range/rowsBelow(count=2)
```

##### <a name="response"></a><span data-ttu-id="8816f-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8816f-145">Response</span></span>
<span data-ttu-id="8816f-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8816f-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

<span data-ttu-id="8816f-149">Si se llama a sin el `count` , esta función utiliza el valor predeterminado para una fila.</span><span class="sxs-lookup"><span data-stu-id="8816f-149">If called without the `count` parameter, this function defaults to one row.</span></span>

##### <a name="request"></a><span data-ttu-id="8816f-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8816f-150">Request</span></span>
<span data-ttu-id="8816f-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8816f-151">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "workbookrange_rowsBelow_nocount",
  "idempotent": true
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/range/rowsBelow
```

##### <a name="response"></a><span data-ttu-id="8816f-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8816f-152">Response</span></span>
<span data-ttu-id="8816f-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8816f-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRange"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnHidden": true,
  "columnIndex": 99
}
```
