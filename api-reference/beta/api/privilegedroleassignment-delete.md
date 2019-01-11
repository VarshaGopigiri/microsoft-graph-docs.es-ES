---
title: Eliminar privilegedRoleAssignment
description: Eliminar privilegedRoleAssignment.
localization_priority: Normal
ms.openlocfilehash: 10d8b10522f26c386e918fb1806c1807d28314e2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888945"
---
# <a name="delete-privilegedroleassignment"></a><span data-ttu-id="55c04-103">Eliminar privilegedRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="55c04-103">Delete privilegedRoleAssignment</span></span>

> <span data-ttu-id="55c04-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="55c04-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="55c04-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="55c04-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="55c04-106">Eliminar [privilegedRoleAssignment](../resources/privilegedroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="55c04-106">Delete [privilegedRoleAssignment](../resources/privilegedroleassignment.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="55c04-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="55c04-107">Permissions</span></span>
<span data-ttu-id="55c04-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="55c04-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="55c04-110">El solicitante debe tener el rol de _Administrador de roles con privilegios_ .</span><span class="sxs-lookup"><span data-stu-id="55c04-110">The requestor needs to have _Privileged Role Administrator_ role.</span></span>
 

|<span data-ttu-id="55c04-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="55c04-111">Permission type</span></span>      | <span data-ttu-id="55c04-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="55c04-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="55c04-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="55c04-113">Delegated (work or school account)</span></span> | <span data-ttu-id="55c04-114">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="55c04-114">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="55c04-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="55c04-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="55c04-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55c04-116">Not supported.</span></span>    |
|<span data-ttu-id="55c04-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="55c04-117">Application</span></span> | <span data-ttu-id="55c04-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55c04-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="55c04-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="55c04-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /privilegedRoleAssignments/{id}
```

<span data-ttu-id="55c04-120">Tenga en cuenta que ``<id>`` está en el formato de 'userId_roleId', donde userId es la cadena GUID para el identificador de usuario de Azure AD y el identificador de función es la cadena GUID para el identificador de rol de administrador de Azure.</span><span class="sxs-lookup"><span data-stu-id="55c04-120">Note that ``<id>`` is in the format of 'userId_roleId', where userId is the GUID string for Azure AD user id, and roleId is the GUID string for Azure administrator role id.</span></span>

## <a name="request-headers"></a><span data-ttu-id="55c04-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="55c04-121">Request headers</span></span>
| <span data-ttu-id="55c04-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="55c04-122">Name</span></span>       | <span data-ttu-id="55c04-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="55c04-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="55c04-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="55c04-124">Authorization</span></span>  | <span data-ttu-id="55c04-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="55c04-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="55c04-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="55c04-127">Request body</span></span>
<span data-ttu-id="55c04-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="55c04-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="55c04-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55c04-129">Response</span></span>

<span data-ttu-id="55c04-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55c04-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

<span data-ttu-id="55c04-132">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="55c04-132">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="55c04-133">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="55c04-133">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>
## <a name="example"></a><span data-ttu-id="55c04-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="55c04-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="55c04-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="55c04-135">Request</span></span>
<span data-ttu-id="55c04-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="55c04-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_privilegedroleassignment"
}-->
```http
DELETE https://graph.microsoft.com/beta/privilegedRoleAssignments/{id}
```
##### <a name="response"></a><span data-ttu-id="55c04-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55c04-137">Response</span></span>
<span data-ttu-id="55c04-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="55c04-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Delete privilegedRoleAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
