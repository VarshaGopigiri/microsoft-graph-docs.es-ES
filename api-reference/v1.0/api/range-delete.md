---
title: 'Range: delete'
description: Elimina las celdas asociadas al rango.
ms.openlocfilehash: fef8caad6099e37698db0c501c7fb8e2c7ef452e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029249"
---
# <a name="range-delete"></a><span data-ttu-id="5f66f-103">Range: delete</span><span class="sxs-lookup"><span data-stu-id="5f66f-103">Range: delete</span></span>

<span data-ttu-id="5f66f-104">Elimina las celdas asociadas al rango.</span><span class="sxs-lookup"><span data-stu-id="5f66f-104">Deletes the cells associated with the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="5f66f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="5f66f-105">Permissions</span></span>
<span data-ttu-id="5f66f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5f66f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5f66f-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5f66f-108">Permission type</span></span>      | <span data-ttu-id="5f66f-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5f66f-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5f66f-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5f66f-110">Delegated (work or school account)</span></span> | <span data-ttu-id="5f66f-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5f66f-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="5f66f-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5f66f-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5f66f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f66f-113">Not supported.</span></span>    |
|<span data-ttu-id="5f66f-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5f66f-114">Application</span></span> | <span data-ttu-id="5f66f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f66f-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5f66f-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5f66f-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/delete
POST /workbook/worksheets/{id|name}/range(address='<address>')/delete
POST /workbook/tables/{id|name}/columns/{id|name}/range/delete

```
## <a name="request-headers"></a><span data-ttu-id="5f66f-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5f66f-117">Request headers</span></span>
| <span data-ttu-id="5f66f-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="5f66f-118">Name</span></span>       | <span data-ttu-id="5f66f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f66f-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="5f66f-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="5f66f-120">Authorization</span></span>  | <span data-ttu-id="5f66f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5f66f-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5f66f-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="5f66f-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="5f66f-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="5f66f-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="5f66f-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5f66f-126">Request body</span></span>
<span data-ttu-id="5f66f-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="5f66f-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="5f66f-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5f66f-128">Parameter</span></span>    | <span data-ttu-id="5f66f-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f66f-129">Type</span></span>   |<span data-ttu-id="5f66f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f66f-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5f66f-131">Shift</span><span class="sxs-lookup"><span data-stu-id="5f66f-131">shift</span></span>|<span data-ttu-id="5f66f-132">string</span><span class="sxs-lookup"><span data-stu-id="5f66f-132">string</span></span>|<span data-ttu-id="5f66f-133">Especifica el modo de desplazar las celdas.</span><span class="sxs-lookup"><span data-stu-id="5f66f-133">Specifies which way to shift the cells.</span></span>  <span data-ttu-id="5f66f-134">Los valores posibles son: `Up`, `Left`.</span><span class="sxs-lookup"><span data-stu-id="5f66f-134">The possible values are: `Up`, `Left`.</span></span>|

## <a name="response"></a><span data-ttu-id="5f66f-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f66f-135">Response</span></span>

<span data-ttu-id="5f66f-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f66f-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5f66f-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5f66f-138">Example</span></span>
<span data-ttu-id="5f66f-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="5f66f-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="5f66f-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5f66f-140">Request</span></span>
<span data-ttu-id="5f66f-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5f66f-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_delete"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/delete
Content-type: application/json
Content-length: 28

{
  "shift": "shift-value"
}
```

##### <a name="response"></a><span data-ttu-id="5f66f-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f66f-142">Response</span></span>
<span data-ttu-id="5f66f-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f66f-143">Here is an example of the response.</span></span> 
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
  "description": "Range: delete",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->