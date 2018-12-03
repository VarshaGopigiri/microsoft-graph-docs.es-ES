---
title: Update alert
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: 9f8040220c64310a04293d43c0c31704c3f49261
ms.sourcegitcommit: 2532b8dd7f2533d956e2600855b3daeabdd9b8ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/30/2018
ms.locfileid: "27091228"
---
# <a name="update-alert"></a><span data-ttu-id="b85fc-104">Update alert</span><span class="sxs-lookup"><span data-stu-id="b85fc-104">Update alert</span></span>

 > <span data-ttu-id="b85fc-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b85fc-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b85fc-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b85fc-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b85fc-107">Actualizar una propiedad modificable **alerta** dentro de cualquier solución integrada para mantener sincronizados estado de la alerta y las asignaciones entre las soluciones.</span><span class="sxs-lookup"><span data-stu-id="b85fc-107">Update an editable **alert** property within any integrated solution to keep alert status and assignments in sync across solutions.</span></span> <span data-ttu-id="b85fc-108">Este método actualiza cualquier solución que tiene un registro de la alerta de que se hace referencia a identificador.</span><span class="sxs-lookup"><span data-stu-id="b85fc-108">This method updates any solution that has a record of the referenced alert ID.</span></span>

## <a name="permissions"></a><span data-ttu-id="b85fc-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="b85fc-109">Permissions</span></span>

<span data-ttu-id="b85fc-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b85fc-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b85fc-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b85fc-112">Permission type</span></span>      | <span data-ttu-id="b85fc-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b85fc-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b85fc-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b85fc-114">Delegated (work or school account)</span></span> |   <span data-ttu-id="b85fc-115">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b85fc-115">SecurityEvents.ReadWrite.All</span></span>  |
|<span data-ttu-id="b85fc-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b85fc-116">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="b85fc-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b85fc-117">Not supported.</span></span>  |
|<span data-ttu-id="b85fc-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b85fc-118">Application</span></span> | <span data-ttu-id="b85fc-119">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b85fc-119">SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b85fc-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b85fc-120">HTTP request</span></span>

> <span data-ttu-id="b85fc-121">**Nota:** Debe incluir el identificador de **alerta** como un parámetro y vendorInformation que contiene el `provider` y `vendor` con este método.</span><span class="sxs-lookup"><span data-stu-id="b85fc-121">**Note:** You must include the **alert** ID as a parameter and vendorInformation containing the `provider` and `vendor` with this method.</span></span>
<!-- { "blockType": "ignored" } -->

```http
PATCH /security/alerts/{alert_id}
```

## <a name="request-headers"></a><span data-ttu-id="b85fc-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b85fc-122">Request headers</span></span>

| <span data-ttu-id="b85fc-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="b85fc-123">Name</span></span>       | <span data-ttu-id="b85fc-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="b85fc-124">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="b85fc-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="b85fc-125">Authorization</span></span>  | <span data-ttu-id="b85fc-p105">{código} del portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="b85fc-p105">Bearer {code}. Required.</span></span>|
|<span data-ttu-id="b85fc-128">Prefer</span><span class="sxs-lookup"><span data-stu-id="b85fc-128">Prefer</span></span> | <span data-ttu-id="b85fc-129">devolver = representación</span><span class="sxs-lookup"><span data-stu-id="b85fc-129">return=representation</span></span> |

## <a name="request-body"></a><span data-ttu-id="b85fc-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b85fc-130">Request body</span></span>

