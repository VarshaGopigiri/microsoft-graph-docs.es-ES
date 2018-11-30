---
title: 'orgContact: getMemberGroups'
description: Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea Permisos.
ms.openlocfilehash: 472cbd5a72f6e01b6aab977cdae347f6711c8619
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083161"
---
# <a name="orgcontact-getmembergroups"></a><span data-ttu-id="35cac-104">orgContact: getMemberGroups</span><span class="sxs-lookup"><span data-stu-id="35cac-104">orgContact: getMemberGroups</span></span>

> <span data-ttu-id="35cac-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="35cac-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="35cac-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="35cac-106">Use of these APIs in production applications is not supported.</span></span>

## <a name="permissions"></a><span data-ttu-id="35cac-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="35cac-107">Permissions</span></span>
<span data-ttu-id="35cac-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="35cac-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="35cac-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="35cac-110">Permission type</span></span>      | <span data-ttu-id="35cac-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="35cac-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="35cac-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="35cac-112">Delegated (work or school account)</span></span> | <span data-ttu-id="35cac-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="35cac-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="35cac-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="35cac-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="35cac-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="35cac-115">Not supported.</span></span>    |
|<span data-ttu-id="35cac-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="35cac-116">Application</span></span> | <span data-ttu-id="35cac-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="35cac-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="35cac-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="35cac-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /contacts/{id}/getMemberGroups

```
## <a name="request-headers"></a><span data-ttu-id="35cac-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="35cac-119">Request headers</span></span>
| <span data-ttu-id="35cac-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="35cac-120">Name</span></span>       | <span data-ttu-id="35cac-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="35cac-121">Type</span></span> | <span data-ttu-id="35cac-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="35cac-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="35cac-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="35cac-123">Authorization</span></span>  | <span data-ttu-id="35cac-124">string</span><span class="sxs-lookup"><span data-stu-id="35cac-124">string</span></span>  | <span data-ttu-id="35cac-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="35cac-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="35cac-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="35cac-127">Request body</span></span>
<span data-ttu-id="35cac-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="35cac-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="35cac-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="35cac-129">Parameter</span></span>    | <span data-ttu-id="35cac-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="35cac-130">Type</span></span>   |<span data-ttu-id="35cac-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="35cac-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="35cac-132">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="35cac-132">securityEnabledOnly</span></span>|<span data-ttu-id="35cac-133">Booleano</span><span class="sxs-lookup"><span data-stu-id="35cac-133">Boolean</span></span>||

## <a name="response"></a><span data-ttu-id="35cac-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35cac-134">Response</span></span>

<span data-ttu-id="35cac-135">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35cac-135">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="35cac-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="35cac-136">Example</span></span>
<span data-ttu-id="35cac-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="35cac-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="35cac-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="35cac-138">Request</span></span>
<span data-ttu-id="35cac-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="35cac-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "orgcontact_getmembergroups"
}-->
```http
POST https://graph.microsoft.com/beta/contacts/{id}/getMemberGroups
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": true
}
```

##### <a name="response"></a><span data-ttu-id="35cac-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35cac-140">Response</span></span>
<span data-ttu-id="35cac-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="35cac-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "orgContact: getMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->