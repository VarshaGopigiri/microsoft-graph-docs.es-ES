---
title: Update alert
description: Actualizar una propiedad modificable **alerta** dentro de cualquier solución integrada para mantener sincronizados estado de la alerta y las asignaciones entre las soluciones. Este método actualiza cualquier solución que tiene un registro de la alerta de que se hace referencia a identificador.
localization_priority: Normal
ms.openlocfilehash: dc5c1197e344aa181d827acc654e24bd5a048a06
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858096"
---
# <a name="update-alert"></a><span data-ttu-id="7d3bb-104">Update alert</span><span class="sxs-lookup"><span data-stu-id="7d3bb-104">Update alert</span></span>

<span data-ttu-id="7d3bb-105">Actualizar una propiedad modificable **alerta** dentro de cualquier solución integrada para mantener sincronizados estado de la alerta y las asignaciones entre las soluciones.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-105">Update an editable **alert** property within any integrated solution to keep alert status and assignments in sync across solutions.</span></span> <span data-ttu-id="7d3bb-106">Este método actualiza cualquier solución que tiene un registro de la alerta de que se hace referencia a identificador.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-106">This method updates any solution that has a record of the referenced alert ID.</span></span>

## <a name="permissions"></a><span data-ttu-id="7d3bb-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="7d3bb-107">Permissions</span></span>

<span data-ttu-id="7d3bb-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7d3bb-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7d3bb-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7d3bb-110">Permission type</span></span>      | <span data-ttu-id="7d3bb-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7d3bb-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7d3bb-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7d3bb-112">Delegated (work or school account)</span></span> |   <span data-ttu-id="7d3bb-113">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7d3bb-113">SecurityEvents.ReadWrite.All</span></span>  |
|<span data-ttu-id="7d3bb-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7d3bb-114">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="7d3bb-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-115">Not supported.</span></span>  |
|<span data-ttu-id="7d3bb-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7d3bb-116">Application</span></span> | <span data-ttu-id="7d3bb-117">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7d3bb-117">SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7d3bb-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7d3bb-118">HTTP request</span></span>

> <span data-ttu-id="7d3bb-119">**Nota:** Debe incluir el identificador de **alerta** como un parámetro y vendorInformation que contiene el `provider` y `vendor` con este método.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-119">**Note:** You must include the **alert** ID as a parameter and vendorInformation containing the `provider` and `vendor` with this method.</span></span>
<!-- { "blockType": "ignored" } -->

```http
PATCH /security/alerts/{alert_id}
```

## <a name="request-headers"></a><span data-ttu-id="7d3bb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7d3bb-120">Request headers</span></span>

| <span data-ttu-id="7d3bb-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="7d3bb-121">Name</span></span>       | <span data-ttu-id="7d3bb-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d3bb-122">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="7d3bb-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="7d3bb-123">Authorization</span></span>  | <span data-ttu-id="7d3bb-p104">{código} del portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-p104">Bearer {code}. Required.</span></span>|
|<span data-ttu-id="7d3bb-126">Prefer</span><span class="sxs-lookup"><span data-stu-id="7d3bb-126">Prefer</span></span> | <span data-ttu-id="7d3bb-127">devolver = representación</span><span class="sxs-lookup"><span data-stu-id="7d3bb-127">return=representation</span></span> |

## <a name="request-body"></a><span data-ttu-id="7d3bb-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7d3bb-128">Request body</span></span>

