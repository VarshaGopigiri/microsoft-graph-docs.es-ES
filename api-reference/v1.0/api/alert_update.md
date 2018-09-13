# <a name="update-alert"></a><span data-ttu-id="feb1c-101">Actualizar alerta</span><span class="sxs-lookup"><span data-stu-id="feb1c-101">Update alert</span></span>

<span data-ttu-id="feb1c-102">Actualizar una propiedad modificable **alert** editable dentro de cualquier solución integrada para mantener sincronizados el estado de la alerta y las asignaciones entre las soluciones.</span><span class="sxs-lookup"><span data-stu-id="feb1c-102">Update an editable **alert** property within any integrated solution to keep alert status and assignments in sync across solutions.</span></span> <span data-ttu-id="feb1c-103">Este método actualiza cualquier solución que tiene un registro del Id. de alerta referenciado.</span><span class="sxs-lookup"><span data-stu-id="feb1c-103">This method updates any solution that has a record of the referenced alert ID.</span></span>

## <a name="permissions"></a><span data-ttu-id="feb1c-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="feb1c-104">Permissions</span></span>

<span data-ttu-id="feb1c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="feb1c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="feb1c-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="feb1c-107">Permission type</span></span>      | <span data-ttu-id="feb1c-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="feb1c-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="feb1c-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="feb1c-109">Delegated (work or school account)</span></span> |   <span data-ttu-id="feb1c-110">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="feb1c-110">SecurityEvents.ReadWrite.All</span></span>  |
|<span data-ttu-id="feb1c-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="feb1c-111">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="feb1c-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="feb1c-112">Not supported.</span></span>  |
|<span data-ttu-id="feb1c-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="feb1c-113">Application</span></span> | <span data-ttu-id="feb1c-114">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="feb1c-114">SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="feb1c-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="feb1c-115">HTTP request</span></span>

> <span data-ttu-id="feb1c-116">**Nota:** Debe incluir el Id. de **alerta** como un parámetro y vendorInformation que contiene el `provider` y `vendor` con este método.</span><span class="sxs-lookup"><span data-stu-id="feb1c-116">**Note:** You must include the **alert** ID as a parameter and vendorInformation containing the `provider` and `vendor` with this method.</span></span>
<!-- { "blockType": "ignored" } -->

```http
PATCH /security/alerts/{alert_id}
```

## <a name="request-headers"></a><span data-ttu-id="feb1c-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="feb1c-117">Request headers</span></span>

| <span data-ttu-id="feb1c-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="feb1c-118">Name</span></span>       | <span data-ttu-id="feb1c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="feb1c-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="feb1c-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="feb1c-120">Authorization</span></span>  | <span data-ttu-id="feb1c-p103">{código} del portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="feb1c-p103">Bearer {code}. Required.</span></span>|
|<span data-ttu-id="feb1c-123">Prefer</span><span class="sxs-lookup"><span data-stu-id="feb1c-123">Prefer</span></span> | <span data-ttu-id="feb1c-124">return=representation</span><span class="sxs-lookup"><span data-stu-id="feb1c-124">return=representation</span></span> |

## <a name="request-body"></a><span data-ttu-id="feb1c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="feb1c-125">Request body</span></span>

