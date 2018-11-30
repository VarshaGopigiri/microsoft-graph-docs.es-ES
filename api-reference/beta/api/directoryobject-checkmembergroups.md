---
title: Comprobar grupos de miembro
description: Comprueba la pertenencia a en una lista especificada de grupos y devuelve desde esa lista de esos grupos
ms.openlocfilehash: b7baccd19b9d5a84ecbca4d75bca053eb51bc3f6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083030"
---
# <a name="check-member-groups"></a><span data-ttu-id="c5665-103">Comprobar grupos de miembro</span><span class="sxs-lookup"><span data-stu-id="c5665-103">Check member groups</span></span>

> <span data-ttu-id="c5665-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c5665-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c5665-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c5665-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c5665-106">Comprueba la pertenencia a en una lista especificada de grupos y devuelve desde esa lista de esos grupos del que el usuario especificado, grupo, servicio entidad de seguridad o el objeto de Active directory es un miembro.</span><span class="sxs-lookup"><span data-stu-id="c5665-106">Check for membership in a specified list of groups, and returns from that list those groups of which the specified user, group, service principal or directory object is a member.</span></span> <span data-ttu-id="c5665-107">Esta función es transitiva.</span><span class="sxs-lookup"><span data-stu-id="c5665-107">This function is transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="c5665-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="c5665-108">Permissions</span></span>
<span data-ttu-id="c5665-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c5665-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="c5665-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c5665-111">Permission type</span></span>      | <span data-ttu-id="c5665-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c5665-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c5665-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c5665-113">Delegated (work or school account)</span></span> | <span data-ttu-id="c5665-114">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="c5665-114">Directory.Read.All</span></span>    |
|<span data-ttu-id="c5665-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c5665-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c5665-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c5665-116">Not supported.</span></span>    |
|<span data-ttu-id="c5665-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c5665-117">Application</span></span> | <span data-ttu-id="c5665-118">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="c5665-118">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c5665-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c5665-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/checkMemberGroups
POST /users/{id | userPrincipalName}/checkMemberGroups
POST /groups/{id}/checkMemberGroups
POST /servciePrincipals/{id}/checkMemberGroups
POST /directoryObjects/{id}/checkMemberGroups
```
## <a name="request-headers"></a><span data-ttu-id="c5665-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c5665-120">Request headers</span></span>
| <span data-ttu-id="c5665-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="c5665-121">Name</span></span>       | <span data-ttu-id="c5665-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5665-122">Type</span></span> | <span data-ttu-id="c5665-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5665-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c5665-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="c5665-124">Authorization</span></span>  | <span data-ttu-id="c5665-125">string</span><span class="sxs-lookup"><span data-stu-id="c5665-125">string</span></span>  | <span data-ttu-id="c5665-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c5665-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c5665-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c5665-128">Content-Type</span></span>  | <span data-ttu-id="c5665-129">application/json</span><span class="sxs-lookup"><span data-stu-id="c5665-129">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c5665-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c5665-130">Request body</span></span>
<span data-ttu-id="c5665-131">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="c5665-131">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c5665-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c5665-132">Parameter</span></span>    | <span data-ttu-id="c5665-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="c5665-133">Type</span></span>   |<span data-ttu-id="c5665-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5665-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c5665-135">groupIds</span><span class="sxs-lookup"><span data-stu-id="c5665-135">groupIds</span></span>|<span data-ttu-id="c5665-136">String</span><span class="sxs-lookup"><span data-stu-id="c5665-136">String</span></span>|<span data-ttu-id="c5665-p105">Colección que contiene los identificadores de objeto de los grupos en los que se comprueba la pertenencia. Pueden especificarse hasta 20 grupos.</span><span class="sxs-lookup"><span data-stu-id="c5665-p105">A collection that contains the object IDs of the groups in which to check membership. Up to 20 groups may be specified.</span></span>|

## <a name="response"></a><span data-ttu-id="c5665-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5665-139">Response</span></span>

<span data-ttu-id="c5665-140">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c5665-140">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c5665-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c5665-141">Example</span></span>

##### <a name="request"></a><span data-ttu-id="c5665-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c5665-142">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "directoryobject_checkmembergroups"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/checkMemberGroups
Content-type: application/json

{
  "groupIds": [
        "fee2c45b-915a-4a64-b130-f4eb9e75525e",
        "4fe90ae7-065a-478b-9400-e0a0e1cbd540"
  ]
}
```

##### <a name="response"></a><span data-ttu-id="c5665-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c5665-143">Response</span></span>
<span data-ttu-id="c5665-p106">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c5665-p106">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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