---
title: Eliminar appRoleAssignment
description: Eliminar appRoleAssignment.
localization_priority: Normal
ms.openlocfilehash: 5802ba04cfe8aa5ab12a27bb013d8a36a17096e8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814199"
---
# <a name="delete-approleassignment"></a><span data-ttu-id="22b45-103">Eliminar appRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="22b45-103">Delete appRoleAssignment</span></span>

> <span data-ttu-id="22b45-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="22b45-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="22b45-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="22b45-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="22b45-106">Eliminar appRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="22b45-106">Delete appRoleAssignment.</span></span>
## <a name="permissions"></a><span data-ttu-id="22b45-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="22b45-107">Permissions</span></span>
<span data-ttu-id="22b45-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="22b45-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="22b45-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="22b45-110">Permission type</span></span>      | <span data-ttu-id="22b45-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="22b45-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="22b45-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="22b45-112">Delegated (work or school account)</span></span> | <span data-ttu-id="22b45-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="22b45-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="22b45-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="22b45-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="22b45-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="22b45-115">Not supported.</span></span>    |
|<span data-ttu-id="22b45-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="22b45-116">Application</span></span> | <span data-ttu-id="22b45-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="22b45-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="22b45-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="22b45-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /users/{id | userPrincipalName}/appRoleAssignments/{id}
DELETE /servicePrincipals/{id}/appRoleAssignedTo
DELETE /groups/{id}/appRoleAssignments/{id}

```
## <a name="request-headers"></a><span data-ttu-id="22b45-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="22b45-119">Request headers</span></span>
| <span data-ttu-id="22b45-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="22b45-120">Name</span></span>       | <span data-ttu-id="22b45-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="22b45-121">Type</span></span> | <span data-ttu-id="22b45-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="22b45-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="22b45-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="22b45-123">Authorization</span></span>  | <span data-ttu-id="22b45-124">string</span><span class="sxs-lookup"><span data-stu-id="22b45-124">string</span></span>  | <span data-ttu-id="22b45-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="22b45-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="22b45-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="22b45-127">Request body</span></span>
<span data-ttu-id="22b45-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="22b45-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="22b45-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="22b45-129">Response</span></span>

<span data-ttu-id="22b45-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="22b45-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="22b45-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="22b45-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="22b45-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="22b45-133">Request</span></span>
<span data-ttu-id="22b45-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="22b45-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_approleassignment"
}-->
```http
DELETE https://graph.microsoft.com/beta/appRoleAssignments/{id}
```
##### <a name="response"></a><span data-ttu-id="22b45-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="22b45-135">Response</span></span>
<span data-ttu-id="22b45-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="22b45-136">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete appRoleAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
