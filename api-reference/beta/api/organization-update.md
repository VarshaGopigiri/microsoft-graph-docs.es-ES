---
title: Actualizar organización
description: Actualice las propiedades de la organización autenticada actualmente.
localization_priority: Normal
ms.openlocfilehash: ae91b0f7cf92619f07f042c515bad2aab0d1035a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890422"
---
# <a name="update-organization"></a><span data-ttu-id="e9930-103">Actualizar organización</span><span class="sxs-lookup"><span data-stu-id="e9930-103">Update organization</span></span>

> <span data-ttu-id="e9930-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e9930-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e9930-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e9930-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e9930-106">Actualice las propiedades de la organización autenticada actualmente.</span><span class="sxs-lookup"><span data-stu-id="e9930-106">Update the properties of the currently authenticated organization.</span></span> <span data-ttu-id="e9930-107">En este caso, `organization` se define como una colección de exactamente un registro, y por lo que se debe especificar su **identificador** en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9930-107">In this case, `organization` is defined as a collection of exactly one record, and so its **ID** must be specified in the request.</span></span>  <span data-ttu-id="e9930-108">El **identificador** es también conocida como **tenantId** de la organización.</span><span class="sxs-lookup"><span data-stu-id="e9930-108">The **ID** is also known as the **tenantId** of the organization.</span></span>

## <a name="permissions"></a><span data-ttu-id="e9930-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="e9930-109">Permissions</span></span>

<span data-ttu-id="e9930-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e9930-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e9930-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e9930-112">Permission type</span></span> | <span data-ttu-id="e9930-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e9930-113">Permissions (from least to most privileged)</span></span> |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e9930-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e9930-114">Delegated (work or school account)</span></span> | <span data-ttu-id="e9930-115">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="e9930-115">Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="e9930-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e9930-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e9930-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9930-117">Not supported.</span></span> |
|<span data-ttu-id="e9930-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e9930-118">Application</span></span> | <span data-ttu-id="e9930-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9930-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e9930-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e9930-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /organization/{id}
```

## <a name="request-headers"></a><span data-ttu-id="e9930-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9930-121">Request headers</span></span>

| <span data-ttu-id="e9930-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="e9930-122">Name</span></span>       | <span data-ttu-id="e9930-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9930-123">Type</span></span> | <span data-ttu-id="e9930-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9930-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="e9930-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="e9930-125">Authorization</span></span>  | <span data-ttu-id="e9930-126">string</span><span class="sxs-lookup"><span data-stu-id="e9930-126">string</span></span>  | <span data-ttu-id="e9930-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e9930-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e9930-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e9930-129">Request body</span></span>

<span data-ttu-id="e9930-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="e9930-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="e9930-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e9930-133">Property</span></span>     | <span data-ttu-id="e9930-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9930-134">Type</span></span>   |<span data-ttu-id="e9930-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9930-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e9930-136">marketingNotificationEmails</span><span class="sxs-lookup"><span data-stu-id="e9930-136">marketingNotificationEmails</span></span>|<span data-ttu-id="e9930-137">Colección String</span><span class="sxs-lookup"><span data-stu-id="e9930-137">String collection</span></span>|                                        <span data-ttu-id="e9930-138">**Notas**: No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="e9930-138">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="e9930-139">privacyProfile</span><span class="sxs-lookup"><span data-stu-id="e9930-139">privacyProfile</span></span>|[<span data-ttu-id="e9930-140">privacyProfile</span><span class="sxs-lookup"><span data-stu-id="e9930-140">privacyProfile</span></span>](../resources/privacyprofile.md)|<span data-ttu-id="e9930-141">Perfil de privacidad de una organización (establecer statementUrl y contactEmail).</span><span class="sxs-lookup"><span data-stu-id="e9930-141">The privacy profile of an organization (set statementUrl and contactEmail).</span></span>            |
|<span data-ttu-id="e9930-142">securityComplianceNotificationMails</span><span class="sxs-lookup"><span data-stu-id="e9930-142">securityComplianceNotificationMails</span></span>|<span data-ttu-id="e9930-143">Colección String</span><span class="sxs-lookup"><span data-stu-id="e9930-143">String collection</span></span>||
|<span data-ttu-id="e9930-144">securityComplianceNotificationPhones</span><span class="sxs-lookup"><span data-stu-id="e9930-144">securityComplianceNotificationPhones</span></span>|<span data-ttu-id="e9930-145">Colección String</span><span class="sxs-lookup"><span data-stu-id="e9930-145">String collection</span></span>||
|<span data-ttu-id="e9930-146">technicalNotificationMails</span><span class="sxs-lookup"><span data-stu-id="e9930-146">technicalNotificationMails</span></span>|<span data-ttu-id="e9930-147">Colección String</span><span class="sxs-lookup"><span data-stu-id="e9930-147">String collection</span></span>|                                        <span data-ttu-id="e9930-148">**Notas**: No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="e9930-148">**Notes**: not nullable.</span></span>            |

<span data-ttu-id="e9930-149">Puesto que el recurso de la **organización** admite [extensiones](/graph/extensibility-overview), puede usar el `PATCH` operación para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia existente de la **organización** .</span><span class="sxs-lookup"><span data-stu-id="e9930-149">Since the **organization** resource supports [extensions](/graph/extensibility-overview), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **organization** instance.</span></span>

## <a name="response"></a><span data-ttu-id="e9930-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9930-150">Response</span></span>

<span data-ttu-id="e9930-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9930-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e9930-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e9930-153">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e9930-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9930-154">Request</span></span>
<span data-ttu-id="e9930-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9930-155">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="e9930-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9930-156">Response</span></span>

<span data-ttu-id="e9930-157">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9930-157">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.organization"
} -->

```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a><span data-ttu-id="e9930-158">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e9930-158">See also</span></span>

- [<span data-ttu-id="e9930-159">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="e9930-159">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="e9930-160">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="e9930-160">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)

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
