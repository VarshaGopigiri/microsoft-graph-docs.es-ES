---
title: 'servicePrincipal: getMemberObjects'
description: Obtener la lista de grupos y roles de Active directory que este servicio principal es un miembro de.  Esta comprobación es transitiva.
ms.openlocfilehash: 82fd1791b32c54a4670977e7ca5a66bdd92c1c14
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087910"
---
# <a name="serviceprincipal-getmemberobjects"></a><span data-ttu-id="283df-104">servicePrincipal: getMemberObjects</span><span class="sxs-lookup"><span data-stu-id="283df-104">servicePrincipal: getMemberObjects</span></span>

> <span data-ttu-id="283df-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="283df-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="283df-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="283df-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="283df-107">Obtener la lista de grupos y roles de Active directory que este servicio principal es un miembro de.</span><span class="sxs-lookup"><span data-stu-id="283df-107">Get the list of groups and directory roles that this service principal is a member of.</span></span>  <span data-ttu-id="283df-108">Esta comprobación es transitiva.</span><span class="sxs-lookup"><span data-stu-id="283df-108">This check is transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="283df-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="283df-109">Permissions</span></span>
<span data-ttu-id="283df-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="283df-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="283df-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="283df-112">Permission type</span></span>      | <span data-ttu-id="283df-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="283df-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="283df-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="283df-114">Delegated (work or school account)</span></span> | <span data-ttu-id="283df-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="283df-115">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="283df-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="283df-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="283df-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="283df-117">Not supported.</span></span>    |
|<span data-ttu-id="283df-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="283df-118">Application</span></span> | <span data-ttu-id="283df-119">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="283df-119">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="283df-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="283df-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /servicePrincipals/{id}/getMemberObjects

```
## <a name="request-headers"></a><span data-ttu-id="283df-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="283df-121">Request headers</span></span>
| <span data-ttu-id="283df-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="283df-122">Name</span></span>       | <span data-ttu-id="283df-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="283df-123">Type</span></span> | <span data-ttu-id="283df-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="283df-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="283df-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="283df-125">Authorization</span></span>  | <span data-ttu-id="283df-126">string</span><span class="sxs-lookup"><span data-stu-id="283df-126">string</span></span>  | <span data-ttu-id="283df-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="283df-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="283df-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="283df-129">Request body</span></span>
<span data-ttu-id="283df-130">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="283df-130">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="283df-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="283df-131">Parameter</span></span>    | <span data-ttu-id="283df-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="283df-132">Type</span></span>   |<span data-ttu-id="283df-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="283df-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="283df-134">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="283df-134">securityEnabledOnly</span></span>|<span data-ttu-id="283df-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="283df-135">Boolean</span></span>||

## <a name="response"></a><span data-ttu-id="283df-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="283df-136">Response</span></span>

<span data-ttu-id="283df-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="283df-137">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="283df-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="283df-138">Example</span></span>
<span data-ttu-id="283df-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="283df-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="283df-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="283df-140">Request</span></span>
<span data-ttu-id="283df-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="283df-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "serviceprincipal_getmemberobjects"
}-->
```http
POST https://graph.microsoft.com/beta/servicePrincipals/{id}/getMemberObjects
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": true
}
```

##### <a name="response"></a><span data-ttu-id="283df-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="283df-142">Response</span></span>
<span data-ttu-id="283df-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="283df-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "servicePrincipal: getMemberObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->