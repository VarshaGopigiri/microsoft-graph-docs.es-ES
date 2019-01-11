---
title: Actualizar organización
description: Actualice las propiedades de la organización autenticada actualmente.
localization_priority: Normal
ms.openlocfilehash: 83b1514831e930e3eabe6e6a78203c44ec3b5b3c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834961"
---
# <a name="update-organization"></a><span data-ttu-id="ad243-103">Actualizar organización</span><span class="sxs-lookup"><span data-stu-id="ad243-103">Update organization</span></span>

<span data-ttu-id="ad243-104">Actualice las propiedades de la organización autenticada actualmente.</span><span class="sxs-lookup"><span data-stu-id="ad243-104">Update the properties of the currently authenticated organization.</span></span> <span data-ttu-id="ad243-105">En este caso, `organization` se define como una colección de exactamente un registro, y por lo que se debe especificar su **identificador** en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ad243-105">In this case, `organization` is defined as a collection of exactly one record, and so its **ID** must be specified in the request.</span></span>  <span data-ttu-id="ad243-106">El **identificador** es también conocida como **tenantId** de la organización.</span><span class="sxs-lookup"><span data-stu-id="ad243-106">The **ID** is also known as the **tenantId** of the organization.</span></span>


## <a name="permissions"></a><span data-ttu-id="ad243-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ad243-107">Permissions</span></span>

<span data-ttu-id="ad243-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ad243-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ad243-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ad243-110">Permission type</span></span> | <span data-ttu-id="ad243-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ad243-111">Permissions (from least to most privileged)</span></span> |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ad243-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ad243-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ad243-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="ad243-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="ad243-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ad243-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ad243-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ad243-115">Not supported.</span></span>    |
|<span data-ttu-id="ad243-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ad243-116">Application</span></span> | <span data-ttu-id="ad243-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ad243-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ad243-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ad243-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /organization/{id}

```

## <a name="request-headers"></a><span data-ttu-id="ad243-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ad243-119">Request headers</span></span>

| <span data-ttu-id="ad243-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="ad243-120">Name</span></span>       | <span data-ttu-id="ad243-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad243-121">Type</span></span> | <span data-ttu-id="ad243-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad243-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="ad243-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ad243-123">Authorization</span></span>  | <span data-ttu-id="ad243-124">string</span><span class="sxs-lookup"><span data-stu-id="ad243-124">string</span></span>  | <span data-ttu-id="ad243-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ad243-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ad243-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ad243-127">Request body</span></span>

<span data-ttu-id="ad243-128">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="ad243-128">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="ad243-129">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="ad243-129">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="ad243-130">Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="ad243-130">For best performance, you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="ad243-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ad243-131">Property</span></span>     | <span data-ttu-id="ad243-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad243-132">Type</span></span>   |<span data-ttu-id="ad243-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad243-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ad243-134">marketingNotificationEmails</span><span class="sxs-lookup"><span data-stu-id="ad243-134">marketingNotificationEmails</span></span>|<span data-ttu-id="ad243-135">Colección String</span><span class="sxs-lookup"><span data-stu-id="ad243-135">String collection</span></span>|                                        <span data-ttu-id="ad243-136">**Notas**: No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="ad243-136">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="ad243-137">privacyProfile</span><span class="sxs-lookup"><span data-stu-id="ad243-137">privacyProfile</span></span>|[<span data-ttu-id="ad243-138">privacyProfile</span><span class="sxs-lookup"><span data-stu-id="ad243-138">privacyProfile</span></span>](../resources/privacyprofile.md)|<span data-ttu-id="ad243-139">Perfil de privacidad de una organización (establecer statementUrl y contactEmail).</span><span class="sxs-lookup"><span data-stu-id="ad243-139">The privacy profile of an organization (set statementUrl and contactEmail).</span></span>            |
|<span data-ttu-id="ad243-140">securityComplianceNotificationMails</span><span class="sxs-lookup"><span data-stu-id="ad243-140">securityComplianceNotificationMails</span></span>|<span data-ttu-id="ad243-141">Colección String</span><span class="sxs-lookup"><span data-stu-id="ad243-141">String collection</span></span>||
|<span data-ttu-id="ad243-142">securityComplianceNotificationPhones</span><span class="sxs-lookup"><span data-stu-id="ad243-142">securityComplianceNotificationPhones</span></span>|<span data-ttu-id="ad243-143">Colección String</span><span class="sxs-lookup"><span data-stu-id="ad243-143">String collection</span></span>||
|<span data-ttu-id="ad243-144">technicalNotificationMails</span><span class="sxs-lookup"><span data-stu-id="ad243-144">technicalNotificationMails</span></span>|<span data-ttu-id="ad243-145">Colección String</span><span class="sxs-lookup"><span data-stu-id="ad243-145">String collection</span></span>|                                        <span data-ttu-id="ad243-146">**Notas**: No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="ad243-146">**Notes**: not nullable.</span></span>            |

## <a name="response"></a><span data-ttu-id="ad243-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad243-147">Response</span></span>

<span data-ttu-id="ad243-148">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="ad243-148">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="ad243-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad243-149">Example</span></span>

### <a name="request"></a><span data-ttu-id="ad243-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ad243-150">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "update_organization"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/organization/{id}
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

### <a name="response"></a><span data-ttu-id="ad243-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad243-151">Response</span></span>

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