<span data-ttu-id="b85fc-131">En el cuerpo de la solicitud, proporcionar una representación JSON de los valores para los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="b85fc-131">In the request body, supply a JSON representation of the values for relevant fields that should be updated.</span></span> <span data-ttu-id="b85fc-132">El cuerpo **debe** contener el `vendorInformation` propiedad con válido `provider` y `vendor` campos.</span><span class="sxs-lookup"><span data-stu-id="b85fc-132">The body **must** contain the `vendorInformation` property with valid `provider` and `vendor` fields.</span></span> <span data-ttu-id="b85fc-133">En la siguiente tabla se enumera los campos que se pueden actualizar para una alerta.</span><span class="sxs-lookup"><span data-stu-id="b85fc-133">The following table lists the fields that can be updated for an alert.</span></span> <span data-ttu-id="b85fc-134">Los valores para las propiedades existentes que no se incluyen en el cuerpo de la solicitud no cambiará.</span><span class="sxs-lookup"><span data-stu-id="b85fc-134">The values for existing properties that are not included in the request body will not change.</span></span> <span data-ttu-id="b85fc-135">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="b85fc-135">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="b85fc-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b85fc-136">Property</span></span>   | <span data-ttu-id="b85fc-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="b85fc-137">Type</span></span> |<span data-ttu-id="b85fc-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="b85fc-138">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b85fc-139">assignedTo</span><span class="sxs-lookup"><span data-stu-id="b85fc-139">assignedTo</span></span>|<span data-ttu-id="b85fc-140">String</span><span class="sxs-lookup"><span data-stu-id="b85fc-140">String</span></span>|<span data-ttu-id="b85fc-141">Nombre del analista de la alerta se asigna a para la evaluación de errores, investigación o corrección.</span><span class="sxs-lookup"><span data-stu-id="b85fc-141">Name of the analyst the alert is assigned to for triage, investigation, or remediation.</span></span>|
|<span data-ttu-id="b85fc-142">closedDateTime</span><span class="sxs-lookup"><span data-stu-id="b85fc-142">closedDateTime</span></span>|<span data-ttu-id="b85fc-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b85fc-143">DateTimeOffset</span></span>|<span data-ttu-id="b85fc-144">Hora a la que se ha cerrado la alerta.</span><span class="sxs-lookup"><span data-stu-id="b85fc-144">Time at which the alert was closed.</span></span> <span data-ttu-id="b85fc-145">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="b85fc-145">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="b85fc-146">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="b85fc-146">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="b85fc-147">comments</span><span class="sxs-lookup"><span data-stu-id="b85fc-147">comments</span></span>|<span data-ttu-id="b85fc-148">Colección String</span><span class="sxs-lookup"><span data-stu-id="b85fc-148">String collection</span></span>|<span data-ttu-id="b85fc-149">Comentarios de los analistas de la alerta (para la administración de alertas del cliente).</span><span class="sxs-lookup"><span data-stu-id="b85fc-149">Analyst comments on the alert (for customer alert management).</span></span>|
|<span data-ttu-id="b85fc-150">comentarios</span><span class="sxs-lookup"><span data-stu-id="b85fc-150">feedback</span></span>|<span data-ttu-id="b85fc-151">enumeración alertFeedback</span><span class="sxs-lookup"><span data-stu-id="b85fc-151">alertFeedback enum</span></span>|<span data-ttu-id="b85fc-152">Comentarios de analistas de la alerta.</span><span class="sxs-lookup"><span data-stu-id="b85fc-152">Analyst feedback on the alert.</span></span> <span data-ttu-id="b85fc-153">Los valores posibles son: `unknown`, `truePositive`, `falsePositive` y `benignPositive`.</span><span class="sxs-lookup"><span data-stu-id="b85fc-153">Possible values are: `unknown`, `truePositive`, `falsePositive`, `benignPositive`.</span></span>|
|<span data-ttu-id="b85fc-154">status</span><span class="sxs-lookup"><span data-stu-id="b85fc-154">status</span></span>|<span data-ttu-id="b85fc-155">enumeración alertStatus</span><span class="sxs-lookup"><span data-stu-id="b85fc-155">alertStatus enum</span></span>|<span data-ttu-id="b85fc-156">Estado de alerta del ciclo de vida (escenario).</span><span class="sxs-lookup"><span data-stu-id="b85fc-156">Alert lifecycle status (stage).</span></span> <span data-ttu-id="b85fc-157">Los valores posibles son: `unknown`, `newAlert`, `inProgress` y `resolved`.</span><span class="sxs-lookup"><span data-stu-id="b85fc-157">Possible values are: `unknown`, `newAlert`, `inProgress`, `resolved`.</span></span>|
|<span data-ttu-id="b85fc-158">de cierre</span><span class="sxs-lookup"><span data-stu-id="b85fc-158">tags</span></span>|<span data-ttu-id="b85fc-159">Colección String</span><span class="sxs-lookup"><span data-stu-id="b85fc-159">String collection</span></span>|<span data-ttu-id="b85fc-160">Rótulos definidos por el usuario que se pueden aplicar a una alerta y pueden servir como condiciones de filtro (por ejemplo, "HVA", "han visto).</span><span class="sxs-lookup"><span data-stu-id="b85fc-160">User-definable labels that can be applied to an alert and can serve as filter conditions (for example, "HVA", "SAW).</span></span>|
|<span data-ttu-id="b85fc-161">vendorInformation</span><span class="sxs-lookup"><span data-stu-id="b85fc-161">vendorInformation</span></span> |[<span data-ttu-id="b85fc-162">securityVendorInformation</span><span class="sxs-lookup"><span data-stu-id="b85fc-162">securityVendorInformation</span></span>](../resources/securityvendorinformation.md)|<span data-ttu-id="b85fc-163">Tipo complejo que contiene detalles sobre el proveedor del producto o servicio de seguridad, el proveedor y la subprovider (por ejemplo, proveedor = Microsoft; proveedor = Windows Defender ATP; subProvider = AppLocker).</span><span class="sxs-lookup"><span data-stu-id="b85fc-163">Complex type containing details about the security product/service vendor, provider, and subprovider (for example, vendor=Microsoft; provider=Windows Defender ATP; subProvider=AppLocker).</span></span> <span data-ttu-id="b85fc-164">**Proveedor y proveedor campos son obligatorios.**</span><span class="sxs-lookup"><span data-stu-id="b85fc-164">**Provider and vendor fields are required.**</span></span>|