<span data-ttu-id="7d3bb-129">En el cuerpo de la solicitud, proporcionar una representación JSON de los valores para los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-129">In the request body, supply a JSON representation of the values for relevant fields that should be updated.</span></span> <span data-ttu-id="7d3bb-130">El cuerpo **debe** contener el `vendorInformation` propiedad con válido `provider` y `vendor` campos.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-130">The body **must** contain the `vendorInformation` property with valid `provider` and `vendor` fields.</span></span> <span data-ttu-id="7d3bb-131">En la siguiente tabla se enumera los campos que se pueden actualizar para una alerta.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-131">The following table lists the fields that can be updated for an alert.</span></span> <span data-ttu-id="7d3bb-132">Los valores para las propiedades existentes que no se incluyen en el cuerpo de la solicitud no cambiará.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-132">The values for existing properties that are not included in the request body will not change.</span></span> <span data-ttu-id="7d3bb-133">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-133">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="7d3bb-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7d3bb-134">Property</span></span>   | <span data-ttu-id="7d3bb-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d3bb-135">Type</span></span> |<span data-ttu-id="7d3bb-136">Description</span><span class="sxs-lookup"><span data-stu-id="7d3bb-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7d3bb-137">assignedTo</span><span class="sxs-lookup"><span data-stu-id="7d3bb-137">assignedTo</span></span>|<span data-ttu-id="7d3bb-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="7d3bb-138">String</span></span>|<span data-ttu-id="7d3bb-139">Nombre del analista de la alerta se asigna a para la evaluación de errores, investigación o corrección.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-139">Name of the analyst the alert is assigned to for triage, investigation, or remediation.</span></span>|
|<span data-ttu-id="7d3bb-140">closedDateTime</span><span class="sxs-lookup"><span data-stu-id="7d3bb-140">closedDateTime</span></span>|<span data-ttu-id="7d3bb-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7d3bb-141">DateTimeOffset</span></span>|<span data-ttu-id="7d3bb-142">Hora a la que se ha cerrado la alerta.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-142">Time at which the alert was closed.</span></span> <span data-ttu-id="7d3bb-143">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-143">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="7d3bb-144">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-144">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="7d3bb-145">comments</span><span class="sxs-lookup"><span data-stu-id="7d3bb-145">comments</span></span>|<span data-ttu-id="7d3bb-146">Colección String</span><span class="sxs-lookup"><span data-stu-id="7d3bb-146">String collection</span></span>|<span data-ttu-id="7d3bb-147">Comentarios de los analistas de la alerta (para la administración de alertas del cliente).</span><span class="sxs-lookup"><span data-stu-id="7d3bb-147">Analyst comments on the alert (for customer alert management).</span></span>|
|<span data-ttu-id="7d3bb-148">comentarios</span><span class="sxs-lookup"><span data-stu-id="7d3bb-148">feedback</span></span>|<span data-ttu-id="7d3bb-149">alertFeedback</span><span class="sxs-lookup"><span data-stu-id="7d3bb-149">alertFeedback</span></span>|<span data-ttu-id="7d3bb-150">Comentarios de analistas de la alerta.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-150">Analyst feedback on the alert.</span></span> <span data-ttu-id="7d3bb-151">Los valores posibles son: `unknown`, `truePositive`, `falsePositive` y `benignPositive`.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-151">Possible values are: `unknown`, `truePositive`, `falsePositive`, `benignPositive`.</span></span>|
|<span data-ttu-id="7d3bb-152">status</span><span class="sxs-lookup"><span data-stu-id="7d3bb-152">status</span></span>|<span data-ttu-id="7d3bb-153">alertStatus</span><span class="sxs-lookup"><span data-stu-id="7d3bb-153">alertStatus</span></span>|<span data-ttu-id="7d3bb-154">Estado de alerta del ciclo de vida (escenario).</span><span class="sxs-lookup"><span data-stu-id="7d3bb-154">Alert lifecycle status (stage).</span></span> <span data-ttu-id="7d3bb-155">Los valores posibles son: `unknown`, `newAlert`, `inProgress` y `resolved`.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-155">Possible values are: `unknown`, `newAlert`, `inProgress`, `resolved`.</span></span>|
|<span data-ttu-id="7d3bb-156">de cierre</span><span class="sxs-lookup"><span data-stu-id="7d3bb-156">tags</span></span>|<span data-ttu-id="7d3bb-157">Colección String</span><span class="sxs-lookup"><span data-stu-id="7d3bb-157">String collection</span></span>|<span data-ttu-id="7d3bb-158">Rótulos definidos por el usuario que se pueden aplicar a una alerta y pueden servir como condiciones de filtro (por ejemplo, "HVA", "han visto).</span><span class="sxs-lookup"><span data-stu-id="7d3bb-158">User-definable labels that can be applied to an alert and can serve as filter conditions (for example, "HVA", "SAW).</span></span>|
|<span data-ttu-id="7d3bb-159">vendorInformation</span><span class="sxs-lookup"><span data-stu-id="7d3bb-159">vendorInformation</span></span> |[<span data-ttu-id="7d3bb-160">securityVendorInformation</span><span class="sxs-lookup"><span data-stu-id="7d3bb-160">securityVendorInformation</span></span>](../resources/securityvendorinformation.md)|<span data-ttu-id="7d3bb-161">Tipo complejo que contiene detalles sobre el proveedor del producto o servicio de seguridad, el proveedor y la subprovider (por ejemplo, proveedor = Microsoft; proveedor = Windows Defender ATP; subProvider = AppLocker).</span><span class="sxs-lookup"><span data-stu-id="7d3bb-161">Complex type containing details about the security product/service vendor, provider, and subprovider (for example, vendor=Microsoft; provider=Windows Defender ATP; subProvider=AppLocker).</span></span> <span data-ttu-id="7d3bb-162">**Proveedor y proveedor campos son obligatorios.**</span><span class="sxs-lookup"><span data-stu-id="7d3bb-162">**Provider and vendor fields are required.**</span></span>|

