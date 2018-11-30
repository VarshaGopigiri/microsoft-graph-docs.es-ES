---
title: Actualizar organización
description: Actualice las propiedades de la organización autenticada actualmente.
ms.openlocfilehash: 62e03d7bee58f14acc5d5ace12d55f95d1d07a2d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085011"
---
# <a name="update-organization"></a><span data-ttu-id="f6961-103">Actualizar organización</span><span class="sxs-lookup"><span data-stu-id="f6961-103">Update organization</span></span>

> <span data-ttu-id="f6961-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f6961-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f6961-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f6961-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f6961-106">Actualice las propiedades de la organización autenticada actualmente.</span><span class="sxs-lookup"><span data-stu-id="f6961-106">Update the properties of the currently authenticated organization.</span></span>
## <a name="permissions"></a><span data-ttu-id="f6961-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="f6961-107">Permissions</span></span>
<span data-ttu-id="f6961-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f6961-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f6961-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f6961-110">Permission type</span></span> | <span data-ttu-id="f6961-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f6961-111">Permissions (from least to most privileged)</span></span> |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f6961-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f6961-112">Delegated (work or school account)</span></span> | <span data-ttu-id="f6961-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f6961-113">Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="f6961-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f6961-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f6961-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f6961-115">Not supported.</span></span> |
|<span data-ttu-id="f6961-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f6961-116">Application</span></span> | <span data-ttu-id="f6961-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f6961-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f6961-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f6961-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /organization

```
## <a name="request-headers"></a><span data-ttu-id="f6961-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f6961-119">Request headers</span></span>
| <span data-ttu-id="f6961-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="f6961-120">Name</span></span>       | <span data-ttu-id="f6961-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6961-121">Type</span></span> | <span data-ttu-id="f6961-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6961-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="f6961-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="f6961-123">Authorization</span></span>  | <span data-ttu-id="f6961-124">string</span><span class="sxs-lookup"><span data-stu-id="f6961-124">string</span></span>  | <span data-ttu-id="f6961-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f6961-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f6961-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f6961-127">Request body</span></span>
<span data-ttu-id="f6961-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="f6961-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="f6961-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f6961-131">Property</span></span>     | <span data-ttu-id="f6961-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6961-132">Type</span></span>   |<span data-ttu-id="f6961-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6961-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f6961-134">marketingNotificationEmails</span><span class="sxs-lookup"><span data-stu-id="f6961-134">marketingNotificationEmails</span></span>|<span data-ttu-id="f6961-135">Colección String</span><span class="sxs-lookup"><span data-stu-id="f6961-135">String collection</span></span>|                                        <span data-ttu-id="f6961-136">**Notas**: No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="f6961-136">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="f6961-137">privacyProfile</span><span class="sxs-lookup"><span data-stu-id="f6961-137">privacyProfile</span></span>|[<span data-ttu-id="f6961-138">privacyProfile</span><span class="sxs-lookup"><span data-stu-id="f6961-138">privacyProfile</span></span>](../resources/privacyprofile.md)|<span data-ttu-id="f6961-139">Perfil de privacidad de una organización (establecer statementUrl y contactEmail).</span><span class="sxs-lookup"><span data-stu-id="f6961-139">The privacy profile of an organization (set statementUrl and contactEmail).</span></span>            |
|<span data-ttu-id="f6961-140">securityComplianceNotificationMails</span><span class="sxs-lookup"><span data-stu-id="f6961-140">securityComplianceNotificationMails</span></span>|<span data-ttu-id="f6961-141">Colección String</span><span class="sxs-lookup"><span data-stu-id="f6961-141">String collection</span></span>||
|<span data-ttu-id="f6961-142">securityComplianceNotificationPhones</span><span class="sxs-lookup"><span data-stu-id="f6961-142">securityComplianceNotificationPhones</span></span>|<span data-ttu-id="f6961-143">Colección String</span><span class="sxs-lookup"><span data-stu-id="f6961-143">String collection</span></span>||
|<span data-ttu-id="f6961-144">technicalNotificationMails</span><span class="sxs-lookup"><span data-stu-id="f6961-144">technicalNotificationMails</span></span>|<span data-ttu-id="f6961-145">Colección String</span><span class="sxs-lookup"><span data-stu-id="f6961-145">String collection</span></span>|                                        <span data-ttu-id="f6961-146">**Notas**: No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="f6961-146">**Notes**: not nullable.</span></span>            |

<span data-ttu-id="f6961-147">Puesto que el recurso de la **organización** admite [extensiones](/graph/extensibility-overview), puede usar el `PATCH` operación para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia existente de la **organización** .</span><span class="sxs-lookup"><span data-stu-id="f6961-147">Since the **organization** resource supports [extensions](/graph/extensibility-overview), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **organization** instance.</span></span>

## <a name="response"></a><span data-ttu-id="f6961-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6961-148">Response</span></span>

<span data-ttu-id="f6961-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f6961-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f6961-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f6961-151">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f6961-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f6961-152">Request</span></span>
<span data-ttu-id="f6961-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f6961-153">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_organization"
}-->
```http
PATCH https://graph.microsoft.com/beta/organization
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
##### <a name="response"></a><span data-ttu-id="f6961-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6961-154">Response</span></span>
<span data-ttu-id="f6961-155">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f6961-155">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.administrativeunit"
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a><span data-ttu-id="f6961-156">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f6961-156">See also</span></span>

- [<span data-ttu-id="f6961-157">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="f6961-157">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="f6961-158">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="f6961-158">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
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
