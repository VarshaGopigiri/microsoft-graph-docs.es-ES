---
title: Quitar un scopedRoleMember
description: Quitar a un miembro de función con ámbito de una unidad administrativa.
author: lleonard-msft
ms.openlocfilehash: 0c312266b672a93d58723fd39a26cf7bd48bd7f4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27303006"
---
# <a name="remove-a-scopedrolemember"></a><span data-ttu-id="2072e-103">Quitar un scopedRoleMember</span><span class="sxs-lookup"><span data-stu-id="2072e-103">Remove a scopedRoleMember</span></span>

> <span data-ttu-id="2072e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2072e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2072e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2072e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2072e-106">Quitar a un miembro de función con ámbito de una unidad administrativa.</span><span class="sxs-lookup"><span data-stu-id="2072e-106">Remove a scoped-role member from an adminstrative unit.</span></span>

## <a name="permissions"></a><span data-ttu-id="2072e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="2072e-107">Permissions</span></span>
<span data-ttu-id="2072e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2072e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="2072e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2072e-110">Permission type</span></span>      | <span data-ttu-id="2072e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2072e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2072e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2072e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="2072e-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="2072e-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="2072e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2072e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2072e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2072e-115">Not supported.</span></span>    |
|<span data-ttu-id="2072e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2072e-116">Application</span></span> | <span data-ttu-id="2072e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2072e-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2072e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2072e-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /administrativeUnits/{id}/scopedRoleMembers/{id}

```
## <a name="request-headers"></a><span data-ttu-id="2072e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2072e-119">Request headers</span></span>
| <span data-ttu-id="2072e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="2072e-120">Name</span></span>       | <span data-ttu-id="2072e-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2072e-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="2072e-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="2072e-122">Authorization</span></span>  | <span data-ttu-id="2072e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2072e-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2072e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2072e-125">Request body</span></span>
<span data-ttu-id="2072e-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2072e-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2072e-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2072e-127">Response</span></span>

<span data-ttu-id="2072e-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2072e-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2072e-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2072e-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2072e-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2072e-131">Request</span></span>
<span data-ttu-id="2072e-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2072e-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_scopedrolemember"
}-->
```http
DELETE https://graph.microsoft.com/beta/administrativeUnits/{id}/scopedRoleMembers/{id}
```
##### <a name="response"></a><span data-ttu-id="2072e-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2072e-133">Response</span></span>
<span data-ttu-id="2072e-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2072e-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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