# <a name="update-organization"></a><span data-ttu-id="9932a-101">Actualizar organización</span><span class="sxs-lookup"><span data-stu-id="9932a-101">Update organization</span></span>

<span data-ttu-id="9932a-102">Actualice las propiedades de la organización autenticada actualmente.</span><span class="sxs-lookup"><span data-stu-id="9932a-102">Update the properties of the currently authenticated organization.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9932a-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9932a-103">Prerequisites</span></span>
<span data-ttu-id="9932a-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="9932a-104">One of the following **scopes** is required to execute this API:</span></span>
## <a name="http-request"></a><span data-ttu-id="9932a-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9932a-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /organization

```
## <a name="request-headers"></a><span data-ttu-id="9932a-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9932a-106">Request headers</span></span>
| <span data-ttu-id="9932a-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="9932a-107">Name</span></span>       | <span data-ttu-id="9932a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="9932a-108">Type</span></span> | <span data-ttu-id="9932a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9932a-109">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="9932a-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="9932a-110">Authorization</span></span>  | <span data-ttu-id="9932a-111">string</span><span class="sxs-lookup"><span data-stu-id="9932a-111">string</span></span>  | <span data-ttu-id="9932a-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9932a-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9932a-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9932a-114">Request body</span></span>
<span data-ttu-id="9932a-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="9932a-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="9932a-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9932a-118">Property</span></span>     | <span data-ttu-id="9932a-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="9932a-119">Type</span></span>   |<span data-ttu-id="9932a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="9932a-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9932a-121">assignedPlans</span><span class="sxs-lookup"><span data-stu-id="9932a-121">assignedPlans</span></span>|<span data-ttu-id="9932a-122">AssignedPlan</span><span class="sxs-lookup"><span data-stu-id="9932a-122">AssignedPlan</span></span>|<span data-ttu-id="9932a-p103">La colección de planes de servicio asociados con el inquilino.                            **Notas**: no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9932a-p103">The collection of service plans associated with the tenant.                            **Notes**: not nullable.</span></span>            |
|<span data-ttu-id="9932a-125">city</span><span class="sxs-lookup"><span data-stu-id="9932a-125">city</span></span>|<span data-ttu-id="9932a-126">String</span><span class="sxs-lookup"><span data-stu-id="9932a-126">String</span></span>|            |
|<span data-ttu-id="9932a-127">companyLastDirSyncTime</span><span class="sxs-lookup"><span data-stu-id="9932a-127">companyLastDirSyncTime</span></span>|<span data-ttu-id="9932a-128">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9932a-128">DateTimeOffset</span></span>|<span data-ttu-id="9932a-129">La fecha y hora en que el inquilino se ha sincronizado por última vez con el directorio local.</span><span class="sxs-lookup"><span data-stu-id="9932a-129">The time and date at which the tenant was last synced with the on-premise directory.</span></span>|
|<span data-ttu-id="9932a-130">country</span><span class="sxs-lookup"><span data-stu-id="9932a-130">country</span></span>|<span data-ttu-id="9932a-131">String</span><span class="sxs-lookup"><span data-stu-id="9932a-131">String</span></span>|            |
|<span data-ttu-id="9932a-132">countryLetterCode</span><span class="sxs-lookup"><span data-stu-id="9932a-132">countryLetterCode</span></span>|<span data-ttu-id="9932a-133">String</span><span class="sxs-lookup"><span data-stu-id="9932a-133">String</span></span>|            |
|<span data-ttu-id="9932a-134">deletionTimestamp</span><span class="sxs-lookup"><span data-stu-id="9932a-134">deletionTimestamp</span></span>|<span data-ttu-id="9932a-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9932a-135">DateTimeOffset</span></span>||
|<span data-ttu-id="9932a-136">dirSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="9932a-136">dirSyncEnabled</span></span>|<span data-ttu-id="9932a-137">Boolean</span><span class="sxs-lookup"><span data-stu-id="9932a-137">Boolean</span></span>|<span data-ttu-id="9932a-138">**true** si este objeto está sincronizado desde un directorio local; **false** si este objeto se ha sincronizado originalmente desde un directorio local, pero ya no está sincronizado; **null** si este objeto no se ha sincronizado nunca desde un directorio local (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="9932a-138">**true** if this object is synced from an on-premises directory; **false** if this object was originally synced from an on-premises directory but is no longer synced; **null** if this object has never been synced from an on-premises directory (default).</span></span>|
|<span data-ttu-id="9932a-139">displayName</span><span class="sxs-lookup"><span data-stu-id="9932a-139">displayName</span></span>|<span data-ttu-id="9932a-140">String</span><span class="sxs-lookup"><span data-stu-id="9932a-140">String</span></span>|<span data-ttu-id="9932a-141">El nombre para mostrar del inquilino.</span><span class="sxs-lookup"><span data-stu-id="9932a-141">The display name for the tenant.</span></span>|
|<span data-ttu-id="9932a-142">marketingNotificationEmails</span><span class="sxs-lookup"><span data-stu-id="9932a-142">marketingNotificationEmails</span></span>|<span data-ttu-id="9932a-143">String</span><span class="sxs-lookup"><span data-stu-id="9932a-143">String</span></span>|                                        <span data-ttu-id="9932a-144">**Notas**: no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9932a-144">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="9932a-145">objectType</span><span class="sxs-lookup"><span data-stu-id="9932a-145">objectType</span></span>|<span data-ttu-id="9932a-146">String</span><span class="sxs-lookup"><span data-stu-id="9932a-146">String</span></span>|<span data-ttu-id="9932a-p104">Una cadena que identifica el tipo de objeto. Para los inquilinos, el valor es siempre "Company". Hereda de [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="9932a-p104">A string that identifies the object type. For tenants the value is always “Company”. Inherited from [directoryObject](../resources/directoryobject.md).</span></span>|
|<span data-ttu-id="9932a-150">postalCode</span><span class="sxs-lookup"><span data-stu-id="9932a-150">postalCode</span></span>|<span data-ttu-id="9932a-151">String</span><span class="sxs-lookup"><span data-stu-id="9932a-151">String</span></span>|            |
|<span data-ttu-id="9932a-152">preferredLanguage</span><span class="sxs-lookup"><span data-stu-id="9932a-152">preferredLanguage</span></span>|<span data-ttu-id="9932a-153">String</span><span class="sxs-lookup"><span data-stu-id="9932a-153">String</span></span>|            |
|<span data-ttu-id="9932a-154">provisionedPlans</span><span class="sxs-lookup"><span data-stu-id="9932a-154">provisionedPlans</span></span>|<span data-ttu-id="9932a-155">ProvisionedPlan</span><span class="sxs-lookup"><span data-stu-id="9932a-155">ProvisionedPlan</span></span>|                                        <span data-ttu-id="9932a-156">**Notas**: no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9932a-156">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="9932a-157">provisioningErrors</span><span class="sxs-lookup"><span data-stu-id="9932a-157">provisioningErrors</span></span>|<span data-ttu-id="9932a-158">ProvisioningError</span><span class="sxs-lookup"><span data-stu-id="9932a-158">ProvisioningError</span></span>|                                        <span data-ttu-id="9932a-159">**Notas**: no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9932a-159">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="9932a-160">securityComplianceNotificationMails</span><span class="sxs-lookup"><span data-stu-id="9932a-160">securityComplianceNotificationMails</span></span>|<span data-ttu-id="9932a-161">String</span><span class="sxs-lookup"><span data-stu-id="9932a-161">String</span></span>||
|<span data-ttu-id="9932a-162">securityComplianceNotificationPhones</span><span class="sxs-lookup"><span data-stu-id="9932a-162">securityComplianceNotificationPhones</span></span>|<span data-ttu-id="9932a-163">String</span><span class="sxs-lookup"><span data-stu-id="9932a-163">String</span></span>||
|<span data-ttu-id="9932a-164">state</span><span class="sxs-lookup"><span data-stu-id="9932a-164">state</span></span>|<span data-ttu-id="9932a-165">String</span><span class="sxs-lookup"><span data-stu-id="9932a-165">String</span></span>|            |
|<span data-ttu-id="9932a-166">street</span><span class="sxs-lookup"><span data-stu-id="9932a-166">street</span></span>|<span data-ttu-id="9932a-167">String</span><span class="sxs-lookup"><span data-stu-id="9932a-167">String</span></span>|            |
|<span data-ttu-id="9932a-168">technicalNotificationMails</span><span class="sxs-lookup"><span data-stu-id="9932a-168">technicalNotificationMails</span></span>|<span data-ttu-id="9932a-169">String</span><span class="sxs-lookup"><span data-stu-id="9932a-169">String</span></span>|                                        <span data-ttu-id="9932a-170">**Notas**: no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9932a-170">**Notes**: not nullable.</span></span>            |
|<span data-ttu-id="9932a-171">telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="9932a-171">telephoneNumber</span></span>|<span data-ttu-id="9932a-172">String</span><span class="sxs-lookup"><span data-stu-id="9932a-172">String</span></span>|            |
|<span data-ttu-id="9932a-173">verifiedDomains</span><span class="sxs-lookup"><span data-stu-id="9932a-173">verifiedDomains</span></span>|<span data-ttu-id="9932a-174">VerifiedDomain</span><span class="sxs-lookup"><span data-stu-id="9932a-174">VerifiedDomain</span></span>|<span data-ttu-id="9932a-p105">La colección de dominios asociados a este inquilino.                            **Notas**: no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="9932a-p105">The collection of domains associated with this tenant.                            **Notes**: not nullable.</span></span>            |

## <a name="response"></a><span data-ttu-id="9932a-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9932a-177">Response</span></span>

<span data-ttu-id="9932a-178">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [organization](../resources/organization.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9932a-178">If successful, this method returns a `200 OK` response code and updated [organization](../resources/organization.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9932a-179">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9932a-179">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9932a-180">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9932a-180">Request</span></span>
<span data-ttu-id="9932a-181">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9932a-181">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="9932a-182">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9932a-182">Response</span></span>
<span data-ttu-id="9932a-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9932a-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update organization",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
