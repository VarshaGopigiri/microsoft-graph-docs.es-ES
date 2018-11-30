---
title: 'Range: merge'
description: Combinar las celdas del rango en una región de la hoja de cálculo.
ms.openlocfilehash: be9ef68a6f3f62e3f9396a4b51a34b9f7e63199b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028701"
---
# <a name="range-merge"></a><span data-ttu-id="5d69e-103">Range: merge</span><span class="sxs-lookup"><span data-stu-id="5d69e-103">Range: merge</span></span>

<span data-ttu-id="5d69e-104">Combinar las celdas del rango en una región de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="5d69e-104">Merge the range cells into one region in the worksheet.</span></span>
## <a name="permissions"></a><span data-ttu-id="5d69e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="5d69e-105">Permissions</span></span>
<span data-ttu-id="5d69e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5d69e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5d69e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5d69e-108">Permission type</span></span>      | <span data-ttu-id="5d69e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5d69e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5d69e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5d69e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="5d69e-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5d69e-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="5d69e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5d69e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5d69e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d69e-113">Not supported.</span></span>    |
|<span data-ttu-id="5d69e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5d69e-114">Application</span></span> | <span data-ttu-id="5d69e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d69e-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5d69e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5d69e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/merge
POST /workbook/worksheets/{id|name}/range(address='<address>')/merge
POST /workbook/tables/{id|name}/columns/{id|name}/range/merge

```
## <a name="request-headers"></a><span data-ttu-id="5d69e-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5d69e-117">Request headers</span></span>
| <span data-ttu-id="5d69e-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="5d69e-118">Name</span></span>       | <span data-ttu-id="5d69e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d69e-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="5d69e-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="5d69e-120">Authorization</span></span>  | <span data-ttu-id="5d69e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5d69e-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5d69e-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="5d69e-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="5d69e-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="5d69e-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="5d69e-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5d69e-126">Request body</span></span>
<span data-ttu-id="5d69e-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="5d69e-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="5d69e-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5d69e-128">Parameter</span></span>    | <span data-ttu-id="5d69e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="5d69e-129">Type</span></span>   |<span data-ttu-id="5d69e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d69e-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5d69e-131">across</span><span class="sxs-lookup"><span data-stu-id="5d69e-131">across</span></span>|<span data-ttu-id="5d69e-132">boolean</span><span class="sxs-lookup"><span data-stu-id="5d69e-132">boolean</span></span>|<span data-ttu-id="5d69e-p104">Opcional. Verdadero para que se combinen las celdas de cada fila del rango especificado como celdas combinadas distintas. El valor predeterminado es falso.</span><span class="sxs-lookup"><span data-stu-id="5d69e-p104">Optional. Set true to merge cells in each row of the specified range as separate merged cells. The default value is false.</span></span>|

## <a name="response"></a><span data-ttu-id="5d69e-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d69e-136">Response</span></span>

<span data-ttu-id="5d69e-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5d69e-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5d69e-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5d69e-139">Example</span></span>
<span data-ttu-id="5d69e-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="5d69e-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="5d69e-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5d69e-141">Request</span></span>
<span data-ttu-id="5d69e-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5d69e-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_merge"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/merge
Content-type: application/json
Content-length: 20

{
  "across": true
}
```

##### <a name="response"></a><span data-ttu-id="5d69e-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d69e-143">Response</span></span>
<span data-ttu-id="5d69e-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5d69e-144">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: merge",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->