# <a name="create-microsoftstoreforbusinessapp"></a><span data-ttu-id="a00a8-101">Crear microsoftStoreForBusinessApp</span><span class="sxs-lookup"><span data-stu-id="a00a8-101">Create microsoftStoreForBusinessApp</span></span>

> <span data-ttu-id="a00a8-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a00a8-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a00a8-103">Crear un objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).</span><span class="sxs-lookup"><span data-stu-id="a00a8-103">Create a new [plannerBucket](../resources/intune_apps_microsoftstoreforbusinessapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a00a8-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a00a8-104">Prerequisites</span></span>
<span data-ttu-id="a00a8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a00a8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a00a8-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a00a8-107">Permission type</span></span>|<span data-ttu-id="a00a8-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a00a8-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a00a8-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a00a8-109">Delegated (work or school account)</span></span>|<span data-ttu-id="a00a8-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a00a8-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="a00a8-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a00a8-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a00a8-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a00a8-112">Not supported.</span></span>|
|<span data-ttu-id="a00a8-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a00a8-113">Application</span></span>|<span data-ttu-id="a00a8-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="a00a8-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a00a8-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a00a8-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="a00a8-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a00a8-116">Request headers</span></span>
|<span data-ttu-id="a00a8-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a00a8-117">Header</span></span>|<span data-ttu-id="a00a8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a00a8-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a00a8-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="a00a8-119">Authorization</span></span>|<span data-ttu-id="a00a8-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a00a8-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="a00a8-121">Accept</span><span class="sxs-lookup"><span data-stu-id="a00a8-121">Accept</span></span>|<span data-ttu-id="a00a8-122">application/json</span><span class="sxs-lookup"><span data-stu-id="a00a8-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a00a8-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a00a8-123">Request body</span></span>
<span data-ttu-id="a00a8-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto microsoftStoreForBusinessApp.</span><span class="sxs-lookup"><span data-stu-id="a00a8-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="a00a8-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto microsoftStoreForBusinessApp.</span><span class="sxs-lookup"><span data-stu-id="a00a8-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="a00a8-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a00a8-126">Property</span></span>|<span data-ttu-id="a00a8-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="a00a8-127">Type</span></span>|<span data-ttu-id="a00a8-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="a00a8-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a00a8-129">id</span><span class="sxs-lookup"><span data-stu-id="a00a8-129">id</span></span>|<span data-ttu-id="a00a8-130">String</span><span class="sxs-lookup"><span data-stu-id="a00a8-130">String</span></span>|<span data-ttu-id="a00a8-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a00a8-131">Key of the setting.</span></span> <span data-ttu-id="a00a8-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a00a8-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a00a8-133">displayName</span><span class="sxs-lookup"><span data-stu-id="a00a8-133">displayName</span></span>|<span data-ttu-id="a00a8-134">String</span><span class="sxs-lookup"><span data-stu-id="a00a8-134">String</span></span>|<span data-ttu-id="a00a8-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="a00a8-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="a00a8-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a00a8-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a00a8-137">description</span><span class="sxs-lookup"><span data-stu-id="a00a8-137">description</span></span>|<span data-ttu-id="a00a8-138">String</span><span class="sxs-lookup"><span data-stu-id="a00a8-138">String</span></span>|<span data-ttu-id="a00a8-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a00a8-139">The description of the app.</span></span> <span data-ttu-id="a00a8-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a00a8-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a00a8-141">publisher</span><span class="sxs-lookup"><span data-stu-id="a00a8-141">Publisher</span></span>|<span data-ttu-id="a00a8-142">String</span><span class="sxs-lookup"><span data-stu-id="a00a8-142">String</span></span>|<span data-ttu-id="a00a8-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a00a8-143">The name of the app.</span></span> <span data-ttu-id="a00a8-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a00a8-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a00a8-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="a00a8-145">largeIcon</span></span>|[<span data-ttu-id="a00a8-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="a00a8-146">mimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="a00a8-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="a00a8-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="a00a8-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a00a8-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a00a8-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a00a8-149">createdDateTime</span></span>|<span data-ttu-id="a00a8-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a00a8-150">DateTimeOffset</span></span>|<span data-ttu-id="a00a8-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a00a8-151">The date and time when the page was created.</span></span> <span data-ttu-id="a00a8-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a00a8-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a00a8-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a00a8-153">lastModifiedDateTime</span></span>|<span data-ttu-id="a00a8-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a00a8-154">DateTimeOffset</span></span>|<span data-ttu-id="a00a8-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a00a8-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="a00a8-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a00a8-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a00a8-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="a00a8-157">isFeatured</span></span>|<span data-ttu-id="a00a8-158">Boolean</span><span class="sxs-lookup"><span data-stu-id="a00a8-158">Boolean</span></span>|<span data-ttu-id="a00a8-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a00a8-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a00a8-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="a00a8-160">privacyInformationUrl</span></span>|<span data-ttu-id="a00a8-161">String</span><span class="sxs-lookup"><span data-stu-id="a00a8-161">String</span></span>|<span data-ttu-id="a00a8-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="a00a8-162">The privacy statement Url.</span></span> <span data-ttu-id="a00a8-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a00a8-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a00a8-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="a00a8-164">informationUrl</span></span>|<span data-ttu-id="a00a8-165">String</span><span class="sxs-lookup"><span data-stu-id="a00a8-165">String</span></span>|<span data-ttu-id="a00a8-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a00a8-166">The more information Url.</span></span> <span data-ttu-id="a00a8-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a00a8-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a00a8-168">owner</span><span class="sxs-lookup"><span data-stu-id="a00a8-168">owner</span></span>|<span data-ttu-id="a00a8-169">String</span><span class="sxs-lookup"><span data-stu-id="a00a8-169">String</span></span>|<span data-ttu-id="a00a8-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a00a8-170">The owner of the timesheet.</span></span> <span data-ttu-id="a00a8-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a00a8-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a00a8-172">developer</span><span class="sxs-lookup"><span data-stu-id="a00a8-172">developer</span></span>|<span data-ttu-id="a00a8-173">String</span><span class="sxs-lookup"><span data-stu-id="a00a8-173">String</span></span>|<span data-ttu-id="a00a8-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a00a8-174">The name of the app.</span></span> <span data-ttu-id="a00a8-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a00a8-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a00a8-176">notes</span><span class="sxs-lookup"><span data-stu-id="a00a8-176">Notes</span></span>|<span data-ttu-id="a00a8-177">String</span><span class="sxs-lookup"><span data-stu-id="a00a8-177">String</span></span>|<span data-ttu-id="a00a8-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a00a8-178">Notes for the app.</span></span> <span data-ttu-id="a00a8-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a00a8-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a00a8-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="a00a8-180">publishingState</span></span>|<span data-ttu-id="a00a8-181">String</span><span class="sxs-lookup"><span data-stu-id="a00a8-181">String</span></span>|<span data-ttu-id="a00a8-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a00a8-182">The publishing state for the app.</span></span> <span data-ttu-id="a00a8-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="a00a8-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="a00a8-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="a00a8-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="a00a8-185">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="a00a8-185">usedLicenseCount</span></span>|<span data-ttu-id="a00a8-186">Int32</span><span class="sxs-lookup"><span data-stu-id="a00a8-186">Int32</span></span>|<span data-ttu-id="a00a8-187">Número de licencias de Microsoft Store para Empresas en uso.</span><span class="sxs-lookup"><span data-stu-id="a00a8-187">The number of Microsoft Store for Business licenses in use.</span></span>|
|<span data-ttu-id="a00a8-188">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="a00a8-188">totalLicenseCount</span></span>|<span data-ttu-id="a00a8-189">Int32</span><span class="sxs-lookup"><span data-stu-id="a00a8-189">Int32</span></span>|<span data-ttu-id="a00a8-190">Número total de licencias de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="a00a8-190">The total number of Microsoft Store for Business licenses.</span></span>|
|<span data-ttu-id="a00a8-191">productKey</span><span class="sxs-lookup"><span data-stu-id="a00a8-191">productKey</span></span>|<span data-ttu-id="a00a8-192">String</span><span class="sxs-lookup"><span data-stu-id="a00a8-192">String</span></span>|<span data-ttu-id="a00a8-193">Clave de producto de la aplicación</span><span class="sxs-lookup"><span data-stu-id="a00a8-193">The app product key</span></span>|
|<span data-ttu-id="a00a8-194">licenseType</span><span class="sxs-lookup"><span data-stu-id="a00a8-194">licenseType</span></span>|<span data-ttu-id="a00a8-195">String</span><span class="sxs-lookup"><span data-stu-id="a00a8-195">String</span></span>|<span data-ttu-id="a00a8-196">Tipo de licencia de la aplicación. Los valores posibles son: `offline` y `online`.</span><span class="sxs-lookup"><span data-stu-id="a00a8-196">The app license type Possible values are: `offline`, `online`.</span></span>|
|<span data-ttu-id="a00a8-197">packageIdentityName</span><span class="sxs-lookup"><span data-stu-id="a00a8-197">packageIdentityName</span></span>|<span data-ttu-id="a00a8-198">String</span><span class="sxs-lookup"><span data-stu-id="a00a8-198">String</span></span>|<span data-ttu-id="a00a8-199">Identificador del paquete de aplicación.</span><span class="sxs-lookup"><span data-stu-id="a00a8-199">The app package identifier</span></span>|



## <a name="response"></a><span data-ttu-id="a00a8-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a00a8-200">Response</span></span>
<span data-ttu-id="a00a8-201">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a00a8-201">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_apps_microsoftstoreforbusinessapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a00a8-202">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a00a8-202">Example</span></span>
### <a name="request"></a><span data-ttu-id="a00a8-203">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a00a8-203">Request</span></span>
<span data-ttu-id="a00a8-204">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a00a8-204">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 833

{
  "@odata.type": "#microsoft.graph.microsoftStoreForBusinessApp",
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

### <a name="response"></a><span data-ttu-id="a00a8-205">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a00a8-205">Response</span></span>
<span data-ttu-id="a00a8-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a00a8-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



