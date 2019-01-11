---
title: 'Filter: clear'
description: Borrar el filtro de la columna especificada.
localization_priority: Normal
ms.openlocfilehash: 9dd13991572d28e61dafce3049698117729161fb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838188"
---
# <a name="filter-clear"></a><span data-ttu-id="1f2e4-103">Filter: clear</span><span class="sxs-lookup"><span data-stu-id="1f2e4-103">Filter: clear</span></span>

> <span data-ttu-id="1f2e4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1f2e4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1f2e4-106">Borrar el filtro de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-106">Clear the filter on the given column.</span></span>
## <a name="permissions"></a><span data-ttu-id="1f2e4-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="1f2e4-107">Permissions</span></span>
<span data-ttu-id="1f2e4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1f2e4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1f2e4-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1f2e4-110">Permission type</span></span>      | <span data-ttu-id="1f2e4-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1f2e4-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1f2e4-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1f2e4-112">Delegated (work or school account)</span></span> | <span data-ttu-id="1f2e4-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1f2e4-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="1f2e4-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1f2e4-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1f2e4-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1f2e4-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="1f2e4-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1f2e4-116">Application</span></span> | <span data-ttu-id="1f2e4-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1f2e4-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1f2e4-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/{id|name}/filter/clear
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/{id|name}/filter/clear

```
## <a name="request-headers"></a><span data-ttu-id="1f2e4-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1f2e4-119">Request headers</span></span>
| <span data-ttu-id="1f2e4-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="1f2e4-120">Name</span></span>       | <span data-ttu-id="1f2e4-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f2e4-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="1f2e4-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="1f2e4-122">Authorization</span></span>  | <span data-ttu-id="1f2e4-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1f2e4-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1f2e4-125">Request body</span></span>

## <a name="response"></a><span data-ttu-id="1f2e4-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1f2e4-126">Response</span></span>

<span data-ttu-id="1f2e4-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1f2e4-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1f2e4-129">Example</span></span>
<span data-ttu-id="1f2e4-130">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-130">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="1f2e4-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1f2e4-131">Request</span></span>
<span data-ttu-id="1f2e4-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "filter_clear"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}/filter/clear
```

##### <a name="response"></a><span data-ttu-id="1f2e4-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1f2e4-133">Response</span></span>
<span data-ttu-id="1f2e4-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1f2e4-134">Here is an example of the response.</span></span> 
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
  "description": "Filter: clear",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