## <a name="response"></a><span data-ttu-id="7d3bb-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d3bb-163">Response</span></span>

<span data-ttu-id="7d3bb-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-164">If successful, this method returns a `204 No Content` response code.</span></span>

<span data-ttu-id="7d3bb-165">Si se utiliza el encabezado de solicitud opcional, el método devuelve un `200 OK` código de respuesta y el objeto actualizado de [alerta](../resources/alert.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-165">If the optional request header is used, the method returns a `200 OK` response code and the updated [alert](../resources/alert.md) object in the response body.</span></span>

## <a name="example-1"></a><span data-ttu-id="7d3bb-166">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="7d3bb-166">Example 1</span></span>

### <a name="request"></a><span data-ttu-id="7d3bb-167">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7d3bb-167">Request</span></span>

<span data-ttu-id="7d3bb-168">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-168">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_alert"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/security/alerts/{alert_id}
Content-type: application/json

{
  "assignedTo": "String",
  "closedDateTime": "String (timestamp)",
  "comments": ["String"],
  "feedback": "@odata.type: microsoft.graph.alertFeedback",
  "status": "@odata.type: microsoft.graph.alertStatus",
  "tags": ["String"],
  "vendorInformation":
    {
      "provider": "String",
      "vendor": "String"
    }
}
```

### <a name="response"></a><span data-ttu-id="7d3bb-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d3bb-169">Response</span></span>

<span data-ttu-id="7d3bb-170">El siguiente es un ejemplo de una respuesta correcta.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-170">The following is an example of a successful response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert"
} -->

```http
HTTP/1.1 204 No Content
```

## <a name="example-2"></a><span data-ttu-id="7d3bb-171">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="7d3bb-171">Example 2</span></span>

### <a name="request"></a><span data-ttu-id="7d3bb-172">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7d3bb-172">Request</span></span>

<span data-ttu-id="7d3bb-173">En el ejemplo siguiente se muestra una solicitud que incluye el `Prefer` encabezado de solicitud.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-173">The following example shows a request that includes the `Prefer` request header.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_alert"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/security/alerts/{alert_id}
Content-type: application/json
Prefer: return=representation

{
  "assignedTo": "String",
  "closedDateTime": "String (timestamp)",
  "comments": ["String"],
  "feedback": "@odata.type: microsoft.graph.alertFeedback",
  "status": "@odata.type: microsoft.graph.alertStatus",
  "tags": ["String"],
  "vendorInformation":
    {
      "provider": "String",
      "vendor": "String"
    }
}
```

### <a name="response"></a><span data-ttu-id="7d3bb-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d3bb-174">Response</span></span>

<span data-ttu-id="7d3bb-175">El siguiente es un ejemplo de la respuesta cuando la opcional `Prefer: return=representation` se utiliza el encabezado de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-175">The following is an example of the response when the optional `Prefer: return=representation` request header is used.</span></span>

><span data-ttu-id="7d3bb-p110">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7d3bb-p110">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "activityGroupName": "activityGroupName-value",
  "assignedTo": "assignedTo-value",
  "azureSubscriptionId": "azureSubscriptionId-value",
  "azureTenantId": "azureTenantId-value",
  "category": "category-value",
  "closedDateTime": "datetime-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update alert",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
