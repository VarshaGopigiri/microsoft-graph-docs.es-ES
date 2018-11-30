---
title: 'Filter: apply'
description: Aplicar los criterios de filtro especificados en la columna especificada.
ms.openlocfilehash: e799b4e4b5f94664e9420e810075205691e1bd96
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083024"
---
# <a name="filter-apply"></a><span data-ttu-id="f1de8-103">Filter: apply</span><span class="sxs-lookup"><span data-stu-id="f1de8-103">Filter: apply</span></span>

> <span data-ttu-id="f1de8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f1de8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f1de8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f1de8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f1de8-106">Aplicar los criterios de filtro especificados en la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="f1de8-106">Apply the given filter criteria on the given column.</span></span>
## <a name="permissions"></a><span data-ttu-id="f1de8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f1de8-107">Permissions</span></span>
<span data-ttu-id="f1de8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f1de8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f1de8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f1de8-110">Permission type</span></span>      | <span data-ttu-id="f1de8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f1de8-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f1de8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f1de8-112">Delegated (work or school account)</span></span> | <span data-ttu-id="f1de8-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f1de8-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f1de8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f1de8-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f1de8-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f1de8-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f1de8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f1de8-116">Application</span></span> | <span data-ttu-id="f1de8-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f1de8-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f1de8-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f1de8-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/{id|name}/filter/apply
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/{id|name}/filter/apply

```
## <a name="request-headers"></a><span data-ttu-id="f1de8-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f1de8-119">Request headers</span></span>
| <span data-ttu-id="f1de8-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="f1de8-120">Name</span></span>       | <span data-ttu-id="f1de8-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1de8-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f1de8-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="f1de8-122">Authorization</span></span>  | <span data-ttu-id="f1de8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f1de8-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f1de8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f1de8-125">Request body</span></span>
<span data-ttu-id="f1de8-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="f1de8-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f1de8-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f1de8-127">Parameter</span></span>    | <span data-ttu-id="f1de8-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1de8-128">Type</span></span>   |<span data-ttu-id="f1de8-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1de8-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f1de8-130">criterios</span><span class="sxs-lookup"><span data-stu-id="f1de8-130">criteria</span></span>|<span data-ttu-id="f1de8-131">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="f1de8-131">FilterCriteria</span></span>|<span data-ttu-id="f1de8-132">Criterios que se aplicarán.</span><span class="sxs-lookup"><span data-stu-id="f1de8-132">The criteria to apply.</span></span>|

## <a name="response"></a><span data-ttu-id="f1de8-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f1de8-133">Response</span></span>

<span data-ttu-id="f1de8-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1de8-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f1de8-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f1de8-136">Example</span></span>
<span data-ttu-id="f1de8-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f1de8-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f1de8-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f1de8-138">Request</span></span>
<span data-ttu-id="f1de8-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f1de8-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "filter_apply"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}/filter/apply
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

##### <a name="response"></a><span data-ttu-id="f1de8-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f1de8-140">Response</span></span>
<span data-ttu-id="f1de8-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1de8-141">Here is an example of the response.</span></span> 
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
  "description": "Filter: apply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->