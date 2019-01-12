---
title: 'user: getMemberObjects'
description: Devuelve todos los grupos, roles de directorio y unidades administrativas de los que el usuario es miembro. La comprobación es transitiva.
localization_priority: Normal
author: dkershaw10
ms.prod: microsoft-identity-platform
ms.openlocfilehash: f4a2b01096b271b26f89c83f22a65246d02023c2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27957819"
---
# <a name="user-getmemberobjects"></a><span data-ttu-id="70bef-104">user: getMemberObjects</span><span class="sxs-lookup"><span data-stu-id="70bef-104">user: getMemberObjects</span></span>

> <span data-ttu-id="70bef-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="70bef-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="70bef-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="70bef-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="70bef-p103">Devuelve todos los grupos, roles de directorio y unidades administrativas de los que el usuario es miembro. La comprobación es transitiva.</span><span class="sxs-lookup"><span data-stu-id="70bef-p103">Return all of the groups, directory roles and administrative units that the user is a member of. The check is transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="70bef-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="70bef-109">Permissions</span></span>
<span data-ttu-id="70bef-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="70bef-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="70bef-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="70bef-112">Permission type</span></span>      | <span data-ttu-id="70bef-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="70bef-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="70bef-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="70bef-114">Delegated (work or school account)</span></span> | <span data-ttu-id="70bef-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="70bef-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="70bef-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="70bef-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="70bef-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="70bef-117">Not supported.</span></span>    |
|<span data-ttu-id="70bef-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="70bef-118">Application</span></span> | <span data-ttu-id="70bef-119">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="70bef-119">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="70bef-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="70bef-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/getMemberObjects
```
## <a name="request-headers"></a><span data-ttu-id="70bef-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="70bef-121">Request headers</span></span>
| <span data-ttu-id="70bef-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70bef-122">Header</span></span>       | <span data-ttu-id="70bef-123">Valor</span><span class="sxs-lookup"><span data-stu-id="70bef-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="70bef-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="70bef-124">Authorization</span></span>  | <span data-ttu-id="70bef-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="70bef-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="70bef-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="70bef-127">Content-Type</span></span>  | <span data-ttu-id="70bef-128">application/json</span><span class="sxs-lookup"><span data-stu-id="70bef-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="70bef-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="70bef-129">Request body</span></span>
<span data-ttu-id="70bef-130">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="70bef-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="70bef-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="70bef-131">Parameter</span></span>    | <span data-ttu-id="70bef-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="70bef-132">Type</span></span>   |<span data-ttu-id="70bef-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="70bef-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="70bef-134">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="70bef-134">securityEnabledOnly</span></span>|<span data-ttu-id="70bef-135">Boolean</span><span class="sxs-lookup"><span data-stu-id="70bef-135">Boolean</span></span>|<span data-ttu-id="70bef-p106">**true** para especificar que solo se deben devolver los grupos de seguridad de los que el usuario es miembro; **false** para especificar que se deben devolver todos los grupos de los que el usuario es miembro. Nota: Establecer este parámetro en **verdadero** solo es posible al llamar este método en un usuario.</span><span class="sxs-lookup"><span data-stu-id="70bef-p106">**true** to specify that only security groups that the user is a member of should be returned; **false** to specify that all groups that the user is a member of should be returned. Note: Setting this parameter to **true** is only supported when calling this method on a user.</span></span>|

## <a name="response"></a><span data-ttu-id="70bef-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70bef-138">Response</span></span>

<span data-ttu-id="70bef-139">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la colección de cadenas en el cuerpo de la respuesta que contiene los identificadores de los grupos y los roles de directorio de los que el usuario sea miembro.</span><span class="sxs-lookup"><span data-stu-id="70bef-139">If successful, this method returns `200 OK` response code and String collection in the response body that contains the IDs of the groups and directory roles that the user is a member of.</span></span>

## <a name="example"></a><span data-ttu-id="70bef-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="70bef-140">Example</span></span>
<span data-ttu-id="70bef-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="70bef-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="70bef-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="70bef-142">Request</span></span>
<span data-ttu-id="70bef-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="70bef-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_getmemberobjects"
}-->
```http
POST https://graph.microsoft.com/beta/me/getMemberObjects
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": true
}
```

##### <a name="response"></a><span data-ttu-id="70bef-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70bef-144">Response</span></span>
<span data-ttu-id="70bef-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="70bef-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
