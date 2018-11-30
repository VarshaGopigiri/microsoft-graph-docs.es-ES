---
title: 'TableSort: reapply'
description: Vuelve a aplicar los parámetros de ordenación actuales a la tabla.
ms.openlocfilehash: e9bb3358476d5eb44a41e7927c46b668b04f6e7a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089571"
---
# <a name="tablesort-reapply"></a><span data-ttu-id="58071-103">TableSort: reapply</span><span class="sxs-lookup"><span data-stu-id="58071-103">TableSort: reapply</span></span>

> <span data-ttu-id="58071-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="58071-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="58071-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="58071-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="58071-106">Vuelve a aplicar los parámetros de ordenación actuales a la tabla.</span><span class="sxs-lookup"><span data-stu-id="58071-106">Reapplies the current sorting parameters to the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="58071-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="58071-107">Permissions</span></span>
<span data-ttu-id="58071-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="58071-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="58071-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="58071-110">Permission type</span></span>      | <span data-ttu-id="58071-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="58071-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="58071-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="58071-112">Delegated (work or school account)</span></span> | <span data-ttu-id="58071-113">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="58071-113">Files.ReadWrite</span></span>    |
|<span data-ttu-id="58071-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="58071-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="58071-115">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="58071-115">Files.ReadWrite</span></span>    |
|<span data-ttu-id="58071-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="58071-116">Application</span></span> | <span data-ttu-id="58071-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="58071-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="58071-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="58071-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/sort/reapply
POST /workbook/worksheets/{id|name}/tables/{id|name}/sort/reapply

```
## <a name="request-headers"></a><span data-ttu-id="58071-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="58071-119">Request headers</span></span>
| <span data-ttu-id="58071-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="58071-120">Name</span></span>       | <span data-ttu-id="58071-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="58071-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="58071-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="58071-122">Authorization</span></span>  | <span data-ttu-id="58071-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="58071-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="58071-125">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="58071-125">Workbook-Session-Id</span></span>  | <span data-ttu-id="58071-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="58071-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="58071-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="58071-128">Request body</span></span>

## <a name="response"></a><span data-ttu-id="58071-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58071-129">Response</span></span>

<span data-ttu-id="58071-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58071-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="58071-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="58071-132">Example</span></span>
<span data-ttu-id="58071-133">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="58071-133">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="58071-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="58071-134">Request</span></span>
<span data-ttu-id="58071-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="58071-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablesort_reapply"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/{id}/workbook/tables/{id|name}/sort/reapply
```

##### <a name="response"></a><span data-ttu-id="58071-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58071-136">Response</span></span>
<span data-ttu-id="58071-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58071-137">Here is an example of the response.</span></span> 
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
  "description": "TableSort: reapply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->