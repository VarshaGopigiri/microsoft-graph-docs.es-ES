---
title: Asignaciones de listas
description: Recuperar una lista de objetos privilegedRoleAssignment que están asociados con el rol. Cada privilegedRoleAssignment representa una asignación de roles a un usuario.
ms.openlocfilehash: 52cc720381baa6b7c82fe3b5c88d469081da3b81
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087867"
---
# <a name="list-assignments"></a><span data-ttu-id="9b284-104">Asignaciones de listas</span><span class="sxs-lookup"><span data-stu-id="9b284-104">List assignments</span></span>

> <span data-ttu-id="9b284-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9b284-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9b284-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9b284-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9b284-107">Recuperar una lista de objetos [privilegedRoleAssignment](../resources/privilegedroleassignment.md) que están asociados con el rol.</span><span class="sxs-lookup"><span data-stu-id="9b284-107">Retrieve a list of [privilegedRoleAssignment](../resources/privilegedroleassignment.md) objects that are associated with the role.</span></span> <span data-ttu-id="9b284-108">Cada [privilegedRoleAssignment](../resources/privilegedroleassignment.md) representa una asignación de roles a un usuario.</span><span class="sxs-lookup"><span data-stu-id="9b284-108">Each [privilegedRoleAssignment](../resources/privilegedroleassignment.md) represents a role assignment to a user.</span></span>
## <a name="permissions"></a><span data-ttu-id="9b284-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="9b284-109">Permissions</span></span>
<span data-ttu-id="9b284-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9b284-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="9b284-112">El solicitante debe tener uno de los siguientes roles: _Administrador de roles con privilegios_, _Administrador Global_, _Administrador de seguridad_o _Lector de seguridad_.</span><span class="sxs-lookup"><span data-stu-id="9b284-112">The requestor needs to have one of the following roles: _Privileged Role Administrator_, _Global Administrator_, _Security Administrator_, or _Security Reader_.</span></span>
 

|<span data-ttu-id="9b284-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b284-113">Permission type</span></span>      | <span data-ttu-id="9b284-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b284-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9b284-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b284-115">Delegated (work or school account)</span></span> | <span data-ttu-id="9b284-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="9b284-116">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="9b284-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b284-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9b284-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b284-118">Not supported.</span></span>    |
|<span data-ttu-id="9b284-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b284-119">Application</span></span> | <span data-ttu-id="9b284-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b284-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9b284-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b284-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedRoles/{id}/assignments
```

<span data-ttu-id="9b284-122">Tenga en cuenta que ``<id>`` es el identificador de la función de destino.</span><span class="sxs-lookup"><span data-stu-id="9b284-122">Note that ``<id>`` is the target role id.</span></span>
## <a name="optional-query-parameters"></a><span data-ttu-id="9b284-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9b284-123">Optional query parameters</span></span>
<span data-ttu-id="9b284-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b284-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9b284-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b284-125">Request headers</span></span>
| <span data-ttu-id="9b284-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="9b284-126">Name</span></span>      |<span data-ttu-id="9b284-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b284-127">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="9b284-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b284-128">Authorization</span></span>  | <span data-ttu-id="9b284-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b284-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9b284-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b284-131">Request body</span></span>
<span data-ttu-id="9b284-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9b284-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9b284-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b284-133">Response</span></span>

<span data-ttu-id="9b284-134">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [privilegedRoleAssignment](../resources/privilegedroleassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b284-134">If successful, this method returns a `200 OK` response code and collection of [privilegedRoleAssignment](../resources/privilegedroleassignment.md) objects in the response body.</span></span>

<span data-ttu-id="9b284-135">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="9b284-135">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="9b284-136">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="9b284-136">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>
## <a name="example"></a><span data-ttu-id="9b284-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b284-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9b284-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b284-138">Request</span></span>
<span data-ttu-id="9b284-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b284-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_assignments"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedRoles/{id}/assignments
```
##### <a name="response"></a><span data-ttu-id="9b284-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b284-140">Response</span></span>
<span data-ttu-id="9b284-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9b284-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleAssignment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 237

{
  "value": [
    {
      "id": "id-value",
      "userId": "userId-value",
      "roleId": "roleId-value",
      "isElevated": true,
      "expirationDateTime": "2016-10-19T10:37:00Z",
      "resultMessage": "resultMessage-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List assignments",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->