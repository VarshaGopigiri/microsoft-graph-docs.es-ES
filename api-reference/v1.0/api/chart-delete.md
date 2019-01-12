---
title: 'Chart: delete'
description: Elimina el objeto chart.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: e543e8188c5f850080daac00c4fe12a686af6a62
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923071"
---
# <a name="chart-delete"></a><span data-ttu-id="ebc98-103">Chart: delete</span><span class="sxs-lookup"><span data-stu-id="ebc98-103">Chart: delete</span></span>

<span data-ttu-id="ebc98-104">Elimina el objeto chart.</span><span class="sxs-lookup"><span data-stu-id="ebc98-104">Deletes the chart object.</span></span>
## <a name="permissions"></a><span data-ttu-id="ebc98-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ebc98-105">Permissions</span></span>
<span data-ttu-id="ebc98-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ebc98-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ebc98-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ebc98-108">Permission type</span></span>      | <span data-ttu-id="ebc98-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ebc98-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ebc98-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ebc98-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ebc98-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ebc98-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="ebc98-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ebc98-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ebc98-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ebc98-113">Not supported.</span></span>    |
|<span data-ttu-id="ebc98-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ebc98-114">Application</span></span> | <span data-ttu-id="ebc98-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ebc98-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ebc98-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ebc98-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/{name}/delete

```
## <a name="request-headers"></a><span data-ttu-id="ebc98-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ebc98-117">Request headers</span></span>
| <span data-ttu-id="ebc98-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="ebc98-118">Name</span></span>       | <span data-ttu-id="ebc98-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebc98-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="ebc98-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="ebc98-120">Authorization</span></span>  | <span data-ttu-id="ebc98-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ebc98-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ebc98-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="ebc98-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="ebc98-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="ebc98-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="ebc98-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ebc98-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="ebc98-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ebc98-127">Response</span></span>

<span data-ttu-id="ebc98-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ebc98-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ebc98-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ebc98-130">Example</span></span>
<span data-ttu-id="ebc98-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="ebc98-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="ebc98-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ebc98-132">Request</span></span>
<span data-ttu-id="ebc98-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ebc98-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chart_delete"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/delete
```

##### <a name="response"></a><span data-ttu-id="ebc98-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ebc98-134">Response</span></span>
<span data-ttu-id="ebc98-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ebc98-135">Here is an example of the response.</span></span> 
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
  "description": "Chart: delete",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
