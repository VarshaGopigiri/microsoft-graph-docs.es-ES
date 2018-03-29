# <a name="create-managediosstoreapp"></a><span data-ttu-id="7db17-101">Crear managedIOSStoreApp</span><span class="sxs-lookup"><span data-stu-id="7db17-101">Create managedIOSStoreApp</span></span>

> <span data-ttu-id="7db17-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7db17-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7db17-103">Cree un objeto [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="7db17-103">Create a new [plannerBucket](../resources/intune_apps_managediosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7db17-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7db17-104">Prerequisites</span></span>
<span data-ttu-id="7db17-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7db17-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7db17-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7db17-107">Permission type</span></span>|<span data-ttu-id="7db17-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7db17-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7db17-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7db17-109">Delegated (work or school account)</span></span>|<span data-ttu-id="7db17-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7db17-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="7db17-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7db17-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7db17-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7db17-112">Not supported.</span></span>|
|<span data-ttu-id="7db17-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7db17-113">Application</span></span>|<span data-ttu-id="7db17-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7db17-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7db17-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7db17-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="7db17-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7db17-116">Request headers</span></span>
|<span data-ttu-id="7db17-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7db17-117">Header</span></span>|<span data-ttu-id="7db17-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7db17-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7db17-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="7db17-119">Authorization</span></span>|<span data-ttu-id="7db17-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7db17-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="7db17-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7db17-121">Accept</span></span>|<span data-ttu-id="7db17-122">application/json</span><span class="sxs-lookup"><span data-stu-id="7db17-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7db17-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7db17-123">Request body</span></span>
<span data-ttu-id="7db17-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedIOSStoreApp.</span><span class="sxs-lookup"><span data-stu-id="7db17-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="7db17-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedIOSStoreApp.</span><span class="sxs-lookup"><span data-stu-id="7db17-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="7db17-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7db17-126">Property</span></span>|<span data-ttu-id="7db17-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="7db17-127">Type</span></span>|<span data-ttu-id="7db17-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="7db17-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7db17-129">id</span><span class="sxs-lookup"><span data-stu-id="7db17-129">id</span></span>|<span data-ttu-id="7db17-130">String</span><span class="sxs-lookup"><span data-stu-id="7db17-130">String</span></span>|<span data-ttu-id="7db17-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7db17-131">Key of the setting.</span></span> <span data-ttu-id="7db17-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7db17-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7db17-133">displayName</span><span class="sxs-lookup"><span data-stu-id="7db17-133">displayName</span></span>|<span data-ttu-id="7db17-134">String</span><span class="sxs-lookup"><span data-stu-id="7db17-134">String</span></span>|<span data-ttu-id="7db17-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="7db17-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="7db17-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7db17-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7db17-137">description</span><span class="sxs-lookup"><span data-stu-id="7db17-137">description</span></span>|<span data-ttu-id="7db17-138">String</span><span class="sxs-lookup"><span data-stu-id="7db17-138">String</span></span>|<span data-ttu-id="7db17-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7db17-139">The description of the app.</span></span> <span data-ttu-id="7db17-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7db17-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7db17-141">publicador</span><span class="sxs-lookup"><span data-stu-id="7db17-141">Publisher</span></span>|<span data-ttu-id="7db17-142">String</span><span class="sxs-lookup"><span data-stu-id="7db17-142">String</span></span>|<span data-ttu-id="7db17-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7db17-143">The name of the app.</span></span> <span data-ttu-id="7db17-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7db17-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7db17-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="7db17-145">largeIcon</span></span>|[<span data-ttu-id="7db17-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="7db17-146">mimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="7db17-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="7db17-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="7db17-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7db17-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7db17-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="7db17-149">createdDateTime</span></span>|<span data-ttu-id="7db17-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7db17-150">DateTimeOffset</span></span>|<span data-ttu-id="7db17-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7db17-151">The date and time when the page was created.</span></span> <span data-ttu-id="7db17-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7db17-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7db17-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7db17-153">lastModifiedDateTime</span></span>|<span data-ttu-id="7db17-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7db17-154">DateTimeOffset</span></span>|<span data-ttu-id="7db17-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7db17-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="7db17-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7db17-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7db17-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="7db17-157">isFeatured</span></span>|<span data-ttu-id="7db17-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="7db17-158">Boolean</span></span>|<span data-ttu-id="7db17-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7db17-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7db17-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="7db17-160">privacyInformationUrl</span></span>|<span data-ttu-id="7db17-161">String</span><span class="sxs-lookup"><span data-stu-id="7db17-161">String</span></span>|<span data-ttu-id="7db17-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="7db17-162">The privacy statement Url.</span></span> <span data-ttu-id="7db17-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7db17-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7db17-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="7db17-164">informationUrl</span></span>|<span data-ttu-id="7db17-165">String</span><span class="sxs-lookup"><span data-stu-id="7db17-165">String</span></span>|<span data-ttu-id="7db17-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="7db17-166">The more information Url.</span></span> <span data-ttu-id="7db17-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7db17-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7db17-168">owner</span><span class="sxs-lookup"><span data-stu-id="7db17-168">owner</span></span>|<span data-ttu-id="7db17-169">String</span><span class="sxs-lookup"><span data-stu-id="7db17-169">String</span></span>|<span data-ttu-id="7db17-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7db17-170">The owner of the timesheet.</span></span> <span data-ttu-id="7db17-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7db17-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7db17-172">developer</span><span class="sxs-lookup"><span data-stu-id="7db17-172">developer</span></span>|<span data-ttu-id="7db17-173">String</span><span class="sxs-lookup"><span data-stu-id="7db17-173">String</span></span>|<span data-ttu-id="7db17-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7db17-174">The name of the app.</span></span> <span data-ttu-id="7db17-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7db17-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7db17-176">notas</span><span class="sxs-lookup"><span data-stu-id="7db17-176">Notes</span></span>|<span data-ttu-id="7db17-177">String</span><span class="sxs-lookup"><span data-stu-id="7db17-177">String</span></span>|<span data-ttu-id="7db17-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7db17-178">Notes for the app.</span></span> <span data-ttu-id="7db17-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7db17-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7db17-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="7db17-180">publishingState</span></span>|<span data-ttu-id="7db17-181">String</span><span class="sxs-lookup"><span data-stu-id="7db17-181">String</span></span>|<span data-ttu-id="7db17-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7db17-182">The publishing state for the app.</span></span> <span data-ttu-id="7db17-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="7db17-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="7db17-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="7db17-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="7db17-185">appAvailability</span><span class="sxs-lookup"><span data-stu-id="7db17-185">appAvailability</span></span>|<span data-ttu-id="7db17-186">String</span><span class="sxs-lookup"><span data-stu-id="7db17-186">String</span></span>|<span data-ttu-id="7db17-187">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7db17-187">The Application's availability.</span></span> <span data-ttu-id="7db17-188">Heredado de [managedApp](../resources/intune_apps_managedapp.md). Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="7db17-188">Inherited from [managedApp](../resources/intune_apps_managedapp.md) Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="7db17-189">version</span><span class="sxs-lookup"><span data-stu-id="7db17-189">version</span></span>|<span data-ttu-id="7db17-190">String</span><span class="sxs-lookup"><span data-stu-id="7db17-190">String</span></span>|<span data-ttu-id="7db17-191">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7db17-191">The Application's version.</span></span> <span data-ttu-id="7db17-192">Heredado de [managedApp](../resources/intune_apps_managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="7db17-192">Inherited from [managedApp](../resources/intune_apps_managedapp.md)</span></span>|
|<span data-ttu-id="7db17-193">bundleId</span><span class="sxs-lookup"><span data-stu-id="7db17-193">bundleId</span></span>|<span data-ttu-id="7db17-194">String</span><span class="sxs-lookup"><span data-stu-id="7db17-194">String</span></span>|<span data-ttu-id="7db17-195">El identificador de lote de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7db17-195">The app's Bundle ID.</span></span>|
|<span data-ttu-id="7db17-196">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="7db17-196">appStoreUrl</span></span>|<span data-ttu-id="7db17-197">String</span><span class="sxs-lookup"><span data-stu-id="7db17-197">String</span></span>|<span data-ttu-id="7db17-198">La AppStoreUrl de Apple.</span><span class="sxs-lookup"><span data-stu-id="7db17-198">The Apple AppStoreUrl.</span></span>|
|<span data-ttu-id="7db17-199">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="7db17-199">applicableDeviceType</span></span>|[<span data-ttu-id="7db17-200">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="7db17-200">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="7db17-201">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="7db17-201">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="7db17-202">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="7db17-202">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="7db17-203">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="7db17-203">iosMinimumOperatingSystem</span></span>](../resources/intune_apps_iosminimumoperatingsystem.md)|<span data-ttu-id="7db17-204">El valor para el sistema operativo mínimo compatible.</span><span class="sxs-lookup"><span data-stu-id="7db17-204">The value for the minimum supported operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="7db17-205">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7db17-205">Response</span></span>
<span data-ttu-id="7db17-206">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7db17-206">If successful, this method returns a `201 Created` response code and a [DriveItemVersion](../resources/intune_apps_managediosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7db17-207">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7db17-207">Example</span></span>
### <a name="request"></a><span data-ttu-id="7db17-208">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7db17-208">Request</span></span>
<span data-ttu-id="7db17-209">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7db17-209">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1128

{
  "@odata.type": "#microsoft.graph.managedIOSStoreApp",
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
  "appAvailability": "lineOfBusiness",
  "version": "Version value",
  "bundleId": "Bundle Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.iosMinimumOperatingSystem",
    "v8_0": true,
    "v9_0": true,
    "v10_0": true,
    "v11_0": true
  }
}
```

### <a name="response"></a><span data-ttu-id="7db17-210">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7db17-210">Response</span></span>
<span data-ttu-id="7db17-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7db17-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1236

{
  "@odata.type": "#microsoft.graph.managedIOSStoreApp",
  "id": "51b9830f-830f-51b9-0f83-b9510f83b951",
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
  "appAvailability": "lineOfBusiness",
  "version": "Version value",
  "bundleId": "Bundle Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.iosMinimumOperatingSystem",
    "v8_0": true,
    "v9_0": true,
    "v10_0": true,
    "v11_0": true
  }
}
```



