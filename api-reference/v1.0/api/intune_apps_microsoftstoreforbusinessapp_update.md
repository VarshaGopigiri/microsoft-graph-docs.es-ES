# <a name="update-microsoftstoreforbusinessapp"></a><span data-ttu-id="377e0-101">Actualizar microsoftStoreForBusinessApp</span><span class="sxs-lookup"><span data-stu-id="377e0-101">Update microsoftStoreForBusinessApp</span></span>

> <span data-ttu-id="377e0-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="377e0-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="377e0-103">Actualice las propiedades de un objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-103">Update the properties of a [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="377e0-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="377e0-104">Prerequisites</span></span>
<span data-ttu-id="377e0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="377e0-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="377e0-107">Permission type</span></span>|<span data-ttu-id="377e0-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="377e0-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="377e0-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="377e0-109">Delegated (work or school account)</span></span>|<span data-ttu-id="377e0-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="377e0-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="377e0-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="377e0-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="377e0-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="377e0-112">Not supported.</span></span>|
|<span data-ttu-id="377e0-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="377e0-113">Application</span></span>|<span data-ttu-id="377e0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="377e0-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="377e0-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="377e0-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="377e0-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="377e0-116">Request headers</span></span>
|<span data-ttu-id="377e0-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="377e0-117">Header</span></span>|<span data-ttu-id="377e0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="377e0-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="377e0-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="377e0-119">Authorization</span></span>|<span data-ttu-id="377e0-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="377e0-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="377e0-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="377e0-121">Accept</span></span>|<span data-ttu-id="377e0-122">application/json</span><span class="sxs-lookup"><span data-stu-id="377e0-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="377e0-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="377e0-123">Request body</span></span>
<span data-ttu-id="377e0-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-124">In the request body, supply a JSON representation for the [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md) object.</span></span>

<span data-ttu-id="377e0-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-125">The following table shows the properties that are required when you create the [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).</span></span>

