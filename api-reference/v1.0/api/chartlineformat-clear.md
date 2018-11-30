---
title: 'ChartLineFormat: clear'
description: Borrar el formato de línea de un elemento de gráfico.
ms.openlocfilehash: 0bb03fc43c9a8b059d384f59c2691b995a4e533e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028579"
---
# <a name="chartlineformat-clear"></a><span data-ttu-id="e3283-103">ChartLineFormat: clear</span><span class="sxs-lookup"><span data-stu-id="e3283-103">ChartLineFormat: clear</span></span>

<span data-ttu-id="e3283-104">Borrar el formato de línea de un elemento de gráfico.</span><span class="sxs-lookup"><span data-stu-id="e3283-104">Clear the line format of a chart element.</span></span>
## <a name="permissions"></a><span data-ttu-id="e3283-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="e3283-105">Permissions</span></span>
<span data-ttu-id="e3283-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e3283-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e3283-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e3283-108">Permission type</span></span>      | <span data-ttu-id="e3283-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e3283-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e3283-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e3283-110">Delegated (work or school account)</span></span> | <span data-ttu-id="e3283-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e3283-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="e3283-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e3283-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e3283-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e3283-113">Not supported.</span></span>    |
|<span data-ttu-id="e3283-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e3283-114">Application</span></span> | <span data-ttu-id="e3283-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e3283-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e3283-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e3283-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/{name}/axes/seriesAxis/format/line/clear
POST /workbook/worksheets/{id|name}/charts/{name}/axes/categoryaxis/format/line/clear
POST /workbook/worksheets/{id|name}/charts/{name}/axes/seriesAxis/majorgridlines/format/line/clear

```
## <a name="request-headers"></a><span data-ttu-id="e3283-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e3283-117">Request headers</span></span>
| <span data-ttu-id="e3283-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="e3283-118">Name</span></span>       | <span data-ttu-id="e3283-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3283-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e3283-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="e3283-120">Authorization</span></span>  | <span data-ttu-id="e3283-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e3283-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e3283-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="e3283-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="e3283-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="e3283-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="e3283-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e3283-126">Request body</span></span>

## <a name="response"></a><span data-ttu-id="e3283-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3283-127">Response</span></span>

<span data-ttu-id="e3283-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e3283-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e3283-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e3283-130">Example</span></span>
<span data-ttu-id="e3283-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="e3283-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="e3283-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e3283-132">Request</span></span>
<span data-ttu-id="e3283-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e3283-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartlineformat_clear"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/axes/seriesAxis/format/line/clear
```

##### <a name="response"></a><span data-ttu-id="e3283-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3283-134">Response</span></span>
<span data-ttu-id="e3283-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e3283-135">Here is an example of the response.</span></span> 
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
  "description": "ChartLineFormat: clear",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->