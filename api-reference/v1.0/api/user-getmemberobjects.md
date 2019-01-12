---
title: 'user: getMemberObjects'
description: Devuelve todos los grupos, roles de directorio y unidades administrativas de los que el usuario es miembro. La comprobación es transitiva.
localization_priority: Priority
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 6b737ee5115060d02ee476b9bd0f1af4a6424e12
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27978154"
---
# <a name="user-getmemberobjects"></a><span data-ttu-id="a5ed6-104">user: getMemberObjects</span><span class="sxs-lookup"><span data-stu-id="a5ed6-104">user: getMemberObjects</span></span>
<span data-ttu-id="a5ed6-p102">Devuelve todos los grupos, roles de directorio y unidades administrativas de los que el usuario es miembro. La comprobación es transitiva.</span><span class="sxs-lookup"><span data-stu-id="a5ed6-p102">Return all of the groups, directory roles and administrative units that the user is a member of. The check is transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="a5ed6-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="a5ed6-107">Permissions</span></span>
<span data-ttu-id="a5ed6-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a5ed6-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="a5ed6-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a5ed6-110">Permission type</span></span>      | <span data-ttu-id="a5ed6-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a5ed6-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a5ed6-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a5ed6-112">Delegated (work or school account)</span></span> | <span data-ttu-id="a5ed6-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="a5ed6-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="a5ed6-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a5ed6-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a5ed6-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5ed6-115">Not supported.</span></span>    |
|<span data-ttu-id="a5ed6-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a5ed6-116">Application</span></span> | <span data-ttu-id="a5ed6-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a5ed6-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a5ed6-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a5ed6-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/getMemberObjects
```
## <a name="request-headers"></a><span data-ttu-id="a5ed6-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a5ed6-119">Request headers</span></span>
| <span data-ttu-id="a5ed6-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5ed6-120">Header</span></span>       | <span data-ttu-id="a5ed6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a5ed6-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="a5ed6-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="a5ed6-122">Authorization</span></span>  | <span data-ttu-id="a5ed6-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a5ed6-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="a5ed6-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a5ed6-125">Content-Type</span></span>  | <span data-ttu-id="a5ed6-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a5ed6-126">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="a5ed6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a5ed6-127">Request body</span></span>
<span data-ttu-id="a5ed6-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="a5ed6-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="a5ed6-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a5ed6-129">Parameter</span></span>    | <span data-ttu-id="a5ed6-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5ed6-130">Type</span></span>   |<span data-ttu-id="a5ed6-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5ed6-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a5ed6-132">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="a5ed6-132">securityEnabledOnly</span></span>|<span data-ttu-id="a5ed6-133">Boolean</span><span class="sxs-lookup"><span data-stu-id="a5ed6-133">Boolean</span></span>|<span data-ttu-id="a5ed6-p105">**true** para especificar que solo deben devolverse los grupos de seguridad de los que el usuario sea miembro; **false** para especificar que deben devolverse todos los grupos y roles de directorio de los que el usuario sea miembro. Nota: Establecer este parámetro en **verdadero** solo es posible al llamar este método en un usuario.</span><span class="sxs-lookup"><span data-stu-id="a5ed6-p105">**true** to specify that only security groups that the user is a member of should be returned; **false** to specify that all groups and directory roles that the user is a member of should be returned. Note: Setting this parameter to **true** is only supported when calling this method on a user.</span></span>|

## <a name="response"></a><span data-ttu-id="a5ed6-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5ed6-136">Response</span></span>

<span data-ttu-id="a5ed6-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la colección de cadenas en el cuerpo de la respuesta que contiene los identificadores de los grupos y los roles de directorio de los que el usuario sea miembro.</span><span class="sxs-lookup"><span data-stu-id="a5ed6-137">If successful, this method returns `200 OK` response code and String collection in the response body that contains the IDs of the groups and directory roles that the user is a member of.</span></span>

## <a name="example"></a><span data-ttu-id="a5ed6-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5ed6-138">Example</span></span>
<span data-ttu-id="a5ed6-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a5ed6-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="a5ed6-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a5ed6-140">Request</span></span>
<span data-ttu-id="a5ed6-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5ed6-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_getmemberobjects"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/getMemberObjects
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": true
}
```

##### <a name="response"></a><span data-ttu-id="a5ed6-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5ed6-142">Response</span></span>
<span data-ttu-id="a5ed6-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a5ed6-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "user: getMemberObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