<span data-ttu-id="feb1c-126">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="feb1c-126">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="feb1c-127">El cuerpo **debe** contener la propiedad `vendorInformation` con los campos `provider` y `vendor` válidos.</span><span class="sxs-lookup"><span data-stu-id="feb1c-127">The body **must** contain the `vendorInformation` property with valid `provider` and `vendor` fields.</span></span> <span data-ttu-id="feb1c-128">En la siguiente tabla se enumeran los campos que se pueden actualizar para una alerta.</span><span class="sxs-lookup"><span data-stu-id="feb1c-128">The following table lists the authentication settings that can be changed for an authentication provider.</span></span> <span data-ttu-id="feb1c-129">Los valores para las propiedades existentes que no se incluyen en el cuerpo de la solicitud no cambiarán.</span><span class="sxs-lookup"><span data-stu-id="feb1c-129">The values for existing properties that are not included in the request body will not change.</span></span> <span data-ttu-id="feb1c-130">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="feb1c-130">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="feb1c-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="feb1c-131">Property</span></span>   | <span data-ttu-id="feb1c-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="feb1c-132">Type</span></span> |<span data-ttu-id="feb1c-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="feb1c-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="feb1c-134">assignedTo</span><span class="sxs-lookup"><span data-stu-id="feb1c-134">assignedTo</span></span>|<span data-ttu-id="feb1c-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="feb1c-135">String</span></span>|<span data-ttu-id="feb1c-136">Nombre del analista al que se asigna la alerta para la evaluación de errores, investigación o corrección.</span><span class="sxs-lookup"><span data-stu-id="feb1c-136">Name of the analyst the alert is assigned to for triage, investigation, or remediation.</span></span>|
|<span data-ttu-id="feb1c-137">closedDateTime</span><span class="sxs-lookup"><span data-stu-id="feb1c-137">closedDateTime</span></span>|<span data-ttu-id="feb1c-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="feb1c-138">DateTimeOffset</span></span>|<span data-ttu-id="feb1c-139">Hora a la que se ha cerrado la alerta.</span><span class="sxs-lookup"><span data-stu-id="feb1c-139">Time at which the alert was closed.</span></span> <span data-ttu-id="feb1c-140">El tipo de marca de hora representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="feb1c-140">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="feb1c-141">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="feb1c-141">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="feb1c-142">comments</span><span class="sxs-lookup"><span data-stu-id="feb1c-142">comments</span></span>|<span data-ttu-id="feb1c-143">Colección String</span><span class="sxs-lookup"><span data-stu-id="feb1c-143">String collection</span></span>|<span data-ttu-id="feb1c-144">Comentarios de los analistas de la alerta (para la administración de alertas del cliente).</span><span class="sxs-lookup"><span data-stu-id="feb1c-144">Analyst comments on the alert (for customer alert management).</span></span>|
|<span data-ttu-id="feb1c-145">feedback</span><span class="sxs-lookup"><span data-stu-id="feb1c-145">Feedback</span></span>|<span data-ttu-id="feb1c-146">alertFeedback</span><span class="sxs-lookup"><span data-stu-id="feb1c-146">alertFeedback</span></span>|<span data-ttu-id="feb1c-147">Comentarios del analista sobre la alerta.</span><span class="sxs-lookup"><span data-stu-id="feb1c-147">Analyst feedback on the alert.</span></span> <span data-ttu-id="feb1c-148">Los valores posibles son: `unknown`, `truePositive`, `falsePositive` y `benignPositive`.</span><span class="sxs-lookup"><span data-stu-id="feb1c-148">Possible values are: `unknown`, `truePositive`, `falsePositive`, `benignPositive`.</span></span>|
|<span data-ttu-id="feb1c-149">status</span><span class="sxs-lookup"><span data-stu-id="feb1c-149">status</span></span>|<span data-ttu-id="feb1c-150">alertStatus</span><span class="sxs-lookup"><span data-stu-id="feb1c-150">alertStatus</span></span>|<span data-ttu-id="feb1c-151">Estado del ciclo de vida de la alerta (fase).</span><span class="sxs-lookup"><span data-stu-id="feb1c-151">Alert lifecycle status (stage).</span></span> <span data-ttu-id="feb1c-152">Los valores posibles son: `unknown`, `newAlert`, `inProgress` y `resolved`.</span><span class="sxs-lookup"><span data-stu-id="feb1c-152">Possible values are: `unknown`, `newAlert`, `inProgress`, `resolved`.</span></span>|
|<span data-ttu-id="feb1c-153">tags</span><span class="sxs-lookup"><span data-stu-id="feb1c-153">tags</span></span>|<span data-ttu-id="feb1c-154">Colección String</span><span class="sxs-lookup"><span data-stu-id="feb1c-154">String collection</span></span>|<span data-ttu-id="feb1c-155">Etiquetas definidas por el usuario que se pueden aplicar a una alerta y pueden servir como condiciones de filtro (por ejemplo, "HVA", "SAW").</span><span class="sxs-lookup"><span data-stu-id="feb1c-155">User-definable labels that can be applied to an alert and can serve as filter conditions (for example, "HVA", "SAW).</span></span>|
|<span data-ttu-id="feb1c-156">vendorInformation \*</span><span class="sxs-lookup"><span data-stu-id="feb1c-156">vendorInformation \*</span></span>|[<span data-ttu-id="feb1c-157">securityVendorInformation</span><span class="sxs-lookup"><span data-stu-id="feb1c-157">securityVendorInformation</span></span>](../resources/securityvendorinformation.md)|<span data-ttu-id="feb1c-158">Tipo complejo que contiene detalles sobre el proveedor del producto o servicio de seguridad, el proveedor y el subproveedor (por ejemplo, vendor=Microsoft; provider=Windows Defender ATP; subProvider=AppLocker).</span><span class="sxs-lookup"><span data-stu-id="feb1c-158">Complex type containing details about the security product/service vendor, provider, and subprovider (for example, vendor=Microsoft; provider=Windows Defender ATP; subProvider=AppLocker).</span></span> <span data-ttu-id="feb1c-159">**Los campos de proveedor son obligatorios.**</span><span class="sxs-lookup"><span data-stu-id="feb1c-159">**Provider and vendor fields are required.**</span></span>|
<span data-ttu-id="feb1c-160">(\* Indica un campo obligatorio.)</span><span class="sxs-lookup"><span data-stu-id="feb1c-160">(\* Indicates a mandatory field.)</span></span>

## <a name="response"></a><span data-ttu-id="feb1c-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="feb1c-161">Response</span></span>

<span data-ttu-id="feb1c-162">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="feb1c-162">If successful, this method returns a `204 No Content` response code.</span></span>

<span data-ttu-id="feb1c-163">Si se utiliza el encabezado de solicitud opcional, el método devuelve un código de respuesta `200 OK` y el objeto [alert](../resources/alert.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="feb1c-163">If the optional request header is used, the method returns a `200 OK` response code and the updated [alert](../resources/alert.md) object in the response body.</span></span>

## <a name="example-1"></a><span data-ttu-id="feb1c-164">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="feb1c-164">Example 1</span></span>

### <a name="request"></a><span data-ttu-id="feb1c-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="feb1c-165">Request</span></span>

<span data-ttu-id="feb1c-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="feb1c-166">The following is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="feb1c-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="feb1c-167">Response</span></span>

<span data-ttu-id="feb1c-168">Este es un ejemplo de respuesta correcta.</span><span class="sxs-lookup"><span data-stu-id="feb1c-168">The following is an example of a response to a  event.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert"
} -->

```http
HTTP/1.1 204 No Content
```

## <a name="example-2"></a><span data-ttu-id="feb1c-169">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="feb1c-169">Example 2</span></span>

### <a name="request"></a><span data-ttu-id="feb1c-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="feb1c-170">Request</span></span>

<span data-ttu-id="feb1c-171">En el ejemplo siguiente se muestra una solicitud que incluye el encabezado de solicitud `Prefer`.</span><span class="sxs-lookup"><span data-stu-id="feb1c-171">The following example shows a request that includes the `Prefer` request header.</span></span>

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

### <a name="response"></a><span data-ttu-id="feb1c-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="feb1c-172">Response</span></span>

<span data-ttu-id="feb1c-173">Este es un ejemplo de la respuesta cuando se utiliza el encabezado de solicitud opcional `Prefer: return=representation`.</span><span class="sxs-lookup"><span data-stu-id="feb1c-173">The following is an example of the response when the optional `Prefer: return=representation` request header is used.</span></span>

><span data-ttu-id="feb1c-p109">**Nota:** Es posible que se haya acortado el objeto de respuesta que se muestra aquí para mejorar la legibilidad. En una llamada real se devolverán todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="feb1c-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
