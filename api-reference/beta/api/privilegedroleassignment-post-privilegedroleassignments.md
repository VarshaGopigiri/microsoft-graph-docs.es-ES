---
title: Crear privilegedRoleAssignment
description: Utilice esta API para crear un nuevo privilegedRoleAssignment.
ms.openlocfilehash: cee00a71ff9ff233902ba19fb1f3f699ab746f98
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087050"
---
# <a name="create-privilegedroleassignment"></a><span data-ttu-id="a2cfc-103">Crear privilegedRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a2cfc-103">Create privilegedRoleAssignment</span></span>

> <span data-ttu-id="a2cfc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a2cfc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a2cfc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a2cfc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a2cfc-106">Utilice esta API para crear un nuevo [privilegedRoleAssignment](../resources/privilegedroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="a2cfc-106">Use this API to create a new  [privilegedRoleAssignment](../resources/privilegedroleassignment.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="a2cfc-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a2cfc-107">Permissions</span></span>
<span data-ttu-id="a2cfc-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a2cfc-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="a2cfc-110">El solicitante debe tener el rol de _Administrador de roles con privilegios_ .</span><span class="sxs-lookup"><span data-stu-id="a2cfc-110">The requestor needs to have _Privileged Role Administrator_ role.</span></span> 

|<span data-ttu-id="a2cfc-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a2cfc-111">Permission type</span></span>      | <span data-ttu-id="a2cfc-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a2cfc-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a2cfc-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a2cfc-113">Delegated (work or school account)</span></span> | <span data-ttu-id="a2cfc-114">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="a2cfc-114">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="a2cfc-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a2cfc-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a2cfc-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2cfc-116">Not supported.</span></span>    |
|<span data-ttu-id="a2cfc-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a2cfc-117">Application</span></span> | <span data-ttu-id="a2cfc-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2cfc-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a2cfc-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a2cfc-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedRoleAssignments
```
## <a name="request-headers"></a><span data-ttu-id="a2cfc-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a2cfc-120">Request headers</span></span>
| <span data-ttu-id="a2cfc-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="a2cfc-121">Name</span></span>       | <span data-ttu-id="a2cfc-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2cfc-122">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="a2cfc-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a2cfc-123">Authorization</span></span>  | <span data-ttu-id="a2cfc-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a2cfc-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a2cfc-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a2cfc-126">Request body</span></span>
<span data-ttu-id="a2cfc-127">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [privilegedRoleAssignment](../resources/privilegedroleassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="a2cfc-127">In the request body, supply a JSON representation of [privilegedRoleAssignment](../resources/privilegedroleassignment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="a2cfc-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2cfc-128">Response</span></span>

<span data-ttu-id="a2cfc-129">Si tiene éxito, este método devuelve `201 Created` objeto de código y [privilegedRoleAssignment](../resources/privilegedroleassignment.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2cfc-129">If successful, this method returns `201 Created` response code and [privilegedRoleAssignment](../resources/privilegedroleassignment.md) object in the response body.</span></span>

<span data-ttu-id="a2cfc-130">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="a2cfc-130">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="a2cfc-131">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="a2cfc-131">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>
## <a name="example"></a><span data-ttu-id="a2cfc-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a2cfc-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a2cfc-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a2cfc-133">Request</span></span>
<span data-ttu-id="a2cfc-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2cfc-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_privilegedroleassignment_from_privilegedroleassignments"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedRoleAssignments
Content-type: application/json
Content-length: 164

{
  "userId": "userId-value",
  "roleId": "roleId-value"
}
```
<span data-ttu-id="a2cfc-135">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [privilegedRoleAssignment](../resources/privilegedroleassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="a2cfc-135">In the request body, supply a JSON representation of [privilegedRoleAssignment](../resources/privilegedroleassignment.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="a2cfc-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2cfc-136">Response</span></span>
<span data-ttu-id="a2cfc-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a2cfc-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleAssignment"
} -->
```http
HTTP/1.1 201 Created
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
  "description": "Create privilegedRoleAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->