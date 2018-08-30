# <a name="update-iosstoreapp"></a><span data-ttu-id="04ddc-101">Actualizar iosStoreApp</span><span class="sxs-lookup"><span data-stu-id="04ddc-101">Update iosStoreApp</span></span>

> <span data-ttu-id="04ddc-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="04ddc-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="04ddc-103">Actualice las propiedades de un objeto [iosStoreApp](../resources/intune_apps_iosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-103">Update the properties of a [iosStoreApp](../resources/intune_apps_iosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="04ddc-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="04ddc-104">Prerequisites</span></span>
<span data-ttu-id="04ddc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="04ddc-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="04ddc-107">Permission type</span></span>|<span data-ttu-id="04ddc-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="04ddc-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="04ddc-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="04ddc-109">Delegated (work or school account)</span></span>|<span data-ttu-id="04ddc-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="04ddc-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="04ddc-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="04ddc-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="04ddc-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="04ddc-112">Not supported.</span></span>|
|<span data-ttu-id="04ddc-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="04ddc-113">Application</span></span>|<span data-ttu-id="04ddc-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="04ddc-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="04ddc-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="04ddc-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="04ddc-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="04ddc-116">Request headers</span></span>
|<span data-ttu-id="04ddc-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04ddc-117">Header</span></span>|<span data-ttu-id="04ddc-118">Valor</span><span class="sxs-lookup"><span data-stu-id="04ddc-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="04ddc-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="04ddc-119">Authorization</span></span>|<span data-ttu-id="04ddc-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="04ddc-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="04ddc-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="04ddc-121">Accept</span></span>|<span data-ttu-id="04ddc-122">application/json</span><span class="sxs-lookup"><span data-stu-id="04ddc-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="04ddc-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="04ddc-123">Request body</span></span>
<span data-ttu-id="04ddc-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosStoreApp](../resources/intune_apps_iosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-124">In the request body, supply a JSON representation for the [iosStoreApp](../resources/intune_apps_iosstoreapp.md) object.</span></span>

<span data-ttu-id="04ddc-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosStoreApp](../resources/intune_apps_iosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-125">The following table shows the properties that are required when you create the [iosStoreApp](../resources/intune_apps_iosstoreapp.md).</span></span>

|<span data-ttu-id="04ddc-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="04ddc-126">Property</span></span>|<span data-ttu-id="04ddc-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="04ddc-127">Type</span></span>|<span data-ttu-id="04ddc-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="04ddc-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="04ddc-129">id</span><span class="sxs-lookup"><span data-stu-id="04ddc-129">id</span></span>|<span data-ttu-id="04ddc-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="04ddc-130">String</span></span>|<span data-ttu-id="04ddc-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="04ddc-131">Key of the entity.</span></span> <span data-ttu-id="04ddc-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="04ddc-133">displayName</span><span class="sxs-lookup"><span data-stu-id="04ddc-133">displayName</span></span>|<span data-ttu-id="04ddc-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="04ddc-134">String</span></span>|<span data-ttu-id="04ddc-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="04ddc-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="04ddc-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="04ddc-137">description</span><span class="sxs-lookup"><span data-stu-id="04ddc-137">description</span></span>|<span data-ttu-id="04ddc-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="04ddc-138">String</span></span>|<span data-ttu-id="04ddc-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="04ddc-139">The description of the app.</span></span> <span data-ttu-id="04ddc-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="04ddc-141">publisher</span><span class="sxs-lookup"><span data-stu-id="04ddc-141">publisher</span></span>|<span data-ttu-id="04ddc-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="04ddc-142">String</span></span>|<span data-ttu-id="04ddc-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="04ddc-143">The publisher of the app.</span></span> <span data-ttu-id="04ddc-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="04ddc-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="04ddc-145">largeIcon</span></span>|[<span data-ttu-id="04ddc-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="04ddc-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="04ddc-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="04ddc-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="04ddc-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="04ddc-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="04ddc-149">createdDateTime</span></span>|<span data-ttu-id="04ddc-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="04ddc-150">DateTimeOffset</span></span>|<span data-ttu-id="04ddc-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="04ddc-151">The date and time the app was created.</span></span> <span data-ttu-id="04ddc-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="04ddc-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="04ddc-153">lastModifiedDateTime</span></span>|<span data-ttu-id="04ddc-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="04ddc-154">DateTimeOffset</span></span>|<span data-ttu-id="04ddc-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="04ddc-155">The date and time the app was last modified.</span></span> <span data-ttu-id="04ddc-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="04ddc-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="04ddc-157">isFeatured</span></span>|<span data-ttu-id="04ddc-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="04ddc-158">Boolean</span></span>|<span data-ttu-id="04ddc-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="04ddc-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="04ddc-160">privacyInformationUrl</span></span>|<span data-ttu-id="04ddc-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="04ddc-161">String</span></span>|<span data-ttu-id="04ddc-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="04ddc-162">The privacy statement Url.</span></span> <span data-ttu-id="04ddc-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="04ddc-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="04ddc-164">informationUrl</span></span>|<span data-ttu-id="04ddc-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="04ddc-165">String</span></span>|<span data-ttu-id="04ddc-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="04ddc-166">The more information Url.</span></span> <span data-ttu-id="04ddc-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="04ddc-168">owner</span><span class="sxs-lookup"><span data-stu-id="04ddc-168">owner</span></span>|<span data-ttu-id="04ddc-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="04ddc-169">String</span></span>|<span data-ttu-id="04ddc-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="04ddc-170">The owner of the app.</span></span> <span data-ttu-id="04ddc-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="04ddc-172">developer</span><span class="sxs-lookup"><span data-stu-id="04ddc-172">developer</span></span>|<span data-ttu-id="04ddc-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="04ddc-173">String</span></span>|<span data-ttu-id="04ddc-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="04ddc-174">The developer of the app.</span></span> <span data-ttu-id="04ddc-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="04ddc-176">notes</span><span class="sxs-lookup"><span data-stu-id="04ddc-176">notes</span></span>|<span data-ttu-id="04ddc-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="04ddc-177">String</span></span>|<span data-ttu-id="04ddc-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="04ddc-178">Notes for the app.</span></span> <span data-ttu-id="04ddc-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="04ddc-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="04ddc-180">publishingState</span></span>|[<span data-ttu-id="04ddc-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="04ddc-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="04ddc-182">Condición de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="04ddc-182">The publishing state for the app.</span></span> <span data-ttu-id="04ddc-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="04ddc-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="04ddc-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="04ddc-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span> <span data-ttu-id="04ddc-185">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="04ddc-185">The possible values are `notPublished`, `processing`, `published`, , , , , , , , , or .</span></span>|
|<span data-ttu-id="04ddc-186">bundleId</span><span class="sxs-lookup"><span data-stu-id="04ddc-186">bundleId</span></span>|<span data-ttu-id="04ddc-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="04ddc-187">String</span></span>|<span data-ttu-id="04ddc-188">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="04ddc-188">The Identity Name.</span></span>|
|<span data-ttu-id="04ddc-189">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="04ddc-189">appStoreUrl</span></span>|<span data-ttu-id="04ddc-190">Cadena</span><span class="sxs-lookup"><span data-stu-id="04ddc-190">String</span></span>|<span data-ttu-id="04ddc-191">Dirección URL de la App Store de Apple</span><span class="sxs-lookup"><span data-stu-id="04ddc-191">The Apple App Store URL</span></span>|
|<span data-ttu-id="04ddc-192">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="04ddc-192">applicableDeviceType</span></span>|[<span data-ttu-id="04ddc-193">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="04ddc-193">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="04ddc-194">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="04ddc-194">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="04ddc-195">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="04ddc-195">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="04ddc-196">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="04ddc-196">iosMinimumOperatingSystem</span></span>](../resources/intune_apps_iosminimumoperatingsystem.md)|<span data-ttu-id="04ddc-197">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="04ddc-197">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="04ddc-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04ddc-198">Response</span></span>
<span data-ttu-id="04ddc-199">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosStoreApp](../resources/intune_apps_iosstoreapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="04ddc-199">If successful, this method returns a `200 OK` response code and an updated [iosStoreApp](../resources/intune_apps_iosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="04ddc-200">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="04ddc-200">Example</span></span>
### <a name="request"></a><span data-ttu-id="04ddc-201">Solicitud</span><span class="sxs-lookup"><span data-stu-id="04ddc-201">Request</span></span>
<span data-ttu-id="04ddc-202">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="04ddc-202">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1000

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

### <a name="response"></a><span data-ttu-id="04ddc-203">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04ddc-203">Response</span></span>
<span data-ttu-id="04ddc-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="04ddc-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



