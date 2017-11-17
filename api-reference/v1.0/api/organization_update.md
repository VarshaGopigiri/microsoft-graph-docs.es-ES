# <a name="update-organization"></a><span data-ttu-id="2b5f6-101">Actualizar organización</span><span class="sxs-lookup"><span data-stu-id="2b5f6-101">Update organization</span></span>

<span data-ttu-id="2b5f6-102">Actualice las propiedades de la organización autenticada actualmente.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-102">Update the properties of the currently authenticated organization.</span></span>

## <a name="permissions"></a><span data-ttu-id="2b5f6-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="2b5f6-103">Permissions</span></span>

<span data-ttu-id="2b5f6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2b5f6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2b5f6-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2b5f6-106">Permission type</span></span>      | <span data-ttu-id="2b5f6-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2b5f6-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2b5f6-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2b5f6-108">Delegated (work or school account)</span></span> | <span data-ttu-id="2b5f6-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-109">Not supported.</span></span>    |
|<span data-ttu-id="2b5f6-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2b5f6-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2b5f6-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-111">Not supported.</span></span>    |
|<span data-ttu-id="2b5f6-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2b5f6-112">Application</span></span> | <span data-ttu-id="2b5f6-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2b5f6-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2b5f6-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PATCH /organization

```

## <a name="request-headers"></a><span data-ttu-id="2b5f6-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2b5f6-115">Request headers</span></span>

| <span data-ttu-id="2b5f6-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="2b5f6-116">Name</span></span>       | <span data-ttu-id="2b5f6-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b5f6-117">Type</span></span> | <span data-ttu-id="2b5f6-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b5f6-118">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="2b5f6-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="2b5f6-119">Authorization</span></span>  | <span data-ttu-id="2b5f6-120">string</span><span class="sxs-lookup"><span data-stu-id="2b5f6-120">string</span></span>  | <span data-ttu-id="2b5f6-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2b5f6-123">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="2b5f6-123">Request body</span></span>
<span data-ttu-id="2b5f6-124">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-124">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="2b5f6-125">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-125">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span> <span data-ttu-id="2b5f6-126">Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-126">For best performance, you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="2b5f6-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2b5f6-127">Property</span></span>     | <span data-ttu-id="2b5f6-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="2b5f6-128">Type</span></span>   |<span data-ttu-id="2b5f6-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b5f6-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2b5f6-130">assignedPlans</span><span class="sxs-lookup"><span data-stu-id="2b5f6-130">assignedPlans</span></span>|<span data-ttu-id="2b5f6-131">AssignedPlan</span><span class="sxs-lookup"><span data-stu-id="2b5f6-131">AssignedPlan</span></span>|<span data-ttu-id="2b5f6-132">La colección de planes de servicio asociados con el inquilino.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-132">The collection of service plans associated with the tenant. Not nullable.</span></span> <span data-ttu-id="2b5f6-133">**Notas**: no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-133">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="2b5f6-134">city</span><span class="sxs-lookup"><span data-stu-id="2b5f6-134">city</span></span>|<span data-ttu-id="2b5f6-135">String</span><span class="sxs-lookup"><span data-stu-id="2b5f6-135">String</span></span>|            |
|<span data-ttu-id="2b5f6-136">companyLastDirSyncTime</span><span class="sxs-lookup"><span data-stu-id="2b5f6-136">companyLastDirSyncTime</span></span>|<span data-ttu-id="2b5f6-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2b5f6-137">DateTimeOffset</span></span>|<span data-ttu-id="2b5f6-138">Fecha y hora en las que el inquilino se ha sincronizado por última vez con el directorio local.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-138">The time and date at which the tenant was last synced with the on-premise directory.</span></span>|
|<span data-ttu-id="2b5f6-139">country</span><span class="sxs-lookup"><span data-stu-id="2b5f6-139">country</span></span>|<span data-ttu-id="2b5f6-140">String</span><span class="sxs-lookup"><span data-stu-id="2b5f6-140">String</span></span>|            |
|<span data-ttu-id="2b5f6-141">countryLetterCode</span><span class="sxs-lookup"><span data-stu-id="2b5f6-141">countryLetterCode</span></span>|<span data-ttu-id="2b5f6-142">String</span><span class="sxs-lookup"><span data-stu-id="2b5f6-142">String</span></span>|            |
|<span data-ttu-id="2b5f6-143">deletionTimestamp</span><span class="sxs-lookup"><span data-stu-id="2b5f6-143">deletionTimestamp</span></span>|<span data-ttu-id="2b5f6-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2b5f6-144">DateTimeOffset</span></span>||
|<span data-ttu-id="2b5f6-145">dirSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="2b5f6-145">dirSyncEnabled</span></span>|<span data-ttu-id="2b5f6-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="2b5f6-146">Boolean</span></span>|<span data-ttu-id="2b5f6-147">**true** si este objeto está sincronizado desde un directorio local; **false** si este objeto se ha sincronizado originalmente desde un directorio local, pero ya no está sincronizado; **null** si este objeto no se ha sincronizado nunca desde un directorio local (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="2b5f6-147">**true** if this object is synced from an on-premises directory; **false** if this object was originally synced from an on-premises directory but is no longer synced; **null** if this object has never been synced from an on-premises directory (default).</span></span>|
|<span data-ttu-id="2b5f6-148">displayName</span><span class="sxs-lookup"><span data-stu-id="2b5f6-148">displayName</span></span>|<span data-ttu-id="2b5f6-149">String</span><span class="sxs-lookup"><span data-stu-id="2b5f6-149">String</span></span>|<span data-ttu-id="2b5f6-150">El nombre para mostrar del inquilino.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-150">The display name for the tenant.</span></span>|
|<span data-ttu-id="2b5f6-151">marketingNotificationEmails</span><span class="sxs-lookup"><span data-stu-id="2b5f6-151">marketingNotificationEmails</span></span>|<span data-ttu-id="2b5f6-152">String</span><span class="sxs-lookup"><span data-stu-id="2b5f6-152">String</span></span>|                                        <span data-ttu-id="2b5f6-153">**Notas**: no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-153">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="2b5f6-154">objectType</span><span class="sxs-lookup"><span data-stu-id="2b5f6-154">objectType</span></span>|<span data-ttu-id="2b5f6-155">String</span><span class="sxs-lookup"><span data-stu-id="2b5f6-155">String</span></span>|<span data-ttu-id="2b5f6-156">Cadena que identifica el tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-156">A string that identifies the object type. For tenants the value is always “Company”.</span></span> <span data-ttu-id="2b5f6-157">Para los inquilinos, el valor es siempre "Company".</span><span class="sxs-lookup"><span data-stu-id="2b5f6-157">A string that identifies the object type. For tenants the value is always “Company”.</span></span> <span data-ttu-id="2b5f6-158">Heredado de [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="2b5f6-158">Inherited from [directoryObject](../resources/directoryobject.md).</span></span>|
|<span data-ttu-id="2b5f6-159">postalCode</span><span class="sxs-lookup"><span data-stu-id="2b5f6-159">postalCode</span></span>|<span data-ttu-id="2b5f6-160">String</span><span class="sxs-lookup"><span data-stu-id="2b5f6-160">String</span></span>|            |
|<span data-ttu-id="2b5f6-161">preferredLanguage</span><span class="sxs-lookup"><span data-stu-id="2b5f6-161">preferredLanguage</span></span>|<span data-ttu-id="2b5f6-162">String</span><span class="sxs-lookup"><span data-stu-id="2b5f6-162">String</span></span>|            |
|<span data-ttu-id="2b5f6-163">provisionedPlans</span><span class="sxs-lookup"><span data-stu-id="2b5f6-163">provisionedPlans</span></span>|<span data-ttu-id="2b5f6-164">ProvisionedPlan</span><span class="sxs-lookup"><span data-stu-id="2b5f6-164">ProvisionedPlan</span></span>|                                        <span data-ttu-id="2b5f6-165">**Notas**: no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-165">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="2b5f6-166">provisioningErrors</span><span class="sxs-lookup"><span data-stu-id="2b5f6-166">provisioningErrors</span></span>|<span data-ttu-id="2b5f6-167">ProvisioningError</span><span class="sxs-lookup"><span data-stu-id="2b5f6-167">ProvisioningError</span></span>|                                        <span data-ttu-id="2b5f6-168">**Notas**: no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-168">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="2b5f6-169">securityComplianceNotificationMails</span><span class="sxs-lookup"><span data-stu-id="2b5f6-169">securityComplianceNotificationMails</span></span>|<span data-ttu-id="2b5f6-170">String</span><span class="sxs-lookup"><span data-stu-id="2b5f6-170">String</span></span>||
|<span data-ttu-id="2b5f6-171">securityComplianceNotificationPhones</span><span class="sxs-lookup"><span data-stu-id="2b5f6-171">securityComplianceNotificationPhones</span></span>|<span data-ttu-id="2b5f6-172">String</span><span class="sxs-lookup"><span data-stu-id="2b5f6-172">String</span></span>||
|<span data-ttu-id="2b5f6-173">state</span><span class="sxs-lookup"><span data-stu-id="2b5f6-173">state</span></span>|<span data-ttu-id="2b5f6-174">String</span><span class="sxs-lookup"><span data-stu-id="2b5f6-174">String</span></span>|            |
|<span data-ttu-id="2b5f6-175">street</span><span class="sxs-lookup"><span data-stu-id="2b5f6-175">street</span></span>|<span data-ttu-id="2b5f6-176">String</span><span class="sxs-lookup"><span data-stu-id="2b5f6-176">String</span></span>|            |
|<span data-ttu-id="2b5f6-177">technicalNotificationMails</span><span class="sxs-lookup"><span data-stu-id="2b5f6-177">technicalNotificationMails</span></span>|<span data-ttu-id="2b5f6-178">String</span><span class="sxs-lookup"><span data-stu-id="2b5f6-178">String</span></span>|                                        <span data-ttu-id="2b5f6-179">**Notas**: no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-179">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="2b5f6-180">telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="2b5f6-180">telephoneNumber</span></span>|<span data-ttu-id="2b5f6-181">String</span><span class="sxs-lookup"><span data-stu-id="2b5f6-181">String</span></span>|            |
|<span data-ttu-id="2b5f6-182">verifiedDomains</span><span class="sxs-lookup"><span data-stu-id="2b5f6-182">verifiedDomains</span></span>|<span data-ttu-id="2b5f6-183">VerifiedDomain</span><span class="sxs-lookup"><span data-stu-id="2b5f6-183">VerifiedDomain</span></span>|<span data-ttu-id="2b5f6-184">La colección de dominios asociados a este inquilino.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-184">The collection of domains associated with this tenant. Not nullable.</span></span> <span data-ttu-id="2b5f6-185">**Notas**: no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-185">**Notes**: not nullable.</span></span>            |

## <a name="response"></a><span data-ttu-id="2b5f6-186">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b5f6-186">Response</span></span>

<span data-ttu-id="2b5f6-187">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [organization](../resources/organization.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-187">If successful, this method returns a `200 OK` response code and updated [organization](../resources/organization.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2b5f6-188">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2b5f6-188">Example</span></span>

### <a name="request"></a><span data-ttu-id="2b5f6-189">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2b5f6-189">Request</span></span>

<span data-ttu-id="2b5f6-190">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-190">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_organization"
}-->

```http
PATCH https://graph.microsoft.com/v1.0/organization
Content-type: application/json
Content-length: 411

