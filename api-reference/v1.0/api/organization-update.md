---
title: Actualizar organización
description: Actualice las propiedades de la organización autenticada actualmente.
ms.openlocfilehash: ac07f3ded31f8d6c7169d24208ed7e8cf967e07a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031775"
---
# <a name="update-organization"></a><span data-ttu-id="6322b-103">Actualizar organización</span><span class="sxs-lookup"><span data-stu-id="6322b-103">Update organization</span></span>

<span data-ttu-id="6322b-104">Actualice las propiedades de la organización autenticada actualmente.</span><span class="sxs-lookup"><span data-stu-id="6322b-104">Update the properties of the currently authenticated organization.</span></span>

## <a name="permissions"></a><span data-ttu-id="6322b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="6322b-105">Permissions</span></span>

<span data-ttu-id="6322b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6322b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6322b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6322b-108">Permission type</span></span> | <span data-ttu-id="6322b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6322b-109">Permissions (from least to most privileged)</span></span> |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6322b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6322b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="6322b-111">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="6322b-111">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="6322b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6322b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6322b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6322b-113">Not supported.</span></span>    |
|<span data-ttu-id="6322b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6322b-114">Application</span></span> | <span data-ttu-id="6322b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6322b-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6322b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6322b-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /organization

```

## <a name="request-headers"></a><span data-ttu-id="6322b-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6322b-117">Request headers</span></span>

| <span data-ttu-id="6322b-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="6322b-118">Name</span></span>       | <span data-ttu-id="6322b-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="6322b-119">Type</span></span> | <span data-ttu-id="6322b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="6322b-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6322b-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="6322b-121">Authorization</span></span>  | <span data-ttu-id="6322b-122">string</span><span class="sxs-lookup"><span data-stu-id="6322b-122">string</span></span>  | <span data-ttu-id="6322b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6322b-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6322b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6322b-125">Request body</span></span>
<span data-ttu-id="6322b-126">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="6322b-126">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="6322b-127">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6322b-127">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="6322b-128">Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="6322b-128">For best performance, you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="6322b-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6322b-129">Property</span></span>     | <span data-ttu-id="6322b-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="6322b-130">Type</span></span>   |<span data-ttu-id="6322b-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="6322b-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6322b-132">marketingNotificationEmails</span><span class="sxs-lookup"><span data-stu-id="6322b-132">marketingNotificationEmails</span></span>|<span data-ttu-id="6322b-133">Colección String</span><span class="sxs-lookup"><span data-stu-id="6322b-133">String collection</span></span>|                                        <span data-ttu-id="6322b-134">**Notas**: No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="6322b-134">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="6322b-135">privacyProfile</span><span class="sxs-lookup"><span data-stu-id="6322b-135">privacyProfile</span></span>|[<span data-ttu-id="6322b-136">privacyProfile</span><span class="sxs-lookup"><span data-stu-id="6322b-136">privacyProfile</span></span>](../resources/privacyprofile.md)|<span data-ttu-id="6322b-137">Perfil de privacidad de una organización (establecer statementUrl y contactEmail).</span><span class="sxs-lookup"><span data-stu-id="6322b-137">The privacy profile of an organization (set statementUrl and contactEmail).</span></span>            |
|<span data-ttu-id="6322b-138">securityComplianceNotificationMails</span><span class="sxs-lookup"><span data-stu-id="6322b-138">securityComplianceNotificationMails</span></span>|<span data-ttu-id="6322b-139">Colección String</span><span class="sxs-lookup"><span data-stu-id="6322b-139">String collection</span></span>||
|<span data-ttu-id="6322b-140">securityComplianceNotificationPhones</span><span class="sxs-lookup"><span data-stu-id="6322b-140">securityComplianceNotificationPhones</span></span>|<span data-ttu-id="6322b-141">Colección String</span><span class="sxs-lookup"><span data-stu-id="6322b-141">String collection</span></span>||
|<span data-ttu-id="6322b-142">technicalNotificationMails</span><span class="sxs-lookup"><span data-stu-id="6322b-142">technicalNotificationMails</span></span>|<span data-ttu-id="6322b-143">Colección String</span><span class="sxs-lookup"><span data-stu-id="6322b-143">String collection</span></span>|                                        <span data-ttu-id="6322b-144">**Notas**: No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="6322b-144">**Notes**: not nullable.</span></span>            |

## <a name="response"></a><span data-ttu-id="6322b-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6322b-145">Response</span></span>

<span data-ttu-id="6322b-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="6322b-146">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="6322b-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6322b-147">Example</span></span>

### <a name="request"></a><span data-ttu-id="6322b-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6322b-148">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "update_organization"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/organization
Content-type: application/json
Content-length: 411

{
  "marketingNotificationEmails" : ["marketing@contoso.com"],
  "privacyProfile" :
    {
      "contactEmail":"alice@contoso.com",
      "statementUrl":"https://contoso.com/privacyStatement"
    },
  "securityComplianceNotificationMails" : ["security@contoso.com"],
  "securityComplianceNotificationPhones" : ["(123) 456-7890"],
  "technicalNotificationMails" : ["tech@contoso.com"]
}
```

### <a name="response"></a><span data-ttu-id="6322b-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6322b-149">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.organization"
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update organization",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
