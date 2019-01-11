---
title: 'workbookRange: columnsBefore'
description: Obtiene un número determinado de columnas a la izquierda del rango especificado.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 8eff3ffd7291f9e3ae3537fc660760550b3b536e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830117"
---
# <a name="workbookrange-columnsbefore"></a><span data-ttu-id="bc0d6-103">workbookRange: columnsBefore</span><span class="sxs-lookup"><span data-stu-id="bc0d6-103">workbookRange: columnsBefore</span></span>

> <span data-ttu-id="bc0d6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bc0d6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bc0d6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bc0d6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bc0d6-106">Obtiene un número determinado de columnas a la izquierda del rango especificado.</span><span class="sxs-lookup"><span data-stu-id="bc0d6-106">Gets a certain number of columns to the left of the given range.</span></span>

## <a name="permissions"></a><span data-ttu-id="bc0d6-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="bc0d6-107">Permissions</span></span>
<span data-ttu-id="bc0d6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bc0d6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bc0d6-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bc0d6-110">Permission type</span></span>      | <span data-ttu-id="bc0d6-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bc0d6-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bc0d6-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bc0d6-112">Delegated (work or school account)</span></span> | <span data-ttu-id="bc0d6-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="bc0d6-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="bc0d6-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bc0d6-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bc0d6-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc0d6-115">Not supported.</span></span>    |
|<span data-ttu-id="bc0d6-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bc0d6-116">Application</span></span> | <span data-ttu-id="bc0d6-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc0d6-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="bc0d6-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bc0d6-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/range/columnsBefore(count=n)

```

## <a name="function-parameters"></a><span data-ttu-id="bc0d6-119">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="bc0d6-119">Function parameters</span></span>

| <span data-ttu-id="bc0d6-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bc0d6-120">Parameter</span></span>    | <span data-ttu-id="bc0d6-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc0d6-121">Type</span></span>   |<span data-ttu-id="bc0d6-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc0d6-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bc0d6-123">count</span><span class="sxs-lookup"><span data-stu-id="bc0d6-123">count</span></span>|<span data-ttu-id="bc0d6-124">Int32</span><span class="sxs-lookup"><span data-stu-id="bc0d6-124">Int32</span></span>|<span data-ttu-id="bc0d6-p103">El número de columnas que se va a incluir en el intervalo resultante. En general, use un número positivo para crear un intervalo fuera del intervalo actual. También puede usar un número negativo para crear un intervalo dentro del intervalo actual. El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="bc0d6-p103">The number of columns to include in the resulting range. In general, use a positive number to create a range outside the current range. You can also use a negative number to create a range within the current range. The default value is 1.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="bc0d6-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bc0d6-129">Request headers</span></span>
| <span data-ttu-id="bc0d6-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="bc0d6-130">Name</span></span>       | <span data-ttu-id="bc0d6-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc0d6-131">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="bc0d6-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="bc0d6-132">Authorization</span></span>  | <span data-ttu-id="bc0d6-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bc0d6-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bc0d6-135">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="bc0d6-135">Workbook-Session-Id</span></span>  | <span data-ttu-id="bc0d6-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="bc0d6-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="bc0d6-138">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bc0d6-138">Request body</span></span>
<span data-ttu-id="bc0d6-139">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bc0d6-139">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bc0d6-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc0d6-140">Response</span></span>
<span data-ttu-id="bc0d6-141">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc0d6-141">If successful, this method returns `200 OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bc0d6-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bc0d6-142">Example</span></span>
<span data-ttu-id="bc0d6-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="bc0d6-143">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="bc0d6-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bc0d6-144">Request</span></span>
<span data-ttu-id="bc0d6-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bc0d6-145">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookrange_columnsbefore"
}-->
```http
POST https://graph.microsoft.com/beta/drive/root/workbook/worksheets/{id}/range/columnsBefore(count=2)
```

##### <a name="response"></a><span data-ttu-id="bc0d6-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc0d6-146">Response</span></span>
<span data-ttu-id="bc0d6-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bc0d6-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
