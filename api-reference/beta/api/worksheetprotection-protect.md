---
title: 'WorksheetProtection: protect'
description: Proteger una hoja de cálculo. Produce una excepción si se ha protegido la hoja de cálculo.
ms.openlocfilehash: 885928c592f6aafe320181e62b3993dfbdadf87e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086693"
---
# <a name="worksheetprotection-protect"></a><span data-ttu-id="ee9be-104">WorksheetProtection: protect</span><span class="sxs-lookup"><span data-stu-id="ee9be-104">WorksheetProtection: protect</span></span>

> <span data-ttu-id="ee9be-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ee9be-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ee9be-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ee9be-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ee9be-p103">Proteger una hoja de cálculo. Produce una excepción si se ha protegido la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="ee9be-p103">Protect a worksheet. It throws if the worksheet has been protected.</span></span>
## <a name="permissions"></a><span data-ttu-id="ee9be-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="ee9be-109">Permissions</span></span>
<span data-ttu-id="ee9be-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ee9be-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ee9be-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ee9be-112">Permission type</span></span>      | <span data-ttu-id="ee9be-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ee9be-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ee9be-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ee9be-114">Delegated (work or school account)</span></span> | <span data-ttu-id="ee9be-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ee9be-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="ee9be-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ee9be-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ee9be-117">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ee9be-117">Files.ReadWrite</span></span>    |
|<span data-ttu-id="ee9be-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ee9be-118">Application</span></span> | <span data-ttu-id="ee9be-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ee9be-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ee9be-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ee9be-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/protection/protect

```
## <a name="request-headers"></a><span data-ttu-id="ee9be-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ee9be-121">Request headers</span></span>
| <span data-ttu-id="ee9be-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="ee9be-122">Name</span></span>       | <span data-ttu-id="ee9be-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee9be-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="ee9be-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="ee9be-124">Authorization</span></span>  | <span data-ttu-id="ee9be-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ee9be-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ee9be-127">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="ee9be-127">Workbook-Session-Id</span></span>  | <span data-ttu-id="ee9be-p106">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="ee9be-p106">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="ee9be-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ee9be-130">Request body</span></span>
<span data-ttu-id="ee9be-131">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="ee9be-131">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="ee9be-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ee9be-132">Parameter</span></span>    | <span data-ttu-id="ee9be-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee9be-133">Type</span></span>   |<span data-ttu-id="ee9be-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee9be-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ee9be-135">opciones</span><span class="sxs-lookup"><span data-stu-id="ee9be-135">options</span></span>|<span data-ttu-id="ee9be-136">WorksheetProtectionOptions</span><span class="sxs-lookup"><span data-stu-id="ee9be-136">WorksheetProtectionOptions</span></span>|<span data-ttu-id="ee9be-p107">Opcional. Opciones de protección de la hoja.</span><span class="sxs-lookup"><span data-stu-id="ee9be-p107">Optional. sheet protection options.</span></span>|

## <a name="response"></a><span data-ttu-id="ee9be-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee9be-139">Response</span></span>

<span data-ttu-id="ee9be-p108">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee9be-p108">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ee9be-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ee9be-142">Example</span></span>
<span data-ttu-id="ee9be-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="ee9be-143">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="ee9be-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ee9be-144">Request</span></span>
<span data-ttu-id="ee9be-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ee9be-145">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheetprotection_protect"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/protection/protect
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

##### <a name="response"></a><span data-ttu-id="ee9be-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee9be-146">Response</span></span>
<span data-ttu-id="ee9be-147">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee9be-147">Here is an example of the response.</span></span> 
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
  "description": "WorksheetProtection: protect",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
