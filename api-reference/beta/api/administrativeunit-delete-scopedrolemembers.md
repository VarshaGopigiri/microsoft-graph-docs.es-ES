---
title: Quitar un scopedRoleMember
description: Quitar a un miembro de función con ámbito de una unidad administrativa.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: c6490047faa31ac78e2cd918c46e3f3699cb3d19
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809656"
---
# <a name="remove-a-scopedrolemember"></a><span data-ttu-id="419a8-103">Quitar un scopedRoleMember</span><span class="sxs-lookup"><span data-stu-id="419a8-103">Remove a scopedRoleMember</span></span>

> <span data-ttu-id="419a8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="419a8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="419a8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="419a8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="419a8-106">Quitar a un miembro de función con ámbito de una unidad administrativa.</span><span class="sxs-lookup"><span data-stu-id="419a8-106">Remove a scoped-role member from an adminstrative unit.</span></span>

## <a name="permissions"></a><span data-ttu-id="419a8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="419a8-107">Permissions</span></span>
<span data-ttu-id="419a8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="419a8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="419a8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="419a8-110">Permission type</span></span>      | <span data-ttu-id="419a8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="419a8-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="419a8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="419a8-112">Delegated (work or school account)</span></span> | <span data-ttu-id="419a8-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="419a8-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="419a8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="419a8-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="419a8-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="419a8-115">Not supported.</span></span>    |
|<span data-ttu-id="419a8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="419a8-116">Application</span></span> | <span data-ttu-id="419a8-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="419a8-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="419a8-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="419a8-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /administrativeUnits/{id}/scopedRoleMembers/{id}

```
## <a name="request-headers"></a><span data-ttu-id="419a8-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="419a8-119">Request headers</span></span>
| <span data-ttu-id="419a8-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="419a8-120">Name</span></span>       | <span data-ttu-id="419a8-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="419a8-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="419a8-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="419a8-122">Authorization</span></span>  | <span data-ttu-id="419a8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="419a8-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="419a8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="419a8-125">Request body</span></span>
<span data-ttu-id="419a8-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="419a8-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="419a8-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="419a8-127">Response</span></span>

<span data-ttu-id="419a8-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="419a8-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="419a8-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="419a8-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="419a8-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="419a8-131">Request</span></span>
<span data-ttu-id="419a8-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="419a8-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_scopedrolemember"
}-->
```http
DELETE https://graph.microsoft.com/beta/administrativeUnits/{id}/scopedRoleMembers/{id}
```
##### <a name="response"></a><span data-ttu-id="419a8-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="419a8-133">Response</span></span>
<span data-ttu-id="419a8-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="419a8-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Delete administrativeUnit",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
