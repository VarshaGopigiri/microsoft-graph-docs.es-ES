---
title: Enumerar joinedTeams
description: Obtener los grupos de usuarios en Microsoft Teams que el usuario es miembro directo.
author: dkershaw10
ms.openlocfilehash: 1e29b21adbf37128ccf8fe7ff9d70596c7b72499
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27317748"
---
# <a name="list-joinedteams"></a><span data-ttu-id="6ed91-103">Enumerar joinedTeams</span><span class="sxs-lookup"><span data-stu-id="6ed91-103">List joinedTeams</span></span>



<span data-ttu-id="6ed91-104">Obtenga los [equipos](../resources/team.md) en Microsoft Teams que el usuario es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="6ed91-104">Get the [teams](../resources/team.md) in Microsoft Teams that the user is a direct member of.</span></span>
 
## <a name="permissions"></a><span data-ttu-id="6ed91-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="6ed91-105">Permissions</span></span>
<span data-ttu-id="6ed91-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6ed91-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6ed91-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6ed91-108">Permission type</span></span>      | <span data-ttu-id="6ed91-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6ed91-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6ed91-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6ed91-110">Delegated (work or school account)</span></span> | <span data-ttu-id="6ed91-111">User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6ed91-111">User.Read.All, User.ReadWrite.All</span></span>    |
|<span data-ttu-id="6ed91-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6ed91-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6ed91-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ed91-113">Not supported.</span></span>    |
|<span data-ttu-id="6ed91-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6ed91-114">Application</span></span> | <span data-ttu-id="6ed91-115">User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6ed91-115">User.Read.All, User.ReadWrite.All</span></span> |

> <span data-ttu-id="6ed91-116">Con permisos de usuario delegado esta operación sólo funciona para el 'me' usuario.</span><span class="sxs-lookup"><span data-stu-id="6ed91-116">With user delegated permissions this operation only works for the 'me' user.</span></span> 
> <span data-ttu-id="6ed91-117">Con permisos de aplicación, funciona para todos los usuarios especificando el identificador de usuario específico. ('' alias no seguirá compatible con los permisos de aplicación)</span><span class="sxs-lookup"><span data-stu-id="6ed91-117">With application permissions, it works for all users by specifying  the specific user id. ('me' alias is not supported with application permissions)</span></span>

## <a name="http-request"></a><span data-ttu-id="6ed91-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6ed91-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/joinedTeams
or
GET /users/{id}/joinedTeams
```

## <a name="optional-query-parameters"></a><span data-ttu-id="6ed91-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6ed91-119">Optional query parameters</span></span>
<span data-ttu-id="6ed91-120">Los [Parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) actualmente no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="6ed91-120">The [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) are not currently supported.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6ed91-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6ed91-121">Request headers</span></span>
| <span data-ttu-id="6ed91-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ed91-122">Header</span></span>       | <span data-ttu-id="6ed91-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6ed91-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="6ed91-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="6ed91-124">Authorization</span></span>  | <span data-ttu-id="6ed91-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6ed91-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="6ed91-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6ed91-127">Accept</span></span>  | <span data-ttu-id="6ed91-128">application/json</span><span class="sxs-lookup"><span data-stu-id="6ed91-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6ed91-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6ed91-129">Request body</span></span>
<span data-ttu-id="6ed91-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6ed91-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6ed91-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ed91-131">Response</span></span>

<span data-ttu-id="6ed91-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ed91-132">If successful, this method returns a `200 OK` response code and collection of [group](../resources/group.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6ed91-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ed91-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6ed91-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ed91-134">Request</span></span>
<span data-ttu-id="6ed91-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ed91-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_joinedteams"
}-->
```http
GET https://graph.microsoft.com/beta/me/joinedTeams
```
##### <a name="response"></a><span data-ttu-id="6ed91-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ed91-136">Response</span></span>
<span data-ttu-id="6ed91-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ed91-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="6ed91-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ed91-140">See also</span></span>
[<span data-ttu-id="6ed91-141">Lista de todos los equipos</span><span class="sxs-lookup"><span data-stu-id="6ed91-141">List all teams</span></span>](/graph/teams-list-all-teams)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List joinedTeams",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
