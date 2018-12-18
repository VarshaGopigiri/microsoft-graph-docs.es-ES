---
title: 'Range: delete'
description: Elimina las celdas asociadas al rango.
author: lumine2008
ms.openlocfilehash: 00b6d8a35012a3e6d1e6c0755a077d0575baa00e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27352706"
---
# <a name="range-delete"></a><span data-ttu-id="14892-103">Range: delete</span><span class="sxs-lookup"><span data-stu-id="14892-103">Range: delete</span></span>

> <span data-ttu-id="14892-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="14892-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="14892-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="14892-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="14892-106">Elimina las celdas asociadas al rango.</span><span class="sxs-lookup"><span data-stu-id="14892-106">Deletes the cells associated with the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="14892-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="14892-107">Permissions</span></span>
<span data-ttu-id="14892-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="14892-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="14892-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="14892-110">Permission type</span></span>      | <span data-ttu-id="14892-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="14892-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="14892-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="14892-112">Delegated (work or school account)</span></span> | <span data-ttu-id="14892-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="14892-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="14892-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="14892-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="14892-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="14892-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="14892-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="14892-116">Application</span></span> | <span data-ttu-id="14892-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="14892-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="14892-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="14892-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/delete
POST /workbook/worksheets/{id|name}/range(address='<address>')/delete
POST /workbook/tables/{id|name}/columns/{id|name}/range/delete

```
## <a name="request-headers"></a><span data-ttu-id="14892-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="14892-119">Request headers</span></span>
| <span data-ttu-id="14892-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="14892-120">Name</span></span>       | <span data-ttu-id="14892-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="14892-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="14892-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="14892-122">Authorization</span></span>  | <span data-ttu-id="14892-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="14892-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="14892-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="14892-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="14892-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="14892-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="14892-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="14892-128">Request body</span></span>
<span data-ttu-id="14892-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="14892-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="14892-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="14892-130">Parameter</span></span>    | <span data-ttu-id="14892-131">Type</span><span class="sxs-lookup"><span data-stu-id="14892-131">Type</span></span>   |<span data-ttu-id="14892-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="14892-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="14892-133">Shift</span><span class="sxs-lookup"><span data-stu-id="14892-133">shift</span></span>|<span data-ttu-id="14892-134">string</span><span class="sxs-lookup"><span data-stu-id="14892-134">string</span></span>|<span data-ttu-id="14892-p105">Especifica hacia dónde se desplazarán las celdas.  Valores posibles: `Up`, `Left`.</span><span class="sxs-lookup"><span data-stu-id="14892-p105">Specifies which way to shift the cells.  Possible values are: `Up`, `Left`.</span></span>|

## <a name="response"></a><span data-ttu-id="14892-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="14892-137">Response</span></span>

<span data-ttu-id="14892-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="14892-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="14892-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="14892-140">Example</span></span>
<span data-ttu-id="14892-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="14892-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="14892-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="14892-142">Request</span></span>
<span data-ttu-id="14892-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="14892-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_delete"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/delete
Content-type: application/json
Content-length: 28

{
  "shift": "shift-value"
}
```

##### <a name="response"></a><span data-ttu-id="14892-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="14892-144">Response</span></span>
<span data-ttu-id="14892-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="14892-145">Here is an example of the response.</span></span> 
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
  "description": "Range: delete",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->