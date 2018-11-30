---
title: Add group owner
description: Agrega un usuario a los propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo.
ms.openlocfilehash: 8c879430c78cb1d06150bade842addcb4ba0af38
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030498"
---
# <a name="add-group-owner"></a><span data-ttu-id="cec9c-104">Add group owner</span><span class="sxs-lookup"><span data-stu-id="cec9c-104">Add group owner</span></span>
<span data-ttu-id="cec9c-p102">Agrega un usuario a los propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="cec9c-p102">Add a user to the group's owners. The owners are a set of non-admin users who are allowed to modify the group object.</span></span>

## <a name="permissions"></a><span data-ttu-id="cec9c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="cec9c-107">Permissions</span></span>
<span data-ttu-id="cec9c-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cec9c-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cec9c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cec9c-110">Permission type</span></span>      | <span data-ttu-id="cec9c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cec9c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cec9c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cec9c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="cec9c-113">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="cec9c-113">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="cec9c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cec9c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cec9c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cec9c-115">Not supported.</span></span>    |
|<span data-ttu-id="cec9c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cec9c-116">Application</span></span> | <span data-ttu-id="cec9c-117">Group.ReadWrite.All y User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cec9c-117">Group.ReadWrite.All and User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="cec9c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cec9c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/owners/$ref
```
## <a name="request-headers"></a><span data-ttu-id="cec9c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cec9c-119">Request headers</span></span>
| <span data-ttu-id="cec9c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="cec9c-120">Name</span></span>       | <span data-ttu-id="cec9c-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="cec9c-121">Type</span></span> | <span data-ttu-id="cec9c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="cec9c-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="cec9c-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="cec9c-123">Authorization</span></span>  | <span data-ttu-id="cec9c-124">string</span><span class="sxs-lookup"><span data-stu-id="cec9c-124">string</span></span>  | <span data-ttu-id="cec9c-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cec9c-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="cec9c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cec9c-127">Request body</span></span>
<span data-ttu-id="cec9c-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="cec9c-128">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="cec9c-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cec9c-129">Response</span></span>
<span data-ttu-id="cec9c-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cec9c-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cec9c-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cec9c-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="cec9c-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cec9c-133">Request</span></span>
<span data-ttu-id="cec9c-134">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cec9c-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/owners/$ref
Content-type: application/json
Content-length: 30

{
  "@odata.id": "https://graph.microsoft.com/v1.0/users/{id}"
}
```
<span data-ttu-id="cec9c-135">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="cec9c-135">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>

#### <a name="response"></a><span data-ttu-id="cec9c-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cec9c-136">Response</span></span>
<span data-ttu-id="cec9c-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cec9c-137">The following is an example of the response.</span></span>
><span data-ttu-id="cec9c-138">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="cec9c-138">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="cec9c-139">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cec9c-139">All the properties will be returned from an actual call.</span></span>
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
  "description": "Create owner",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
