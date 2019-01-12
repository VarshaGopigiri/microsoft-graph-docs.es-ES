---
title: 'orgContact: checkMemberGroups'
description: Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea Permisos.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 15fef20514d63a2009f943ca5956af5f026b2fa5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27973345"
---
# <a name="orgcontact-checkmembergroups"></a><span data-ttu-id="5bdbe-104">orgContact: checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="5bdbe-104">orgContact: checkMemberGroups</span></span>

> <span data-ttu-id="5bdbe-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5bdbe-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5bdbe-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5bdbe-106">Use of these APIs in production applications is not supported.</span></span>

## <a name="permissions"></a><span data-ttu-id="5bdbe-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5bdbe-107">Permissions</span></span>
<span data-ttu-id="5bdbe-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5bdbe-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5bdbe-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5bdbe-110">Permission type</span></span>      | <span data-ttu-id="5bdbe-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5bdbe-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5bdbe-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5bdbe-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5bdbe-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="5bdbe-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="5bdbe-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5bdbe-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5bdbe-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5bdbe-115">Not supported.</span></span>    |
|<span data-ttu-id="5bdbe-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5bdbe-116">Application</span></span> | <span data-ttu-id="5bdbe-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5bdbe-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5bdbe-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5bdbe-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /contacts/{id}/checkMemberGroups

```
## <a name="request-headers"></a><span data-ttu-id="5bdbe-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5bdbe-119">Request headers</span></span>
| <span data-ttu-id="5bdbe-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="5bdbe-120">Name</span></span>       | <span data-ttu-id="5bdbe-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="5bdbe-121">Type</span></span> | <span data-ttu-id="5bdbe-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="5bdbe-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="5bdbe-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="5bdbe-123">Authorization</span></span>  | <span data-ttu-id="5bdbe-124">string</span><span class="sxs-lookup"><span data-stu-id="5bdbe-124">string</span></span>  | <span data-ttu-id="5bdbe-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5bdbe-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5bdbe-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5bdbe-127">Request body</span></span>
<span data-ttu-id="5bdbe-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="5bdbe-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="5bdbe-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5bdbe-129">Parameter</span></span>    | <span data-ttu-id="5bdbe-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="5bdbe-130">Type</span></span>   |<span data-ttu-id="5bdbe-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="5bdbe-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5bdbe-132">groupIds</span><span class="sxs-lookup"><span data-stu-id="5bdbe-132">groupIds</span></span>|<span data-ttu-id="5bdbe-133">String</span><span class="sxs-lookup"><span data-stu-id="5bdbe-133">String</span></span>||

## <a name="response"></a><span data-ttu-id="5bdbe-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5bdbe-134">Response</span></span>

<span data-ttu-id="5bdbe-135">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5bdbe-135">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5bdbe-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5bdbe-136">Example</span></span>
<span data-ttu-id="5bdbe-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="5bdbe-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="5bdbe-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5bdbe-138">Request</span></span>
<span data-ttu-id="5bdbe-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5bdbe-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "orgcontact_checkmembergroups"
}-->
```http
POST https://graph.microsoft.com/beta/contacts/{id}/checkMemberGroups
Content-type: application/json
Content-length: 44

{
  "groupIds": [
    "groupIds-value"
  ]
}
```

##### <a name="response"></a><span data-ttu-id="5bdbe-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5bdbe-140">Response</span></span>
<span data-ttu-id="5bdbe-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5bdbe-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "orgContact: checkMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
