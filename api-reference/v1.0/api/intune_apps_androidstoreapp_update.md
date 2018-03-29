# <a name="update-androidstoreapp"></a><span data-ttu-id="75deb-101">Actualizar androidStoreApp</span><span class="sxs-lookup"><span data-stu-id="75deb-101">Update androidStoreApp</span></span>

> <span data-ttu-id="75deb-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="75deb-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="75deb-103">Actualice las propiedades de un objeto [androidStoreApp](../resources/intune_apps_androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-103">Update the properties of a [calendar](../resources/intune_apps_androidstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="75deb-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="75deb-104">Prerequisites</span></span>
<span data-ttu-id="75deb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="75deb-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="75deb-107">Permission type</span></span>|<span data-ttu-id="75deb-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="75deb-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="75deb-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="75deb-109">Delegated (work or school account)</span></span>|<span data-ttu-id="75deb-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="75deb-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="75deb-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="75deb-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="75deb-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="75deb-112">Not supported.</span></span>|
|<span data-ttu-id="75deb-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="75deb-113">Application</span></span>|<span data-ttu-id="75deb-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="75deb-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="75deb-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="75deb-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="75deb-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="75deb-116">Request headers</span></span>
|<span data-ttu-id="75deb-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75deb-117">Header</span></span>|<span data-ttu-id="75deb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="75deb-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="75deb-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="75deb-119">Authorization</span></span>|<span data-ttu-id="75deb-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="75deb-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="75deb-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="75deb-121">Accept</span></span>|<span data-ttu-id="75deb-122">application/json</span><span class="sxs-lookup"><span data-stu-id="75deb-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="75deb-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="75deb-123">Request body</span></span>
<span data-ttu-id="75deb-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidStoreApp](../resources/intune_apps_androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_apps_androidstoreapp.md) object.</span></span>

<span data-ttu-id="75deb-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidStoreApp](../resources/intune_apps_androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="75deb-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="75deb-126">Property</span></span>|<span data-ttu-id="75deb-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="75deb-127">Type</span></span>|<span data-ttu-id="75deb-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="75deb-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="75deb-129">id</span><span class="sxs-lookup"><span data-stu-id="75deb-129">id</span></span>|<span data-ttu-id="75deb-130">String</span><span class="sxs-lookup"><span data-stu-id="75deb-130">String</span></span>|<span data-ttu-id="75deb-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="75deb-131">Key of the setting.</span></span> <span data-ttu-id="75deb-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="75deb-133">displayName</span><span class="sxs-lookup"><span data-stu-id="75deb-133">displayName</span></span>|<span data-ttu-id="75deb-134">String</span><span class="sxs-lookup"><span data-stu-id="75deb-134">String</span></span>|<span data-ttu-id="75deb-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="75deb-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="75deb-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="75deb-137">description</span><span class="sxs-lookup"><span data-stu-id="75deb-137">description</span></span>|<span data-ttu-id="75deb-138">String</span><span class="sxs-lookup"><span data-stu-id="75deb-138">String</span></span>|<span data-ttu-id="75deb-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75deb-139">The description of the app.</span></span> <span data-ttu-id="75deb-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="75deb-141">publicador</span><span class="sxs-lookup"><span data-stu-id="75deb-141">Publisher</span></span>|<span data-ttu-id="75deb-142">String</span><span class="sxs-lookup"><span data-stu-id="75deb-142">String</span></span>|<span data-ttu-id="75deb-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75deb-143">The name of the app.</span></span> <span data-ttu-id="75deb-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="75deb-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="75deb-145">largeIcon</span></span>|[<span data-ttu-id="75deb-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="75deb-146">mimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="75deb-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="75deb-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="75deb-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="75deb-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="75deb-149">createdDateTime</span></span>|<span data-ttu-id="75deb-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="75deb-150">DateTimeOffset</span></span>|<span data-ttu-id="75deb-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75deb-151">The date and time when the page was created.</span></span> <span data-ttu-id="75deb-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="75deb-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="75deb-153">lastModifiedDateTime</span></span>|<span data-ttu-id="75deb-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="75deb-154">DateTimeOffset</span></span>|<span data-ttu-id="75deb-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75deb-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="75deb-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="75deb-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="75deb-157">isFeatured</span></span>|<span data-ttu-id="75deb-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="75deb-158">Boolean</span></span>|<span data-ttu-id="75deb-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="75deb-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="75deb-160">privacyInformationUrl</span></span>|<span data-ttu-id="75deb-161">String</span><span class="sxs-lookup"><span data-stu-id="75deb-161">String</span></span>|<span data-ttu-id="75deb-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="75deb-162">The privacy statement Url.</span></span> <span data-ttu-id="75deb-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="75deb-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="75deb-164">informationUrl</span></span>|<span data-ttu-id="75deb-165">String</span><span class="sxs-lookup"><span data-stu-id="75deb-165">String</span></span>|<span data-ttu-id="75deb-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="75deb-166">The more information Url.</span></span> <span data-ttu-id="75deb-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="75deb-168">owner</span><span class="sxs-lookup"><span data-stu-id="75deb-168">owner</span></span>|<span data-ttu-id="75deb-169">String</span><span class="sxs-lookup"><span data-stu-id="75deb-169">String</span></span>|<span data-ttu-id="75deb-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75deb-170">The owner of the timesheet.</span></span> <span data-ttu-id="75deb-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="75deb-172">developer</span><span class="sxs-lookup"><span data-stu-id="75deb-172">developer</span></span>|<span data-ttu-id="75deb-173">String</span><span class="sxs-lookup"><span data-stu-id="75deb-173">String</span></span>|<span data-ttu-id="75deb-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75deb-174">The name of the app.</span></span> <span data-ttu-id="75deb-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="75deb-176">notas</span><span class="sxs-lookup"><span data-stu-id="75deb-176">Notes</span></span>|<span data-ttu-id="75deb-177">String</span><span class="sxs-lookup"><span data-stu-id="75deb-177">String</span></span>|<span data-ttu-id="75deb-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75deb-178">Notes for the app.</span></span> <span data-ttu-id="75deb-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="75deb-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="75deb-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="75deb-180">publishingState</span></span>|<span data-ttu-id="75deb-181">String</span><span class="sxs-lookup"><span data-stu-id="75deb-181">String</span></span>|<span data-ttu-id="75deb-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75deb-182">The publishing state for the app.</span></span> <span data-ttu-id="75deb-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="75deb-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="75deb-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="75deb-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="75deb-185">packageId</span><span class="sxs-lookup"><span data-stu-id="75deb-185">packageId</span></span>|<span data-ttu-id="75deb-186">String</span><span class="sxs-lookup"><span data-stu-id="75deb-186">String</span></span>|<span data-ttu-id="75deb-187">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="75deb-187">The package identifier.</span></span>|
|<span data-ttu-id="75deb-188">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="75deb-188">appStoreUrl</span></span>|<span data-ttu-id="75deb-189">String</span><span class="sxs-lookup"><span data-stu-id="75deb-189">String</span></span>|<span data-ttu-id="75deb-190">La dirección URL de la tienda de aplicaciones de Android.</span><span class="sxs-lookup"><span data-stu-id="75deb-190">The Android app store URL.</span></span>|
|<span data-ttu-id="75deb-191">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="75deb-191">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="75deb-192">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="75deb-192">androidMinimumOperatingSystem</span></span>](../resources/intune_apps_androidminimumoperatingsystem.md)|<span data-ttu-id="75deb-193">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="75deb-193">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="75deb-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="75deb-194">Response</span></span>
<span data-ttu-id="75deb-195">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidStoreApp](../resources/intune_apps_androidstoreapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="75deb-195">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_apps_androidstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="75deb-196">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="75deb-196">Example</span></span>
### <a name="request"></a><span data-ttu-id="75deb-197">Solicitud</span><span class="sxs-lookup"><span data-stu-id="75deb-197">Request</span></span>
<span data-ttu-id="75deb-198">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="75deb-198">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 948

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

### <a name="response"></a><span data-ttu-id="75deb-199">Respuesta</span><span class="sxs-lookup"><span data-stu-id="75deb-199">Response</span></span>
<span data-ttu-id="75deb-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="75deb-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1110

{
  "@odata.type": "#microsoft.graph.androidStoreApp",
  "id": "1f2b7654-7654-1f2b-5476-2b1f54762b1f",
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



