# <a name="create-iosstoreapp"></a><span data-ttu-id="53e2f-101">Crear iosStoreApp</span><span class="sxs-lookup"><span data-stu-id="53e2f-101">Create iosStoreApp</span></span>

> <span data-ttu-id="53e2f-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="53e2f-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="53e2f-103">Cree un objeto [iosStoreApp](../resources/intune_apps_iosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="53e2f-103">Create a new [iosStoreApp](../resources/intune_apps_iosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="53e2f-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="53e2f-104">Prerequisites</span></span>
<span data-ttu-id="53e2f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="53e2f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="53e2f-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="53e2f-107">Permission type</span></span>|<span data-ttu-id="53e2f-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="53e2f-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="53e2f-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="53e2f-109">Delegated (work or school account)</span></span>|<span data-ttu-id="53e2f-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="53e2f-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="53e2f-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="53e2f-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="53e2f-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="53e2f-112">Not supported.</span></span>|
|<span data-ttu-id="53e2f-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="53e2f-113">Application</span></span>|<span data-ttu-id="53e2f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="53e2f-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="53e2f-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="53e2f-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="53e2f-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="53e2f-116">Request headers</span></span>
|<span data-ttu-id="53e2f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53e2f-117">Header</span></span>|<span data-ttu-id="53e2f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="53e2f-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="53e2f-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="53e2f-119">Authorization</span></span>|<span data-ttu-id="53e2f-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="53e2f-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="53e2f-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="53e2f-121">Accept</span></span>|<span data-ttu-id="53e2f-122">application/json</span><span class="sxs-lookup"><span data-stu-id="53e2f-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="53e2f-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="53e2f-123">Request body</span></span>
<span data-ttu-id="53e2f-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosStoreApp.</span><span class="sxs-lookup"><span data-stu-id="53e2f-124">In the request body, supply a JSON representation for the iosStoreApp object.</span></span>

<span data-ttu-id="53e2f-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosStoreApp.</span><span class="sxs-lookup"><span data-stu-id="53e2f-125">The following table shows the properties that are required when you create the iosStoreApp.</span></span>

|<span data-ttu-id="53e2f-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53e2f-126">Property</span></span>|<span data-ttu-id="53e2f-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="53e2f-127">Type</span></span>|<span data-ttu-id="53e2f-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="53e2f-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="53e2f-129">id</span><span class="sxs-lookup"><span data-stu-id="53e2f-129">id</span></span>|<span data-ttu-id="53e2f-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="53e2f-130">String</span></span>|<span data-ttu-id="53e2f-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="53e2f-131">Key of the entity.</span></span> <span data-ttu-id="53e2f-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53e2f-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="53e2f-133">displayName</span><span class="sxs-lookup"><span data-stu-id="53e2f-133">displayName</span></span>|<span data-ttu-id="53e2f-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="53e2f-134">String</span></span>|<span data-ttu-id="53e2f-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="53e2f-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="53e2f-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53e2f-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="53e2f-137">descripción</span><span class="sxs-lookup"><span data-stu-id="53e2f-137">description</span></span>|<span data-ttu-id="53e2f-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="53e2f-138">String</span></span>|<span data-ttu-id="53e2f-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53e2f-139">The description of the app.</span></span> <span data-ttu-id="53e2f-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53e2f-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="53e2f-141">publicador</span><span class="sxs-lookup"><span data-stu-id="53e2f-141">publisher</span></span>|<span data-ttu-id="53e2f-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="53e2f-142">String</span></span>|<span data-ttu-id="53e2f-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53e2f-143">The publisher of the app.</span></span> <span data-ttu-id="53e2f-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53e2f-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="53e2f-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="53e2f-145">largeIcon</span></span>|[<span data-ttu-id="53e2f-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="53e2f-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="53e2f-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="53e2f-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="53e2f-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53e2f-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="53e2f-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="53e2f-149">createdDateTime</span></span>|<span data-ttu-id="53e2f-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53e2f-150">DateTimeOffset</span></span>|<span data-ttu-id="53e2f-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53e2f-151">The date and time the app was created.</span></span> <span data-ttu-id="53e2f-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53e2f-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="53e2f-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="53e2f-153">lastModifiedDateTime</span></span>|<span data-ttu-id="53e2f-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53e2f-154">DateTimeOffset</span></span>|<span data-ttu-id="53e2f-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53e2f-155">The date and time the app was last modified.</span></span> <span data-ttu-id="53e2f-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53e2f-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="53e2f-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="53e2f-157">isFeatured</span></span>|<span data-ttu-id="53e2f-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="53e2f-158">Boolean</span></span>|<span data-ttu-id="53e2f-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53e2f-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="53e2f-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="53e2f-160">privacyInformationUrl</span></span>|<span data-ttu-id="53e2f-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="53e2f-161">String</span></span>|<span data-ttu-id="53e2f-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="53e2f-162">The privacy statement Url.</span></span> <span data-ttu-id="53e2f-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53e2f-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="53e2f-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="53e2f-164">informationUrl</span></span>|<span data-ttu-id="53e2f-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="53e2f-165">String</span></span>|<span data-ttu-id="53e2f-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="53e2f-166">The more information Url.</span></span> <span data-ttu-id="53e2f-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53e2f-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="53e2f-168">owner</span><span class="sxs-lookup"><span data-stu-id="53e2f-168">owner</span></span>|<span data-ttu-id="53e2f-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="53e2f-169">String</span></span>|<span data-ttu-id="53e2f-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53e2f-170">The owner of the app.</span></span> <span data-ttu-id="53e2f-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53e2f-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="53e2f-172">developer</span><span class="sxs-lookup"><span data-stu-id="53e2f-172">developer</span></span>|<span data-ttu-id="53e2f-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="53e2f-173">String</span></span>|<span data-ttu-id="53e2f-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53e2f-174">The developer of the app.</span></span> <span data-ttu-id="53e2f-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53e2f-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="53e2f-176">notas</span><span class="sxs-lookup"><span data-stu-id="53e2f-176">notes</span></span>|<span data-ttu-id="53e2f-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="53e2f-177">String</span></span>|<span data-ttu-id="53e2f-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="53e2f-178">Notes for the app.</span></span> <span data-ttu-id="53e2f-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="53e2f-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="53e2f-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="53e2f-180">publishingState</span></span>|[<span data-ttu-id="53e2f-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="53e2f-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="53e2f-p114">El estado de publicación de la aplicación. La aplicación no se puede asignar a menos que se publique la aplicación. Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="53e2f-p114">The publishing state for the app. The app cannot be assigned unless the app is published. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md). The possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="53e2f-186">bundleId</span><span class="sxs-lookup"><span data-stu-id="53e2f-186">bundleId</span></span>|<span data-ttu-id="53e2f-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="53e2f-187">String</span></span>|<span data-ttu-id="53e2f-188">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="53e2f-188">The Identity Name.</span></span>|
|<span data-ttu-id="53e2f-189">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="53e2f-189">appStoreUrl</span></span>|<span data-ttu-id="53e2f-190">Cadena</span><span class="sxs-lookup"><span data-stu-id="53e2f-190">String</span></span>|<span data-ttu-id="53e2f-191">Dirección URL de la App Store de Apple</span><span class="sxs-lookup"><span data-stu-id="53e2f-191">The Apple App Store URL</span></span>|
|<span data-ttu-id="53e2f-192">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="53e2f-192">applicableDeviceType</span></span>|[<span data-ttu-id="53e2f-193">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="53e2f-193">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="53e2f-194">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="53e2f-194">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="53e2f-195">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="53e2f-195">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="53e2f-196">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="53e2f-196">iosMinimumOperatingSystem</span></span>](../resources/intune_apps_iosminimumoperatingsystem.md)|<span data-ttu-id="53e2f-197">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="53e2f-197">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="53e2f-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53e2f-198">Response</span></span>
<span data-ttu-id="53e2f-199">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosStoreApp](../resources/intune_apps_iosstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="53e2f-199">If successful, this method returns a `201 Created` response code and a [iosStoreApp](../resources/intune_apps_iosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="53e2f-200">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53e2f-200">Example</span></span>
### <a name="request"></a><span data-ttu-id="53e2f-201">Solicitud</span><span class="sxs-lookup"><span data-stu-id="53e2f-201">Request</span></span>
<span data-ttu-id="53e2f-202">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="53e2f-202">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="53e2f-203">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53e2f-203">Response</span></span>
<span data-ttu-id="53e2f-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="53e2f-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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








