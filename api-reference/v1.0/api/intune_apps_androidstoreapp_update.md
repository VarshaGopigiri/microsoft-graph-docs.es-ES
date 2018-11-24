# <a name="update-androidstoreapp"></a><span data-ttu-id="e805a-101">Actualizar androidStoreApp</span><span class="sxs-lookup"><span data-stu-id="e805a-101">Update androidStoreApp</span></span>

> <span data-ttu-id="e805a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e805a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e805a-103">Actualice las propiedades de un objeto [androidStoreApp](../resources/intune_apps_androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-103">Update the properties of a [androidStoreApp](../resources/intune_apps_androidstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e805a-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e805a-104">Prerequisites</span></span>
<span data-ttu-id="e805a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e805a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e805a-107">Permission type</span></span>|<span data-ttu-id="e805a-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e805a-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e805a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e805a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="e805a-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e805a-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="e805a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e805a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e805a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e805a-112">Not supported.</span></span>|
|<span data-ttu-id="e805a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e805a-113">Application</span></span>|<span data-ttu-id="e805a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e805a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e805a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e805a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="e805a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e805a-116">Request headers</span></span>
|<span data-ttu-id="e805a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e805a-117">Header</span></span>|<span data-ttu-id="e805a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e805a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e805a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="e805a-119">Authorization</span></span>|<span data-ttu-id="e805a-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e805a-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e805a-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e805a-121">Accept</span></span>|<span data-ttu-id="e805a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="e805a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e805a-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e805a-123">Request body</span></span>
<span data-ttu-id="e805a-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidStoreApp](../resources/intune_apps_androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-124">In the request body, supply a JSON representation for the [androidStoreApp](../resources/intune_apps_androidstoreapp.md) object.</span></span>

<span data-ttu-id="e805a-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidStoreApp](../resources/intune_apps_androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-125">The following table shows the properties that are required when you create the [androidStoreApp](../resources/intune_apps_androidstoreapp.md).</span></span>

|<span data-ttu-id="e805a-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e805a-126">Property</span></span>|<span data-ttu-id="e805a-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="e805a-127">Type</span></span>|<span data-ttu-id="e805a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="e805a-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e805a-129">id</span><span class="sxs-lookup"><span data-stu-id="e805a-129">id</span></span>|<span data-ttu-id="e805a-130">String</span><span class="sxs-lookup"><span data-stu-id="e805a-130">String</span></span>|<span data-ttu-id="e805a-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e805a-131">Key of the entity.</span></span> <span data-ttu-id="e805a-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e805a-133">displayName</span><span class="sxs-lookup"><span data-stu-id="e805a-133">displayName</span></span>|<span data-ttu-id="e805a-134">String</span><span class="sxs-lookup"><span data-stu-id="e805a-134">String</span></span>|<span data-ttu-id="e805a-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="e805a-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="e805a-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e805a-137">description</span><span class="sxs-lookup"><span data-stu-id="e805a-137">description</span></span>|<span data-ttu-id="e805a-138">String</span><span class="sxs-lookup"><span data-stu-id="e805a-138">String</span></span>|<span data-ttu-id="e805a-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e805a-139">The description of the app.</span></span> <span data-ttu-id="e805a-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e805a-141">publicador</span><span class="sxs-lookup"><span data-stu-id="e805a-141">publisher</span></span>|<span data-ttu-id="e805a-142">String</span><span class="sxs-lookup"><span data-stu-id="e805a-142">String</span></span>|<span data-ttu-id="e805a-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e805a-143">The publisher of the app.</span></span> <span data-ttu-id="e805a-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e805a-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="e805a-145">largeIcon</span></span>|[<span data-ttu-id="e805a-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="e805a-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="e805a-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="e805a-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="e805a-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e805a-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e805a-149">createdDateTime</span></span>|<span data-ttu-id="e805a-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e805a-150">DateTimeOffset</span></span>|<span data-ttu-id="e805a-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e805a-151">The date and time the app was created.</span></span> <span data-ttu-id="e805a-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e805a-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e805a-153">lastModifiedDateTime</span></span>|<span data-ttu-id="e805a-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e805a-154">DateTimeOffset</span></span>|<span data-ttu-id="e805a-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e805a-155">The date and time the app was last modified.</span></span> <span data-ttu-id="e805a-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e805a-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="e805a-157">isFeatured</span></span>|<span data-ttu-id="e805a-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="e805a-158">Boolean</span></span>|<span data-ttu-id="e805a-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e805a-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="e805a-160">privacyInformationUrl</span></span>|<span data-ttu-id="e805a-161">String</span><span class="sxs-lookup"><span data-stu-id="e805a-161">String</span></span>|<span data-ttu-id="e805a-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="e805a-162">The privacy statement Url.</span></span> <span data-ttu-id="e805a-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e805a-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="e805a-164">informationUrl</span></span>|<span data-ttu-id="e805a-165">String</span><span class="sxs-lookup"><span data-stu-id="e805a-165">String</span></span>|<span data-ttu-id="e805a-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="e805a-166">The more information Url.</span></span> <span data-ttu-id="e805a-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e805a-168">owner</span><span class="sxs-lookup"><span data-stu-id="e805a-168">owner</span></span>|<span data-ttu-id="e805a-169">String</span><span class="sxs-lookup"><span data-stu-id="e805a-169">String</span></span>|<span data-ttu-id="e805a-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e805a-170">The owner of the app.</span></span> <span data-ttu-id="e805a-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e805a-172">developer</span><span class="sxs-lookup"><span data-stu-id="e805a-172">developer</span></span>|<span data-ttu-id="e805a-173">String</span><span class="sxs-lookup"><span data-stu-id="e805a-173">String</span></span>|<span data-ttu-id="e805a-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e805a-174">The developer of the app.</span></span> <span data-ttu-id="e805a-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e805a-176">notas</span><span class="sxs-lookup"><span data-stu-id="e805a-176">notes</span></span>|<span data-ttu-id="e805a-177">String</span><span class="sxs-lookup"><span data-stu-id="e805a-177">String</span></span>|<span data-ttu-id="e805a-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e805a-178">Notes for the app.</span></span> <span data-ttu-id="e805a-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e805a-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="e805a-180">publishingState</span></span>|[<span data-ttu-id="e805a-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="e805a-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="e805a-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e805a-182">The publishing state for the app.</span></span> <span data-ttu-id="e805a-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="e805a-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="e805a-184">Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e805a-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md).</span></span> <span data-ttu-id="e805a-185">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="e805a-185">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="e805a-186">packageId</span><span class="sxs-lookup"><span data-stu-id="e805a-186">packageId</span></span>|<span data-ttu-id="e805a-187">String</span><span class="sxs-lookup"><span data-stu-id="e805a-187">String</span></span>|<span data-ttu-id="e805a-188">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="e805a-188">The package identifier.</span></span>|
|<span data-ttu-id="e805a-189">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="e805a-189">appStoreUrl</span></span>|<span data-ttu-id="e805a-190">String</span><span class="sxs-lookup"><span data-stu-id="e805a-190">String</span></span>|<span data-ttu-id="e805a-191">La dirección URL de la tienda de aplicaciones de Android.</span><span class="sxs-lookup"><span data-stu-id="e805a-191">The Android app store URL.</span></span>|
|<span data-ttu-id="e805a-192">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e805a-192">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="e805a-193">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e805a-193">androidMinimumOperatingSystem</span></span>](../resources/intune_apps_androidminimumoperatingsystem.md)|<span data-ttu-id="e805a-194">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="e805a-194">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="e805a-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e805a-195">Response</span></span>
<span data-ttu-id="e805a-196">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidStoreApp](../resources/intune_apps_androidstoreapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e805a-196">If successful, this method returns a `200 OK` response code and an updated [androidStoreApp](../resources/intune_apps_androidstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e805a-197">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e805a-197">Example</span></span>
### <a name="request"></a><span data-ttu-id="e805a-198">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e805a-198">Request</span></span>
<span data-ttu-id="e805a-199">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e805a-199">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 938

{
  "@odata.type": "#microsoft.graph.androidStoreApp",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
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

### <a name="response"></a><span data-ttu-id="e805a-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e805a-200">Response</span></span>
<span data-ttu-id="e805a-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e805a-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



