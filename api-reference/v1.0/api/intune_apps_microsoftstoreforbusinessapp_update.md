# <a name="update-microsoftstoreforbusinessapp"></a><span data-ttu-id="eb2c9-101">Actualizar microsoftStoreForBusinessApp</span><span class="sxs-lookup"><span data-stu-id="eb2c9-101">Update microsoftStoreForBusinessApp</span></span>

> <span data-ttu-id="eb2c9-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eb2c9-103">Actualice las propiedades de un objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-103">Update the properties of a [calendar](../resources/intune_apps_microsoftstoreforbusinessapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="eb2c9-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="eb2c9-104">Prerequisites</span></span>
<span data-ttu-id="eb2c9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="eb2c9-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eb2c9-107">Permission type</span></span>|<span data-ttu-id="eb2c9-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eb2c9-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="eb2c9-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eb2c9-109">Delegated (work or school account)</span></span>|<span data-ttu-id="eb2c9-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eb2c9-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="eb2c9-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eb2c9-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="eb2c9-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-112">Not supported.</span></span>|
|<span data-ttu-id="eb2c9-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eb2c9-113">Application</span></span>|<span data-ttu-id="eb2c9-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="eb2c9-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eb2c9-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="eb2c9-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eb2c9-116">Request headers</span></span>
|<span data-ttu-id="eb2c9-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb2c9-117">Header</span></span>|<span data-ttu-id="eb2c9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="eb2c9-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="eb2c9-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="eb2c9-119">Authorization</span></span>|<span data-ttu-id="eb2c9-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="eb2c9-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="eb2c9-121">Accept</span></span>|<span data-ttu-id="eb2c9-122">application/json</span><span class="sxs-lookup"><span data-stu-id="eb2c9-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="eb2c9-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eb2c9-123">Request body</span></span>
<span data-ttu-id="eb2c9-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_apps_microsoftstoreforbusinessapp.md) object.</span></span>

