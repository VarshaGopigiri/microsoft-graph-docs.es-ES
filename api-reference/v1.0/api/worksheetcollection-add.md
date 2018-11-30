---
title: 'WorksheetCollection: add'
description: .Activate() en él.
ms.openlocfilehash: 992524aae6dfca0619c043eb0ddb7a4100f50206
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030191"
---
# <a name="worksheetcollection-add"></a><span data-ttu-id="c5270-103">WorksheetCollection: add</span><span class="sxs-lookup"><span data-stu-id="c5270-103">WorksheetCollection: add</span></span>

<span data-ttu-id="c5270-p101">Agrega una nueva hoja al libro. La hoja de cálculo se agregará al final de las hojas de cálculo existentes. Si desea activar la hoja de cálculo recién agregada, llame en ella a ".activate().</span><span class="sxs-lookup"><span data-stu-id="c5270-p101">Adds a new worksheet to the workbook. The worksheet will be added at the end of existing worksheets. If you wish to activate the newly added worksheet, call ".activate() on it.</span></span>
## <a name="permissions"></a><span data-ttu-id="c5270-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c5270-107">Permissions</span></span>
<span data-ttu-id="c5270-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c5270-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c5270-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c5270-110">Permission type</span></span>      | <span data-ttu-id="c5270-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c5270-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c5270-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c5270-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c5270-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c5270-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="c5270-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c5270-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c5270-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c5270-115">Not supported.</span></span>    |
|<span data-ttu-id="c5270-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c5270-116">Application</span></span> | <span data-ttu-id="c5270-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c5270-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c5270-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c5270-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/

```
## <a name="request-headers"></a><span data-ttu-id="c5270-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c5270-119">Request headers</span></span>
| <span data-ttu-id="c5270-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c5270-120">Name</span></span>       | <span data-ttu-id="c5270-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5270-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="c5270-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c5270-122">Authorization</span></span>  | <span data-ttu-id="c5270-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c5270-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c5270-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="c5270-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="c5270-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="c5270-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c5270-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c5270-128">Request body</span></span>
<span data-ttu-id="c5270-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="c5270-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c5270-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c5270-130">Parameter</span></span>    | <span data-ttu-id="c5270-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5270-131">Type</span></span>   |<span data-ttu-id="c5270-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5270-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c5270-133">name</span><span class="sxs-lookup"><span data-stu-id="c5270-133">name</span></span>|<span data-ttu-id="c5270-134">string</span><span class="sxs-lookup"><span data-stu-id="c5270-134">string</span></span>|<span data-ttu-id="c5270-p105">Opcional. Nombre de la hoja de cálculo que se va a agregar. Si se especifica, el nombre debe ser único. Si no se especifica, Excel determina el nombre de la nueva hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="c5270-p105">Optional. The name of the worksheet to be added. If specified, name should be unqiue. If not specified, Excel determines the name of the new worksheet.</span></span>|

## <a name="response"></a><span data-ttu-id="c5270-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5270-139">Response</span></span>

<span data-ttu-id="c5270-140">Si tiene éxito, este método devuelve `200 OK` código de respuesta y [WorkbookWorksheet](../resources/worksheet.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c5270-140">If successful, this method returns `200 OK` response code and [WorkbookWorksheet](../resources/worksheet.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c5270-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c5270-141">Example</span></span>
<span data-ttu-id="c5270-142">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c5270-142">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c5270-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c5270-143">Request</span></span>
<span data-ttu-id="c5270-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c5270-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheetcollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/add
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```

##### <a name="response"></a><span data-ttu-id="c5270-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5270-145">Response</span></span>
<span data-ttu-id="c5270-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c5270-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookWorksheet"
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