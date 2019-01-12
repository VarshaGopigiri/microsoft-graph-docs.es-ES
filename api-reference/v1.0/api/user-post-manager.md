---
title: Assign a manager
description: Use esta API para asignar un administrador de usuarios.
localization_priority: Normal
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 356c78fb41f641a0736a83ae05e64ad4696921fc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931695"
---
# <a name="assign-a-manager"></a><span data-ttu-id="6f176-103">Assign a manager</span><span class="sxs-lookup"><span data-stu-id="6f176-103">Assign a manager</span></span>

<span data-ttu-id="6f176-104">Use esta API para asignar un administrador de usuarios.</span><span class="sxs-lookup"><span data-stu-id="6f176-104">Use this API to assign a user's manager.</span></span>
> <span data-ttu-id="6f176-105">Nota: No puede asignar subordinados directos; en lugar de ello, use esta API.</span><span class="sxs-lookup"><span data-stu-id="6f176-105">Note: You cannot assign direct reports - instead use this API.</span></span>

## <a name="permissions"></a><span data-ttu-id="6f176-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="6f176-106">Permissions</span></span>
<span data-ttu-id="6f176-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6f176-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6f176-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6f176-109">Permission type</span></span>      | <span data-ttu-id="6f176-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6f176-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6f176-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6f176-111">Delegated (work or school account)</span></span> | <span data-ttu-id="6f176-112">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="6f176-112">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="6f176-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6f176-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6f176-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6f176-114">Not supported.</span></span>    |
|<span data-ttu-id="6f176-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6f176-115">Application</span></span> | <span data-ttu-id="6f176-116">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6f176-116">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6f176-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6f176-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PUT /users/{id}/manager/$ref
```
## <a name="request-headers"></a><span data-ttu-id="6f176-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6f176-118">Request headers</span></span>
| <span data-ttu-id="6f176-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="6f176-119">Name</span></span>       | <span data-ttu-id="6f176-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f176-120">Type</span></span> | <span data-ttu-id="6f176-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f176-121">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="6f176-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="6f176-122">Authorization</span></span>  | <span data-ttu-id="6f176-123">string</span><span class="sxs-lookup"><span data-stu-id="6f176-123">string</span></span>  | <span data-ttu-id="6f176-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f176-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6f176-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6f176-126">Request body</span></span>
<span data-ttu-id="6f176-127">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md) o [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="6f176-127">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) or [user](../resources/user.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="6f176-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f176-128">Response</span></span>

<span data-ttu-id="6f176-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6f176-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6f176-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f176-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6f176-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6f176-132">Request</span></span>
<span data-ttu-id="6f176-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f176-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
PUT https://graph.microsoft.com/v1.0/users/{id}/manager/$ref
Content-type: application/json
Content-length: xxx

{
  "@odata.id": "https://graph.microsoft.com/v1.0/users/{id}"
}
```
<span data-ttu-id="6f176-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="6f176-134">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>
##### <a name="response"></a><span data-ttu-id="6f176-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f176-135">Response</span></span>
<span data-ttu-id="6f176-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6f176-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 204 No Content
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
