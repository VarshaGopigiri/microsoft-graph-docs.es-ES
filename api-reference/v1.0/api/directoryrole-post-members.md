---
title: Add directory role member
description: Usa esta API para crear un miembro de rol de directorio.
author: lleonard-msft
ms.openlocfilehash: e82907c47667072fa7234a6d7444298a5e4546f5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27347127"
---
# <a name="add-directory-role-member"></a><span data-ttu-id="4426c-103">Add directory role member</span><span class="sxs-lookup"><span data-stu-id="4426c-103">Add directory role member</span></span>

<span data-ttu-id="4426c-104">Usa esta API para crear un miembro de rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="4426c-104">Use this API to create a new directory role member.</span></span>

## <a name="permissions"></a><span data-ttu-id="4426c-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="4426c-105">Permissions</span></span>
<span data-ttu-id="4426c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4426c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4426c-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4426c-108">Permission type</span></span>      | <span data-ttu-id="4426c-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4426c-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4426c-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4426c-110">Delegated (work or school account)</span></span> | <span data-ttu-id="4426c-111">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4426c-111">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="4426c-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4426c-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4426c-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4426c-113">Not supported.</span></span>    |
|<span data-ttu-id="4426c-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4426c-114">Application</span></span> | <span data-ttu-id="4426c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4426c-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4426c-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4426c-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /directoryRoles/{id}/members/$ref

```
## <a name="request-headers"></a><span data-ttu-id="4426c-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4426c-117">Request headers</span></span>
| <span data-ttu-id="4426c-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="4426c-118">Name</span></span>       | <span data-ttu-id="4426c-119">Type</span><span class="sxs-lookup"><span data-stu-id="4426c-119">Type</span></span> | <span data-ttu-id="4426c-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="4426c-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="4426c-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="4426c-121">Authorization</span></span>  | <span data-ttu-id="4426c-122">string</span><span class="sxs-lookup"><span data-stu-id="4426c-122">string</span></span>  | <span data-ttu-id="4426c-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4426c-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4426c-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="4426c-125">Content-Type</span></span>  | <span data-ttu-id="4426c-126">string</span><span class="sxs-lookup"><span data-stu-id="4426c-126">string</span></span>  | <span data-ttu-id="4426c-127">application/json</span><span class="sxs-lookup"><span data-stu-id="4426c-127">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="4426c-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4426c-128">Request body</span></span>
<span data-ttu-id="4426c-129">En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [directoryObject](../resources/directoryobject.md) o [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="4426c-129">In the request body, supply a JSON representation of a [directoryObject](../resources/directoryobject.md) or [user](../resources/user.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="4426c-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4426c-130">Response</span></span>

<span data-ttu-id="4426c-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="4426c-131">If successful, this method returns `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="4426c-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4426c-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4426c-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4426c-133">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_directoryrole"
}-->
```http
POST https://graph.microsoft.com/v1.0/directoryRoles/{id}/members/$ref
Content-type: application/json

{
  "@odata.id": "https://graph.microsoft.com/v1.0/directoryObjects/{id}"
}
```

##### <a name="response"></a><span data-ttu-id="4426c-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4426c-134">Response</span></span>
<span data-ttu-id="4426c-135">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="4426c-135">Note: The response object shown here may be truncated for brevity.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 204 No Content
Content-type: text/plain

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create member",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->