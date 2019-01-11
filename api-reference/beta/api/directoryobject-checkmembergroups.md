---
title: Comprobar grupos de miembro
description: Comprueba la pertenencia a en una lista especificada de grupos y devuelve desde esa lista de esos grupos
localization_priority: Normal
ms.openlocfilehash: cfa9f1a50ffd284233707799a8d05d6b5c46dfc1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854043"
---
# <a name="check-member-groups"></a><span data-ttu-id="1d241-103">Comprobar grupos de miembro</span><span class="sxs-lookup"><span data-stu-id="1d241-103">Check member groups</span></span>

> <span data-ttu-id="1d241-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1d241-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1d241-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1d241-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1d241-106">Comprueba la pertenencia a en una lista especificada de grupos y devuelve desde esa lista de esos grupos del que el usuario especificado, grupo, servicio entidad de seguridad o el objeto de Active directory es un miembro.</span><span class="sxs-lookup"><span data-stu-id="1d241-106">Check for membership in a specified list of groups, and returns from that list those groups of which the specified user, group, service principal or directory object is a member.</span></span> <span data-ttu-id="1d241-107">Esta función es transitiva.</span><span class="sxs-lookup"><span data-stu-id="1d241-107">This function is transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="1d241-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="1d241-108">Permissions</span></span>
<span data-ttu-id="1d241-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1d241-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="1d241-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1d241-111">Permission type</span></span>      | <span data-ttu-id="1d241-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1d241-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1d241-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1d241-113">Delegated (work or school account)</span></span> | <span data-ttu-id="1d241-114">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="1d241-114">Directory.Read.All</span></span>    |
|<span data-ttu-id="1d241-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1d241-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1d241-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d241-116">Not supported.</span></span>    |
|<span data-ttu-id="1d241-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1d241-117">Application</span></span> | <span data-ttu-id="1d241-118">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="1d241-118">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="1d241-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d241-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/checkMemberGroups
POST /users/{id | userPrincipalName}/checkMemberGroups
POST /groups/{id}/checkMemberGroups
POST /servciePrincipals/{id}/checkMemberGroups
POST /directoryObjects/{id}/checkMemberGroups
```
## <a name="request-headers"></a><span data-ttu-id="1d241-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d241-120">Request headers</span></span>
| <span data-ttu-id="1d241-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="1d241-121">Name</span></span>       | <span data-ttu-id="1d241-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d241-122">Type</span></span> | <span data-ttu-id="1d241-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d241-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="1d241-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="1d241-124">Authorization</span></span>  | <span data-ttu-id="1d241-125">string</span><span class="sxs-lookup"><span data-stu-id="1d241-125">string</span></span>  | <span data-ttu-id="1d241-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1d241-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1d241-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1d241-128">Content-Type</span></span>  | <span data-ttu-id="1d241-129">application/json</span><span class="sxs-lookup"><span data-stu-id="1d241-129">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="1d241-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1d241-130">Request body</span></span>
<span data-ttu-id="1d241-131">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="1d241-131">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="1d241-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1d241-132">Parameter</span></span>    | <span data-ttu-id="1d241-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d241-133">Type</span></span>   |<span data-ttu-id="1d241-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d241-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1d241-135">groupIds</span><span class="sxs-lookup"><span data-stu-id="1d241-135">groupIds</span></span>|<span data-ttu-id="1d241-136">String</span><span class="sxs-lookup"><span data-stu-id="1d241-136">String</span></span>|<span data-ttu-id="1d241-p105">Colección que contiene los identificadores de objeto de los grupos en los que se comprueba la pertenencia. Pueden especificarse hasta 20 grupos.</span><span class="sxs-lookup"><span data-stu-id="1d241-p105">A collection that contains the object IDs of the groups in which to check membership. Up to 20 groups may be specified.</span></span>|

## <a name="response"></a><span data-ttu-id="1d241-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d241-139">Response</span></span>

<span data-ttu-id="1d241-140">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d241-140">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1d241-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d241-141">Example</span></span>

##### <a name="request"></a><span data-ttu-id="1d241-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d241-142">Request</span></span>

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

##### <a name="response"></a><span data-ttu-id="1d241-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d241-143">Response</span></span>
<span data-ttu-id="1d241-p106">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d241-p106">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
