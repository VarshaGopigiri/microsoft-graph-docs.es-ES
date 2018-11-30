---
title: Add group owner
description: Agrega un usuario a los propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo.
ms.openlocfilehash: e65db3a57f6a50afb95b432a53b1821065e5867a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083949"
---
# <a name="add-group-owner"></a><span data-ttu-id="f9e9f-104">Add group owner</span><span class="sxs-lookup"><span data-stu-id="f9e9f-104">Add group owner</span></span>

> <span data-ttu-id="f9e9f-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f9e9f-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f9e9f-p103">Agrega un usuario a los propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-p103">Add a user to the group's owners. The owners are a set of non-admin users who are allowed to modify the group object.</span></span>

## <a name="permissions"></a><span data-ttu-id="f9e9f-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="f9e9f-109">Permissions</span></span>
<span data-ttu-id="f9e9f-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f9e9f-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f9e9f-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f9e9f-112">Permission type</span></span>      | <span data-ttu-id="f9e9f-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f9e9f-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f9e9f-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f9e9f-114">Delegated (work or school account)</span></span> | <span data-ttu-id="f9e9f-115">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f9e9f-115">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="f9e9f-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f9e9f-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f9e9f-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-117">Not supported.</span></span>    |
|<span data-ttu-id="f9e9f-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f9e9f-118">Application</span></span> | <span data-ttu-id="f9e9f-119">Group.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f9e9f-119">Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f9e9f-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f9e9f-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/owners/$ref
```
## <a name="request-headers"></a><span data-ttu-id="f9e9f-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f9e9f-121">Request headers</span></span>
| <span data-ttu-id="f9e9f-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="f9e9f-122">Name</span></span>       | <span data-ttu-id="f9e9f-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9e9f-123">Type</span></span> | <span data-ttu-id="f9e9f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9e9f-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="f9e9f-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="f9e9f-125">Authorization</span></span>  | <span data-ttu-id="f9e9f-126">string</span><span class="sxs-lookup"><span data-stu-id="f9e9f-126">string</span></span>  | <span data-ttu-id="f9e9f-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f9e9f-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f9e9f-129">Request body</span></span>
<span data-ttu-id="f9e9f-130">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-130">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="f9e9f-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9e9f-131">Response</span></span>
<span data-ttu-id="f9e9f-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f9e9f-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9e9f-134">Example</span></span>
#### <a name="request"></a><span data-ttu-id="f9e9f-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f9e9f-135">Request</span></span>
<span data-ttu-id="f9e9f-136">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/owners/$ref
Content-type: application/json
Content-length: 30

{
  "@odata.id": "https://graph.microsoft.com/beta/users/{id}"
}
```
<span data-ttu-id="f9e9f-137">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-137">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>

#### <a name="response"></a><span data-ttu-id="f9e9f-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9e9f-138">Response</span></span>
<span data-ttu-id="f9e9f-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-139">The following is an example of the response.</span></span>
><span data-ttu-id="f9e9f-140">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-140">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="f9e9f-141">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f9e9f-141">All the properties will be returned from an actual call.</span></span>
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
