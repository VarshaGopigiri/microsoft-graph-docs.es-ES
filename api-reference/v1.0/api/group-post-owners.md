---
title: Add group owner
description: Agrega un usuario a los propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo.
localization_priority: Priority
author: dkershaw10
ms.prod: groups
ms.openlocfilehash: b3057a270aa2c503d96747e173cc54b13013ce6a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917996"
---
# <a name="add-group-owner"></a><span data-ttu-id="b966b-104">Add group owner</span><span class="sxs-lookup"><span data-stu-id="b966b-104">Add group owner</span></span>
<span data-ttu-id="b966b-p102">Agrega un usuario a los propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="b966b-p102">Add a user to the group's owners. The owners are a set of non-admin users who are allowed to modify the group object.</span></span>

><span data-ttu-id="b966b-107">**Importante:** Si actualiza los propietarios del grupo y ha creado un equipo para el grupo, puede tardar hasta 2 horas para los propietarios de la que se sincronizará con Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b966b-107">**Important:** If you update the group owners and you created a team for the group, it can take up to 2 hours for the owners to be synchronized with Microsoft Teams.</span></span> <span data-ttu-id="b966b-108">Además, si desea que el propietario de la que puedan realizar cambios en un equipo - por ejemplo, mediante la creación de un plan de organizador - el propietario también debe agregarse como un miembro del equipo o grupo.</span><span class="sxs-lookup"><span data-stu-id="b966b-108">Also, if you want the owner to be able to make changes in a team - for example, by creating a Planner plan - the owner also needs to be added as a group/team member.</span></span> 

## <a name="permissions"></a><span data-ttu-id="b966b-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="b966b-109">Permissions</span></span>
<span data-ttu-id="b966b-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b966b-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b966b-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b966b-112">Permission type</span></span>      | <span data-ttu-id="b966b-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b966b-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b966b-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b966b-114">Delegated (work or school account)</span></span> | <span data-ttu-id="b966b-115">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="b966b-115">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="b966b-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b966b-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b966b-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b966b-117">Not supported.</span></span>    |
|<span data-ttu-id="b966b-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b966b-118">Application</span></span> | <span data-ttu-id="b966b-119">Group.ReadWrite.All y User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b966b-119">Group.ReadWrite.All and User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b966b-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b966b-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/owners/$ref
```
## <a name="request-headers"></a><span data-ttu-id="b966b-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b966b-121">Request headers</span></span>
| <span data-ttu-id="b966b-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="b966b-122">Name</span></span>       | <span data-ttu-id="b966b-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="b966b-123">Type</span></span> | <span data-ttu-id="b966b-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="b966b-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="b966b-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="b966b-125">Authorization</span></span>  | <span data-ttu-id="b966b-126">string</span><span class="sxs-lookup"><span data-stu-id="b966b-126">string</span></span>  | <span data-ttu-id="b966b-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b966b-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b966b-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b966b-129">Request body</span></span>
<span data-ttu-id="b966b-130">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="b966b-130">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="b966b-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b966b-131">Response</span></span>
<span data-ttu-id="b966b-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b966b-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b966b-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b966b-134">Example</span></span>
#### <a name="request"></a><span data-ttu-id="b966b-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b966b-135">Request</span></span>
<span data-ttu-id="b966b-136">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b966b-136">The following is an example of the request.</span></span>
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
<span data-ttu-id="b966b-137">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="b966b-137">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>

#### <a name="response"></a><span data-ttu-id="b966b-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b966b-138">Response</span></span>
<span data-ttu-id="b966b-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b966b-139">The following is an example of the response.</span></span>
><span data-ttu-id="b966b-140">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="b966b-140">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="b966b-141">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b966b-141">All the properties will be returned from an actual call.</span></span>
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

