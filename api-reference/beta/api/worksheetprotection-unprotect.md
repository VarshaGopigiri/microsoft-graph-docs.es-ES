---
title: 'WorksheetProtection: unprotect'
description: Desproteger una hoja de cálculo.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 52feaf77964949fee9bbedbf3ced2967226bb486
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27850522"
---
# <a name="worksheetprotection-unprotect"></a><span data-ttu-id="a0e2e-103">WorksheetProtection: unprotect</span><span class="sxs-lookup"><span data-stu-id="a0e2e-103">WorksheetProtection: unprotect</span></span>

> <span data-ttu-id="a0e2e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a0e2e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a0e2e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a0e2e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a0e2e-106">Desproteger una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="a0e2e-106">Unprotect a worksheet</span></span>
## <a name="permissions"></a><span data-ttu-id="a0e2e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a0e2e-107">Permissions</span></span>
<span data-ttu-id="a0e2e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a0e2e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a0e2e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a0e2e-110">Permission type</span></span>      | <span data-ttu-id="a0e2e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a0e2e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a0e2e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a0e2e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="a0e2e-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a0e2e-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="a0e2e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a0e2e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a0e2e-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a0e2e-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="a0e2e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a0e2e-116">Application</span></span> | <span data-ttu-id="a0e2e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a0e2e-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a0e2e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a0e2e-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/protection/unprotect

```
## <a name="request-headers"></a><span data-ttu-id="a0e2e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a0e2e-119">Request headers</span></span>
| <span data-ttu-id="a0e2e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="a0e2e-120">Name</span></span>       | <span data-ttu-id="a0e2e-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0e2e-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="a0e2e-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="a0e2e-122">Authorization</span></span>  | <span data-ttu-id="a0e2e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a0e2e-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a0e2e-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="a0e2e-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="a0e2e-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="a0e2e-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="a0e2e-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a0e2e-128">Request body</span></span>
<span data-ttu-id="a0e2e-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="a0e2e-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="a0e2e-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a0e2e-130">Parameter</span></span>    | <span data-ttu-id="a0e2e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0e2e-131">Type</span></span>   |<span data-ttu-id="a0e2e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0e2e-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a0e2e-133">password</span><span class="sxs-lookup"><span data-stu-id="a0e2e-133">password</span></span>|<span data-ttu-id="a0e2e-134">string</span><span class="sxs-lookup"><span data-stu-id="a0e2e-134">string</span></span>|<span data-ttu-id="a0e2e-p105">Opcional. Contraseña de protección de la hoja.</span><span class="sxs-lookup"><span data-stu-id="a0e2e-p105">Optional. sheet protection password.</span></span>|

## <a name="response"></a><span data-ttu-id="a0e2e-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0e2e-137">Response</span></span>

<span data-ttu-id="a0e2e-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0e2e-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a0e2e-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0e2e-140">Example</span></span>
<span data-ttu-id="a0e2e-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a0e2e-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="a0e2e-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a0e2e-142">Request</span></span>
<span data-ttu-id="a0e2e-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a0e2e-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheetprotection_unprotect"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/protection/unprotect
Content-type: application/json
Content-length: 34

{
  "password": "password-value"
}
```

##### <a name="response"></a><span data-ttu-id="a0e2e-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0e2e-144">Response</span></span>
<span data-ttu-id="a0e2e-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0e2e-145">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "WorksheetProtection: unprotect",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
