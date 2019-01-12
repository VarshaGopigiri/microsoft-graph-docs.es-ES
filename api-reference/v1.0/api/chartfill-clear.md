---
title: 'ChartFill: clear'
description: Borrar el color de relleno de un elemento de gráfico.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: b9a43093d00f6230e10333bf3ea0d8adb5a859f1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918045"
---
# <a name="chartfill-clear"></a><span data-ttu-id="ff83f-103">ChartFill: clear</span><span class="sxs-lookup"><span data-stu-id="ff83f-103">ChartFill: clear</span></span>

<span data-ttu-id="ff83f-104">Borrar el color de relleno de un elemento de gráfico.</span><span class="sxs-lookup"><span data-stu-id="ff83f-104">Clear the fill color of a chart element.</span></span>
## <a name="permissions"></a><span data-ttu-id="ff83f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="ff83f-105">Permissions</span></span>
<span data-ttu-id="ff83f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ff83f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ff83f-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ff83f-108">Permission type</span></span>      | <span data-ttu-id="ff83f-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ff83f-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ff83f-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ff83f-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ff83f-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ff83f-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="ff83f-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ff83f-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ff83f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ff83f-113">Not supported.</span></span>    |
|<span data-ttu-id="ff83f-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ff83f-114">Application</span></span> | <span data-ttu-id="ff83f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ff83f-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ff83f-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ff83f-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/{name}/format/fill/clear
POST /workbook/worksheets/{id|name}/charts/{name}/title/format/fill/clear
POST /workbook/worksheets/{id|name}/charts/{name}/legend/format/fill/clear

```
## <a name="request-headers"></a><span data-ttu-id="ff83f-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ff83f-117">Request headers</span></span>
| <span data-ttu-id="ff83f-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="ff83f-118">Name</span></span>       | <span data-ttu-id="ff83f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff83f-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="ff83f-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="ff83f-120">Authorization</span></span>  | <span data-ttu-id="ff83f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ff83f-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ff83f-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="ff83f-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="ff83f-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="ff83f-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="ff83f-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ff83f-126">Request body</span></span>
<span data-ttu-id="ff83f-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ff83f-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ff83f-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ff83f-128">Response</span></span>

<span data-ttu-id="ff83f-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ff83f-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ff83f-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ff83f-131">Example</span></span>
<span data-ttu-id="ff83f-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="ff83f-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="ff83f-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ff83f-133">Request</span></span>
<span data-ttu-id="ff83f-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ff83f-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartfill_clear"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/format/fill/clear
```

##### <a name="response"></a><span data-ttu-id="ff83f-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ff83f-135">Response</span></span>
<span data-ttu-id="ff83f-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ff83f-136">Here is an example of the response.</span></span> 
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
  "description": "ChartFill: clear",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
