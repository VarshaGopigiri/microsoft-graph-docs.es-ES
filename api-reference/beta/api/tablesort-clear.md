---
title: 'TableSort: clear'
description: Borra la ordenación que se aplica actualmente en la tabla. Aunque esto no modifica la ordenación de la tabla, borra el estado de los botones de encabezado.
ms.openlocfilehash: f93b640188faedc228c56b6e13497ade84190765
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090019"
---
# <a name="tablesort-clear"></a><span data-ttu-id="813a8-104">TableSort: clear</span><span class="sxs-lookup"><span data-stu-id="813a8-104">TableSort: clear</span></span>

> <span data-ttu-id="813a8-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="813a8-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="813a8-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="813a8-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="813a8-p103">Borra la ordenación que se aplica actualmente en la tabla. Aunque esto no modifica la ordenación de la tabla, borra el estado de los botones de encabezado.</span><span class="sxs-lookup"><span data-stu-id="813a8-p103">Clears the sorting that is currently on the table. While this doesn't modify the table's ordering, it clears the state of the header buttons.</span></span>
## <a name="permissions"></a><span data-ttu-id="813a8-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="813a8-109">Permissions</span></span>
<span data-ttu-id="813a8-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="813a8-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="813a8-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="813a8-112">Permission type</span></span>      | <span data-ttu-id="813a8-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="813a8-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="813a8-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="813a8-114">Delegated (work or school account)</span></span> | <span data-ttu-id="813a8-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="813a8-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="813a8-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="813a8-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="813a8-117">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="813a8-117">Files.ReadWrite</span></span>    |
|<span data-ttu-id="813a8-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="813a8-118">Application</span></span> | <span data-ttu-id="813a8-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="813a8-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="813a8-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="813a8-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/sort/clear
POST /workbook/worksheets/{id|name}/tables/{id|name}/sort/clear

```
## <a name="request-headers"></a><span data-ttu-id="813a8-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="813a8-121">Request headers</span></span>
| <span data-ttu-id="813a8-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="813a8-122">Name</span></span>       | <span data-ttu-id="813a8-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="813a8-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="813a8-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="813a8-124">Authorization</span></span>  | <span data-ttu-id="813a8-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="813a8-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="813a8-127">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="813a8-127">Workbook-Session-Id</span></span>  | <span data-ttu-id="813a8-p106">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="813a8-p106">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="813a8-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="813a8-130">Request body</span></span>

## <a name="response"></a><span data-ttu-id="813a8-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="813a8-131">Response</span></span>

<span data-ttu-id="813a8-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="813a8-p107">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="813a8-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="813a8-134">Example</span></span>
<span data-ttu-id="813a8-135">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="813a8-135">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="813a8-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="813a8-136">Request</span></span>
<span data-ttu-id="813a8-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="813a8-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablesort_clear"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/sort/clear
```

##### <a name="response"></a><span data-ttu-id="813a8-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="813a8-138">Response</span></span>
<span data-ttu-id="813a8-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="813a8-139">Here is an example of the response.</span></span> 
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