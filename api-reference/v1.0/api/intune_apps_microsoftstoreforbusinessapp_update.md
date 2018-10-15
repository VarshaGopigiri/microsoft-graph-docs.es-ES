# <a name="update-microsoftstoreforbusinessapp"></a><span data-ttu-id="eb3d7-101">Actualizar microsoftStoreForBusinessApp</span><span class="sxs-lookup"><span data-stu-id="eb3d7-101">Update microsoftStoreForBusinessApp</span></span>

> <span data-ttu-id="eb3d7-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eb3d7-103">Actualice las propiedades de un objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-103">Update the properties of a [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="eb3d7-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="eb3d7-104">Prerequisites</span></span>
<span data-ttu-id="eb3d7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="eb3d7-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eb3d7-107">Permission type</span></span>|<span data-ttu-id="eb3d7-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eb3d7-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="eb3d7-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eb3d7-109">Delegated (work or school account)</span></span>|<span data-ttu-id="eb3d7-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eb3d7-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="eb3d7-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eb3d7-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="eb3d7-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-112">Not supported.</span></span>|
|<span data-ttu-id="eb3d7-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eb3d7-113">Application</span></span>|<span data-ttu-id="eb3d7-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="eb3d7-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eb3d7-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="eb3d7-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eb3d7-116">Request headers</span></span>
|<span data-ttu-id="eb3d7-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb3d7-117">Header</span></span>|<span data-ttu-id="eb3d7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="eb3d7-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="eb3d7-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="eb3d7-119">Authorization</span></span>|<span data-ttu-id="eb3d7-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="eb3d7-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="eb3d7-121">Accept</span></span>|<span data-ttu-id="eb3d7-122">application/json</span><span class="sxs-lookup"><span data-stu-id="eb3d7-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="eb3d7-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eb3d7-123">Request body</span></span>
<span data-ttu-id="eb3d7-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-124">In the request body, supply a JSON representation for the [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md) object.</span></span>

<span data-ttu-id="eb3d7-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-125">The following table shows the properties that are required when you create the [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).</span></span>

