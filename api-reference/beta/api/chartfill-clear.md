---
title: 'ChartFill: clear'
description: Borrar el color de relleno de un elemento de gráfico.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 3dc40f7ece8eb8bb5821e6ee924a80f0c19cf5f5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27843809"
---
# <a name="chartfill-clear"></a><span data-ttu-id="01fad-103">ChartFill: clear</span><span class="sxs-lookup"><span data-stu-id="01fad-103">ChartFill: clear</span></span>

> <span data-ttu-id="01fad-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="01fad-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="01fad-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="01fad-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="01fad-106">Borrar el color de relleno de un elemento de gráfico.</span><span class="sxs-lookup"><span data-stu-id="01fad-106">Clear the fill color of a chart element.</span></span>
## <a name="permissions"></a><span data-ttu-id="01fad-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="01fad-107">Permissions</span></span>
<span data-ttu-id="01fad-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="01fad-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="01fad-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="01fad-110">Permission type</span></span>      | <span data-ttu-id="01fad-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="01fad-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="01fad-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="01fad-112">Delegated (work or school account)</span></span> | <span data-ttu-id="01fad-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="01fad-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="01fad-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="01fad-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="01fad-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="01fad-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="01fad-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="01fad-116">Application</span></span> | <span data-ttu-id="01fad-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01fad-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="01fad-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01fad-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/format/fill/clear
POST /workbook/worksheets/{id|name}/charts(<name>)/title/format/fill/clear
POST /workbook/worksheets/{id|name}/charts(<name>)/legend/format/fill/clear

```
## <a name="request-headers"></a><span data-ttu-id="01fad-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="01fad-119">Request headers</span></span>
| <span data-ttu-id="01fad-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="01fad-120">Name</span></span>       | <span data-ttu-id="01fad-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="01fad-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="01fad-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="01fad-122">Authorization</span></span>  | <span data-ttu-id="01fad-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="01fad-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="01fad-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="01fad-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="01fad-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="01fad-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="01fad-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="01fad-128">Request body</span></span>

## <a name="response"></a><span data-ttu-id="01fad-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01fad-129">Response</span></span>

<span data-ttu-id="01fad-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01fad-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="01fad-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01fad-132">Example</span></span>
<span data-ttu-id="01fad-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="01fad-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="01fad-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01fad-134">Request</span></span>
<span data-ttu-id="01fad-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="01fad-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartfill_clear"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/format/fill/clear
```

##### <a name="response"></a><span data-ttu-id="01fad-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01fad-136">Response</span></span>
<span data-ttu-id="01fad-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01fad-137">Here is an example of the response.</span></span> 
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
  "description": "ChartFill: clear",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
