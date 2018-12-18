---
title: 'WorksheetCollection: add'
description: .Activate() en él.
author: lumine2008
ms.openlocfilehash: fc22e4b45732c9ef197ad9b1172ec87c8becbfc5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27346602"
---
# <a name="worksheetcollection-add"></a><span data-ttu-id="dacce-103">WorksheetCollection: add</span><span class="sxs-lookup"><span data-stu-id="dacce-103">WorksheetCollection: add</span></span>

<span data-ttu-id="dacce-p101">Agrega una nueva hoja al libro. La hoja de cálculo se agregará al final de las hojas de cálculo existentes. Si desea activar la hoja de cálculo recién agregada, llame en ella a ".activate().</span><span class="sxs-lookup"><span data-stu-id="dacce-p101">Adds a new worksheet to the workbook. The worksheet will be added at the end of existing worksheets. If you wish to activate the newly added worksheet, call ".activate() on it.</span></span>
## <a name="permissions"></a><span data-ttu-id="dacce-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="dacce-107">Permissions</span></span>
<span data-ttu-id="dacce-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dacce-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dacce-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dacce-110">Permission type</span></span>      | <span data-ttu-id="dacce-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dacce-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dacce-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dacce-112">Delegated (work or school account)</span></span> | <span data-ttu-id="dacce-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="dacce-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="dacce-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dacce-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dacce-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dacce-115">Not supported.</span></span>    |
|<span data-ttu-id="dacce-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dacce-116">Application</span></span> | <span data-ttu-id="dacce-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dacce-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="dacce-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dacce-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/

```
## <a name="request-headers"></a><span data-ttu-id="dacce-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dacce-119">Request headers</span></span>
| <span data-ttu-id="dacce-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="dacce-120">Name</span></span>       | <span data-ttu-id="dacce-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="dacce-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="dacce-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="dacce-122">Authorization</span></span>  | <span data-ttu-id="dacce-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dacce-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="dacce-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="dacce-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="dacce-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="dacce-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="dacce-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dacce-128">Request body</span></span>
<span data-ttu-id="dacce-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="dacce-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="dacce-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dacce-130">Parameter</span></span>    | <span data-ttu-id="dacce-131">Type</span><span class="sxs-lookup"><span data-stu-id="dacce-131">Type</span></span>   |<span data-ttu-id="dacce-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="dacce-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dacce-133">name</span><span class="sxs-lookup"><span data-stu-id="dacce-133">name</span></span>|<span data-ttu-id="dacce-134">string</span><span class="sxs-lookup"><span data-stu-id="dacce-134">string</span></span>|<span data-ttu-id="dacce-p105">Opcional. Nombre de la hoja de cálculo que se va a agregar. Si se especifica, el nombre debe ser único. Si no se especifica, Excel determina el nombre de la nueva hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="dacce-p105">Optional. The name of the worksheet to be added. If specified, name should be unqiue. If not specified, Excel determines the name of the new worksheet.</span></span>|

## <a name="response"></a><span data-ttu-id="dacce-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dacce-139">Response</span></span>

<span data-ttu-id="dacce-140">Si tiene éxito, este método devuelve `200 OK` código de respuesta y [WorkbookWorksheet](../resources/worksheet.md) objeto en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dacce-140">If successful, this method returns `200 OK` response code and [WorkbookWorksheet](../resources/worksheet.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dacce-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dacce-141">Example</span></span>
<span data-ttu-id="dacce-142">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="dacce-142">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="dacce-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dacce-143">Request</span></span>
<span data-ttu-id="dacce-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dacce-144">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="dacce-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dacce-145">Response</span></span>
<span data-ttu-id="dacce-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dacce-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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