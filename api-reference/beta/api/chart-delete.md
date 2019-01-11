---
title: 'Chart: delete'
description: Elimina el objeto chart.
author: lumine2008
localization_priority: Normal
ms.openlocfilehash: 7988c515d7b350653460721f9352b617b7853f7f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27813569"
---
# <a name="chart-delete"></a><span data-ttu-id="2baa2-103">Chart: delete</span><span class="sxs-lookup"><span data-stu-id="2baa2-103">Chart: delete</span></span>

> <span data-ttu-id="2baa2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2baa2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2baa2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2baa2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2baa2-106">Elimina el objeto chart.</span><span class="sxs-lookup"><span data-stu-id="2baa2-106">Deletes the chart object.</span></span>
## <a name="permissions"></a><span data-ttu-id="2baa2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="2baa2-107">Permissions</span></span>
<span data-ttu-id="2baa2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2baa2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2baa2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2baa2-110">Permission type</span></span>      | <span data-ttu-id="2baa2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2baa2-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2baa2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2baa2-112">Delegated (work or school account)</span></span> | <span data-ttu-id="2baa2-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2baa2-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="2baa2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2baa2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2baa2-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2baa2-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="2baa2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2baa2-116">Application</span></span> | <span data-ttu-id="2baa2-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2baa2-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2baa2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2baa2-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/delete

```
## <a name="request-headers"></a><span data-ttu-id="2baa2-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2baa2-119">Request headers</span></span>
| <span data-ttu-id="2baa2-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="2baa2-120">Name</span></span>       | <span data-ttu-id="2baa2-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2baa2-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="2baa2-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="2baa2-122">Authorization</span></span>  | <span data-ttu-id="2baa2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2baa2-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2baa2-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="2baa2-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="2baa2-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="2baa2-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="2baa2-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2baa2-128">Request body</span></span>

## <a name="response"></a><span data-ttu-id="2baa2-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2baa2-129">Response</span></span>

<span data-ttu-id="2baa2-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2baa2-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2baa2-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2baa2-132">Example</span></span>
<span data-ttu-id="2baa2-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2baa2-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="2baa2-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2baa2-134">Request</span></span>
<span data-ttu-id="2baa2-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2baa2-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chart_delete"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/delete
```

##### <a name="response"></a><span data-ttu-id="2baa2-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2baa2-136">Response</span></span>
<span data-ttu-id="2baa2-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2baa2-137">Here is an example of the response.</span></span> 
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
  "description": "Chart: delete",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
