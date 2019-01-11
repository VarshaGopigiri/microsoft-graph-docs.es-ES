---
title: Obtener objetos de miembro
description: " Devuelve todos los grupos y roles de directorio de los que un usuario, grupo u objeto de directorio sea miembro. Esta función es transitiva. "
localization_priority: Normal
ms.openlocfilehash: b7c4c09991d31141e12fb6cd900309f81e22f8e6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815914"
---
# <a name="get-member-objects"></a><span data-ttu-id="19dd2-104">Obtener objetos de miembro</span><span class="sxs-lookup"><span data-stu-id="19dd2-104">Get member objects</span></span>

 <span data-ttu-id="19dd2-p102">Devuelve todos los grupos y roles de directorio de los que un usuario, grupo u objeto de directorio sea miembro. Esta función es transitiva.</span><span class="sxs-lookup"><span data-stu-id="19dd2-p102">Returns all the groups and directory roles that a user, group, or directory object is a member of. This function is transitive.</span></span> 
 > <span data-ttu-id="19dd2-107">Nota: Solo los usuarios pueden ser miembros de roles de directorio.</span><span class="sxs-lookup"><span data-stu-id="19dd2-107">Note: Only users can be members of directory roles.</span></span>

## <a name="permissions"></a><span data-ttu-id="19dd2-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="19dd2-108">Permissions</span></span>
<span data-ttu-id="19dd2-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="19dd2-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="19dd2-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="19dd2-111">Permission type</span></span>      | <span data-ttu-id="19dd2-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="19dd2-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="19dd2-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="19dd2-113">Delegated (work or school account)</span></span> | <span data-ttu-id="19dd2-114">User.Read.All y Group.Read.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="19dd2-114">User.Read.All and Group.Read.All, Directory.Read.All</span></span>    |
|<span data-ttu-id="19dd2-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="19dd2-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="19dd2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="19dd2-116">Not supported.</span></span>    |
|<span data-ttu-id="19dd2-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="19dd2-117">Application</span></span> | <span data-ttu-id="19dd2-118">User.Read.All y Group.Read.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="19dd2-118">User.Read.All and Group.Read.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="19dd2-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="19dd2-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/getMemberObjects
POST /users/{id | userPrincipalName}/getMemberObjects
POST /groups/{id}/getMemberGroups
POST /directoryObjects/{id}/getMemberObjects

```
## <a name="request-headers"></a><span data-ttu-id="19dd2-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="19dd2-120">Request headers</span></span>
| <span data-ttu-id="19dd2-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="19dd2-121">Name</span></span>       | <span data-ttu-id="19dd2-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="19dd2-122">Type</span></span> | <span data-ttu-id="19dd2-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="19dd2-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="19dd2-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="19dd2-124">Authorization</span></span>  | <span data-ttu-id="19dd2-125">string</span><span class="sxs-lookup"><span data-stu-id="19dd2-125">string</span></span>  | <span data-ttu-id="19dd2-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="19dd2-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="19dd2-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="19dd2-128">Content-Type</span></span>   | <span data-ttu-id="19dd2-129">string</span><span class="sxs-lookup"><span data-stu-id="19dd2-129">string</span></span>  | <span data-ttu-id="19dd2-130">application/json</span><span class="sxs-lookup"><span data-stu-id="19dd2-130">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="19dd2-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="19dd2-131">Request body</span></span>
<span data-ttu-id="19dd2-132">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="19dd2-132">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="19dd2-133">Parámetro</span><span class="sxs-lookup"><span data-stu-id="19dd2-133">Parameter</span></span>    | <span data-ttu-id="19dd2-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="19dd2-134">Type</span></span>   |<span data-ttu-id="19dd2-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="19dd2-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="19dd2-136">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="19dd2-136">securityEnabledOnly</span></span>|<span data-ttu-id="19dd2-137">Boolean</span><span class="sxs-lookup"><span data-stu-id="19dd2-137">Boolean</span></span>| <span data-ttu-id="19dd2-p105">**true** para especificar que solo deben devolverse los grupos de seguridad de los que la entidad es miembro; **false** para especificar que deben devolverse todos los grupos y roles de directorio de los que la entidad es miembro. **Nota:** Solo se puede llamar la función en un usuario si el parámetro es **true**.</span><span class="sxs-lookup"><span data-stu-id="19dd2-p105">**true** to specify that only security groups that the entity is a member of should be returned; **false** to specify that all groups and directory roles that the entity is a member of should be returned. **Note**: The function can only be called on a user if the parameter is **true**.</span></span> |

## <a name="response"></a><span data-ttu-id="19dd2-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19dd2-140">Response</span></span>

<span data-ttu-id="19dd2-141">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="19dd2-141">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="19dd2-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="19dd2-142">Example</span></span>

##### <a name="request"></a><span data-ttu-id="19dd2-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="19dd2-143">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "directoryobject_getmemberobjects"
}-->
```http
POST https://graph.microsoft.com/v1.0/directoryObjects/{object-id}/getMemberObjects
Content-type: application/json

{
  "securityEnabledOnly": true
}
```

##### <a name="response"></a><span data-ttu-id="19dd2-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19dd2-144">Response</span></span>
<span data-ttu-id="19dd2-p106">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="19dd2-p106">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
        "c9ee2d50-9e8a-4352-b97c-4c2c99557c22",
        "e0c3beaf-eeb4-43d8-abc5-94f037a65697"
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject: getMemberObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
