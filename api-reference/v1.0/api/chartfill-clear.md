---
title: 'ChartFill: clear'
description: Borrar el color de relleno de un elemento de gráfico.
author: lumine2008
ms.openlocfilehash: 440cffba49522621372201cdca8a4ddcdadf5c5f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27341317"
---
# <a name="chartfill-clear"></a><span data-ttu-id="3d10b-103">ChartFill: clear</span><span class="sxs-lookup"><span data-stu-id="3d10b-103">ChartFill: clear</span></span>

<span data-ttu-id="3d10b-104">Borrar el color de relleno de un elemento de gráfico.</span><span class="sxs-lookup"><span data-stu-id="3d10b-104">Clear the fill color of a chart element.</span></span>
## <a name="permissions"></a><span data-ttu-id="3d10b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="3d10b-105">Permissions</span></span>
<span data-ttu-id="3d10b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3d10b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3d10b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3d10b-108">Permission type</span></span>      | <span data-ttu-id="3d10b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3d10b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3d10b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3d10b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="3d10b-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3d10b-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="3d10b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3d10b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3d10b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3d10b-113">Not supported.</span></span>    |
|<span data-ttu-id="3d10b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3d10b-114">Application</span></span> | <span data-ttu-id="3d10b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3d10b-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="3d10b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3d10b-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/{name}/format/fill/clear
POST /workbook/worksheets/{id|name}/charts/{name}/title/format/fill/clear
POST /workbook/worksheets/{id|name}/charts/{name}/legend/format/fill/clear

```
## <a name="request-headers"></a><span data-ttu-id="3d10b-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3d10b-117">Request headers</span></span>
| <span data-ttu-id="3d10b-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="3d10b-118">Name</span></span>       | <span data-ttu-id="3d10b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d10b-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="3d10b-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="3d10b-120">Authorization</span></span>  | <span data-ttu-id="3d10b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3d10b-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="3d10b-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="3d10b-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="3d10b-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="3d10b-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="3d10b-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3d10b-126">Request body</span></span>
<span data-ttu-id="3d10b-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3d10b-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3d10b-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d10b-128">Response</span></span>

<span data-ttu-id="3d10b-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d10b-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3d10b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d10b-131">Example</span></span>
<span data-ttu-id="3d10b-132">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="3d10b-132">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="3d10b-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3d10b-133">Request</span></span>
<span data-ttu-id="3d10b-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3d10b-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartfill_clear"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/format/fill/clear
```

##### <a name="response"></a><span data-ttu-id="3d10b-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d10b-135">Response</span></span>
<span data-ttu-id="3d10b-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d10b-136">Here is an example of the response.</span></span> 
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