---
title: 'WorksheetProtection: unprotect'
description: Desproteger una hoja de cálculo.
ms.openlocfilehash: 32909d81119c326172a12d346ea53d9f8eb2b71b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089667"
---
# <a name="worksheetprotection-unprotect"></a><span data-ttu-id="f0ad1-103">WorksheetProtection: unprotect</span><span class="sxs-lookup"><span data-stu-id="f0ad1-103">WorksheetProtection: unprotect</span></span>

> <span data-ttu-id="f0ad1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f0ad1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f0ad1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f0ad1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f0ad1-106">Desproteger una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="f0ad1-106">Unprotect a worksheet</span></span>
## <a name="permissions"></a><span data-ttu-id="f0ad1-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f0ad1-107">Permissions</span></span>
<span data-ttu-id="f0ad1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f0ad1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f0ad1-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f0ad1-110">Permission type</span></span>      | <span data-ttu-id="f0ad1-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f0ad1-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f0ad1-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f0ad1-112">Delegated (work or school account)</span></span> | <span data-ttu-id="f0ad1-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f0ad1-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f0ad1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f0ad1-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f0ad1-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f0ad1-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f0ad1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f0ad1-116">Application</span></span> | <span data-ttu-id="f0ad1-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f0ad1-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f0ad1-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f0ad1-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/protection/unprotect

```
## <a name="request-headers"></a><span data-ttu-id="f0ad1-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f0ad1-119">Request headers</span></span>
| <span data-ttu-id="f0ad1-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="f0ad1-120">Name</span></span>       | <span data-ttu-id="f0ad1-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0ad1-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f0ad1-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="f0ad1-122">Authorization</span></span>  | <span data-ttu-id="f0ad1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f0ad1-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f0ad1-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="f0ad1-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="f0ad1-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="f0ad1-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="f0ad1-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f0ad1-128">Request body</span></span>
<span data-ttu-id="f0ad1-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="f0ad1-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f0ad1-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f0ad1-130">Parameter</span></span>    | <span data-ttu-id="f0ad1-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0ad1-131">Type</span></span>   |<span data-ttu-id="f0ad1-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0ad1-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f0ad1-133">password</span><span class="sxs-lookup"><span data-stu-id="f0ad1-133">password</span></span>|<span data-ttu-id="f0ad1-134">string</span><span class="sxs-lookup"><span data-stu-id="f0ad1-134">string</span></span>|<span data-ttu-id="f0ad1-p105">Opcional. Contraseña de protección de la hoja.</span><span class="sxs-lookup"><span data-stu-id="f0ad1-p105">Optional. sheet protection password.</span></span>|

## <a name="response"></a><span data-ttu-id="f0ad1-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f0ad1-137">Response</span></span>

<span data-ttu-id="f0ad1-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f0ad1-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f0ad1-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f0ad1-140">Example</span></span>
<span data-ttu-id="f0ad1-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f0ad1-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f0ad1-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f0ad1-142">Request</span></span>
<span data-ttu-id="f0ad1-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f0ad1-143">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="f0ad1-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f0ad1-144">Response</span></span>
<span data-ttu-id="f0ad1-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f0ad1-145">Here is an example of the response.</span></span> 
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