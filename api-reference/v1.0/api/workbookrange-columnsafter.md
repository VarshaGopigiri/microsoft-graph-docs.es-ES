---
title: 'workbookRange: columnsAfter'
description: Obtiene un número determinado de columnas a la derecha del rango especificado.
ms.openlocfilehash: 7879bdac135f8f54a661d9e40e74c676011e36fa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030104"
---
# <a name="workbookrange-columnsafter"></a><span data-ttu-id="806df-103">workbookRange: columnsAfter</span><span class="sxs-lookup"><span data-stu-id="806df-103">workbookRange: columnsAfter</span></span>

<span data-ttu-id="806df-104">Obtiene un número determinado de columnas a la derecha del rango especificado.</span><span class="sxs-lookup"><span data-stu-id="806df-104">Gets a certain number of columns to the right of the given range.</span></span>

## <a name="permissions"></a><span data-ttu-id="806df-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="806df-105">Permissions</span></span>
<span data-ttu-id="806df-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="806df-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="806df-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="806df-108">Permission type</span></span>      | <span data-ttu-id="806df-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="806df-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="806df-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="806df-110">Delegated (work or school account)</span></span> | <span data-ttu-id="806df-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="806df-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="806df-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="806df-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="806df-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="806df-113">Not supported.</span></span>    |
|<span data-ttu-id="806df-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="806df-114">Application</span></span> | <span data-ttu-id="806df-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="806df-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="806df-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="806df-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/range/columnsAfter(count=n)

```

## <a name="function-parameters"></a><span data-ttu-id="806df-117">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="806df-117">Function parameters</span></span>

| <span data-ttu-id="806df-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="806df-118">Parameter</span></span>    | <span data-ttu-id="806df-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="806df-119">Type</span></span>   |<span data-ttu-id="806df-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="806df-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="806df-121">count</span><span class="sxs-lookup"><span data-stu-id="806df-121">count</span></span>|<span data-ttu-id="806df-122">Int32</span><span class="sxs-lookup"><span data-stu-id="806df-122">Int32</span></span>|<span data-ttu-id="806df-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="806df-123">Optional.</span></span> <span data-ttu-id="806df-124">El número de columnas que se incluirán en el intervalo resultante.</span><span class="sxs-lookup"><span data-stu-id="806df-124">The number of columns to include in the resulting range.</span></span> <span data-ttu-id="806df-125">En general, use un número positivo para crear un intervalo fuera del intervalo actual.</span><span class="sxs-lookup"><span data-stu-id="806df-125">In general, use a positive number to create a range outside the current range.</span></span> <span data-ttu-id="806df-126">También puede utilizar un número negativo para crear un intervalo dentro del intervalo actual.</span><span class="sxs-lookup"><span data-stu-id="806df-126">You can also use a negative number to create a range within the current range.</span></span> <span data-ttu-id="806df-127">El valor predeterminado es 1</span><span class="sxs-lookup"><span data-stu-id="806df-127">The default value is 1</span></span>|

## <a name="request-headers"></a><span data-ttu-id="806df-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="806df-128">Request headers</span></span>
| <span data-ttu-id="806df-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="806df-129">Name</span></span>       | <span data-ttu-id="806df-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="806df-130">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="806df-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="806df-131">Authorization</span></span>  | <span data-ttu-id="806df-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="806df-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="806df-134">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="806df-134">Workbook-Session-Id</span></span>  | <span data-ttu-id="806df-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="806df-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="806df-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="806df-137">Request body</span></span>
<span data-ttu-id="806df-138">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="806df-138">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="806df-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="806df-139">Response</span></span>
<span data-ttu-id="806df-140">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="806df-140">If successful, this method returns `200 OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="806df-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="806df-141">Example</span></span>
<span data-ttu-id="806df-142">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="806df-142">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="806df-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="806df-143">Request</span></span>
<span data-ttu-id="806df-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="806df-144">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "workbookrange_columnsafter",
  "idempotent": true
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/range/columnsAfter(count=2)
```

##### <a name="response"></a><span data-ttu-id="806df-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="806df-145">Response</span></span>
<span data-ttu-id="806df-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="806df-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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