{
  "assignedPlans": [
    {
      "assignedDateTime": "datetime-value",
      "capabilityStatus": "capabilityStatus-value",
      "service": "service-value",
      "servicePlanId": "servicePlanId-value"
    }
  ],
  "businessPhones": [
    "businessPhones-value"
  ],
  "city": "city-value",
  "country": "country-value",
  "countryLetterCode": "countryLetterCode-value",
  "displayName": "displayName-value"
}
```

<br/>

### <a name="response"></a><span data-ttu-id="2b5f6-191">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2b5f6-191">Response</span></span>

<span data-ttu-id="2b5f6-192">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-192">Here is an example of the response.</span></span> <span data-ttu-id="2b5f6-193">**Nota**: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-193">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="2b5f6-194">Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2b5f6-194">All default properties will be returned from the actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.organization"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 411

{
  "assignedPlans": [
    {
      "assignedDateTime": "datetime-value",
      "capabilityStatus": "capabilityStatus-value",
      "service": "service-value",
      "servicePlanId": "servicePlanId-value"
    }
  ],
  "businessPhones": [
    "businessPhones-value"
  ],
  "city": "city-value",
  "country": "country-value",
  "countryLetterCode": "countryLetterCode-value",
  "displayName": "displayName-value"
}
```

<br/>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update organization",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
