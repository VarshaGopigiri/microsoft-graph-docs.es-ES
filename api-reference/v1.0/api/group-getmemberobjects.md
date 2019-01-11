---
title: 'group: getMemberObjects'
description: 'Devuelve todos los grupos de los que el grupo es miembro. La comprobación es transitiva. Nota: Los grupos no pueden ser miembros de roles de directorio, por lo que no se devolverá ningún rol de directorio.'
localization_priority: Normal
ms.openlocfilehash: fac39adebc8220458b3fcd0a46a5de5f6e27ab4a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27891262"
---
# <a name="group-getmemberobjects"></a><span data-ttu-id="7af52-105">group: getMemberObjects</span><span class="sxs-lookup"><span data-stu-id="7af52-105">group: getMemberObjects</span></span>
<span data-ttu-id="7af52-p102">Devuelve todos los grupos de los que el grupo es miembro. La comprobación es transitiva. Nota: Los grupos no pueden ser miembros de roles de directorio, por lo que no se devolverá ningún rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="7af52-p102">Return all of the groups that this group is a member of. The check is transitive. Note: Groups cannot be members of directory roles, so no directory roles will be returned.</span></span>

## <a name="permissions"></a><span data-ttu-id="7af52-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="7af52-109">Permissions</span></span>
<span data-ttu-id="7af52-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7af52-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7af52-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7af52-112">Permission type</span></span>      | <span data-ttu-id="7af52-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7af52-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7af52-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7af52-114">Delegated (work or school account)</span></span> | <span data-ttu-id="7af52-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="7af52-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="7af52-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7af52-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7af52-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7af52-117">Not supported.</span></span>    |
|<span data-ttu-id="7af52-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7af52-118">Application</span></span> | <span data-ttu-id="7af52-119">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7af52-119">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7af52-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7af52-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/getMemberObjects
```

## <a name="request-headers"></a><span data-ttu-id="7af52-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7af52-121">Request headers</span></span>
| <span data-ttu-id="7af52-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="7af52-122">Name</span></span>       | <span data-ttu-id="7af52-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="7af52-123">Type</span></span> | <span data-ttu-id="7af52-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7af52-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="7af52-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="7af52-125">Authorization</span></span>  | <span data-ttu-id="7af52-126">string</span><span class="sxs-lookup"><span data-stu-id="7af52-126">string</span></span>  | <span data-ttu-id="7af52-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7af52-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7af52-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7af52-129">Request body</span></span>
<span data-ttu-id="7af52-130">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="7af52-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="7af52-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7af52-131">Parameter</span></span>    | <span data-ttu-id="7af52-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="7af52-132">Type</span></span>   |<span data-ttu-id="7af52-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="7af52-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7af52-134">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="7af52-134">securityEnabledOnly</span></span>|<span data-ttu-id="7af52-135">Boolean</span><span class="sxs-lookup"><span data-stu-id="7af52-135">Boolean</span></span>| <span data-ttu-id="7af52-p105">Establecer en **false**. La devolución solo de grupos con la seguridad activada solo es compatible para usuarios.</span><span class="sxs-lookup"><span data-stu-id="7af52-p105">Set to **false**. Returning only security-enabled groups is supported for users only.</span></span>|

## <a name="response"></a><span data-ttu-id="7af52-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7af52-138">Response</span></span>
<span data-ttu-id="7af52-139">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la colección String en el cuerpo de la respuesta que contiene los identificadores de los grupos de los que el grupo sea miembro.</span><span class="sxs-lookup"><span data-stu-id="7af52-139">If successful, this method returns `200 OK` response code and String collection in the response body that contains the IDs of the groups that the group is a member of.</span></span>

## <a name="example"></a><span data-ttu-id="7af52-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7af52-140">Example</span></span>
#### <a name="request"></a><span data-ttu-id="7af52-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7af52-141">Request</span></span>
<span data-ttu-id="7af52-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7af52-142">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_getmemberobjects"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/getMemberObjects
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": false
}
```

#### <a name="response"></a><span data-ttu-id="7af52-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7af52-143">Response</span></span>
<span data-ttu-id="7af52-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7af52-144">The following is an example of the response.</span></span>
><span data-ttu-id="7af52-145">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="7af52-145">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="7af52-146">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7af52-146">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "string",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "value": [
    "string-value"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: getMemberObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
