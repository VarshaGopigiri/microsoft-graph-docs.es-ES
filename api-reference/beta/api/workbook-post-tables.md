---
title: Crear tabla
description: Use esta API para crear un objeto Table.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: 39251598191c89c3d5189c7d9191cf3dfd7e1936
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27948299"
---
# <a name="create-table"></a><span data-ttu-id="3851d-103">Crear tabla</span><span class="sxs-lookup"><span data-stu-id="3851d-103">Create table</span></span>

> <span data-ttu-id="3851d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3851d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3851d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3851d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3851d-106">Use esta API para crear un objeto Table.</span><span class="sxs-lookup"><span data-stu-id="3851d-106">Use this API to create a new Table.</span></span>
## <a name="permissions"></a><span data-ttu-id="3851d-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3851d-107">Permissions</span></span>
<span data-ttu-id="3851d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3851d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3851d-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3851d-110">Permission type</span></span>      | <span data-ttu-id="3851d-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3851d-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3851d-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3851d-112">Delegated (work or school account)</span></span> | <span data-ttu-id="3851d-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3851d-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="3851d-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3851d-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3851d-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3851d-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="3851d-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3851d-116">Application</span></span> | <span data-ttu-id="3851d-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3851d-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="3851d-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3851d-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/$/add

```
## <a name="request-headers"></a><span data-ttu-id="3851d-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3851d-119">Request headers</span></span>
| <span data-ttu-id="3851d-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="3851d-120">Name</span></span>       | <span data-ttu-id="3851d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="3851d-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="3851d-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="3851d-122">Authorization</span></span>  | <span data-ttu-id="3851d-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3851d-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="3851d-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="3851d-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="3851d-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="3851d-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="3851d-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3851d-128">Request body</span></span>
<span data-ttu-id="3851d-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="3851d-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="3851d-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3851d-130">Parameter</span></span>           | <span data-ttu-id="3851d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="3851d-131">Type</span></span>      |<span data-ttu-id="3851d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="3851d-132">Description</span></span>|
|:---------------|:----------|:----------|
| <span data-ttu-id="3851d-133">Dirección</span><span class="sxs-lookup"><span data-stu-id="3851d-133">Address</span></span>  | <span data-ttu-id="3851d-134">string</span><span class="sxs-lookup"><span data-stu-id="3851d-134">string</span></span>| <span data-ttu-id="3851d-p105">Dirección de intervalo. Si llama a esta API desde la ruta de acceso `worksheets/{id or name}/tables/add`, no tiene que proporcionar el prefijo del nombre de hoja en la dirección. En cambio, si la llama desde la ruta de acceso `workbook/tables/add`, deberá proporcionar el nombre de la hoja en la que se debe crear la tabla (ejemplo: `sheet1!A1:D4`)</span><span class="sxs-lookup"><span data-stu-id="3851d-p105">Range address. If you are calling this API off of `worksheets/{id or name}/tables/add` path, there is no need to for sheet name prefix in the address. However, if you are calling this off of `workbook/tables/add` path, then supply the sheet name on which the table needs to be created (example: `sheet1!A1:D4`)</span></span>|
| <span data-ttu-id="3851d-138">hasHeaders</span><span class="sxs-lookup"><span data-stu-id="3851d-138">hasHeaders</span></span>  | <span data-ttu-id="3851d-139">boolean</span><span class="sxs-lookup"><span data-stu-id="3851d-139">boolean</span></span>|<span data-ttu-id="3851d-p106">Valor booleano que indica si el intervalo tiene etiquetas de columna. Si el origen no contiene encabezados (es decir, cuando esta propiedad se establece en false), Excel generará de forma automática el encabezado desplazando los datos hacia abajo una fila.</span><span class="sxs-lookup"><span data-stu-id="3851d-p106">Boolean value that indicates whether the range has column labels. If the source does not contain headers (i.e,. when this property set to false), Excel will automatically generate header shifting the data down by one row.</span></span>|

## <a name="response"></a><span data-ttu-id="3851d-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3851d-143">Response</span></span>

<span data-ttu-id="3851d-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [Table](../resources/table.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3851d-144">If successful, this method returns `201 Created` response code and [Table](../resources/table.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3851d-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3851d-145">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3851d-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3851d-146">Request</span></span>
<span data-ttu-id="3851d-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3851d-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_table_from_workbook"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/$/add
Content-type: application/json
Content-length: 109

{
  "address": "A1:D8",
  "hasHeaders": false
}
```
##### <a name="response"></a><span data-ttu-id="3851d-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3851d-148">Response</span></span>
<span data-ttu-id="3851d-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3851d-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.table"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 109

{
  "id": "99",
  "name": "name-value",
  "showHeaders": true,
  "showTotals": true,
  "style": "style-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Table",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
