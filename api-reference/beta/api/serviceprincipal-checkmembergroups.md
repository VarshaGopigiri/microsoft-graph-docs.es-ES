---
title: 'servicePrincipal: checkMemberGroups'
description: Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea Permisos.
ms.openlocfilehash: bf16206e9029ddcf687738c3a7db5a0a27a43903
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27082901"
---
# <a name="serviceprincipal-checkmembergroups"></a><span data-ttu-id="0fccb-104">servicePrincipal: checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="0fccb-104">servicePrincipal: checkMemberGroups</span></span>

> <span data-ttu-id="0fccb-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0fccb-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0fccb-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0fccb-106">Use of these APIs in production applications is not supported.</span></span>

## <a name="permissions"></a><span data-ttu-id="0fccb-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0fccb-107">Permissions</span></span>
<span data-ttu-id="0fccb-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0fccb-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0fccb-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0fccb-110">Permission type</span></span>      | <span data-ttu-id="0fccb-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0fccb-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0fccb-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0fccb-112">Delegated (work or school account)</span></span> | <span data-ttu-id="0fccb-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="0fccb-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="0fccb-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0fccb-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0fccb-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0fccb-115">Not supported.</span></span>    |
|<span data-ttu-id="0fccb-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0fccb-116">Application</span></span> | <span data-ttu-id="0fccb-117">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="0fccb-117">Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0fccb-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0fccb-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/checkMemberGroups

```
## <a name="request-headers"></a><span data-ttu-id="0fccb-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0fccb-119">Request headers</span></span>
| <span data-ttu-id="0fccb-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="0fccb-120">Name</span></span>       | <span data-ttu-id="0fccb-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="0fccb-121">Type</span></span> | <span data-ttu-id="0fccb-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fccb-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="0fccb-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="0fccb-123">Authorization</span></span>  | <span data-ttu-id="0fccb-124">string</span><span class="sxs-lookup"><span data-stu-id="0fccb-124">string</span></span>  | <span data-ttu-id="0fccb-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0fccb-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0fccb-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0fccb-127">Request body</span></span>
<span data-ttu-id="0fccb-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="0fccb-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="0fccb-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0fccb-129">Parameter</span></span>    | <span data-ttu-id="0fccb-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="0fccb-130">Type</span></span>   |<span data-ttu-id="0fccb-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fccb-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0fccb-132">groupIds</span><span class="sxs-lookup"><span data-stu-id="0fccb-132">groupIds</span></span>|<span data-ttu-id="0fccb-133">String</span><span class="sxs-lookup"><span data-stu-id="0fccb-133">String</span></span>||

## <a name="response"></a><span data-ttu-id="0fccb-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0fccb-134">Response</span></span>

<span data-ttu-id="0fccb-135">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0fccb-135">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0fccb-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0fccb-136">Example</span></span>
<span data-ttu-id="0fccb-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0fccb-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="0fccb-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0fccb-138">Request</span></span>
<span data-ttu-id="0fccb-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0fccb-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "serviceprincipal_checkmembergroups"
}-->
```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/checkMemberGroups
Content-type: application/json
Content-length: 44

{
  "groupIds": [
    "groupIds-value"
  ]
}
```

##### <a name="response"></a><span data-ttu-id="0fccb-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0fccb-140">Response</span></span>
<span data-ttu-id="0fccb-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0fccb-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "servicePrincipal: checkMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->