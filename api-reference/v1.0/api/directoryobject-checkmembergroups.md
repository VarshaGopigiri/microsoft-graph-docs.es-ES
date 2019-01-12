---
title: Comprobar grupos de miembro
description: Comprueba la pertenencia a en una lista especificada de grupos y devuelve desde esa lista de esos grupos
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 99ebf38b8f230233b50fa642f7503302afd02b33
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941789"
---
# <a name="check-member-groups"></a><span data-ttu-id="c36d3-103">Comprobar grupos de miembro</span><span class="sxs-lookup"><span data-stu-id="c36d3-103">Check member groups</span></span>

<span data-ttu-id="c36d3-p101">Comprueba la pertenencia en una lista especificada de grupos y devuelve de la lista los grupos de los que el objeto especificado de usuario, grupo o directorio sea miembro. Esta función es transitiva.</span><span class="sxs-lookup"><span data-stu-id="c36d3-p101">Check for membership in a specified list of groups, and returns from that list those groups of which the specified user, group, or directory object is a member. This function is transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="c36d3-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="c36d3-106">Permissions</span></span>
<span data-ttu-id="c36d3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c36d3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c36d3-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c36d3-109">Permission type</span></span>      | <span data-ttu-id="c36d3-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c36d3-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c36d3-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c36d3-111">Delegated (work or school account)</span></span> | <span data-ttu-id="c36d3-112">User.Read.All y Group.Read.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="c36d3-112">User.Read.All and Group.Read.All, Directory.Read.All</span></span>    |
|<span data-ttu-id="c36d3-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c36d3-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c36d3-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c36d3-114">Not supported.</span></span>    |
|<span data-ttu-id="c36d3-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c36d3-115">Application</span></span> | <span data-ttu-id="c36d3-116">User.Read.All y Group.Read.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="c36d3-116">User.Read.All and Group.Read.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c36d3-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c36d3-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/checkMemberGroups
POST /users/{id | userPrincipalName}/checkMemberGroups
POST /groups/{id}/checkMemberGroups
POST /directoryObjects/{id}/checkMemberGroups
```
## <a name="request-headers"></a><span data-ttu-id="c36d3-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c36d3-118">Request headers</span></span>
| <span data-ttu-id="c36d3-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="c36d3-119">Name</span></span>       | <span data-ttu-id="c36d3-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="c36d3-120">Type</span></span> | <span data-ttu-id="c36d3-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c36d3-121">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c36d3-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c36d3-122">Authorization</span></span>  | <span data-ttu-id="c36d3-123">string</span><span class="sxs-lookup"><span data-stu-id="c36d3-123">string</span></span>  | <span data-ttu-id="c36d3-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c36d3-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c36d3-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c36d3-126">Content-Type</span></span>  | <span data-ttu-id="c36d3-127">string</span><span class="sxs-lookup"><span data-stu-id="c36d3-127">string</span></span> | <span data-ttu-id="c36d3-128">application/json</span><span class="sxs-lookup"><span data-stu-id="c36d3-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c36d3-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c36d3-129">Request body</span></span>
<span data-ttu-id="c36d3-130">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="c36d3-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c36d3-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c36d3-131">Parameter</span></span>    | <span data-ttu-id="c36d3-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="c36d3-132">Type</span></span>   |<span data-ttu-id="c36d3-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="c36d3-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c36d3-134">groupIds</span><span class="sxs-lookup"><span data-stu-id="c36d3-134">groupIds</span></span>|<span data-ttu-id="c36d3-135">Colección String</span><span class="sxs-lookup"><span data-stu-id="c36d3-135">String collection</span></span>|<span data-ttu-id="c36d3-p104">Colección que contiene los identificadores de objeto de los grupos en los que se comprueba la pertenencia. Pueden especificarse hasta 20 grupos.</span><span class="sxs-lookup"><span data-stu-id="c36d3-p104">A collection that contains the object IDs of the groups in which to check membership. Up to 20 groups may be specified.</span></span>|

## <a name="response"></a><span data-ttu-id="c36d3-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c36d3-138">Response</span></span>

<span data-ttu-id="c36d3-139">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c36d3-139">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c36d3-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c36d3-140">Example</span></span>

##### <a name="request"></a><span data-ttu-id="c36d3-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c36d3-141">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "directoryobject_checkmembergroups"
}-->
```http
POST https://graph.microsoft.com/v1.0/directoryObjects/{id}/checkMemberGroups
Content-type: application/json

{
  "groupIds": [
        "fee2c45b-915a-4a64b130f4eb9e75525e",
        "4fe90ae065a-478b9400e0a0e1cbd540"
  ]
}
```

##### <a name="response"></a><span data-ttu-id="c36d3-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c36d3-142">Response</span></span>
<span data-ttu-id="c36d3-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c36d3-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "string",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
        "fee2c45b-915a-4a64-b130-f4eb9e75525e"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject: checkMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
