---
title: 'Table: clearFilters'
description: Borra todos los filtros aplicados actualmente en la tabla.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 781af9b09270d2e165113edd03dcb25fc0ecfeab
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889757"
---
# <a name="table-clearfilters"></a><span data-ttu-id="76dda-103">Table: clearFilters</span><span class="sxs-lookup"><span data-stu-id="76dda-103">Table: clearFilters</span></span>

<span data-ttu-id="76dda-104">Borra todos los filtros aplicados actualmente en la tabla.</span><span class="sxs-lookup"><span data-stu-id="76dda-104">Clears all the filters currently applied on the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="76dda-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="76dda-105">Permissions</span></span>
<span data-ttu-id="76dda-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="76dda-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="76dda-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="76dda-108">Permission type</span></span>      | <span data-ttu-id="76dda-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="76dda-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="76dda-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="76dda-110">Delegated (work or school account)</span></span> | <span data-ttu-id="76dda-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="76dda-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="76dda-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="76dda-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="76dda-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="76dda-113">Not supported.</span></span>    |
|<span data-ttu-id="76dda-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="76dda-114">Application</span></span> | <span data-ttu-id="76dda-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="76dda-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="76dda-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="76dda-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/clearFilters
POST /workbook/worksheets/{id|name}/tables/{id|name}/clearFilters

```
## <a name="request-headers"></a><span data-ttu-id="76dda-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="76dda-117">Request headers</span></span>
| <span data-ttu-id="76dda-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="76dda-118">Name</span></span>       | <span data-ttu-id="76dda-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="76dda-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="76dda-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="76dda-120">Authorization</span></span>  | <span data-ttu-id="76dda-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="76dda-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="76dda-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="76dda-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="76dda-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="76dda-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="76dda-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="76dda-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="76dda-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76dda-127">Response</span></span>

<span data-ttu-id="76dda-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="76dda-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="76dda-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="76dda-130">Example</span></span>
<span data-ttu-id="76dda-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="76dda-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="76dda-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="76dda-132">Request</span></span>
<span data-ttu-id="76dda-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="76dda-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "table_clearfilters"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/clearFilters
```

##### <a name="response"></a><span data-ttu-id="76dda-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76dda-134">Response</span></span>
<span data-ttu-id="76dda-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="76dda-135">Here is an example of the response.</span></span> 
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
  "description": "Table: clearFilters",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
