# <a name="create-androidstoreapp"></a><span data-ttu-id="8463a-101">Crear androidStoreApp</span><span class="sxs-lookup"><span data-stu-id="8463a-101">Create androidStoreApp</span></span>

> <span data-ttu-id="8463a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8463a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8463a-103">Cree un objeto [androidStoreApp](../resources/intune_apps_androidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="8463a-103">Create a new [androidStoreApp](../resources/intune_apps_androidstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8463a-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8463a-104">Prerequisites</span></span>
<span data-ttu-id="8463a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8463a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8463a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8463a-107">Permission type</span></span>|<span data-ttu-id="8463a-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8463a-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8463a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8463a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="8463a-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8463a-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="8463a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8463a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8463a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8463a-112">Not supported.</span></span>|
|<span data-ttu-id="8463a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8463a-113">Application</span></span>|<span data-ttu-id="8463a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8463a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8463a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8463a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="8463a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8463a-116">Request headers</span></span>
|<span data-ttu-id="8463a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8463a-117">Header</span></span>|<span data-ttu-id="8463a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8463a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8463a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="8463a-119">Authorization</span></span>|<span data-ttu-id="8463a-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8463a-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8463a-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8463a-121">Accept</span></span>|<span data-ttu-id="8463a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="8463a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8463a-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8463a-123">Request body</span></span>
<span data-ttu-id="8463a-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidStoreApp.</span><span class="sxs-lookup"><span data-stu-id="8463a-124">In the request body, supply a JSON representation for the androidStoreApp object.</span></span>

<span data-ttu-id="8463a-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidStoreApp.</span><span class="sxs-lookup"><span data-stu-id="8463a-125">The following table shows the properties that are required when you create the androidStoreApp.</span></span>

|<span data-ttu-id="8463a-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8463a-126">Property</span></span>|<span data-ttu-id="8463a-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="8463a-127">Type</span></span>|<span data-ttu-id="8463a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="8463a-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8463a-129">id</span><span class="sxs-lookup"><span data-stu-id="8463a-129">id</span></span>|<span data-ttu-id="8463a-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="8463a-130">String</span></span>|<span data-ttu-id="8463a-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8463a-131">Key of the entity.</span></span> <span data-ttu-id="8463a-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8463a-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8463a-133">displayName</span><span class="sxs-lookup"><span data-stu-id="8463a-133">displayName</span></span>|<span data-ttu-id="8463a-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="8463a-134">String</span></span>|<span data-ttu-id="8463a-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="8463a-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="8463a-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8463a-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8463a-137">description</span><span class="sxs-lookup"><span data-stu-id="8463a-137">description</span></span>|<span data-ttu-id="8463a-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="8463a-138">String</span></span>|<span data-ttu-id="8463a-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8463a-139">The description of the app.</span></span> <span data-ttu-id="8463a-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8463a-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8463a-141">publisher</span><span class="sxs-lookup"><span data-stu-id="8463a-141">publisher</span></span>|<span data-ttu-id="8463a-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="8463a-142">String</span></span>|<span data-ttu-id="8463a-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8463a-143">The publisher of the app.</span></span> <span data-ttu-id="8463a-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8463a-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8463a-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="8463a-145">largeIcon</span></span>|[<span data-ttu-id="8463a-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="8463a-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="8463a-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="8463a-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="8463a-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8463a-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8463a-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8463a-149">createdDateTime</span></span>|<span data-ttu-id="8463a-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8463a-150">DateTimeOffset</span></span>|<span data-ttu-id="8463a-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8463a-151">The date and time the app was created.</span></span> <span data-ttu-id="8463a-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8463a-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8463a-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8463a-153">lastModifiedDateTime</span></span>|<span data-ttu-id="8463a-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8463a-154">DateTimeOffset</span></span>|<span data-ttu-id="8463a-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8463a-155">The date and time the app was last modified.</span></span> <span data-ttu-id="8463a-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8463a-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8463a-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="8463a-157">isFeatured</span></span>|<span data-ttu-id="8463a-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="8463a-158">Boolean</span></span>|<span data-ttu-id="8463a-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8463a-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8463a-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="8463a-160">privacyInformationUrl</span></span>|<span data-ttu-id="8463a-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="8463a-161">String</span></span>|<span data-ttu-id="8463a-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="8463a-162">The privacy statement Url.</span></span> <span data-ttu-id="8463a-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8463a-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8463a-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="8463a-164">informationUrl</span></span>|<span data-ttu-id="8463a-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="8463a-165">String</span></span>|<span data-ttu-id="8463a-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8463a-166">The more information Url.</span></span> <span data-ttu-id="8463a-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8463a-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8463a-168">owner</span><span class="sxs-lookup"><span data-stu-id="8463a-168">owner</span></span>|<span data-ttu-id="8463a-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="8463a-169">String</span></span>|<span data-ttu-id="8463a-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8463a-170">The owner of the app.</span></span> <span data-ttu-id="8463a-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8463a-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8463a-172">developer</span><span class="sxs-lookup"><span data-stu-id="8463a-172">developer</span></span>|<span data-ttu-id="8463a-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="8463a-173">String</span></span>|<span data-ttu-id="8463a-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8463a-174">The developer of the app.</span></span> <span data-ttu-id="8463a-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8463a-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8463a-176">notes</span><span class="sxs-lookup"><span data-stu-id="8463a-176">notes</span></span>|<span data-ttu-id="8463a-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="8463a-177">String</span></span>|<span data-ttu-id="8463a-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8463a-178">Notes for the app.</span></span> <span data-ttu-id="8463a-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8463a-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8463a-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="8463a-180">publishingState</span></span>|[<span data-ttu-id="8463a-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="8463a-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="8463a-p114">El estado de publicación para la aplicación. La aplicación no se puede asignar a menos que se publique la aplicación. Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing`, `published`.</span><span class="sxs-lookup"><span data-stu-id="8463a-p114">The publishing state for the app. The app cannot be assigned unless the app is published. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md). The possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="8463a-186">packageId</span><span class="sxs-lookup"><span data-stu-id="8463a-186">packageId</span></span>|<span data-ttu-id="8463a-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="8463a-187">String</span></span>|<span data-ttu-id="8463a-188">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="8463a-188">The package identifier.</span></span>|
|<span data-ttu-id="8463a-189">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="8463a-189">appStoreUrl</span></span>|<span data-ttu-id="8463a-190">Cadena</span><span class="sxs-lookup"><span data-stu-id="8463a-190">String</span></span>|<span data-ttu-id="8463a-191">La dirección URL de la tienda de aplicaciones de Android.</span><span class="sxs-lookup"><span data-stu-id="8463a-191">The Android app store URL.</span></span>|
|<span data-ttu-id="8463a-192">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="8463a-192">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="8463a-193">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="8463a-193">androidMinimumOperatingSystem</span></span>](../resources/intune_apps_androidminimumoperatingsystem.md)|<span data-ttu-id="8463a-194">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="8463a-194">The value for the minimum applicable operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="8463a-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8463a-195">Response</span></span>
<span data-ttu-id="8463a-196">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidStoreApp](../resources/intune_apps_androidstoreapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8463a-196">If successful, this method returns a `201 Created` response code and a [androidStoreApp](../resources/intune_apps_androidstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8463a-197">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8463a-197">Example</span></span>
### <a name="request"></a><span data-ttu-id="8463a-198">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8463a-198">Request</span></span>
<span data-ttu-id="8463a-199">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8463a-199">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1002

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

### <a name="response"></a><span data-ttu-id="8463a-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8463a-200">Response</span></span>
<span data-ttu-id="8463a-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8463a-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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








