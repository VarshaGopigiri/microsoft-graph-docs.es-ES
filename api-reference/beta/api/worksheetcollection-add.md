---
title: 'WorksheetCollection: add'
description: .Activate() en él.
author: lumine2008
ms.openlocfilehash: 560a66c4beb589fbb736f0aa27784827740c0440
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27363581"
---
# <a name="worksheetcollection-add"></a><span data-ttu-id="8f394-103">WorksheetCollection: add</span><span class="sxs-lookup"><span data-stu-id="8f394-103">WorksheetCollection: add</span></span>

> <span data-ttu-id="8f394-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8f394-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8f394-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8f394-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8f394-p102">Agrega una nueva hoja al libro. La hoja de cálculo se agregará al final de las hojas de cálculo existentes. Si desea activar la hoja de cálculo recién agregada, llame en ella a ".activate().</span><span class="sxs-lookup"><span data-stu-id="8f394-p102">Adds a new worksheet to the workbook. The worksheet will be added at the end of existing worksheets. If you wish to activate the newly added worksheet, call ".activate() on it.</span></span>
## <a name="permissions"></a><span data-ttu-id="8f394-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="8f394-109">Permissions</span></span>
<span data-ttu-id="8f394-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8f394-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8f394-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8f394-112">Permission type</span></span>      | <span data-ttu-id="8f394-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8f394-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8f394-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8f394-114">Delegated (work or school account)</span></span> | <span data-ttu-id="8f394-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f394-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="8f394-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8f394-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8f394-117">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f394-117">Files.ReadWrite</span></span>    |
|<span data-ttu-id="8f394-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8f394-118">Application</span></span> | <span data-ttu-id="8f394-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f394-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="8f394-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8f394-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/

```
## <a name="request-headers"></a><span data-ttu-id="8f394-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8f394-121">Request headers</span></span>
| <span data-ttu-id="8f394-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="8f394-122">Name</span></span>       | <span data-ttu-id="8f394-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f394-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="8f394-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="8f394-124">Authorization</span></span>  | <span data-ttu-id="8f394-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8f394-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="8f394-127">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="8f394-127">Workbook-Session-Id</span></span>  | <span data-ttu-id="8f394-p105">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="8f394-p105">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="8f394-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8f394-130">Request body</span></span>
<span data-ttu-id="8f394-131">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="8f394-131">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="8f394-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="8f394-132">Parameter</span></span>    | <span data-ttu-id="8f394-133">Type</span><span class="sxs-lookup"><span data-stu-id="8f394-133">Type</span></span>   |<span data-ttu-id="8f394-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f394-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8f394-135">name</span><span class="sxs-lookup"><span data-stu-id="8f394-135">name</span></span>|<span data-ttu-id="8f394-136">string</span><span class="sxs-lookup"><span data-stu-id="8f394-136">string</span></span>|<span data-ttu-id="8f394-p106">Opcional. Nombre de la hoja de cálculo que se va a agregar. Si se especifica, el nombre debe ser único. Si no se especifica, Excel determina el nombre de la nueva hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="8f394-p106">Optional. The name of the worksheet to be added. If specified, name should be unqiue. If not specified, Excel determines the name of the new worksheet.</span></span>|

## <a name="response"></a><span data-ttu-id="8f394-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f394-141">Response</span></span>

<span data-ttu-id="8f394-142">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Worksheet](../resources/worksheet.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f394-142">If successful, this method returns `200 OK` response code and [Worksheet](../resources/worksheet.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8f394-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8f394-143">Example</span></span>
<span data-ttu-id="8f394-144">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="8f394-144">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="8f394-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8f394-145">Request</span></span>
<span data-ttu-id="8f394-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f394-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheetcollection_add"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/add
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```

##### <a name="response"></a><span data-ttu-id="8f394-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f394-147">Response</span></span>
<span data-ttu-id="8f394-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8f394-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.worksheet"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 100

{
  "id": "id-value",
  "position": 99,
  "name": "name-value",
  "visibility": "visibility-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "WorksheetCollection: add",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->