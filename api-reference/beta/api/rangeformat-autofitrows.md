---
title: 'RangeFormat: autofitRows'
description: Cambia el alto de las filas del rango actual para obtener el ajuste perfecto (según los datos actuales de las columnas).
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 6983ea7668bd6bf41956c93df8988f81928012ea
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27949538"
---
# <a name="rangeformat-autofitrows"></a><span data-ttu-id="12e8f-103">RangeFormat: autofitRows</span><span class="sxs-lookup"><span data-stu-id="12e8f-103">RangeFormat: autofitRows</span></span>

> <span data-ttu-id="12e8f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="12e8f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="12e8f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="12e8f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="12e8f-106">Cambia el alto de las filas del rango actual para obtener el ajuste perfecto (según los datos actuales de las columnas).</span><span class="sxs-lookup"><span data-stu-id="12e8f-106">Changes the height of the rows of the current range to achieve the best fit, based on the current data in the columns.</span></span>
## <a name="permissions"></a><span data-ttu-id="12e8f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="12e8f-107">Permissions</span></span>
<span data-ttu-id="12e8f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="12e8f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="12e8f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="12e8f-110">Permission type</span></span>      | <span data-ttu-id="12e8f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="12e8f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="12e8f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="12e8f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="12e8f-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="12e8f-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="12e8f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="12e8f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="12e8f-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="12e8f-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="12e8f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="12e8f-116">Application</span></span> | <span data-ttu-id="12e8f-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="12e8f-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="12e8f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="12e8f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/format/autofitRows
POST /workbook/worksheets/{id|name}/range(address='<address>')/format/autofitRows
POST /workbook/tables/{id|name}/columns/{id|name}/range/format/autofitRows

```
## <a name="request-headers"></a><span data-ttu-id="12e8f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="12e8f-119">Request headers</span></span>
| <span data-ttu-id="12e8f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="12e8f-120">Name</span></span>       | <span data-ttu-id="12e8f-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="12e8f-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="12e8f-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="12e8f-122">Authorization</span></span>  | <span data-ttu-id="12e8f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="12e8f-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="12e8f-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="12e8f-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="12e8f-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="12e8f-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="12e8f-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="12e8f-128">Request body</span></span>

## <a name="response"></a><span data-ttu-id="12e8f-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="12e8f-129">Response</span></span>

<span data-ttu-id="12e8f-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="12e8f-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="12e8f-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="12e8f-132">Example</span></span>
<span data-ttu-id="12e8f-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="12e8f-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="12e8f-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="12e8f-134">Request</span></span>
<span data-ttu-id="12e8f-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="12e8f-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "rangeformat_autofitrows"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/names(<name>)/range/format/autofitRows
```

##### <a name="response"></a><span data-ttu-id="12e8f-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="12e8f-136">Response</span></span>
<span data-ttu-id="12e8f-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="12e8f-137">Here is an example of the response.</span></span> 
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
  "description": "RangeFormat: autofitRows",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
