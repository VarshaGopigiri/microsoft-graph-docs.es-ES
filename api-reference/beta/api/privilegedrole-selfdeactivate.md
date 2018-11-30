---
title: 'privilegedRole: selfDeactivate'
description: Desactivación de la función que se asigna al solicitante.
ms.openlocfilehash: f9f72a4f61dfd154829406eb535b394f8f137069
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083676"
---
# <a name="privilegedrole-selfdeactivate"></a><span data-ttu-id="27c1c-103">privilegedRole: selfDeactivate</span><span class="sxs-lookup"><span data-stu-id="27c1c-103">privilegedRole: selfDeactivate</span></span>

> <span data-ttu-id="27c1c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="27c1c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="27c1c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="27c1c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="27c1c-106">Desactivación de la función que se asigna al solicitante.</span><span class="sxs-lookup"><span data-stu-id="27c1c-106">Deactivate the role that is assigned to the requestor.</span></span>
## <a name="permissions"></a><span data-ttu-id="27c1c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="27c1c-107">Permissions</span></span>
<span data-ttu-id="27c1c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="27c1c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="27c1c-110">El solicitante sólo puede llamar a ```selfDeactivate``` para la función que se asigna a él.</span><span class="sxs-lookup"><span data-stu-id="27c1c-110">The requestor can only call ```selfDeactivate``` for the role that is assigned to him.</span></span> 

|<span data-ttu-id="27c1c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="27c1c-111">Permission type</span></span>      | <span data-ttu-id="27c1c-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="27c1c-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="27c1c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="27c1c-113">Delegated (work or school account)</span></span> | <span data-ttu-id="27c1c-114">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="27c1c-114">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="27c1c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="27c1c-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="27c1c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="27c1c-116">Not supported.</span></span>    |
|<span data-ttu-id="27c1c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="27c1c-117">Application</span></span> | <span data-ttu-id="27c1c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="27c1c-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="27c1c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="27c1c-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedRoles/{id}/selfDeactivate
```

<span data-ttu-id="27c1c-120">Tenga en cuenta que ``<id>`` es el identificador de la función de destino.</span><span class="sxs-lookup"><span data-stu-id="27c1c-120">Note that ``<id>`` is the target role id.</span></span>
## <a name="request-headers"></a><span data-ttu-id="27c1c-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="27c1c-121">Request headers</span></span>
| <span data-ttu-id="27c1c-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="27c1c-122">Name</span></span>       | <span data-ttu-id="27c1c-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="27c1c-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="27c1c-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="27c1c-124">Authorization</span></span>  | <span data-ttu-id="27c1c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="27c1c-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="27c1c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="27c1c-127">Request body</span></span>
<span data-ttu-id="27c1c-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="27c1c-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="27c1c-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27c1c-129">Response</span></span>

<span data-ttu-id="27c1c-130">Si tiene éxito, este método devuelve `200 OK` objeto de código y [privilegedRoleAssignment](../resources/privilegedroleassignment.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27c1c-130">If successful, this method returns `200 OK` response code and [privilegedRoleAssignment](../resources/privilegedroleassignment.md) object in the response body.</span></span>

<span data-ttu-id="27c1c-131">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="27c1c-131">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="27c1c-132">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="27c1c-132">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>
## <a name="example"></a><span data-ttu-id="27c1c-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="27c1c-133">Example</span></span>
<span data-ttu-id="27c1c-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="27c1c-134">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="27c1c-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="27c1c-135">Request</span></span>
<span data-ttu-id="27c1c-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="27c1c-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "privilegedrole_selfdeactivate"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedRoles/{id}/selfDeactivate
```

##### <a name="response"></a><span data-ttu-id="27c1c-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27c1c-137">Response</span></span>
<span data-ttu-id="27c1c-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="27c1c-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleAssignment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 184

{
  "id": "id-value",
  "userId": "userId-value",
  "roleId": "roleId-value",
  "isElevated": true,
  "expirationDateTime": "2016-10-19T10:37:00Z",
  "resultMessage": "resultMessage-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedRole: selfDeactivate",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->