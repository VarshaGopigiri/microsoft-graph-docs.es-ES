# <a name="update-alert"></a><span data-ttu-id="ce766-101">Update alert</span><span class="sxs-lookup"><span data-stu-id="ce766-101">Update alert</span></span>

<span data-ttu-id="ce766-102">Actualizar una propiedad modificable **alerta** dentro de cualquier solución integrada para mantener sincronizados estado de la alerta y las asignaciones entre las soluciones.</span><span class="sxs-lookup"><span data-stu-id="ce766-102">Update an editable **alert** property within any integrated solution to keep alert status and assignments in sync across solutions.</span></span> <span data-ttu-id="ce766-103">Este método actualiza cualquier solución que tiene un registro de la alerta de que se hace referencia a identificador.</span><span class="sxs-lookup"><span data-stu-id="ce766-103">This method updates any solution that has a record of the referenced alert ID.</span></span>

## <a name="permissions"></a><span data-ttu-id="ce766-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="ce766-104">Permissions</span></span>

<span data-ttu-id="ce766-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ce766-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ce766-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ce766-107">Permission type</span></span>      | <span data-ttu-id="ce766-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ce766-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ce766-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ce766-109">Delegated (work or school account)</span></span> |   <span data-ttu-id="ce766-110">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ce766-110">SecurityEvents.ReadWrite.All</span></span>  |
|<span data-ttu-id="ce766-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ce766-111">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="ce766-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ce766-112">Not supported.</span></span>  |
|<span data-ttu-id="ce766-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ce766-113">Application</span></span> | <span data-ttu-id="ce766-114">SecurityEvents.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ce766-114">SecurityEvents.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ce766-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ce766-115">HTTP request</span></span>

> <span data-ttu-id="ce766-116">**Nota:** Debe incluir el identificador de **alerta** como un parámetro y vendorInformation que contiene el `provider` y `vendor` con este método.</span><span class="sxs-lookup"><span data-stu-id="ce766-116">**Note:** You must include the **alert** ID as a parameter and vendorInformation containing the `provider` and `vendor` with this method.</span></span>
<!-- { "blockType": "ignored" } -->

```http
PATCH /security/alerts/{alert_id}
```

## <a name="request-headers"></a><span data-ttu-id="ce766-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ce766-117">Request headers</span></span>

| <span data-ttu-id="ce766-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="ce766-118">Name</span></span>       | <span data-ttu-id="ce766-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce766-119">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="ce766-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="ce766-120">Authorization</span></span>  | <span data-ttu-id="ce766-p103">{código} del portador. Necesario.</span><span class="sxs-lookup"><span data-stu-id="ce766-p103">Bearer {code}. Required.</span></span>|
|<span data-ttu-id="ce766-123">Prefer</span><span class="sxs-lookup"><span data-stu-id="ce766-123">Prefer</span></span> | <span data-ttu-id="ce766-124">devolver = representación</span><span class="sxs-lookup"><span data-stu-id="ce766-124">return=representation</span></span> |

## <a name="request-body"></a><span data-ttu-id="ce766-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ce766-125">Request body</span></span>

<span data-ttu-id="ce766-126">En el cuerpo de la solicitud, proporcionar una representación JSON de los valores para los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="ce766-126">In the request body, supply a JSON representation of the values for relevant fields that should be updated.</span></span> <span data-ttu-id="ce766-127">El cuerpo **debe** contener el `vendorInformation` propiedad con válido `provider` y `vendor` campos.</span><span class="sxs-lookup"><span data-stu-id="ce766-127">The body **must** contain the `vendorInformation` property with valid `provider` and `vendor` fields.</span></span> <span data-ttu-id="ce766-128">En la siguiente tabla se enumera los campos que se pueden actualizar para una alerta.</span><span class="sxs-lookup"><span data-stu-id="ce766-128">The following table lists the fields that can be updated for an alert.</span></span> <span data-ttu-id="ce766-129">Los valores para las propiedades existentes que no se incluyen en el cuerpo de la solicitud no cambiará.</span><span class="sxs-lookup"><span data-stu-id="ce766-129">The values for existing properties that are not included in the request body will not change.</span></span> <span data-ttu-id="ce766-130">Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="ce766-130">For best performance, don't include existing values that haven't changed.</span></span>

