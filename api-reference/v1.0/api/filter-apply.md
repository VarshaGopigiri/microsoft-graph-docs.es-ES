---
title: 'Filter: apply'
description: Aplicar los criterios de filtro especificados en la columna especificada.
ms.openlocfilehash: b60c3da521f2b5700650450d308b7f26fcd4d1a8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029943"
---
# <a name="filter-apply"></a><span data-ttu-id="2c5c0-103">Filter: apply</span><span class="sxs-lookup"><span data-stu-id="2c5c0-103">Filter: apply</span></span>

<span data-ttu-id="2c5c0-104">Aplicar los criterios de filtro especificados en la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="2c5c0-104">Apply the given filter criteria on the given column.</span></span>
## <a name="permissions"></a><span data-ttu-id="2c5c0-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="2c5c0-105">Permissions</span></span>
<span data-ttu-id="2c5c0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2c5c0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2c5c0-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2c5c0-108">Permission type</span></span>      | <span data-ttu-id="2c5c0-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2c5c0-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2c5c0-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2c5c0-110">Delegated (work or school account)</span></span> | <span data-ttu-id="2c5c0-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2c5c0-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="2c5c0-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2c5c0-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2c5c0-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2c5c0-113">Not supported.</span></span>    |
|<span data-ttu-id="2c5c0-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2c5c0-114">Application</span></span> | <span data-ttu-id="2c5c0-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2c5c0-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2c5c0-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2c5c0-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/{id|name}/filter/apply
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/{id|name}/filter/apply

```
## <a name="request-headers"></a><span data-ttu-id="2c5c0-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2c5c0-117">Request headers</span></span>
| <span data-ttu-id="2c5c0-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c5c0-118">Name</span></span>       | <span data-ttu-id="2c5c0-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c5c0-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="2c5c0-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="2c5c0-120">Authorization</span></span>  | <span data-ttu-id="2c5c0-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c5c0-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2c5c0-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2c5c0-123">Request body</span></span>
<span data-ttu-id="2c5c0-124">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="2c5c0-124">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="2c5c0-125">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2c5c0-125">Parameter</span></span>    | <span data-ttu-id="2c5c0-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="2c5c0-126">Type</span></span>   |<span data-ttu-id="2c5c0-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c5c0-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2c5c0-128">criterios</span><span class="sxs-lookup"><span data-stu-id="2c5c0-128">criteria</span></span>|<span data-ttu-id="2c5c0-129">WorkbookFilterCriteria</span><span class="sxs-lookup"><span data-stu-id="2c5c0-129">WorkbookFilterCriteria</span></span>|<span data-ttu-id="2c5c0-130">Criterios que se aplicarán.</span><span class="sxs-lookup"><span data-stu-id="2c5c0-130">The criteria to apply.</span></span>|

## <a name="response"></a><span data-ttu-id="2c5c0-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c5c0-131">Response</span></span>

<span data-ttu-id="2c5c0-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c5c0-p103">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2c5c0-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2c5c0-134">Example</span></span>
<span data-ttu-id="2c5c0-135">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2c5c0-135">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="2c5c0-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2c5c0-136">Request</span></span>
<span data-ttu-id="2c5c0-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2c5c0-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "filter_apply"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}/filter/apply
Content-type: application/json
Content-length: 321

{
  "criteria": {
    "criterion1": "criterion1-value",
    "criterion2": "criterion2-value",
    "color": "color-value",
    "operator": {
    },
    "icon": {
      "set": "set-value",
      "index": 99
    },
    "dynamicCriteria": "dynamicCriteria-value",
    "values": {
    },
    "filterOn": "filterOn-value"
  }
}
```

##### <a name="response"></a><span data-ttu-id="2c5c0-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c5c0-138">Response</span></span>
<span data-ttu-id="2c5c0-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c5c0-139">Here is an example of the response.</span></span> 
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
  "description": "Filter: apply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->