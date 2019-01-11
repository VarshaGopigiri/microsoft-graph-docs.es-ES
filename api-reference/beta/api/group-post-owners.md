---
title: Add group owner
description: Agrega un usuario a los propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo.
localization_priority: Normal
ms.openlocfilehash: 3fe136b0ea76ae2d6f535af421d016bf27c58a6b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883198"
---
# <a name="add-group-owner"></a><span data-ttu-id="90cf2-104">Add group owner</span><span class="sxs-lookup"><span data-stu-id="90cf2-104">Add group owner</span></span>

> <span data-ttu-id="90cf2-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="90cf2-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="90cf2-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="90cf2-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="90cf2-p103">Agrega un usuario a los propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="90cf2-p103">Add a user to the group's owners. The owners are a set of non-admin users who are allowed to modify the group object.</span></span>

><span data-ttu-id="90cf2-109">**Importante:** Si actualiza los propietarios del grupo y ha creado un equipo para el grupo, puede tardar hasta 2 horas para los propietarios de la que se sincronizará con Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="90cf2-109">**Important:** If you update the group owners and you created a team for the group, it can take up to 2 hours for the owners to be synchronized with Microsoft Teams.</span></span> <span data-ttu-id="90cf2-110">Además, si desea que el propietario de la que puedan realizar cambios en un equipo - por ejemplo, mediante la creación de un plan de organizador - el propietario también debe agregarse como un miembro del equipo o grupo.</span><span class="sxs-lookup"><span data-stu-id="90cf2-110">Also, if you want the owner to be able to make changes in a team - for example, by creating a Planner plan - the owner also needs to be added as a group/team member.</span></span> 

## <a name="permissions"></a><span data-ttu-id="90cf2-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="90cf2-111">Permissions</span></span>
<span data-ttu-id="90cf2-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="90cf2-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="90cf2-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="90cf2-114">Permission type</span></span>      | <span data-ttu-id="90cf2-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="90cf2-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="90cf2-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="90cf2-116">Delegated (work or school account)</span></span> | <span data-ttu-id="90cf2-117">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="90cf2-117">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="90cf2-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="90cf2-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="90cf2-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="90cf2-119">Not supported.</span></span>    |
|<span data-ttu-id="90cf2-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="90cf2-120">Application</span></span> | <span data-ttu-id="90cf2-121">Group.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="90cf2-121">Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="90cf2-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="90cf2-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/owners/$ref
```
## <a name="request-headers"></a><span data-ttu-id="90cf2-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="90cf2-123">Request headers</span></span>
| <span data-ttu-id="90cf2-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="90cf2-124">Name</span></span>       | <span data-ttu-id="90cf2-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="90cf2-125">Type</span></span> | <span data-ttu-id="90cf2-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="90cf2-126">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="90cf2-127">Autorización</span><span class="sxs-lookup"><span data-stu-id="90cf2-127">Authorization</span></span>  | <span data-ttu-id="90cf2-128">string</span><span class="sxs-lookup"><span data-stu-id="90cf2-128">string</span></span>  | <span data-ttu-id="90cf2-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90cf2-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="90cf2-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="90cf2-131">Request body</span></span>
<span data-ttu-id="90cf2-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="90cf2-132">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="90cf2-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90cf2-133">Response</span></span>
<span data-ttu-id="90cf2-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90cf2-p107">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="90cf2-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="90cf2-136">Example</span></span>
#### <a name="request"></a><span data-ttu-id="90cf2-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="90cf2-137">Request</span></span>
<span data-ttu-id="90cf2-138">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="90cf2-138">The following is an example of the request.</span></span>
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
<span data-ttu-id="90cf2-139">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="90cf2-139">In the request body, supply a JSON representation of [user](../resources/user.md) object to be added.</span></span>

#### <a name="response"></a><span data-ttu-id="90cf2-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90cf2-140">Response</span></span>
<span data-ttu-id="90cf2-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90cf2-141">The following is an example of the response.</span></span>
><span data-ttu-id="90cf2-142">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="90cf2-142">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="90cf2-143">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="90cf2-143">All the properties will be returned from an actual call.</span></span>
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
