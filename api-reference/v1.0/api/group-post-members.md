---
title: Add member
description: Use esta API para agregar un miembro a un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**.
ms.openlocfilehash: 1fe2d5c259b4e1974168df30e282d97d3342e0bb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030546"
---
# <a name="add-member"></a><span data-ttu-id="10a22-103">Add member</span><span class="sxs-lookup"><span data-stu-id="10a22-103">Add member</span></span>
<span data-ttu-id="10a22-104">Use esta API para agregar un miembro a un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**.</span><span class="sxs-lookup"><span data-stu-id="10a22-104">Use this API to add a member to an Office 365 Group, a security group, or a mail-enabled security group through the **members** navigation property.</span></span>

<span data-ttu-id="10a22-105">Puede agregar usuarios u otros grupos.</span><span class="sxs-lookup"><span data-stu-id="10a22-105">You can add users or other groups.</span></span> <span data-ttu-id="10a22-106">Importante: Solo se pueden agregar usuarios a Grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="10a22-106">Important: You can add only users to Office 365 Groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="10a22-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="10a22-107">Permissions</span></span>
<span data-ttu-id="10a22-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="10a22-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="10a22-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="10a22-110">Permission type</span></span>      | <span data-ttu-id="10a22-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="10a22-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="10a22-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="10a22-112">Delegated (work or school account)</span></span> | <span data-ttu-id="10a22-113">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="10a22-113">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="10a22-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="10a22-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="10a22-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="10a22-115">Not supported.</span></span>    |
|<span data-ttu-id="10a22-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="10a22-116">Application</span></span> | <span data-ttu-id="10a22-117">Group.ReadWrite.All y Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="10a22-117">Group.ReadWrite.All and Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="10a22-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="10a22-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/members/$ref
```

## <a name="request-headers"></a><span data-ttu-id="10a22-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="10a22-119">Request headers</span></span>
| <span data-ttu-id="10a22-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="10a22-120">Name</span></span>       | <span data-ttu-id="10a22-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="10a22-121">Type</span></span> | <span data-ttu-id="10a22-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="10a22-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="10a22-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="10a22-123">Authorization</span></span>  | <span data-ttu-id="10a22-124">string</span><span class="sxs-lookup"><span data-stu-id="10a22-124">string</span></span>  | <span data-ttu-id="10a22-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="10a22-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="10a22-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="10a22-127">Request body</span></span>
<span data-ttu-id="10a22-128">En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) o [group](../resources/group.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="10a22-128">In the request body, supply a JSON representation of a [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) or [group](../resources/group.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="10a22-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="10a22-129">Response</span></span>
<span data-ttu-id="10a22-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="10a22-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="10a22-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="10a22-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="10a22-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="10a22-133">Request</span></span>
<span data-ttu-id="10a22-134">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="10a22-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/members/$ref
Content-type: application/json
Content-length: 30

{
  "@odata.id": "https://graph.microsoft.com/v1.0/directoryObjects/{id}"
}
```
<span data-ttu-id="10a22-135">En el cuerpo de la solicitud, proporcione una representación JSON del `id` de un objeto [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) o [group](../resources/group.md) que quiera agregar.</span><span class="sxs-lookup"><span data-stu-id="10a22-135">In the request body, supply a JSON representation of the `id` of the [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) or [group](../resources/group.md) object you want to add.</span></span>

#### <a name="response"></a><span data-ttu-id="10a22-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="10a22-136">Response</span></span>
<span data-ttu-id="10a22-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="10a22-137">The following is an example of the response.</span></span>
><span data-ttu-id="10a22-138">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="10a22-138">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="10a22-139">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="10a22-139">All the properties will be returned from an actual call.</span></span>
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