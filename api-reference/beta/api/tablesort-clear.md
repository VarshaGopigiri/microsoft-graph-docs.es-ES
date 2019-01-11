---
title: 'TableSort: clear'
description: Borra la ordenación que se aplica actualmente en la tabla. Aunque esto no modifica la ordenación de la tabla, borra el estado de los botones de encabezado.
localization_priority: Normal
ms.openlocfilehash: 1d7d695bfc1d1e6d951f44e0e3e7cde21c4e5904
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27841331"
---
# <a name="tablesort-clear"></a><span data-ttu-id="fe751-104">TableSort: clear</span><span class="sxs-lookup"><span data-stu-id="fe751-104">TableSort: clear</span></span>

> <span data-ttu-id="fe751-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fe751-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fe751-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fe751-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fe751-p103">Borra la ordenación que se aplica actualmente en la tabla. Aunque esto no modifica la ordenación de la tabla, borra el estado de los botones de encabezado.</span><span class="sxs-lookup"><span data-stu-id="fe751-p103">Clears the sorting that is currently on the table. While this doesn't modify the table's ordering, it clears the state of the header buttons.</span></span>
## <a name="permissions"></a><span data-ttu-id="fe751-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="fe751-109">Permissions</span></span>
<span data-ttu-id="fe751-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fe751-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fe751-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fe751-112">Permission type</span></span>      | <span data-ttu-id="fe751-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fe751-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fe751-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fe751-114">Delegated (work or school account)</span></span> | <span data-ttu-id="fe751-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fe751-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="fe751-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fe751-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fe751-117">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fe751-117">Files.ReadWrite</span></span>    |
|<span data-ttu-id="fe751-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fe751-118">Application</span></span> | <span data-ttu-id="fe751-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fe751-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fe751-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fe751-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/sort/clear
POST /workbook/worksheets/{id|name}/tables/{id|name}/sort/clear

```
## <a name="request-headers"></a><span data-ttu-id="fe751-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fe751-121">Request headers</span></span>
| <span data-ttu-id="fe751-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="fe751-122">Name</span></span>       | <span data-ttu-id="fe751-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe751-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="fe751-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="fe751-124">Authorization</span></span>  | <span data-ttu-id="fe751-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fe751-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="fe751-127">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="fe751-127">Workbook-Session-Id</span></span>  | <span data-ttu-id="fe751-p106">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="fe751-p106">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="fe751-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fe751-130">Request body</span></span>

## <a name="response"></a><span data-ttu-id="fe751-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe751-131">Response</span></span>

<span data-ttu-id="fe751-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe751-p107">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fe751-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fe751-134">Example</span></span>
<span data-ttu-id="fe751-135">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="fe751-135">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="fe751-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fe751-136">Request</span></span>
<span data-ttu-id="fe751-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fe751-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablesort_clear"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/sort/clear
```

##### <a name="response"></a><span data-ttu-id="fe751-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe751-138">Response</span></span>
<span data-ttu-id="fe751-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe751-139">Here is an example of the response.</span></span> 
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
  "description": "TableSort: clear",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