## <a name="response"></a><span data-ttu-id="b85fc-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b85fc-165">Response</span></span>

<span data-ttu-id="b85fc-166">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="b85fc-166">If successful, this method returns a `204 No Content` response code.</span></span>

<span data-ttu-id="b85fc-167">Si se utiliza el encabezado de solicitud opcional, el método devuelve un `200 OK` código de respuesta y el objeto actualizado de [alerta](../resources/alert.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b85fc-167">If the optional request header is used, the method returns a `200 OK` response code and the updated [alert](../resources/alert.md) object in the response body.</span></span>

## <a name="example-1"></a><span data-ttu-id="b85fc-168">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="b85fc-168">Example 1</span></span>

### <a name="request"></a><span data-ttu-id="b85fc-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b85fc-169">Request</span></span>

<span data-ttu-id="b85fc-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b85fc-170">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_alert"
}-->

```http
PATCH https://graph.microsoft.com/beta/security/alerts/{alert_id}
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

### <a name="response"></a><span data-ttu-id="b85fc-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b85fc-171">Response</span></span>

<span data-ttu-id="b85fc-172">El siguiente es un ejemplo de una respuesta correcta.</span><span class="sxs-lookup"><span data-stu-id="b85fc-172">The following is an example of a successful response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert"
} -->

```http
HTTP/1.1 204 No Content
```

## <a name="example-2"></a><span data-ttu-id="b85fc-173">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="b85fc-173">Example 2</span></span>

### <a name="request"></a><span data-ttu-id="b85fc-174">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b85fc-174">Request</span></span>

<span data-ttu-id="b85fc-175">En el ejemplo siguiente se muestra una solicitud que incluye el `Prefer` encabezado de solicitud.</span><span class="sxs-lookup"><span data-stu-id="b85fc-175">The following example shows a request that includes the `Prefer` request header.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_alert"
}-->

```http
PATCH https://graph.microsoft.com/beta/security/alerts/{alert_id}
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

### <a name="response"></a><span data-ttu-id="b85fc-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b85fc-176">Response</span></span>

<span data-ttu-id="b85fc-177">El siguiente es un ejemplo de la respuesta cuando la opcional `Prefer: return=representation` se utiliza el encabezado de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b85fc-177">The following is an example of the response when the optional `Prefer: return=representation` request header is used.</span></span>

><span data-ttu-id="b85fc-p111">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b85fc-p111">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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