| <span data-ttu-id="ce766-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ce766-131">Property</span></span>   | <span data-ttu-id="ce766-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce766-132">Type</span></span> |<span data-ttu-id="ce766-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce766-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ce766-134">assignedTo</span><span class="sxs-lookup"><span data-stu-id="ce766-134">assignedTo</span></span>|<span data-ttu-id="ce766-135">String</span><span class="sxs-lookup"><span data-stu-id="ce766-135">String</span></span>|<span data-ttu-id="ce766-136">Nombre del analista de la alerta se asigna a para la evaluación de errores, investigación o corrección.</span><span class="sxs-lookup"><span data-stu-id="ce766-136">Name of the analyst the alert is assigned to for triage, investigation, or remediation.</span></span>|
|<span data-ttu-id="ce766-137">closedDateTime</span><span class="sxs-lookup"><span data-stu-id="ce766-137">closedDateTime</span></span>|<span data-ttu-id="ce766-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ce766-138">DateTimeOffset</span></span>|<span data-ttu-id="ce766-139">Hora a la que se ha cerrado la alerta.</span><span class="sxs-lookup"><span data-stu-id="ce766-139">Time at which the alert was closed.</span></span> <span data-ttu-id="ce766-140">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="ce766-140">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="ce766-141">Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.</span><span class="sxs-lookup"><span data-stu-id="ce766-141">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.</span></span>|
|<span data-ttu-id="ce766-142">comments</span><span class="sxs-lookup"><span data-stu-id="ce766-142">comments</span></span>|<span data-ttu-id="ce766-143">Colección String</span><span class="sxs-lookup"><span data-stu-id="ce766-143">String collection</span></span>|<span data-ttu-id="ce766-144">Comentarios de los analistas de la alerta (para la administración de alertas del cliente).</span><span class="sxs-lookup"><span data-stu-id="ce766-144">Analyst comments on the alert (for customer alert management).</span></span>|
|<span data-ttu-id="ce766-145">comentarios</span><span class="sxs-lookup"><span data-stu-id="ce766-145">feedback</span></span>|<span data-ttu-id="ce766-146">alertFeedback</span><span class="sxs-lookup"><span data-stu-id="ce766-146">alertFeedback</span></span>|<span data-ttu-id="ce766-147">Comentarios de analistas de la alerta.</span><span class="sxs-lookup"><span data-stu-id="ce766-147">Analyst feedback on the alert.</span></span> <span data-ttu-id="ce766-148">Los valores posibles son: `unknown`, `truePositive`, `falsePositive` y `benignPositive`.</span><span class="sxs-lookup"><span data-stu-id="ce766-148">Possible values are: `unknown`, `truePositive`, `falsePositive`, `benignPositive`.</span></span>|
|<span data-ttu-id="ce766-149">status</span><span class="sxs-lookup"><span data-stu-id="ce766-149">status</span></span>|<span data-ttu-id="ce766-150">alertStatus</span><span class="sxs-lookup"><span data-stu-id="ce766-150">alertStatus</span></span>|<span data-ttu-id="ce766-151">Estado de alerta del ciclo de vida (escenario).</span><span class="sxs-lookup"><span data-stu-id="ce766-151">Alert lifecycle status (stage).</span></span> <span data-ttu-id="ce766-152">Los valores posibles son: `unknown`, `newAlert`, `inProgress` y `resolved`.</span><span class="sxs-lookup"><span data-stu-id="ce766-152">Possible values are: `unknown`, `newAlert`, `inProgress`, `resolved`.</span></span>|
|<span data-ttu-id="ce766-153">de cierre</span><span class="sxs-lookup"><span data-stu-id="ce766-153">tags</span></span>|<span data-ttu-id="ce766-154">Colección String</span><span class="sxs-lookup"><span data-stu-id="ce766-154">String collection</span></span>|<span data-ttu-id="ce766-155">Rótulos definidos por el usuario que se pueden aplicar a una alerta y pueden servir como condiciones de filtro (por ejemplo, "HVA", "han visto).</span><span class="sxs-lookup"><span data-stu-id="ce766-155">User-definable labels that can be applied to an alert and can serve as filter conditions (for example, "HVA", "SAW).</span></span>|
|<span data-ttu-id="ce766-156">vendorInformation</span><span class="sxs-lookup"><span data-stu-id="ce766-156">vendorInformation</span></span> |[<span data-ttu-id="ce766-157">securityVendorInformation</span><span class="sxs-lookup"><span data-stu-id="ce766-157">securityVendorInformation</span></span>](../resources/securityvendorinformation.md)|<span data-ttu-id="ce766-158">Tipo complejo que contiene detalles sobre el proveedor del producto o servicio de seguridad, el proveedor y la subprovider (por ejemplo, proveedor = Microsoft; proveedor = Windows Defender ATP; subProvider = AppLocker).</span><span class="sxs-lookup"><span data-stu-id="ce766-158">Complex type containing details about the security product/service vendor, provider, and subprovider (for example, vendor=Microsoft; provider=Windows Defender ATP; subProvider=AppLocker).</span></span> <span data-ttu-id="ce766-159">**Proveedor y proveedor campos son obligatorios.**</span><span class="sxs-lookup"><span data-stu-id="ce766-159">**Provider and vendor fields are required.**</span></span>|

## <a name="response"></a><span data-ttu-id="ce766-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce766-160">Response</span></span>

<span data-ttu-id="ce766-161">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="ce766-161">If successful, this method returns a `204 No Content` response code.</span></span>

<span data-ttu-id="ce766-162">Si se utiliza el encabezado de solicitud opcional, el método devuelve un `200 OK` código de respuesta y el objeto actualizado de [alerta](../resources/alert.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce766-162">If the optional request header is used, the method returns a `200 OK` response code and the updated [alert](../resources/alert.md) object in the response body.</span></span>

## <a name="example-1"></a><span data-ttu-id="ce766-163">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce766-163">Example 1</span></span>

### <a name="request"></a><span data-ttu-id="ce766-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ce766-164">Request</span></span>

<span data-ttu-id="ce766-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce766-165">The following is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="ce766-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce766-166">Response</span></span>

<span data-ttu-id="ce766-167">El siguiente es un ejemplo de una respuesta correcta.</span><span class="sxs-lookup"><span data-stu-id="ce766-167">The following is an example of a successful response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert"
} -->

```http
HTTP/1.1 204 No Content
```

## <a name="example-2"></a><span data-ttu-id="ce766-168">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="ce766-168">Example 2</span></span>

### <a name="request"></a><span data-ttu-id="ce766-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ce766-169">Request</span></span>

<span data-ttu-id="ce766-170">En el ejemplo siguiente se muestra una solicitud que incluye el `Prefer` encabezado de solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce766-170">The following example shows a request that includes the `Prefer` request header.</span></span>

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

### <a name="response"></a><span data-ttu-id="ce766-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce766-171">Response</span></span>

<span data-ttu-id="ce766-172">El siguiente es un ejemplo de la respuesta cuando la opcional `Prefer: return=representation` se utiliza el encabezado de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce766-172">The following is an example of the response when the optional `Prefer: return=representation` request header is used.</span></span>

><span data-ttu-id="ce766-p109">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ce766-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
