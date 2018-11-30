---
title: 'workbookRange: rowsAbove'
description: Obtiene un número determinado de filas encima de un rango dado.
ms.openlocfilehash: a83528ddb0de5c5f82a4dae6537b2052821e725d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087072"
---
# <a name="workbookrange-rowsabove"></a><span data-ttu-id="3f13c-103">workbookRange: rowsAbove</span><span class="sxs-lookup"><span data-stu-id="3f13c-103">workbookRange: rowsAbove</span></span>

> <span data-ttu-id="3f13c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3f13c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3f13c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3f13c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3f13c-106">Obtiene un número determinado de filas encima de un rango dado.</span><span class="sxs-lookup"><span data-stu-id="3f13c-106">Gets a certain number of rows above a given range.</span></span>

## <a name="permissions"></a><span data-ttu-id="3f13c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3f13c-107">Permissions</span></span>
<span data-ttu-id="3f13c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3f13c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3f13c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3f13c-110">Permission type</span></span>      | <span data-ttu-id="3f13c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3f13c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3f13c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3f13c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="3f13c-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3f13c-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="3f13c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3f13c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3f13c-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3f13c-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="3f13c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3f13c-116">Application</span></span> | <span data-ttu-id="3f13c-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f13c-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="3f13c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3f13c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/range/rowsAbove(count=n)

```

## <a name="function-parameters"></a><span data-ttu-id="3f13c-119">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="3f13c-119">Function parameters</span></span>

| <span data-ttu-id="3f13c-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3f13c-120">Parameter</span></span>    | <span data-ttu-id="3f13c-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f13c-121">Type</span></span>   |<span data-ttu-id="3f13c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f13c-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3f13c-123">count</span><span class="sxs-lookup"><span data-stu-id="3f13c-123">count</span></span>|<span data-ttu-id="3f13c-124">Int32</span><span class="sxs-lookup"><span data-stu-id="3f13c-124">Int32</span></span>|<span data-ttu-id="3f13c-p103">Opcional. El número de filas que se va a incluir en el intervalo resultante. En general, use un número positivo para crear un intervalo fuera del intervalo actual. También puede usar un número negativo para crear un intervalo dentro del intervalo actual. El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="3f13c-p103">Optional. The number of rows to include in the resulting range. In general, use a positive number to create a range outside the current range. You can also use a negative number to create a range within the current range. The default value is 1.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="3f13c-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3f13c-130">Request headers</span></span>
| <span data-ttu-id="3f13c-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="3f13c-131">Name</span></span>       | <span data-ttu-id="3f13c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f13c-132">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="3f13c-133">Authorization</span><span class="sxs-lookup"><span data-stu-id="3f13c-133">Authorization</span></span>  | <span data-ttu-id="3f13c-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3f13c-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="3f13c-136">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="3f13c-136">Workbook-Session-Id</span></span>  | <span data-ttu-id="3f13c-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="3f13c-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="3f13c-139">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3f13c-139">Request body</span></span>
<span data-ttu-id="3f13c-140">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3f13c-140">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3f13c-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f13c-141">Response</span></span>

<span data-ttu-id="3f13c-142">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f13c-142">If successful, this method returns `200 OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3f13c-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3f13c-143">Example</span></span>
<span data-ttu-id="3f13c-144">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="3f13c-144">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="3f13c-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3f13c-145">Request</span></span>
<span data-ttu-id="3f13c-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3f13c-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookrange_rowsAbove"
}-->
```http
POST https://graph.microsoft.com/beta/drive/root/workbook/worksheets/{id}/range/rowsAbove(count=2)
```

##### <a name="response"></a><span data-ttu-id="3f13c-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f13c-147">Response</span></span>
<span data-ttu-id="3f13c-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3f13c-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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