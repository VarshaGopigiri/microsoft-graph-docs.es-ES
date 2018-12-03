---
title: Obtener grupos de miembro
description: Devuelve todos los grupos de los que el usuario, grupo u objeto de directorio que se especifique sea miembro. Esta función es transitiva.
ms.openlocfilehash: 370de10e1bba582270290877ba508ec4eebf47ca
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031985"
---
# <a name="get-member-groups"></a><span data-ttu-id="18e1f-104">Obtener grupos de miembro</span><span class="sxs-lookup"><span data-stu-id="18e1f-104">Get member groups</span></span>

<span data-ttu-id="18e1f-p102">Devuelve todos los grupos de los que el usuario, grupo u objeto de directorio que se especifique sea miembro. Esta función es transitiva.</span><span class="sxs-lookup"><span data-stu-id="18e1f-p102">Return all the groups that the specified user, group, or directory object is a member of. This function is transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="18e1f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="18e1f-107">Permissions</span></span>
<span data-ttu-id="18e1f-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="18e1f-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="18e1f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="18e1f-110">Permission type</span></span>      | <span data-ttu-id="18e1f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="18e1f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="18e1f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="18e1f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="18e1f-113">User.Read.All y Group.Read.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="18e1f-113">User.Read.All and Group.Read.All, Directory.Read.All</span></span>    |
|<span data-ttu-id="18e1f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="18e1f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="18e1f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="18e1f-115">Not supported.</span></span>    |
|<span data-ttu-id="18e1f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="18e1f-116">Application</span></span> | <span data-ttu-id="18e1f-117">User.Read.All y Group.Read.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="18e1f-117">User.Read.All and Group.Read.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="18e1f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="18e1f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/getMemberGroups
POST /users/{id | userPrincipalName}/getMemberGroups
POST /groups/{id}/getMemberGroups
POST /directoryObjects/{id}/getMemberGroups
```
## <a name="request-headers"></a><span data-ttu-id="18e1f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="18e1f-119">Request headers</span></span>
| <span data-ttu-id="18e1f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="18e1f-120">Name</span></span>       | <span data-ttu-id="18e1f-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="18e1f-121">Type</span></span> | <span data-ttu-id="18e1f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="18e1f-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="18e1f-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="18e1f-123">Authorization</span></span>  | <span data-ttu-id="18e1f-124">string</span><span class="sxs-lookup"><span data-stu-id="18e1f-124">string</span></span>  | <span data-ttu-id="18e1f-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18e1f-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="18e1f-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="18e1f-127">Content-Type</span></span>   | <span data-ttu-id="18e1f-128">string</span><span class="sxs-lookup"><span data-stu-id="18e1f-128">string</span></span>  | <span data-ttu-id="18e1f-129">application/json</span><span class="sxs-lookup"><span data-stu-id="18e1f-129">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="18e1f-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="18e1f-130">Request body</span></span>
<span data-ttu-id="18e1f-131">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="18e1f-131">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="18e1f-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="18e1f-132">Parameter</span></span>    | <span data-ttu-id="18e1f-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="18e1f-133">Type</span></span>   |<span data-ttu-id="18e1f-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="18e1f-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="18e1f-135">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="18e1f-135">securityEnabledOnly</span></span>|<span data-ttu-id="18e1f-136">Boolean</span><span class="sxs-lookup"><span data-stu-id="18e1f-136">Boolean</span></span>| <span data-ttu-id="18e1f-p105">**true** para especificar que solo deben devolverse los grupos de seguridad de los que la entidad es miembro; **false** para especificar que deben devolverse todos los grupos y roles de directorio de los que la entidad es miembro. **Nota:** Solo se puede llamar la función en un usuario si el parámetro es **true**.</span><span class="sxs-lookup"><span data-stu-id="18e1f-p105">**true** to specify that only security groups that the entity is a member of should be returned; **false** to specify that all groups and directory roles that the entity is a member of should be returned. **Note**: The function can only be called on a user if the parameter is **true**.</span></span> |

## <a name="response"></a><span data-ttu-id="18e1f-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18e1f-139">Response</span></span>

<span data-ttu-id="18e1f-140">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18e1f-140">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="18e1f-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="18e1f-141">Example</span></span>

##### <a name="request"></a><span data-ttu-id="18e1f-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="18e1f-142">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "directoryobject_getmembergroups"
}-->
```http
POST https://graph.microsoft.com/v1.0/directoryObjects/{object-id}/getMemberGroups
Content-type: application/json

{
  "securityEnabledOnly": true
}
```

##### <a name="response"></a><span data-ttu-id="18e1f-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18e1f-143">Response</span></span>
<span data-ttu-id="18e1f-p106">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="18e1f-p106">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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