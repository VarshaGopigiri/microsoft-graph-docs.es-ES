---
title: Actualizar organización
description: Actualice las propiedades de la organización autenticada actualmente.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 5ed49dcd0546fedf16572bcf75a8c4366395f1fe
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27964441"
---
# <a name="update-organization"></a><span data-ttu-id="3b275-103">Actualizar organización</span><span class="sxs-lookup"><span data-stu-id="3b275-103">Update organization</span></span>

> <span data-ttu-id="3b275-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3b275-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3b275-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3b275-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3b275-106">Actualice las propiedades de la organización autenticada actualmente.</span><span class="sxs-lookup"><span data-stu-id="3b275-106">Update the properties of the currently authenticated organization.</span></span> <span data-ttu-id="3b275-107">En este caso, `organization` se define como una colección de exactamente un registro, y por lo que se debe especificar su **identificador** en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3b275-107">In this case, `organization` is defined as a collection of exactly one record, and so its **ID** must be specified in the request.</span></span>  <span data-ttu-id="3b275-108">El **identificador** es también conocida como **tenantId** de la organización.</span><span class="sxs-lookup"><span data-stu-id="3b275-108">The **ID** is also known as the **tenantId** of the organization.</span></span>

## <a name="permissions"></a><span data-ttu-id="3b275-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="3b275-109">Permissions</span></span>

<span data-ttu-id="3b275-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3b275-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3b275-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3b275-112">Permission type</span></span> | <span data-ttu-id="3b275-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3b275-113">Permissions (from least to most privileged)</span></span> |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3b275-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3b275-114">Delegated (work or school account)</span></span> | <span data-ttu-id="3b275-115">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="3b275-115">Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="3b275-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3b275-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3b275-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3b275-117">Not supported.</span></span> |
|<span data-ttu-id="3b275-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3b275-118">Application</span></span> | <span data-ttu-id="3b275-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3b275-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="3b275-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3b275-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /organization/{id}
```

## <a name="request-headers"></a><span data-ttu-id="3b275-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3b275-121">Request headers</span></span>

| <span data-ttu-id="3b275-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="3b275-122">Name</span></span>       | <span data-ttu-id="3b275-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="3b275-123">Type</span></span> | <span data-ttu-id="3b275-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b275-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="3b275-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="3b275-125">Authorization</span></span>  | <span data-ttu-id="3b275-126">string</span><span class="sxs-lookup"><span data-stu-id="3b275-126">string</span></span>  | <span data-ttu-id="3b275-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3b275-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3b275-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3b275-129">Request body</span></span>

<span data-ttu-id="3b275-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="3b275-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="3b275-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3b275-133">Property</span></span>     | <span data-ttu-id="3b275-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="3b275-134">Type</span></span>   |<span data-ttu-id="3b275-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b275-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3b275-136">marketingNotificationEmails</span><span class="sxs-lookup"><span data-stu-id="3b275-136">marketingNotificationEmails</span></span>|<span data-ttu-id="3b275-137">Colección String</span><span class="sxs-lookup"><span data-stu-id="3b275-137">String collection</span></span>|                                        <span data-ttu-id="3b275-138">**Notas**: No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="3b275-138">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="3b275-139">privacyProfile</span><span class="sxs-lookup"><span data-stu-id="3b275-139">privacyProfile</span></span>|[<span data-ttu-id="3b275-140">privacyProfile</span><span class="sxs-lookup"><span data-stu-id="3b275-140">privacyProfile</span></span>](../resources/privacyprofile.md)|<span data-ttu-id="3b275-141">Perfil de privacidad de una organización (establecer statementUrl y contactEmail).</span><span class="sxs-lookup"><span data-stu-id="3b275-141">The privacy profile of an organization (set statementUrl and contactEmail).</span></span>            |
|<span data-ttu-id="3b275-142">securityComplianceNotificationMails</span><span class="sxs-lookup"><span data-stu-id="3b275-142">securityComplianceNotificationMails</span></span>|<span data-ttu-id="3b275-143">Colección String</span><span class="sxs-lookup"><span data-stu-id="3b275-143">String collection</span></span>||
|<span data-ttu-id="3b275-144">securityComplianceNotificationPhones</span><span class="sxs-lookup"><span data-stu-id="3b275-144">securityComplianceNotificationPhones</span></span>|<span data-ttu-id="3b275-145">Colección String</span><span class="sxs-lookup"><span data-stu-id="3b275-145">String collection</span></span>||
|<span data-ttu-id="3b275-146">technicalNotificationMails</span><span class="sxs-lookup"><span data-stu-id="3b275-146">technicalNotificationMails</span></span>|<span data-ttu-id="3b275-147">Colección String</span><span class="sxs-lookup"><span data-stu-id="3b275-147">String collection</span></span>|                                        <span data-ttu-id="3b275-148">**Notas**: No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="3b275-148">**Notes**: not nullable.</span></span>            |

<span data-ttu-id="3b275-149">Puesto que el recurso de la **organización** admite [extensiones](/graph/extensibility-overview), puede usar el `PATCH` operación para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia existente de la **organización** .</span><span class="sxs-lookup"><span data-stu-id="3b275-149">Since the **organization** resource supports [extensions](/graph/extensibility-overview), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **organization** instance.</span></span>

## <a name="response"></a><span data-ttu-id="3b275-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b275-150">Response</span></span>

<span data-ttu-id="3b275-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3b275-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3b275-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3b275-153">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3b275-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3b275-154">Request</span></span>
<span data-ttu-id="3b275-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3b275-155">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_organization"
}-->

```http
PATCH https://graph.microsoft.com/beta/organization/{id}
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

##### <a name="response"></a><span data-ttu-id="3b275-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b275-156">Response</span></span>

<span data-ttu-id="3b275-157">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3b275-157">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.organization"
} -->

```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a><span data-ttu-id="3b275-158">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3b275-158">See also</span></span>

- [<span data-ttu-id="3b275-159">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="3b275-159">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="3b275-160">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="3b275-160">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)

<!--
- [Add custom data to groups using schema extensions (preview)](/graph/extensibility-schema-groups)
-->

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update organization",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
