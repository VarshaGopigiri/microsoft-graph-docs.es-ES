---
title: Obtener objetos de miembro
description: " Devuelve todos los grupos, unidades administrativas y funciones de Active directory que un usuario, grupo, entidades de seguridad de servicio o el objeto de Active directory es un miembro de. Esta función es transitiva. "
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 00709d0a71b5c13a07d1f07ba41d1273ea0fb034
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946367"
---
# <a name="get-member-objects"></a><span data-ttu-id="1b725-104">Obtener objetos de miembro</span><span class="sxs-lookup"><span data-stu-id="1b725-104">Get member objects</span></span>

> <span data-ttu-id="1b725-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1b725-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1b725-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1b725-106">Use of these APIs in production applications is not supported.</span></span>

 <span data-ttu-id="1b725-107">Devuelve todos los grupos, unidades administrativas y funciones de Active directory que un usuario, grupo, entidades de seguridad de servicio o el objeto de Active directory es un miembro de.</span><span class="sxs-lookup"><span data-stu-id="1b725-107">Returns all the groups, administrative units and directory roles that a user, group, service principals or directory object is a member of.</span></span> <span data-ttu-id="1b725-108">Esta función es transitiva.</span><span class="sxs-lookup"><span data-stu-id="1b725-108">This function is transitive.</span></span> 
 > <span data-ttu-id="1b725-109">Nota: Solo los usuarios pueden ser miembros de roles de directorio.</span><span class="sxs-lookup"><span data-stu-id="1b725-109">Note: Only users can be members of directory roles.</span></span>

## <a name="permissions"></a><span data-ttu-id="1b725-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="1b725-110">Permissions</span></span>
<span data-ttu-id="1b725-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1b725-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="1b725-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1b725-113">Permission type</span></span>      | <span data-ttu-id="1b725-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1b725-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1b725-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1b725-115">Delegated (work or school account)</span></span> | <span data-ttu-id="1b725-116">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="1b725-116">Directory.Read.All</span></span>    |
|<span data-ttu-id="1b725-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1b725-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1b725-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1b725-118">Not supported.</span></span>    |
|<span data-ttu-id="1b725-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1b725-119">Application</span></span> | <span data-ttu-id="1b725-120">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="1b725-120">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="1b725-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1b725-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/getMemberObjects
POST /users/{id | userPrincipalName}/getMemberObjects
POST /groups/{id}/getMemberObjects
POST /servicePrincipals/{id}/getMemberObjects
POST /directoryObjects/{id}/getMemberObjects

```
## <a name="request-headers"></a><span data-ttu-id="1b725-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1b725-122">Request headers</span></span>
| <span data-ttu-id="1b725-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="1b725-123">Name</span></span>       | <span data-ttu-id="1b725-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b725-124">Type</span></span> | <span data-ttu-id="1b725-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b725-125">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="1b725-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="1b725-126">Authorization</span></span>  | <span data-ttu-id="1b725-127">string</span><span class="sxs-lookup"><span data-stu-id="1b725-127">string</span></span>  | <span data-ttu-id="1b725-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1b725-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1b725-130">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1b725-130">Content-Type</span></span>  | <span data-ttu-id="1b725-131">application/json</span><span class="sxs-lookup"><span data-stu-id="1b725-131">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="1b725-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1b725-132">Request body</span></span>
<span data-ttu-id="1b725-133">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="1b725-133">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="1b725-134">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1b725-134">Parameter</span></span>    | <span data-ttu-id="1b725-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b725-135">Type</span></span>   |<span data-ttu-id="1b725-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b725-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1b725-137">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="1b725-137">securityEnabledOnly</span></span>|<span data-ttu-id="1b725-138">Boolean</span><span class="sxs-lookup"><span data-stu-id="1b725-138">Boolean</span></span>| <span data-ttu-id="1b725-p106">**true** para especificar que solo deben devolverse los grupos de seguridad de los que la entidad es miembro; **false** para especificar que deben devolverse todos los grupos y roles de directorio de los que la entidad es miembro. **Nota:** Solo se puede llamar la función en un usuario si el parámetro es **true**.</span><span class="sxs-lookup"><span data-stu-id="1b725-p106">**true** to specify that only security groups that the entity is a member of should be returned; **false** to specify that all groups and directory roles that the entity is a member of should be returned. **Note**: The function can only be called on a user if the parameter is **true**.</span></span> |

## <a name="response"></a><span data-ttu-id="1b725-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b725-141">Response</span></span>

<span data-ttu-id="1b725-142">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b725-142">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1b725-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1b725-143">Example</span></span>

##### <a name="request"></a><span data-ttu-id="1b725-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1b725-144">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "directoryobject_getmemberobjects"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/getMemberObjects
Content-type: application/json

{
  "securityEnabledOnly": true
}
```

##### <a name="response"></a><span data-ttu-id="1b725-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b725-145">Response</span></span>
<span data-ttu-id="1b725-p107">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1b725-p107">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
