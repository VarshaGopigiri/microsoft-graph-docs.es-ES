---
title: 'WorksheetProtection: unprotect'
description: Desproteger una hoja de cálculo.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 19674e2c3ce10ee7cccef3e0c45a445827a5fb2b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956972"
---
# <a name="worksheetprotection-unprotect"></a><span data-ttu-id="f8859-103">WorksheetProtection: unprotect</span><span class="sxs-lookup"><span data-stu-id="f8859-103">WorksheetProtection: unprotect</span></span>

<span data-ttu-id="f8859-104">Desproteger una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="f8859-104">Unprotect a worksheet</span></span>
## <a name="permissions"></a><span data-ttu-id="f8859-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f8859-105">Permissions</span></span>
<span data-ttu-id="f8859-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f8859-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f8859-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f8859-108">Permission type</span></span>      | <span data-ttu-id="f8859-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f8859-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f8859-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f8859-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f8859-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f8859-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f8859-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f8859-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f8859-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f8859-113">Not supported.</span></span>    |
|<span data-ttu-id="f8859-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f8859-114">Application</span></span> | <span data-ttu-id="f8859-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f8859-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f8859-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f8859-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/protection/unprotect

```
## <a name="request-headers"></a><span data-ttu-id="f8859-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f8859-117">Request headers</span></span>
| <span data-ttu-id="f8859-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="f8859-118">Name</span></span>       | <span data-ttu-id="f8859-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8859-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f8859-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="f8859-120">Authorization</span></span>  | <span data-ttu-id="f8859-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f8859-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f8859-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="f8859-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="f8859-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="f8859-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="f8859-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f8859-126">Request body</span></span>
<span data-ttu-id="f8859-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="f8859-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f8859-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f8859-128">Parameter</span></span>    | <span data-ttu-id="f8859-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f8859-129">Type</span></span>   |<span data-ttu-id="f8859-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8859-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f8859-131">password</span><span class="sxs-lookup"><span data-stu-id="f8859-131">password</span></span>|<span data-ttu-id="f8859-132">string</span><span class="sxs-lookup"><span data-stu-id="f8859-132">string</span></span>|<span data-ttu-id="f8859-p104">Opcional. Contraseña de protección de la hoja.</span><span class="sxs-lookup"><span data-stu-id="f8859-p104">Optional. sheet protection password.</span></span>|

## <a name="response"></a><span data-ttu-id="f8859-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8859-135">Response</span></span>

<span data-ttu-id="f8859-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f8859-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f8859-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f8859-138">Example</span></span>
<span data-ttu-id="f8859-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f8859-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f8859-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f8859-140">Request</span></span>
<span data-ttu-id="f8859-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f8859-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheetprotection_unprotect"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/protection/unprotect
Content-type: application/json
Content-length: 34

{
  "password": "password-value"
}
```

##### <a name="response"></a><span data-ttu-id="f8859-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8859-142">Response</span></span>
<span data-ttu-id="f8859-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f8859-143">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
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
