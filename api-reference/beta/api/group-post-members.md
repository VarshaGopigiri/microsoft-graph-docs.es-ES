---
title: Add member
description: Use esta API para agregar un miembro a un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**.
ms.openlocfilehash: 3ebfad3b3e1fe2c3411653108d75d44d0fc53913
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27082931"
---
# <a name="add-member"></a><span data-ttu-id="cd9f9-103">Add member</span><span class="sxs-lookup"><span data-stu-id="cd9f9-103">Add member</span></span>

> <span data-ttu-id="cd9f9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cd9f9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cd9f9-106">Use esta API para agregar un miembro a un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-106">Use this API to add a member to an Office 365 Group, a security group, or a mail-enabled security group through the **members** navigation property.</span></span>

<span data-ttu-id="cd9f9-107">Puede agregar usuarios u otros grupos.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-107">You can add users or other groups.</span></span> <span data-ttu-id="cd9f9-108">Importante: Solo se pueden agregar usuarios a Grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-108">Important: You can add only users to Office 365 Groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="cd9f9-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="cd9f9-109">Permissions</span></span>
<span data-ttu-id="cd9f9-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cd9f9-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cd9f9-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cd9f9-112">Permission type</span></span>      | <span data-ttu-id="cd9f9-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cd9f9-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cd9f9-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cd9f9-114">Delegated (work or school account)</span></span> | <span data-ttu-id="cd9f9-115">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="cd9f9-115">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="cd9f9-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cd9f9-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cd9f9-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-117">Not supported.</span></span>    |
|<span data-ttu-id="cd9f9-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cd9f9-118">Application</span></span> | <span data-ttu-id="cd9f9-119">Group.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cd9f9-119">Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="cd9f9-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cd9f9-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/members/$ref
```

## <a name="request-headers"></a><span data-ttu-id="cd9f9-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cd9f9-121">Request headers</span></span>
| <span data-ttu-id="cd9f9-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="cd9f9-122">Name</span></span>       | <span data-ttu-id="cd9f9-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd9f9-123">Type</span></span> | <span data-ttu-id="cd9f9-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd9f9-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="cd9f9-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="cd9f9-125">Authorization</span></span>  | <span data-ttu-id="cd9f9-126">string</span><span class="sxs-lookup"><span data-stu-id="cd9f9-126">string</span></span>  | <span data-ttu-id="cd9f9-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="cd9f9-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cd9f9-129">Request body</span></span>
<span data-ttu-id="cd9f9-130">En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) o [group](../resources/group.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-130">In the request body, supply a JSON representation of a [directoryObject](../resources/directoryobject.md), [user](../resources/user.md) or [group](../resources/group.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="cd9f9-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd9f9-131">Response</span></span>
<span data-ttu-id="cd9f9-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cd9f9-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd9f9-134">Example</span></span>
#### <a name="request"></a><span data-ttu-id="cd9f9-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cd9f9-135">Request</span></span>
<span data-ttu-id="cd9f9-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "add_group_member"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/members/$ref
Content-type: application/json
Content-length: 30

{
  "@odata.id": "https://graph.microsoft.com/beta/directoryObjects/{id}"
}
```
<span data-ttu-id="cd9f9-137">En el cuerpo de la solicitud, proporcionar una representación JSON de la `id` del objeto [directoryObject](../resources/directoryobject.md), [usuario](../resources/user.md)o [grupo](../resources/group.md) que desea agregar.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-137">In the request body, supply a JSON representation of the `id` of the [directoryObject](../resources/directoryobject.md), [user](../resources/user.md), or [group](../resources/group.md) object you want to add.</span></span>

#### <a name="response"></a><span data-ttu-id="cd9f9-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd9f9-138">Response</span></span>
<span data-ttu-id="cd9f9-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-139">The following is an example of the response.</span></span>
><span data-ttu-id="cd9f9-140">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-140">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="cd9f9-141">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cd9f9-141">All the properties will be returned from an actual call.</span></span>
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