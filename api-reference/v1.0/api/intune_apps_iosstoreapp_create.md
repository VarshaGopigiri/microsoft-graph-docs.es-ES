# <a name="create-iosstoreapp"></a><span data-ttu-id="da8dd-101">Crear iosStoreApp</span><span class="sxs-lookup"><span data-stu-id="da8dd-101">Create iosStoreApp</span></span>

> <span data-ttu-id="da8dd-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="da8dd-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="da8dd-103">Cree un objeto [iosStoreApp](../resources/intune_apps_iosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="da8dd-103">Create a new [plannerBucket](../resources/intune_apps_iosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="da8dd-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="da8dd-104">Prerequisites</span></span>
<span data-ttu-id="da8dd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="da8dd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="da8dd-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="da8dd-107">Permission type</span></span>|<span data-ttu-id="da8dd-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="da8dd-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="da8dd-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="da8dd-109">Delegated (work or school account)</span></span>|<span data-ttu-id="da8dd-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="da8dd-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="da8dd-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="da8dd-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="da8dd-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="da8dd-112">Not supported.</span></span>|
|<span data-ttu-id="da8dd-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="da8dd-113">Application</span></span>|<span data-ttu-id="da8dd-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="da8dd-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="da8dd-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="da8dd-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="da8dd-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="da8dd-116">Request headers</span></span>
|<span data-ttu-id="da8dd-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da8dd-117">Header</span></span>|<span data-ttu-id="da8dd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="da8dd-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="da8dd-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="da8dd-119">Authorization</span></span>|<span data-ttu-id="da8dd-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="da8dd-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="da8dd-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="da8dd-121">Accept</span></span>|<span data-ttu-id="da8dd-122">application/json</span><span class="sxs-lookup"><span data-stu-id="da8dd-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="da8dd-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="da8dd-123">Request body</span></span>
<span data-ttu-id="da8dd-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosStoreApp.</span><span class="sxs-lookup"><span data-stu-id="da8dd-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="da8dd-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosStoreApp.</span><span class="sxs-lookup"><span data-stu-id="da8dd-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="da8dd-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="da8dd-126">Property</span></span>|<span data-ttu-id="da8dd-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="da8dd-127">Type</span></span>|<span data-ttu-id="da8dd-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="da8dd-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="da8dd-129">id</span><span class="sxs-lookup"><span data-stu-id="da8dd-129">id</span></span>|<span data-ttu-id="da8dd-130">String</span><span class="sxs-lookup"><span data-stu-id="da8dd-130">String</span></span>|<span data-ttu-id="da8dd-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="da8dd-131">Key of the setting.</span></span> <span data-ttu-id="da8dd-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="da8dd-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="da8dd-133">displayName</span><span class="sxs-lookup"><span data-stu-id="da8dd-133">displayName</span></span>|<span data-ttu-id="da8dd-134">String</span><span class="sxs-lookup"><span data-stu-id="da8dd-134">String</span></span>|<span data-ttu-id="da8dd-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="da8dd-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="da8dd-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="da8dd-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="da8dd-137">description</span><span class="sxs-lookup"><span data-stu-id="da8dd-137">description</span></span>|<span data-ttu-id="da8dd-138">String</span><span class="sxs-lookup"><span data-stu-id="da8dd-138">String</span></span>|<span data-ttu-id="da8dd-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="da8dd-139">The description of the app.</span></span> <span data-ttu-id="da8dd-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="da8dd-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="da8dd-141">publicador</span><span class="sxs-lookup"><span data-stu-id="da8dd-141">Publisher</span></span>|<span data-ttu-id="da8dd-142">String</span><span class="sxs-lookup"><span data-stu-id="da8dd-142">String</span></span>|<span data-ttu-id="da8dd-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="da8dd-143">The name of the app.</span></span> <span data-ttu-id="da8dd-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="da8dd-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="da8dd-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="da8dd-145">largeIcon</span></span>|[<span data-ttu-id="da8dd-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="da8dd-146">mimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="da8dd-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="da8dd-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="da8dd-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="da8dd-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="da8dd-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="da8dd-149">createdDateTime</span></span>|<span data-ttu-id="da8dd-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="da8dd-150">DateTimeOffset</span></span>|<span data-ttu-id="da8dd-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="da8dd-151">The date and time when the page was created.</span></span> <span data-ttu-id="da8dd-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="da8dd-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="da8dd-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="da8dd-153">lastModifiedDateTime</span></span>|<span data-ttu-id="da8dd-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="da8dd-154">DateTimeOffset</span></span>|<span data-ttu-id="da8dd-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="da8dd-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="da8dd-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="da8dd-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="da8dd-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="da8dd-157">isFeatured</span></span>|<span data-ttu-id="da8dd-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="da8dd-158">Boolean</span></span>|<span data-ttu-id="da8dd-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="da8dd-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="da8dd-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="da8dd-160">privacyInformationUrl</span></span>|<span data-ttu-id="da8dd-161">String</span><span class="sxs-lookup"><span data-stu-id="da8dd-161">String</span></span>|<span data-ttu-id="da8dd-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="da8dd-162">The privacy statement Url.</span></span> <span data-ttu-id="da8dd-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="da8dd-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="da8dd-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="da8dd-164">informationUrl</span></span>|<span data-ttu-id="da8dd-165">String</span><span class="sxs-lookup"><span data-stu-id="da8dd-165">String</span></span>|<span data-ttu-id="da8dd-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="da8dd-166">The more information Url.</span></span> <span data-ttu-id="da8dd-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="da8dd-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="da8dd-168">owner</span><span class="sxs-lookup"><span data-stu-id="da8dd-168">owner</span></span>|<span data-ttu-id="da8dd-169">String</span><span class="sxs-lookup"><span data-stu-id="da8dd-169">String</span></span>|<span data-ttu-id="da8dd-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="da8dd-170">The owner of the timesheet.</span></span> <span data-ttu-id="da8dd-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="da8dd-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="da8dd-172">developer</span><span class="sxs-lookup"><span data-stu-id="da8dd-172">developer</span></span>|<span data-ttu-id="da8dd-173">String</span><span class="sxs-lookup"><span data-stu-id="da8dd-173">String</span></span>|<span data-ttu-id="da8dd-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="da8dd-174">The name of the app.</span></span> <span data-ttu-id="da8dd-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="da8dd-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="da8dd-176">notas</span><span class="sxs-lookup"><span data-stu-id="da8dd-176">Notes</span></span>|<span data-ttu-id="da8dd-177">String</span><span class="sxs-lookup"><span data-stu-id="da8dd-177">String</span></span>|<span data-ttu-id="da8dd-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="da8dd-178">Notes for the app.</span></span> <span data-ttu-id="da8dd-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="da8dd-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="da8dd-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="da8dd-180">publishingState</span></span>|<span data-ttu-id="da8dd-181">String</span><span class="sxs-lookup"><span data-stu-id="da8dd-181">String</span></span>|<span data-ttu-id="da8dd-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="da8dd-182">The publishing state for the app.</span></span> <span data-ttu-id="da8dd-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="da8dd-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="da8dd-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="da8dd-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="da8dd-185">bundleId</span><span class="sxs-lookup"><span data-stu-id="da8dd-185">bundleId</span></span>|<span data-ttu-id="da8dd-186">String</span><span class="sxs-lookup"><span data-stu-id="da8dd-186">String</span></span>|<span data-ttu-id="da8dd-187">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="da8dd-187">The Identity Name.</span></span>|
|<span data-ttu-id="da8dd-188">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="da8dd-188">appStoreUrl</span></span>|<span data-ttu-id="da8dd-189">String</span><span class="sxs-lookup"><span data-stu-id="da8dd-189">String</span></span>|<span data-ttu-id="da8dd-190">Dirección URL de la App Store de Apple</span><span class="sxs-lookup"><span data-stu-id="da8dd-190">The Apple App Store URL</span></span>|
|<span data-ttu-id="da8dd-191">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="da8dd-191">applicableDeviceType</span></span>|[<span data-ttu-id="da8dd-192">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="da8dd-192">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="da8dd-193">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="da8dd-193">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="da8dd-194">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="da8dd-194">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="da8dd-195">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="da8dd-195">iosMinimumOperatingSystem</span></span>](../resources/intune_apps_iosminimumoperatingsystem.md)|<span data-ttu-id="da8dd-196">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="da8dd-196">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="da8dd-197">Respuesta</span><span class="sxs-lookup"><span data-stu-id="da8dd-197">Response</span></span>
<span data-ttu-id="da8dd-198">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosStoreApp](../resources/intune_apps_iosstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="da8dd-198">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_apps_iosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="da8dd-199">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="da8dd-199">Example</span></span>
### <a name="request"></a><span data-ttu-id="da8dd-200">Solicitud</span><span class="sxs-lookup"><span data-stu-id="da8dd-200">Request</span></span>
<span data-ttu-id="da8dd-201">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="da8dd-201">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1050

{
  "@odata.type": "#microsoft.graph.iosStoreApp",
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

### <a name="response"></a><span data-ttu-id="da8dd-202">Respuesta</span><span class="sxs-lookup"><span data-stu-id="da8dd-202">Response</span></span>
<span data-ttu-id="da8dd-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="da8dd-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1158

{
  "@odata.type": "#microsoft.graph.iosStoreApp",
  "id": "a04adbe2-dbe2-a04a-e2db-4aa0e2db4aa0",
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