<span data-ttu-id="eb2c9-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="eb2c9-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eb2c9-126">Property</span></span>|<span data-ttu-id="eb2c9-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb2c9-127">Type</span></span>|<span data-ttu-id="eb2c9-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb2c9-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="eb2c9-129">id</span><span class="sxs-lookup"><span data-stu-id="eb2c9-129">id</span></span>|<span data-ttu-id="eb2c9-130">String</span><span class="sxs-lookup"><span data-stu-id="eb2c9-130">String</span></span>|<span data-ttu-id="eb2c9-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-131">Key of the setting.</span></span> <span data-ttu-id="eb2c9-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb2c9-133">displayName</span><span class="sxs-lookup"><span data-stu-id="eb2c9-133">displayName</span></span>|<span data-ttu-id="eb2c9-134">String</span><span class="sxs-lookup"><span data-stu-id="eb2c9-134">String</span></span>|<span data-ttu-id="eb2c9-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="eb2c9-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb2c9-137">description</span><span class="sxs-lookup"><span data-stu-id="eb2c9-137">description</span></span>|<span data-ttu-id="eb2c9-138">String</span><span class="sxs-lookup"><span data-stu-id="eb2c9-138">String</span></span>|<span data-ttu-id="eb2c9-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-139">The description of the app.</span></span> <span data-ttu-id="eb2c9-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb2c9-141">publicador</span><span class="sxs-lookup"><span data-stu-id="eb2c9-141">Publisher</span></span>|<span data-ttu-id="eb2c9-142">String</span><span class="sxs-lookup"><span data-stu-id="eb2c9-142">String</span></span>|<span data-ttu-id="eb2c9-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-143">The name of the app.</span></span> <span data-ttu-id="eb2c9-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb2c9-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="eb2c9-145">largeIcon</span></span>|[<span data-ttu-id="eb2c9-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="eb2c9-146">mimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="eb2c9-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="eb2c9-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb2c9-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="eb2c9-149">createdDateTime</span></span>|<span data-ttu-id="eb2c9-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="eb2c9-150">DateTimeOffset</span></span>|<span data-ttu-id="eb2c9-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-151">The date and time when the page was created.</span></span> <span data-ttu-id="eb2c9-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb2c9-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="eb2c9-153">lastModifiedDateTime</span></span>|<span data-ttu-id="eb2c9-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="eb2c9-154">DateTimeOffset</span></span>|<span data-ttu-id="eb2c9-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="eb2c9-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb2c9-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="eb2c9-157">isFeatured</span></span>|<span data-ttu-id="eb2c9-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="eb2c9-158">Boolean</span></span>|<span data-ttu-id="eb2c9-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb2c9-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="eb2c9-160">privacyInformationUrl</span></span>|<span data-ttu-id="eb2c9-161">String</span><span class="sxs-lookup"><span data-stu-id="eb2c9-161">String</span></span>|<span data-ttu-id="eb2c9-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-162">The privacy statement Url.</span></span> <span data-ttu-id="eb2c9-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb2c9-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="eb2c9-164">informationUrl</span></span>|<span data-ttu-id="eb2c9-165">String</span><span class="sxs-lookup"><span data-stu-id="eb2c9-165">String</span></span>|<span data-ttu-id="eb2c9-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-166">The more information Url.</span></span> <span data-ttu-id="eb2c9-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb2c9-168">owner</span><span class="sxs-lookup"><span data-stu-id="eb2c9-168">owner</span></span>|<span data-ttu-id="eb2c9-169">String</span><span class="sxs-lookup"><span data-stu-id="eb2c9-169">String</span></span>|<span data-ttu-id="eb2c9-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-170">The owner of the timesheet.</span></span> <span data-ttu-id="eb2c9-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb2c9-172">developer</span><span class="sxs-lookup"><span data-stu-id="eb2c9-172">developer</span></span>|<span data-ttu-id="eb2c9-173">String</span><span class="sxs-lookup"><span data-stu-id="eb2c9-173">String</span></span>|<span data-ttu-id="eb2c9-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-174">The name of the app.</span></span> <span data-ttu-id="eb2c9-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb2c9-176">notas</span><span class="sxs-lookup"><span data-stu-id="eb2c9-176">Notes</span></span>|<span data-ttu-id="eb2c9-177">String</span><span class="sxs-lookup"><span data-stu-id="eb2c9-177">String</span></span>|<span data-ttu-id="eb2c9-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-178">Notes for the app.</span></span> <span data-ttu-id="eb2c9-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb2c9-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="eb2c9-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="eb2c9-180">publishingState</span></span>|<span data-ttu-id="eb2c9-181">String</span><span class="sxs-lookup"><span data-stu-id="eb2c9-181">String</span></span>|<span data-ttu-id="eb2c9-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-182">The publishing state for the app.</span></span> <span data-ttu-id="eb2c9-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="eb2c9-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="eb2c9-185">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="eb2c9-185">usedLicenseCount</span></span>|<span data-ttu-id="eb2c9-186">Int32</span><span class="sxs-lookup"><span data-stu-id="eb2c9-186">Int32</span></span>|<span data-ttu-id="eb2c9-187">Número de licencias de Microsoft Store para Empresas en uso.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-187">The number of Microsoft Store for Business licenses in use.</span></span>|
|<span data-ttu-id="eb2c9-188">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="eb2c9-188">totalLicenseCount</span></span>|<span data-ttu-id="eb2c9-189">Int32</span><span class="sxs-lookup"><span data-stu-id="eb2c9-189">Int32</span></span>|<span data-ttu-id="eb2c9-190">Número total de licencias de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-190">The total number of Microsoft Store for Business licenses.</span></span>|
|<span data-ttu-id="eb2c9-191">productKey</span><span class="sxs-lookup"><span data-stu-id="eb2c9-191">productKey</span></span>|<span data-ttu-id="eb2c9-192">String</span><span class="sxs-lookup"><span data-stu-id="eb2c9-192">String</span></span>|<span data-ttu-id="eb2c9-193">Clave de producto de la aplicación</span><span class="sxs-lookup"><span data-stu-id="eb2c9-193">The app product key</span></span>|
|<span data-ttu-id="eb2c9-194">licenseType</span><span class="sxs-lookup"><span data-stu-id="eb2c9-194">licenseType</span></span>|<span data-ttu-id="eb2c9-195">String</span><span class="sxs-lookup"><span data-stu-id="eb2c9-195">String</span></span>|<span data-ttu-id="eb2c9-196">Tipo de licencia de la aplicación. Los valores posibles son: `offline` y `online`.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-196">The app license type Possible values are: `offline`, `online`.</span></span>|
|<span data-ttu-id="eb2c9-197">packageIdentityName</span><span class="sxs-lookup"><span data-stu-id="eb2c9-197">packageIdentityName</span></span>|<span data-ttu-id="eb2c9-198">String</span><span class="sxs-lookup"><span data-stu-id="eb2c9-198">String</span></span>|<span data-ttu-id="eb2c9-199">Identificador del paquete de aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-199">The app package identifier</span></span>|



## <a name="response"></a><span data-ttu-id="eb2c9-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb2c9-200">Response</span></span>
<span data-ttu-id="eb2c9-201">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-201">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_apps_microsoftstoreforbusinessapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eb2c9-202">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eb2c9-202">Example</span></span>
### <a name="request"></a><span data-ttu-id="eb2c9-203">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eb2c9-203">Request</span></span>
<span data-ttu-id="eb2c9-204">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-204">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="eb2c9-205">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb2c9-205">Response</span></span>
<span data-ttu-id="eb2c9-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eb2c9-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



