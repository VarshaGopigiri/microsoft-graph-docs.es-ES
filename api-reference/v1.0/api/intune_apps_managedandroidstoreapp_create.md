# <a name="create-managedandroidstoreapp"></a><span data-ttu-id="94a6a-101">Crear managedAndroidStoreApp</span><span class="sxs-lookup"><span data-stu-id="94a6a-101">Create managedAndroidStoreApp</span></span>

> <span data-ttu-id="94a6a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="94a6a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="94a6a-103">Cree un objeto [managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="94a6a-103">Create a new [plannerBucket](../resources/intune_apps_managedandroidstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="94a6a-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="94a6a-104">Prerequisites</span></span>
<span data-ttu-id="94a6a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="94a6a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="94a6a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="94a6a-107">Permission type</span></span>|<span data-ttu-id="94a6a-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="94a6a-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="94a6a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="94a6a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="94a6a-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="94a6a-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="94a6a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="94a6a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="94a6a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="94a6a-112">Not supported.</span></span>|
|<span data-ttu-id="94a6a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="94a6a-113">Application</span></span>|<span data-ttu-id="94a6a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="94a6a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="94a6a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="94a6a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="94a6a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="94a6a-116">Request headers</span></span>
|<span data-ttu-id="94a6a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94a6a-117">Header</span></span>|<span data-ttu-id="94a6a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="94a6a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="94a6a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="94a6a-119">Authorization</span></span>|<span data-ttu-id="94a6a-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="94a6a-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="94a6a-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="94a6a-121">Accept</span></span>|<span data-ttu-id="94a6a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="94a6a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="94a6a-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="94a6a-123">Request body</span></span>
<span data-ttu-id="94a6a-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedAndroidStoreApp.</span><span class="sxs-lookup"><span data-stu-id="94a6a-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="94a6a-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedAndroidStoreApp.</span><span class="sxs-lookup"><span data-stu-id="94a6a-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="94a6a-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="94a6a-126">Property</span></span>|<span data-ttu-id="94a6a-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="94a6a-127">Type</span></span>|<span data-ttu-id="94a6a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="94a6a-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="94a6a-129">id</span><span class="sxs-lookup"><span data-stu-id="94a6a-129">id</span></span>|<span data-ttu-id="94a6a-130">String</span><span class="sxs-lookup"><span data-stu-id="94a6a-130">String</span></span>|<span data-ttu-id="94a6a-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="94a6a-131">Key of the setting.</span></span> <span data-ttu-id="94a6a-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="94a6a-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="94a6a-133">displayName</span><span class="sxs-lookup"><span data-stu-id="94a6a-133">displayName</span></span>|<span data-ttu-id="94a6a-134">String</span><span class="sxs-lookup"><span data-stu-id="94a6a-134">String</span></span>|<span data-ttu-id="94a6a-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="94a6a-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="94a6a-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="94a6a-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="94a6a-137">description</span><span class="sxs-lookup"><span data-stu-id="94a6a-137">description</span></span>|<span data-ttu-id="94a6a-138">String</span><span class="sxs-lookup"><span data-stu-id="94a6a-138">String</span></span>|<span data-ttu-id="94a6a-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94a6a-139">The description of the app.</span></span> <span data-ttu-id="94a6a-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="94a6a-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="94a6a-141">publicador</span><span class="sxs-lookup"><span data-stu-id="94a6a-141">Publisher</span></span>|<span data-ttu-id="94a6a-142">String</span><span class="sxs-lookup"><span data-stu-id="94a6a-142">String</span></span>|<span data-ttu-id="94a6a-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94a6a-143">The name of the app.</span></span> <span data-ttu-id="94a6a-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="94a6a-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="94a6a-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="94a6a-145">largeIcon</span></span>|[<span data-ttu-id="94a6a-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="94a6a-146">mimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="94a6a-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="94a6a-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="94a6a-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="94a6a-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="94a6a-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="94a6a-149">createdDateTime</span></span>|<span data-ttu-id="94a6a-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="94a6a-150">DateTimeOffset</span></span>|<span data-ttu-id="94a6a-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94a6a-151">The date and time when the page was created.</span></span> <span data-ttu-id="94a6a-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="94a6a-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="94a6a-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="94a6a-153">lastModifiedDateTime</span></span>|<span data-ttu-id="94a6a-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="94a6a-154">DateTimeOffset</span></span>|<span data-ttu-id="94a6a-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94a6a-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="94a6a-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="94a6a-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="94a6a-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="94a6a-157">isFeatured</span></span>|<span data-ttu-id="94a6a-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="94a6a-158">Boolean</span></span>|<span data-ttu-id="94a6a-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="94a6a-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="94a6a-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="94a6a-160">privacyInformationUrl</span></span>|<span data-ttu-id="94a6a-161">String</span><span class="sxs-lookup"><span data-stu-id="94a6a-161">String</span></span>|<span data-ttu-id="94a6a-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="94a6a-162">The privacy statement Url.</span></span> <span data-ttu-id="94a6a-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="94a6a-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="94a6a-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="94a6a-164">informationUrl</span></span>|<span data-ttu-id="94a6a-165">String</span><span class="sxs-lookup"><span data-stu-id="94a6a-165">String</span></span>|<span data-ttu-id="94a6a-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="94a6a-166">The more information Url.</span></span> <span data-ttu-id="94a6a-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="94a6a-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="94a6a-168">owner</span><span class="sxs-lookup"><span data-stu-id="94a6a-168">owner</span></span>|<span data-ttu-id="94a6a-169">String</span><span class="sxs-lookup"><span data-stu-id="94a6a-169">String</span></span>|<span data-ttu-id="94a6a-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94a6a-170">The owner of the timesheet.</span></span> <span data-ttu-id="94a6a-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="94a6a-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="94a6a-172">developer</span><span class="sxs-lookup"><span data-stu-id="94a6a-172">developer</span></span>|<span data-ttu-id="94a6a-173">String</span><span class="sxs-lookup"><span data-stu-id="94a6a-173">String</span></span>|<span data-ttu-id="94a6a-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94a6a-174">The name of the app.</span></span> <span data-ttu-id="94a6a-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="94a6a-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="94a6a-176">notas</span><span class="sxs-lookup"><span data-stu-id="94a6a-176">Notes</span></span>|<span data-ttu-id="94a6a-177">String</span><span class="sxs-lookup"><span data-stu-id="94a6a-177">String</span></span>|<span data-ttu-id="94a6a-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94a6a-178">Notes for the app.</span></span> <span data-ttu-id="94a6a-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="94a6a-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="94a6a-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="94a6a-180">publishingState</span></span>|<span data-ttu-id="94a6a-181">String</span><span class="sxs-lookup"><span data-stu-id="94a6a-181">String</span></span>|<span data-ttu-id="94a6a-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94a6a-182">The publishing state for the app.</span></span> <span data-ttu-id="94a6a-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="94a6a-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="94a6a-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="94a6a-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="94a6a-185">appAvailability</span><span class="sxs-lookup"><span data-stu-id="94a6a-185">appAvailability</span></span>|<span data-ttu-id="94a6a-186">String</span><span class="sxs-lookup"><span data-stu-id="94a6a-186">String</span></span>|<span data-ttu-id="94a6a-187">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94a6a-187">The Application's availability.</span></span> <span data-ttu-id="94a6a-188">Heredado de [managedApp](../resources/intune_apps_managedapp.md). Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="94a6a-188">Inherited from [managedApp](../resources/intune_apps_managedapp.md) Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="94a6a-189">version</span><span class="sxs-lookup"><span data-stu-id="94a6a-189">version</span></span>|<span data-ttu-id="94a6a-190">String</span><span class="sxs-lookup"><span data-stu-id="94a6a-190">String</span></span>|<span data-ttu-id="94a6a-191">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94a6a-191">The Application's version.</span></span> <span data-ttu-id="94a6a-192">Heredado de [managedApp](../resources/intune_apps_managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="94a6a-192">Inherited from [managedApp](../resources/intune_apps_managedapp.md)</span></span>|
|<span data-ttu-id="94a6a-193">packageId</span><span class="sxs-lookup"><span data-stu-id="94a6a-193">packageId</span></span>|<span data-ttu-id="94a6a-194">String</span><span class="sxs-lookup"><span data-stu-id="94a6a-194">String</span></span>|<span data-ttu-id="94a6a-195">El identificador de paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94a6a-195">The app's package ID.</span></span>|
|<span data-ttu-id="94a6a-196">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="94a6a-196">appStoreUrl</span></span>|<span data-ttu-id="94a6a-197">String</span><span class="sxs-lookup"><span data-stu-id="94a6a-197">String</span></span>|<span data-ttu-id="94a6a-198">La AppStoreUrl de Android.</span><span class="sxs-lookup"><span data-stu-id="94a6a-198">The Android AppStoreUrl.</span></span>|
|<span data-ttu-id="94a6a-199">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="94a6a-199">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="94a6a-200">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="94a6a-200">androidMinimumOperatingSystem</span></span>](../resources/intune_apps_androidminimumoperatingsystem.md)|<span data-ttu-id="94a6a-201">El valor para el sistema operativo mínimo compatible.</span><span class="sxs-lookup"><span data-stu-id="94a6a-201">The value for the minimum supported operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="94a6a-202">Respuesta</span><span class="sxs-lookup"><span data-stu-id="94a6a-202">Response</span></span>
<span data-ttu-id="94a6a-203">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="94a6a-203">If successful, this method returns a `201 Created` response code and a [ListItemVersion](../resources/intune_apps_managedandroidstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="94a6a-204">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="94a6a-204">Example</span></span>
### <a name="request"></a><span data-ttu-id="94a6a-205">Solicitud</span><span class="sxs-lookup"><span data-stu-id="94a6a-205">Request</span></span>
<span data-ttu-id="94a6a-206">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="94a6a-206">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1080

{
  "@odata.type": "#microsoft.graph.managedAndroidStoreApp",
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
  "packageId": "Package Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
    "v4_0": true,
    "v4_0_3": true,
    "v4_1": true,
    "v4_2": true,
    "v4_3": true,
    "v4_4": true,
    "v5_0": true,
    "v5_1": true
  }
}
```

### <a name="response"></a><span data-ttu-id="94a6a-207">Respuesta</span><span class="sxs-lookup"><span data-stu-id="94a6a-207">Response</span></span>
<span data-ttu-id="94a6a-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="94a6a-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1188

{
  "@odata.type": "#microsoft.graph.managedAndroidStoreApp",
  "id": "89e7e991-e991-89e7-91e9-e78991e9e789",
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
  "packageId": "Package Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
    "v4_0": true,
    "v4_0_3": true,
    "v4_1": true,
    "v4_2": true,
    "v4_3": true,
    "v4_4": true,
    "v5_0": true,
    "v5_1": true
  }
}
```



