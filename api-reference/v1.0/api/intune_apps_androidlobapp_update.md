# <a name="update-androidlobapp"></a><span data-ttu-id="77405-101">Actualizar androidLobApp</span><span class="sxs-lookup"><span data-stu-id="77405-101">Update androidLobApp</span></span>

> <span data-ttu-id="77405-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="77405-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="77405-103">Actualice las propiedades de un objeto [androidLobApp](../resources/intune_apps_androidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-103">Update the properties of a [androidLobApp](../resources/intune_apps_androidlobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="77405-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="77405-104">Prerequisites</span></span>
<span data-ttu-id="77405-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="77405-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="77405-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="77405-107">Permission type</span></span>|<span data-ttu-id="77405-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="77405-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="77405-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="77405-109">Delegated (work or school account)</span></span>|<span data-ttu-id="77405-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="77405-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="77405-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="77405-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="77405-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="77405-112">Not supported.</span></span>|
|<span data-ttu-id="77405-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="77405-113">Application</span></span>|<span data-ttu-id="77405-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="77405-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="77405-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="77405-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="77405-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="77405-116">Request headers</span></span>
|<span data-ttu-id="77405-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77405-117">Header</span></span>|<span data-ttu-id="77405-118">Valor</span><span class="sxs-lookup"><span data-stu-id="77405-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="77405-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="77405-119">Authorization</span></span>|<span data-ttu-id="77405-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="77405-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="77405-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="77405-121">Accept</span></span>|<span data-ttu-id="77405-122">application/json</span><span class="sxs-lookup"><span data-stu-id="77405-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="77405-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="77405-123">Request body</span></span>
<span data-ttu-id="77405-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidLobApp](../resources/intune_apps_androidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-124">In the request body, supply a JSON representation for the [androidLobApp](../resources/intune_apps_androidlobapp.md) object.</span></span>

<span data-ttu-id="77405-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidLobApp](../resources/intune_apps_androidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-125">The following table shows the properties that are required when you create the [androidLobApp](../resources/intune_apps_androidlobapp.md).</span></span>

|<span data-ttu-id="77405-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="77405-126">Property</span></span>|<span data-ttu-id="77405-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="77405-127">Type</span></span>|<span data-ttu-id="77405-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="77405-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="77405-129">id.</span><span class="sxs-lookup"><span data-stu-id="77405-129">id</span></span>|<span data-ttu-id="77405-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="77405-130">String</span></span>|<span data-ttu-id="77405-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="77405-131">Key of the entity.</span></span> <span data-ttu-id="77405-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="77405-133">displayName</span><span class="sxs-lookup"><span data-stu-id="77405-133">displayName</span></span>|<span data-ttu-id="77405-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="77405-134">String</span></span>|<span data-ttu-id="77405-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="77405-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="77405-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="77405-137">descripción</span><span class="sxs-lookup"><span data-stu-id="77405-137">description</span></span>|<span data-ttu-id="77405-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="77405-138">String</span></span>|<span data-ttu-id="77405-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="77405-139">The description of the app.</span></span> <span data-ttu-id="77405-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="77405-141">publicador</span><span class="sxs-lookup"><span data-stu-id="77405-141">publisher</span></span>|<span data-ttu-id="77405-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="77405-142">String</span></span>|<span data-ttu-id="77405-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="77405-143">The publisher of the app.</span></span> <span data-ttu-id="77405-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="77405-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="77405-145">largeIcon</span></span>|[<span data-ttu-id="77405-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="77405-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="77405-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="77405-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="77405-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="77405-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="77405-149">createdDateTime</span></span>|<span data-ttu-id="77405-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="77405-150">DateTimeOffset</span></span>|<span data-ttu-id="77405-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="77405-151">The date and time the app was created.</span></span> <span data-ttu-id="77405-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="77405-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="77405-153">lastModifiedDateTime</span></span>|<span data-ttu-id="77405-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="77405-154">DateTimeOffset</span></span>|<span data-ttu-id="77405-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="77405-155">The date and time the app was last modified.</span></span> <span data-ttu-id="77405-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="77405-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="77405-157">isFeatured</span></span>|<span data-ttu-id="77405-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="77405-158">Boolean</span></span>|<span data-ttu-id="77405-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="77405-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="77405-160">privacyInformationUrl</span></span>|<span data-ttu-id="77405-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="77405-161">String</span></span>|<span data-ttu-id="77405-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="77405-162">The privacy statement Url.</span></span> <span data-ttu-id="77405-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="77405-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="77405-164">informationUrl</span></span>|<span data-ttu-id="77405-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="77405-165">String</span></span>|<span data-ttu-id="77405-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="77405-166">The more information Url.</span></span> <span data-ttu-id="77405-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="77405-168">propietario/a</span><span class="sxs-lookup"><span data-stu-id="77405-168">owner</span></span>|<span data-ttu-id="77405-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="77405-169">String</span></span>|<span data-ttu-id="77405-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="77405-170">The owner of the app.</span></span> <span data-ttu-id="77405-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="77405-172">programador</span><span class="sxs-lookup"><span data-stu-id="77405-172">developer</span></span>|<span data-ttu-id="77405-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="77405-173">String</span></span>|<span data-ttu-id="77405-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="77405-174">The developer of the app.</span></span> <span data-ttu-id="77405-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="77405-176">notas</span><span class="sxs-lookup"><span data-stu-id="77405-176">notes</span></span>|<span data-ttu-id="77405-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="77405-177">String</span></span>|<span data-ttu-id="77405-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="77405-178">Notes for the app.</span></span> <span data-ttu-id="77405-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="77405-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="77405-180">publishingState</span></span>|[<span data-ttu-id="77405-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="77405-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="77405-p114">El estado de publicación para la aplicación. La aplicación no se puede asignar a menos que se publique la aplicación. Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing`, `published`.</span><span class="sxs-lookup"><span data-stu-id="77405-p114">The publishing state for the app. The app cannot be assigned unless the app is published. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md). The possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="77405-186">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="77405-186">committedContentVersion</span></span>|<span data-ttu-id="77405-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="77405-187">String</span></span>|<span data-ttu-id="77405-188">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="77405-188">The internal committed content version.</span></span> <span data-ttu-id="77405-189">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-189">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="77405-190">fileName</span><span class="sxs-lookup"><span data-stu-id="77405-190">fileName</span></span>|<span data-ttu-id="77405-191">Cadena</span><span class="sxs-lookup"><span data-stu-id="77405-191">String</span></span>|<span data-ttu-id="77405-192">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="77405-192">The name of the main Lob application file.</span></span> <span data-ttu-id="77405-193">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-193">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="77405-194">tamaño</span><span class="sxs-lookup"><span data-stu-id="77405-194">size</span></span>|<span data-ttu-id="77405-195">Int64</span><span class="sxs-lookup"><span data-stu-id="77405-195">Int64</span></span>|<span data-ttu-id="77405-196">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="77405-196">The total size, including all uploaded files.</span></span> <span data-ttu-id="77405-197">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="77405-197">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="77405-198">packageId</span><span class="sxs-lookup"><span data-stu-id="77405-198">packageId</span></span>|<span data-ttu-id="77405-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="77405-199">String</span></span>|<span data-ttu-id="77405-200">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="77405-200">The package identifier.</span></span>|
|<span data-ttu-id="77405-201">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="77405-201">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="77405-202">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="77405-202">androidMinimumOperatingSystem</span></span>](../resources/intune_apps_androidminimumoperatingsystem.md)|<span data-ttu-id="77405-203">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="77405-203">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="77405-204">versionName</span><span class="sxs-lookup"><span data-stu-id="77405-204">versionName</span></span>|<span data-ttu-id="77405-205">Cadena</span><span class="sxs-lookup"><span data-stu-id="77405-205">String</span></span>|<span data-ttu-id="77405-206">El nombre de la versión de la aplicación de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="77405-206">The version name of Android Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="77405-207">versionCode</span><span class="sxs-lookup"><span data-stu-id="77405-207">versionCode</span></span>|<span data-ttu-id="77405-208">Cadena</span><span class="sxs-lookup"><span data-stu-id="77405-208">String</span></span>|<span data-ttu-id="77405-209">El código de versión de la aplicación de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="77405-209">The version code of Android Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="77405-210">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77405-210">Response</span></span>
<span data-ttu-id="77405-211">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidLobApp](../resources/intune_apps_androidlobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77405-211">If successful, this method returns a `200 OK` response code and an updated [androidLobApp](../resources/intune_apps_androidlobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="77405-212">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="77405-212">Example</span></span>
### <a name="request"></a><span data-ttu-id="77405-213">Solicitud</span><span class="sxs-lookup"><span data-stu-id="77405-213">Request</span></span>
<span data-ttu-id="77405-214">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="77405-214">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1087

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
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "packageId": "Package Id value",
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
  },
  "versionName": "Version Name value",
  "versionCode": "Version Code value"
}
```

### <a name="response"></a><span data-ttu-id="77405-215">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77405-215">Response</span></span>
<span data-ttu-id="77405-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="77405-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1247

{
  "@odata.type": "#microsoft.graph.androidLobApp",
  "id": "4b9a27d0-27d0-4b9a-d027-9a4bd0279a4b",
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
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "packageId": "Package Id value",
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
  },
  "versionName": "Version Name value",
  "versionCode": "Version Code value"
}
```








