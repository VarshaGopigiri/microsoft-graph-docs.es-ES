---
title: Lista joinedTeams
description: Obtener los grupos de usuarios en Microsoft Teams que el usuario es miembro directo.
ms.openlocfilehash: 8eabc9a27de2deb80153c9cbec5e8266dd38ed7d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085379"
---
# <a name="list-joinedteams"></a><span data-ttu-id="ed7a9-103">Lista joinedTeams</span><span class="sxs-lookup"><span data-stu-id="ed7a9-103">List joinedTeams</span></span>

> <span data-ttu-id="ed7a9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ed7a9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ed7a9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ed7a9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ed7a9-106">Obtenga los [equipos](../resources/team.md) en Microsoft Teams que el usuario es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="ed7a9-106">Get the [teams](../resources/team.md) in Microsoft Teams that the user is a direct member of.</span></span>
 
## <a name="permissions"></a><span data-ttu-id="ed7a9-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ed7a9-107">Permissions</span></span>
<span data-ttu-id="ed7a9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ed7a9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ed7a9-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ed7a9-110">Permission type</span></span>      | <span data-ttu-id="ed7a9-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ed7a9-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ed7a9-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ed7a9-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ed7a9-113">User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed7a9-113">User.Read.All, User.ReadWrite.All</span></span>    |
|<span data-ttu-id="ed7a9-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ed7a9-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ed7a9-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed7a9-115">Not supported.</span></span>    |
|<span data-ttu-id="ed7a9-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ed7a9-116">Application</span></span> | <span data-ttu-id="ed7a9-117">User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed7a9-117">User.Read.All, User.ReadWrite.All</span></span> |

> <span data-ttu-id="ed7a9-118">Actualmente, con los permisos de usuario delegado esta operación sólo funciona para el 'me' usuario.</span><span class="sxs-lookup"><span data-stu-id="ed7a9-118">Currently, with user delegated permissions this operation only works for the 'me' user.</span></span> 
> <span data-ttu-id="ed7a9-119">Con permisos de aplicación, funciona para todos los usuarios especificando el identificador de usuario específico. ('' alias no seguirá compatible con los permisos de aplicación) Para obtener más información, vea [problemas conocidos](/graph/known-issues#microsoft-teams-users-list-of-joined-teams-preview).</span><span class="sxs-lookup"><span data-stu-id="ed7a9-119">With application permissions, it works for all users by specifying  the specific user  id. ('me' alias is not supported with application permissions) For details, see [Known issues](/graph/known-issues#microsoft-teams-users-list-of-joined-teams-preview).</span></span>

## <a name="http-request"></a><span data-ttu-id="ed7a9-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ed7a9-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/joinedTeams
or
GET /users/{id}/joinedTeams
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ed7a9-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ed7a9-121">Optional query parameters</span></span>
<span data-ttu-id="ed7a9-122">Los [Parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) actualmente no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="ed7a9-122">The [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) are not currently supported.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ed7a9-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ed7a9-123">Request headers</span></span>
| <span data-ttu-id="ed7a9-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed7a9-124">Header</span></span>       | <span data-ttu-id="ed7a9-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ed7a9-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ed7a9-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="ed7a9-126">Authorization</span></span>  | <span data-ttu-id="ed7a9-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ed7a9-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="ed7a9-129">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ed7a9-129">Accept</span></span>  | <span data-ttu-id="ed7a9-130">application/json</span><span class="sxs-lookup"><span data-stu-id="ed7a9-130">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ed7a9-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ed7a9-131">Request body</span></span>
<span data-ttu-id="ed7a9-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ed7a9-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ed7a9-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed7a9-133">Response</span></span>

<span data-ttu-id="ed7a9-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed7a9-134">If successful, this method returns a `200 OK` response code and collection of [group](../resources/group.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ed7a9-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ed7a9-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ed7a9-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ed7a9-136">Request</span></span>
<span data-ttu-id="ed7a9-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ed7a9-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_joinedteams"
}-->
```http
GET https://graph.microsoft.com/beta/me/joinedTeams
```
##### <a name="response"></a><span data-ttu-id="ed7a9-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed7a9-138">Response</span></span>
<span data-ttu-id="ed7a9-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ed7a9-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```

## <a name="see-also"></a><span data-ttu-id="ed7a9-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed7a9-142">See also</span></span>
[<span data-ttu-id="ed7a9-143">Lista de todos los equipos</span><span class="sxs-lookup"><span data-stu-id="ed7a9-143">List all teams</span></span>](/graph/teams-list-all-teams)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List joinedTeams",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->