|<span data-ttu-id="377e0-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="377e0-126">Property</span></span>|<span data-ttu-id="377e0-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="377e0-127">Type</span></span>|<span data-ttu-id="377e0-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="377e0-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="377e0-129">id</span><span class="sxs-lookup"><span data-stu-id="377e0-129">id</span></span>|<span data-ttu-id="377e0-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="377e0-130">String</span></span>|<span data-ttu-id="377e0-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="377e0-131">Key of the entity.</span></span> <span data-ttu-id="377e0-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="377e0-133">displayName</span><span class="sxs-lookup"><span data-stu-id="377e0-133">displayName</span></span>|<span data-ttu-id="377e0-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="377e0-134">String</span></span>|<span data-ttu-id="377e0-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="377e0-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="377e0-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="377e0-137">descripción</span><span class="sxs-lookup"><span data-stu-id="377e0-137">description</span></span>|<span data-ttu-id="377e0-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="377e0-138">String</span></span>|<span data-ttu-id="377e0-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="377e0-139">The description of the app.</span></span> <span data-ttu-id="377e0-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="377e0-141">publicador</span><span class="sxs-lookup"><span data-stu-id="377e0-141">publisher</span></span>|<span data-ttu-id="377e0-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="377e0-142">String</span></span>|<span data-ttu-id="377e0-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="377e0-143">The publisher of the app.</span></span> <span data-ttu-id="377e0-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="377e0-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="377e0-145">largeIcon</span></span>|[<span data-ttu-id="377e0-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="377e0-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="377e0-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="377e0-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="377e0-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="377e0-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="377e0-149">createdDateTime</span></span>|<span data-ttu-id="377e0-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="377e0-150">DateTimeOffset</span></span>|<span data-ttu-id="377e0-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="377e0-151">The date and time the app was created.</span></span> <span data-ttu-id="377e0-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="377e0-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="377e0-153">lastModifiedDateTime</span></span>|<span data-ttu-id="377e0-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="377e0-154">DateTimeOffset</span></span>|<span data-ttu-id="377e0-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="377e0-155">The date and time the app was last modified.</span></span> <span data-ttu-id="377e0-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="377e0-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="377e0-157">isFeatured</span></span>|<span data-ttu-id="377e0-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="377e0-158">Boolean</span></span>|<span data-ttu-id="377e0-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="377e0-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="377e0-160">privacyInformationUrl</span></span>|<span data-ttu-id="377e0-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="377e0-161">String</span></span>|<span data-ttu-id="377e0-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="377e0-162">The privacy statement Url.</span></span> <span data-ttu-id="377e0-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="377e0-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="377e0-164">informationUrl</span></span>|<span data-ttu-id="377e0-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="377e0-165">String</span></span>|<span data-ttu-id="377e0-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="377e0-166">The more information Url.</span></span> <span data-ttu-id="377e0-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="377e0-168">owner</span><span class="sxs-lookup"><span data-stu-id="377e0-168">owner</span></span>|<span data-ttu-id="377e0-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="377e0-169">String</span></span>|<span data-ttu-id="377e0-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="377e0-170">The owner of the app.</span></span> <span data-ttu-id="377e0-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="377e0-172">developer</span><span class="sxs-lookup"><span data-stu-id="377e0-172">developer</span></span>|<span data-ttu-id="377e0-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="377e0-173">String</span></span>|<span data-ttu-id="377e0-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="377e0-174">The developer of the app.</span></span> <span data-ttu-id="377e0-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="377e0-176">notas</span><span class="sxs-lookup"><span data-stu-id="377e0-176">notes</span></span>|<span data-ttu-id="377e0-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="377e0-177">String</span></span>|<span data-ttu-id="377e0-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="377e0-178">Notes for the app.</span></span> <span data-ttu-id="377e0-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="377e0-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="377e0-180">publishingState</span></span>|[<span data-ttu-id="377e0-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="377e0-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="377e0-182">El estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="377e0-182">The publishing state for the app.</span></span> <span data-ttu-id="377e0-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="377e0-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="377e0-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span> <span data-ttu-id="377e0-185">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="377e0-185">The possible values are `notPublished`, `processing`, `published`, , , , , , , , , or .</span></span>|
|<span data-ttu-id="377e0-186">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="377e0-186">usedLicenseCount</span></span>|<span data-ttu-id="377e0-187">Int32</span><span class="sxs-lookup"><span data-stu-id="377e0-187">Int32</span></span>|<span data-ttu-id="377e0-188">Número de licencias de Microsoft Store para Empresas en uso.</span><span class="sxs-lookup"><span data-stu-id="377e0-188">The number of Microsoft Store for Business licenses in use.</span></span>|
|<span data-ttu-id="377e0-189">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="377e0-189">totalLicenseCount</span></span>|<span data-ttu-id="377e0-190">Int32</span><span class="sxs-lookup"><span data-stu-id="377e0-190">Int32</span></span>|<span data-ttu-id="377e0-191">Número total de licencias de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="377e0-191">The total number of Microsoft Store for Business licenses.</span></span>|
|<span data-ttu-id="377e0-192">productKey</span><span class="sxs-lookup"><span data-stu-id="377e0-192">productKey</span></span>|<span data-ttu-id="377e0-193">Cadena</span><span class="sxs-lookup"><span data-stu-id="377e0-193">String</span></span>|<span data-ttu-id="377e0-194">Clave de producto de la aplicación</span><span class="sxs-lookup"><span data-stu-id="377e0-194">The app product key</span></span>|
|<span data-ttu-id="377e0-195">licenseType</span><span class="sxs-lookup"><span data-stu-id="377e0-195">licenseType</span></span>|[<span data-ttu-id="377e0-196">microsoftStoreForBusinessLicenseType</span><span class="sxs-lookup"><span data-stu-id="377e0-196">microsoftStoreForBusinessLicenseType</span></span>](../resources/intune_apps_microsoftstoreforbusinesslicensetype.md)|<span data-ttu-id="377e0-197">El tipo de licencia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="377e0-197">The app license type Possible values are: , .</span></span> <span data-ttu-id="377e0-198">Los valores posibles son: `offline` y `online`.</span><span class="sxs-lookup"><span data-stu-id="377e0-198">The possible values are:</span></span>|
|<span data-ttu-id="377e0-199">packageIdentityName</span><span class="sxs-lookup"><span data-stu-id="377e0-199">packageIdentityName</span></span>|<span data-ttu-id="377e0-200">Cadena</span><span class="sxs-lookup"><span data-stu-id="377e0-200">String</span></span>|<span data-ttu-id="377e0-201">Identificador del paquete de aplicación.</span><span class="sxs-lookup"><span data-stu-id="377e0-201">The app package identifier</span></span>|



## <a name="response"></a><span data-ttu-id="377e0-202">Respuesta</span><span class="sxs-lookup"><span data-stu-id="377e0-202">Response</span></span>
<span data-ttu-id="377e0-203">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="377e0-203">If successful, this method returns a `200 OK` response code and an updated [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="377e0-204">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="377e0-204">Example</span></span>
### <a name="request"></a><span data-ttu-id="377e0-205">Solicitud</span><span class="sxs-lookup"><span data-stu-id="377e0-205">Request</span></span>
<span data-ttu-id="377e0-206">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="377e0-206">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 766

{
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "publishingState": "processing",
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "productKey": "Product Key value",
  "licenseType": "online",
  "packageIdentityName": "Package Identity Name value"
}
```

### <a name="response"></a><span data-ttu-id="377e0-207">Respuesta</span><span class="sxs-lookup"><span data-stu-id="377e0-207">Response</span></span>
<span data-ttu-id="377e0-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="377e0-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 941

{
  "@odata.type": "#microsoft.graph.microsoftStoreForBusinessApp",
  "id": "f33358bc-58bc-f333-bc58-33f3bc5833f3",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "publishingState": "processing",
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "productKey": "Product Key value",
  "licenseType": "online",
  "packageIdentityName": "Package Identity Name value"
}
```



