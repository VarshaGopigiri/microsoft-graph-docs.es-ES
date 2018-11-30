---
title: Actualizar secureScoreControlProfiles
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: afbfcd1889c55dd53241ff8d796bb3ab492b2acf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083138"
---
# <a name="update-securescorecontrolprofiles"></a><span data-ttu-id="5e0e8-104">Actualizar secureScoreControlProfiles</span><span class="sxs-lookup"><span data-stu-id="5e0e8-104">Update secureScoreControlProfiles</span></span>

 > <span data-ttu-id="5e0e8-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5e0e8-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5e0e8-107">Actualizar una propiedad modificable **secureScoreControlProfiles** dentro de cualquier solución integrada para cambiar varias propiedades, como **assignedTo** o **tenantNote**.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-107">Update an editable **secureScoreControlProfiles** property within any integrated solution to change various properties, such as **assignedTo** or **tenantNote**.</span></span>

## <a name="permissions"></a><span data-ttu-id="5e0e8-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="5e0e8-108">Permissions</span></span>

<span data-ttu-id="5e0e8-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5e0e8-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5e0e8-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5e0e8-111">Permission type</span></span>      | <span data-ttu-id="5e0e8-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5e0e8-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5e0e8-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5e0e8-113">Delegated (work or school account)</span></span> |   <span data-ttu-id="5e0e8-114">SecurityEvents.ReadWrite.All.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-114">SecurityEvents.ReadWrite.All.</span></span>  |
|<span data-ttu-id="5e0e8-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5e0e8-115">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="5e0e8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-116">Not supported.</span></span>  |
|<span data-ttu-id="5e0e8-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5e0e8-117">Application</span></span> | <span data-ttu-id="5e0e8-118">SecurityEvents.ReadWrite.All.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-118">SecurityEvents.ReadWrite.All.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5e0e8-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5e0e8-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /security/secureScoreControlProfiles/{id}
```

## <a name="request-headers"></a><span data-ttu-id="5e0e8-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5e0e8-120">Request headers</span></span>

| <span data-ttu-id="5e0e8-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="5e0e8-121">Name</span></span>       | <span data-ttu-id="5e0e8-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e0e8-122">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="5e0e8-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="5e0e8-123">Authorization</span></span>  | <span data-ttu-id="5e0e8-p104">{código} del portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-p104">Bearer {code}. Required.</span></span>|
|<span data-ttu-id="5e0e8-126">Prefer</span><span class="sxs-lookup"><span data-stu-id="5e0e8-126">Prefer</span></span> | <span data-ttu-id="5e0e8-127">devolver = representación.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-127">return=representation.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5e0e8-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5e0e8-128">Request body</span></span>

<span data-ttu-id="5e0e8-129">En el cuerpo de la solicitud, proporcionar una representación JSON de los valores para los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-129">In the request body, supply a JSON representation of the values for relevant fields that should be updated.</span></span> <span data-ttu-id="5e0e8-130">En la siguiente tabla se enumera los campos que se pueden actualizar para un secureScoreControlProfile.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-130">The following table lists the fields that can be updated for a secureScoreControlProfile.</span></span> <span data-ttu-id="5e0e8-131">Los valores para las propiedades existentes que no se incluyen en el cuerpo de la solicitud no cambiará.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-131">The values for existing properties that are not included in the request body will not change.</span></span> <span data-ttu-id="5e0e8-132">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-132">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="5e0e8-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5e0e8-133">Property</span></span>   | <span data-ttu-id="5e0e8-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="5e0e8-134">Type</span></span> |<span data-ttu-id="5e0e8-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e0e8-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5e0e8-136">assignedTo</span><span class="sxs-lookup"><span data-stu-id="5e0e8-136">assignedTo</span></span>|<span data-ttu-id="5e0e8-137">String</span><span class="sxs-lookup"><span data-stu-id="5e0e8-137">String</span></span>|<span data-ttu-id="5e0e8-138">Nombre de la analista el control se asigna a para la evaluación de errores, la implementación o la corrección.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-138">Name of the analyst the control is assigned to for triage, implementation, or remediation.</span></span>|
|<span data-ttu-id="5e0e8-139">tenantNote</span><span class="sxs-lookup"><span data-stu-id="5e0e8-139">tenantNote</span></span>|<span data-ttu-id="5e0e8-140">String</span><span class="sxs-lookup"><span data-stu-id="5e0e8-140">String</span></span>|<span data-ttu-id="5e0e8-141">Comentarios de los analistas en el control (para la administración de control de clientes).</span><span class="sxs-lookup"><span data-stu-id="5e0e8-141">Analyst comments on the control (for customer control management).</span></span>|
|<span data-ttu-id="5e0e8-142">controlStateUpdates</span><span class="sxs-lookup"><span data-stu-id="5e0e8-142">controlStateUpdates</span></span>| <span data-ttu-id="5e0e8-143">String</span><span class="sxs-lookup"><span data-stu-id="5e0e8-143">String</span></span>|<span data-ttu-id="5e0e8-144">Analista controlado por el valor en el control.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-144">Analyst driven setting on the control.</span></span> <span data-ttu-id="5e0e8-145">Los valores posibles son: `ignore`, `thirdParty` y `reviewed`.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-145">Possible values are: `ignore`, `thirdParty`, `reviewed`.</span></span>|


## <a name="response"></a><span data-ttu-id="5e0e8-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e0e8-146">Response</span></span>

<span data-ttu-id="5e0e8-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-147">If successful, this method returns a `204 No Content` response code.</span></span>

<span data-ttu-id="5e0e8-148">Si se utiliza el encabezado de solicitud opcional, el método devuelve un `200 OK` código de respuesta y el objeto actualizado [secureScoreControlProfiles](../resources/securescorecontrolprofiles.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-148">If the optional request header is used, the method returns a `200 OK` response code and the updated [secureScoreControlProfiles](../resources/securescorecontrolprofiles.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5e0e8-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5e0e8-149">Example</span></span>

### <a name="request"></a><span data-ttu-id="5e0e8-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5e0e8-150">Request</span></span>

<span data-ttu-id="5e0e8-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-151">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "securescorecontrolprofiles_update"
}-->

```http
PATCH https://graph.microsoft.com/beta/security/secureScoreControlProfiles/AdminMFA
Content-type: application/json

{
  "assignedTo": "assignedTo-value",
  "controlStateUpdates": "controlStateUpdates-value",
  "tenantNote": "tenantNote-value"
}
```

### <a name="response"></a><span data-ttu-id="5e0e8-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e0e8-152">Response</span></span>

<span data-ttu-id="5e0e8-153">El siguiente es un ejemplo de una respuesta correcta.</span><span class="sxs-lookup"><span data-stu-id="5e0e8-153">The following is an example of a successful response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.secureScoreControlProfiles"
} -->

```http
HTTP/1.1 204 No Content
```




<!-- {
  "type": "#page.annotation",
  "description": "Update secureScoreControlProfiles",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
