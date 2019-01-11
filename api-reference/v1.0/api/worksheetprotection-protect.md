---
title: 'WorksheetProtection: protect'
description: Proteger una hoja de cálculo. Produce una excepción si se ha protegido la hoja de cálculo.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 03d2c9edf6f814f7bd5e460d340b07e714eb18ee
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816159"
---
# <a name="worksheetprotection-protect"></a><span data-ttu-id="07805-104">WorksheetProtection: protect</span><span class="sxs-lookup"><span data-stu-id="07805-104">WorksheetProtection: protect</span></span>

<span data-ttu-id="07805-p102">Proteger una hoja de cálculo. Produce una excepción si se ha protegido la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="07805-p102">Protect a worksheet. It throws if the worksheet has been protected.</span></span>
## <a name="permissions"></a><span data-ttu-id="07805-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="07805-107">Permissions</span></span>
<span data-ttu-id="07805-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="07805-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="07805-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="07805-110">Permission type</span></span>      | <span data-ttu-id="07805-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="07805-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="07805-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="07805-112">Delegated (work or school account)</span></span> | <span data-ttu-id="07805-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07805-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="07805-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="07805-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="07805-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="07805-115">Not supported.</span></span>    |
|<span data-ttu-id="07805-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="07805-116">Application</span></span> | <span data-ttu-id="07805-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="07805-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="07805-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="07805-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/protection/protect

```
## <a name="request-headers"></a><span data-ttu-id="07805-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="07805-119">Request headers</span></span>
| <span data-ttu-id="07805-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="07805-120">Name</span></span>       | <span data-ttu-id="07805-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="07805-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="07805-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="07805-122">Authorization</span></span>  | <span data-ttu-id="07805-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="07805-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="07805-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="07805-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="07805-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="07805-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="07805-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="07805-128">Request body</span></span>
<span data-ttu-id="07805-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="07805-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="07805-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="07805-130">Parameter</span></span>    | <span data-ttu-id="07805-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="07805-131">Type</span></span>   |<span data-ttu-id="07805-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="07805-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="07805-133">opciones</span><span class="sxs-lookup"><span data-stu-id="07805-133">options</span></span>|<span data-ttu-id="07805-134">WorkbookWorksheetProtectionOptions</span><span class="sxs-lookup"><span data-stu-id="07805-134">WorkbookWorksheetProtectionOptions</span></span>|<span data-ttu-id="07805-p106">Opcional. Opciones de protección de la hoja.</span><span class="sxs-lookup"><span data-stu-id="07805-p106">Optional. sheet protection options.</span></span>|

## <a name="response"></a><span data-ttu-id="07805-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="07805-137">Response</span></span>

<span data-ttu-id="07805-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="07805-p107">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="07805-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="07805-140">Example</span></span>
<span data-ttu-id="07805-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="07805-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="07805-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="07805-142">Request</span></span>
<span data-ttu-id="07805-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="07805-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheetprotection_protect"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/protection/protect
Content-type: application/json
Content-length: 383

{
  "options": {
    "allowFormatCells": true,
    "allowFormatColumns": true,
    "allowFormatRows": true,
    "allowInsertColumns": true,
    "allowInsertRows": true,
    "allowInsertHyperlinks": true,
    "allowDeleteColumns": true,
    "allowDeleteRows": true,
    "allowSort": true,
    "allowAutoFilter": true,
    "allowPivotTables": true
  }
}
```

##### <a name="response"></a><span data-ttu-id="07805-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="07805-144">Response</span></span>
<span data-ttu-id="07805-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="07805-145">Here is an example of the response.</span></span> 
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
  "description": "WorksheetProtection: protect",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
