---
title: 'servicePrincipal: getMemberGroups'
description: Obtener la lista de grupos a los que esta entidad de seguridad de servicio es un miembro de.  La comprobación es transitiva.
ms.openlocfilehash: 3ea35e86269f370a3f4fc500555ae04705c038fc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083416"
---
# <a name="serviceprincipal-getmembergroups"></a><span data-ttu-id="7c6e7-104">servicePrincipal: getMemberGroups</span><span class="sxs-lookup"><span data-stu-id="7c6e7-104">servicePrincipal: getMemberGroups</span></span>

> <span data-ttu-id="7c6e7-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7c6e7-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7c6e7-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7c6e7-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7c6e7-107">Obtener la lista de grupos a los que esta entidad de seguridad de servicio es un miembro de.</span><span class="sxs-lookup"><span data-stu-id="7c6e7-107">Get the list of groups that this service principal is a member of.</span></span>  <span data-ttu-id="7c6e7-108">La comprobación es transitiva.</span><span class="sxs-lookup"><span data-stu-id="7c6e7-108">The check is transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="7c6e7-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="7c6e7-109">Permissions</span></span>
<span data-ttu-id="7c6e7-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7c6e7-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="7c6e7-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7c6e7-112">Permission type</span></span>      | <span data-ttu-id="7c6e7-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7c6e7-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7c6e7-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7c6e7-114">Delegated (work or school account)</span></span> | <span data-ttu-id="7c6e7-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="7c6e7-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="7c6e7-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7c6e7-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7c6e7-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7c6e7-117">Not supported.</span></span>    |
|<span data-ttu-id="7c6e7-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7c6e7-118">Application</span></span> | <span data-ttu-id="7c6e7-119">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7c6e7-119">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7c6e7-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7c6e7-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/getMemberGroups

```
## <a name="request-headers"></a><span data-ttu-id="7c6e7-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7c6e7-121">Request headers</span></span>
| <span data-ttu-id="7c6e7-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="7c6e7-122">Name</span></span>       | <span data-ttu-id="7c6e7-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c6e7-123">Type</span></span> | <span data-ttu-id="7c6e7-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c6e7-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="7c6e7-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="7c6e7-125">Authorization</span></span>  | <span data-ttu-id="7c6e7-126">string</span><span class="sxs-lookup"><span data-stu-id="7c6e7-126">string</span></span>  | <span data-ttu-id="7c6e7-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7c6e7-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7c6e7-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7c6e7-129">Request body</span></span>
<span data-ttu-id="7c6e7-130">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="7c6e7-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="7c6e7-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7c6e7-131">Parameter</span></span>    | <span data-ttu-id="7c6e7-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c6e7-132">Type</span></span>   |<span data-ttu-id="7c6e7-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c6e7-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7c6e7-134">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="7c6e7-134">securityEnabledOnly</span></span>|<span data-ttu-id="7c6e7-135">Boolean</span><span class="sxs-lookup"><span data-stu-id="7c6e7-135">Boolean</span></span>|<span data-ttu-id="7c6e7-p106">Establecer en **false**. La devolución solo de grupos con la seguridad activada solo es compatible para usuarios.</span><span class="sxs-lookup"><span data-stu-id="7c6e7-p106">Set to **false**. Returning only security-enabled groups is supported for users only.</span></span>|

## <a name="response"></a><span data-ttu-id="7c6e7-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7c6e7-138">Response</span></span>

<span data-ttu-id="7c6e7-139">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7c6e7-139">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7c6e7-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7c6e7-140">Example</span></span>
<span data-ttu-id="7c6e7-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="7c6e7-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="7c6e7-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7c6e7-142">Request</span></span>
<span data-ttu-id="7c6e7-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7c6e7-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "serviceprincipal_getmembergroups"
}-->
```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/getMemberGroups
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": true
}
```

##### <a name="response"></a><span data-ttu-id="7c6e7-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7c6e7-144">Response</span></span>
<span data-ttu-id="7c6e7-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7c6e7-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "servicePrincipal: getMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->