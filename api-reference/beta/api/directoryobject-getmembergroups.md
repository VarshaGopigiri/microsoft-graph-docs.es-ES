---
title: Obtener grupos de miembro
description: Devolver todos los grupos que el usuario especificado, grupo, servicio entidad de seguridad o el objeto de Active directory es un miembro de. Esta función es transitiva.
localization_priority: Normal
ms.openlocfilehash: 1e9cc785bccd9b5bc6d1c7e3da8d38874a440cf3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27808802"
---
# <a name="get-member-groups"></a><span data-ttu-id="addab-104">Obtener grupos de miembro</span><span class="sxs-lookup"><span data-stu-id="addab-104">Get member groups</span></span>

> <span data-ttu-id="addab-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="addab-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="addab-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="addab-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="addab-107">Devolver todos los grupos que el usuario especificado, grupo, servicio entidad de seguridad o el objeto de Active directory es un miembro de.</span><span class="sxs-lookup"><span data-stu-id="addab-107">Return all the groups that the specified user, group, service principal or directory object is a member of.</span></span> <span data-ttu-id="addab-108">Esta función es transitiva.</span><span class="sxs-lookup"><span data-stu-id="addab-108">This function is transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="addab-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="addab-109">Permissions</span></span>
<span data-ttu-id="addab-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="addab-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="addab-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="addab-112">Permission type</span></span>      | <span data-ttu-id="addab-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="addab-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="addab-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="addab-114">Delegated (work or school account)</span></span> | <span data-ttu-id="addab-115">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="addab-115">Directory.Read.All</span></span>    |
|<span data-ttu-id="addab-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="addab-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="addab-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="addab-117">Not supported.</span></span>    |
|<span data-ttu-id="addab-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="addab-118">Application</span></span> | <span data-ttu-id="addab-119">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="addab-119">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="addab-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="addab-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/getMemberGroups
POST /users/{id | userPrincipalName}/getMemberGroups
POST /groups/{id}/getMemberGroups
POST /servicePrincipals/{id}/getMemberGroups
POST /directoryObjects/{id}/getMemberGroups
```
## <a name="request-headers"></a><span data-ttu-id="addab-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="addab-121">Request headers</span></span>
| <span data-ttu-id="addab-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="addab-122">Name</span></span>       | <span data-ttu-id="addab-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="addab-123">Type</span></span> | <span data-ttu-id="addab-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="addab-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="addab-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="addab-125">Authorization</span></span>  | <span data-ttu-id="addab-126">string</span><span class="sxs-lookup"><span data-stu-id="addab-126">string</span></span>  | <span data-ttu-id="addab-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="addab-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="addab-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="addab-129">Content-Type</span></span>  | <span data-ttu-id="addab-130">application/json</span><span class="sxs-lookup"><span data-stu-id="addab-130">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="addab-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="addab-131">Request body</span></span>
<span data-ttu-id="addab-132">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="addab-132">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="addab-133">Parámetro</span><span class="sxs-lookup"><span data-stu-id="addab-133">Parameter</span></span>    | <span data-ttu-id="addab-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="addab-134">Type</span></span>   |<span data-ttu-id="addab-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="addab-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="addab-136">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="addab-136">securityEnabledOnly</span></span>|<span data-ttu-id="addab-137">Boolean</span><span class="sxs-lookup"><span data-stu-id="addab-137">Boolean</span></span>| <span data-ttu-id="addab-p106">**true** para especificar que solo deben devolverse los grupos de seguridad de los que la entidad es miembro; **false** para especificar que deben devolverse todos los grupos y roles de directorio de los que la entidad es miembro. **Nota:** Solo se puede llamar la función en un usuario si el parámetro es **true**.</span><span class="sxs-lookup"><span data-stu-id="addab-p106">**true** to specify that only security groups that the entity is a member of should be returned; **false** to specify that all groups and directory roles that the entity is a member of should be returned. **Note**: The function can only be called on a user if the parameter is **true**.</span></span> |

## <a name="response"></a><span data-ttu-id="addab-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="addab-140">Response</span></span>

<span data-ttu-id="addab-141">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="addab-141">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="addab-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="addab-142">Example</span></span>

##### <a name="request"></a><span data-ttu-id="addab-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="addab-143">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "directoryobject_getmembergroups"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/getMemberGroups
Content-type: application/json

{
  "securityEnabledOnly": true
}
```

##### <a name="response"></a><span data-ttu-id="addab-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="addab-144">Response</span></span>
<span data-ttu-id="addab-p107">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="addab-p107">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Collection(Edm.String)",
    "value": [
        "fee2c45b-915a-4a64-b130-f4eb9e75525e",
        "4fe90ae7-065a-478b-9400-e0a0e1cbd540",
        "e0c3beaf-eeb4-43d8-abc5-94f037a65697"
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject: getMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