|<span data-ttu-id="eb3d7-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eb3d7-126">Property</span></span>|<span data-ttu-id="eb3d7-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb3d7-127">Type</span></span>|<span data-ttu-id="eb3d7-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb3d7-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="eb3d7-129">id</span><span class="sxs-lookup"><span data-stu-id="eb3d7-129">id</span></span>|<span data-ttu-id="eb3d7-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb3d7-130">String</span></span>|<span data-ttu-id="eb3d7-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-131">Key of the entity.</span></span> <span data-ttu-id="eb3d7-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb3d7-133">displayName</span><span class="sxs-lookup"><span data-stu-id="eb3d7-133">displayName</span></span>|<span data-ttu-id="eb3d7-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb3d7-134">String</span></span>|<span data-ttu-id="eb3d7-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="eb3d7-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb3d7-137">description</span><span class="sxs-lookup"><span data-stu-id="eb3d7-137">description</span></span>|<span data-ttu-id="eb3d7-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb3d7-138">String</span></span>|<span data-ttu-id="eb3d7-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-139">The description of the app.</span></span> <span data-ttu-id="eb3d7-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb3d7-141">publisher</span><span class="sxs-lookup"><span data-stu-id="eb3d7-141">publisher</span></span>|<span data-ttu-id="eb3d7-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb3d7-142">String</span></span>|<span data-ttu-id="eb3d7-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-143">The publisher of the app.</span></span> <span data-ttu-id="eb3d7-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb3d7-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="eb3d7-145">largeIcon</span></span>|[<span data-ttu-id="eb3d7-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="eb3d7-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="eb3d7-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="eb3d7-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb3d7-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="eb3d7-149">createdDateTime</span></span>|<span data-ttu-id="eb3d7-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="eb3d7-150">DateTimeOffset</span></span>|<span data-ttu-id="eb3d7-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-151">The date and time the app was created.</span></span> <span data-ttu-id="eb3d7-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb3d7-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="eb3d7-153">lastModifiedDateTime</span></span>|<span data-ttu-id="eb3d7-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="eb3d7-154">DateTimeOffset</span></span>|<span data-ttu-id="eb3d7-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-155">The date and time the app was last modified.</span></span> <span data-ttu-id="eb3d7-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb3d7-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="eb3d7-157">isFeatured</span></span>|<span data-ttu-id="eb3d7-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="eb3d7-158">Boolean</span></span>|<span data-ttu-id="eb3d7-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb3d7-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="eb3d7-160">privacyInformationUrl</span></span>|<span data-ttu-id="eb3d7-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb3d7-161">String</span></span>|<span data-ttu-id="eb3d7-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-162">The privacy statement Url.</span></span> <span data-ttu-id="eb3d7-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb3d7-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="eb3d7-164">informationUrl</span></span>|<span data-ttu-id="eb3d7-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb3d7-165">String</span></span>|<span data-ttu-id="eb3d7-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-166">The more information Url.</span></span> <span data-ttu-id="eb3d7-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb3d7-168">owner</span><span class="sxs-lookup"><span data-stu-id="eb3d7-168">owner</span></span>|<span data-ttu-id="eb3d7-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb3d7-169">String</span></span>|<span data-ttu-id="eb3d7-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-170">The owner of the app.</span></span> <span data-ttu-id="eb3d7-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb3d7-172">developer</span><span class="sxs-lookup"><span data-stu-id="eb3d7-172">developer</span></span>|<span data-ttu-id="eb3d7-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb3d7-173">String</span></span>|<span data-ttu-id="eb3d7-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-174">The developer of the app.</span></span> <span data-ttu-id="eb3d7-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb3d7-176">notas</span><span class="sxs-lookup"><span data-stu-id="eb3d7-176">notes</span></span>|<span data-ttu-id="eb3d7-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb3d7-177">String</span></span>|<span data-ttu-id="eb3d7-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-178">Notes for the app.</span></span> <span data-ttu-id="eb3d7-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb3d7-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb3d7-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="eb3d7-180">publishingState</span></span>|[<span data-ttu-id="eb3d7-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="eb3d7-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="eb3d7-p114">El estado de publicación para la aplicación. La aplicación no se puede asignar a menos que se publique la aplicación. Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing`, `published`.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-p114">The publishing state for the app. The app cannot be assigned unless the app is published. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md). The possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="eb3d7-186">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="eb3d7-186">usedLicenseCount</span></span>|<span data-ttu-id="eb3d7-187">Int32</span><span class="sxs-lookup"><span data-stu-id="eb3d7-187">Int32</span></span>|<span data-ttu-id="eb3d7-188">Número de licencias de Microsoft Store para Empresas en uso.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-188">The number of Microsoft Store for Business licenses in use.</span></span>|
|<span data-ttu-id="eb3d7-189">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="eb3d7-189">totalLicenseCount</span></span>|<span data-ttu-id="eb3d7-190">Int32</span><span class="sxs-lookup"><span data-stu-id="eb3d7-190">Int32</span></span>|<span data-ttu-id="eb3d7-191">Número total de licencias de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-191">The total number of Microsoft Store for Business licenses.</span></span>|
|<span data-ttu-id="eb3d7-192">productKey</span><span class="sxs-lookup"><span data-stu-id="eb3d7-192">productKey</span></span>|<span data-ttu-id="eb3d7-193">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb3d7-193">String</span></span>|<span data-ttu-id="eb3d7-194">Clave de producto de la aplicación</span><span class="sxs-lookup"><span data-stu-id="eb3d7-194">The app product key</span></span>|
|<span data-ttu-id="eb3d7-195">licenseType</span><span class="sxs-lookup"><span data-stu-id="eb3d7-195">licenseType</span></span>|[<span data-ttu-id="eb3d7-196">microsoftStoreForBusinessLicenseType</span><span class="sxs-lookup"><span data-stu-id="eb3d7-196">microsoftStoreForBusinessLicenseType</span></span>](../resources/intune_apps_microsoftstoreforbusinesslicensetype.md)|<span data-ttu-id="eb3d7-p115">Tipo de licencia de la aplicación. Los valores posibles son: `offline` y `online`.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-p115">The app license type Possible values are: `offline`, `online`.</span></span>|
|<span data-ttu-id="eb3d7-199">packageIdentityName</span><span class="sxs-lookup"><span data-stu-id="eb3d7-199">packageIdentityName</span></span>|<span data-ttu-id="eb3d7-200">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb3d7-200">String</span></span>|<span data-ttu-id="eb3d7-201">Identificador del paquete de aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-201">The app package identifier</span></span>|



## <a name="response"></a><span data-ttu-id="eb3d7-202">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb3d7-202">Response</span></span>
<span data-ttu-id="eb3d7-203">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-203">If successful, this method returns a `200 OK` response code and an updated [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eb3d7-204">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eb3d7-204">Example</span></span>
### <a name="request"></a><span data-ttu-id="eb3d7-205">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eb3d7-205">Request</span></span>
<span data-ttu-id="eb3d7-206">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-206">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="eb3d7-207">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb3d7-207">Response</span></span>
<span data-ttu-id="eb3d7-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eb3d7-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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








