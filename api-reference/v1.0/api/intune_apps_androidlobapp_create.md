# <a name="create-androidlobapp"></a><span data-ttu-id="3ea75-101">Crear androidLobApp</span><span class="sxs-lookup"><span data-stu-id="3ea75-101">Create androidLobApp</span></span>

> <span data-ttu-id="3ea75-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3ea75-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3ea75-103">Cree un objeto [androidLobApp](../resources/intune_apps_androidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-103">Create a new [plannerBucket](../resources/intune_apps_androidlobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3ea75-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3ea75-104">Prerequisites</span></span>
<span data-ttu-id="3ea75-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="3ea75-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3ea75-107">Permission type</span></span>|<span data-ttu-id="3ea75-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3ea75-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3ea75-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3ea75-109">Delegated (work or school account)</span></span>|<span data-ttu-id="3ea75-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3ea75-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="3ea75-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3ea75-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3ea75-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3ea75-112">Not supported.</span></span>|
|<span data-ttu-id="3ea75-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3ea75-113">Application</span></span>|<span data-ttu-id="3ea75-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3ea75-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3ea75-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3ea75-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="3ea75-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3ea75-116">Request headers</span></span>
|<span data-ttu-id="3ea75-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ea75-117">Header</span></span>|<span data-ttu-id="3ea75-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3ea75-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3ea75-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="3ea75-119">Authorization</span></span>|<span data-ttu-id="3ea75-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3ea75-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="3ea75-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3ea75-121">Accept</span></span>|<span data-ttu-id="3ea75-122">application/json</span><span class="sxs-lookup"><span data-stu-id="3ea75-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3ea75-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3ea75-123">Request body</span></span>
<span data-ttu-id="3ea75-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidLobApp.</span><span class="sxs-lookup"><span data-stu-id="3ea75-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="3ea75-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidLobApp.</span><span class="sxs-lookup"><span data-stu-id="3ea75-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="3ea75-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3ea75-126">Property</span></span>|<span data-ttu-id="3ea75-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ea75-127">Type</span></span>|<span data-ttu-id="3ea75-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ea75-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3ea75-129">id</span><span class="sxs-lookup"><span data-stu-id="3ea75-129">id</span></span>|<span data-ttu-id="3ea75-130">String</span><span class="sxs-lookup"><span data-stu-id="3ea75-130">String</span></span>|<span data-ttu-id="3ea75-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="3ea75-131">Key of the setting.</span></span> <span data-ttu-id="3ea75-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="3ea75-133">displayName</span><span class="sxs-lookup"><span data-stu-id="3ea75-133">displayName</span></span>|<span data-ttu-id="3ea75-134">String</span><span class="sxs-lookup"><span data-stu-id="3ea75-134">String</span></span>|<span data-ttu-id="3ea75-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="3ea75-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="3ea75-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="3ea75-137">description</span><span class="sxs-lookup"><span data-stu-id="3ea75-137">description</span></span>|<span data-ttu-id="3ea75-138">String</span><span class="sxs-lookup"><span data-stu-id="3ea75-138">String</span></span>|<span data-ttu-id="3ea75-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3ea75-139">The description of the app.</span></span> <span data-ttu-id="3ea75-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="3ea75-141">publicador</span><span class="sxs-lookup"><span data-stu-id="3ea75-141">Publisher</span></span>|<span data-ttu-id="3ea75-142">String</span><span class="sxs-lookup"><span data-stu-id="3ea75-142">String</span></span>|<span data-ttu-id="3ea75-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3ea75-143">The name of the app.</span></span> <span data-ttu-id="3ea75-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="3ea75-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="3ea75-145">largeIcon</span></span>|[<span data-ttu-id="3ea75-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="3ea75-146">mimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="3ea75-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="3ea75-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="3ea75-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="3ea75-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="3ea75-149">createdDateTime</span></span>|<span data-ttu-id="3ea75-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3ea75-150">DateTimeOffset</span></span>|<span data-ttu-id="3ea75-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3ea75-151">The date and time when the page was created.</span></span> <span data-ttu-id="3ea75-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="3ea75-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="3ea75-153">lastModifiedDateTime</span></span>|<span data-ttu-id="3ea75-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3ea75-154">DateTimeOffset</span></span>|<span data-ttu-id="3ea75-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3ea75-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="3ea75-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="3ea75-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="3ea75-157">isFeatured</span></span>|<span data-ttu-id="3ea75-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="3ea75-158">Boolean</span></span>|<span data-ttu-id="3ea75-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="3ea75-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="3ea75-160">privacyInformationUrl</span></span>|<span data-ttu-id="3ea75-161">String</span><span class="sxs-lookup"><span data-stu-id="3ea75-161">String</span></span>|<span data-ttu-id="3ea75-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="3ea75-162">The privacy statement Url.</span></span> <span data-ttu-id="3ea75-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="3ea75-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="3ea75-164">informationUrl</span></span>|<span data-ttu-id="3ea75-165">String</span><span class="sxs-lookup"><span data-stu-id="3ea75-165">String</span></span>|<span data-ttu-id="3ea75-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="3ea75-166">The more information Url.</span></span> <span data-ttu-id="3ea75-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="3ea75-168">owner</span><span class="sxs-lookup"><span data-stu-id="3ea75-168">owner</span></span>|<span data-ttu-id="3ea75-169">String</span><span class="sxs-lookup"><span data-stu-id="3ea75-169">String</span></span>|<span data-ttu-id="3ea75-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3ea75-170">The owner of the timesheet.</span></span> <span data-ttu-id="3ea75-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="3ea75-172">developer</span><span class="sxs-lookup"><span data-stu-id="3ea75-172">developer</span></span>|<span data-ttu-id="3ea75-173">String</span><span class="sxs-lookup"><span data-stu-id="3ea75-173">String</span></span>|<span data-ttu-id="3ea75-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3ea75-174">The name of the app.</span></span> <span data-ttu-id="3ea75-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="3ea75-176">notas</span><span class="sxs-lookup"><span data-stu-id="3ea75-176">Notes</span></span>|<span data-ttu-id="3ea75-177">String</span><span class="sxs-lookup"><span data-stu-id="3ea75-177">String</span></span>|<span data-ttu-id="3ea75-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3ea75-178">Notes for the app.</span></span> <span data-ttu-id="3ea75-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="3ea75-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="3ea75-180">publishingState</span></span>|<span data-ttu-id="3ea75-181">String</span><span class="sxs-lookup"><span data-stu-id="3ea75-181">String</span></span>|<span data-ttu-id="3ea75-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3ea75-182">The publishing state for the app.</span></span> <span data-ttu-id="3ea75-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="3ea75-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="3ea75-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="3ea75-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="3ea75-185">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="3ea75-185">committedContentVersion</span></span>|<span data-ttu-id="3ea75-186">String</span><span class="sxs-lookup"><span data-stu-id="3ea75-186">String</span></span>|<span data-ttu-id="3ea75-187">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="3ea75-187">The internal committed content version.</span></span> <span data-ttu-id="3ea75-188">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-188">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="3ea75-189">fileName</span><span class="sxs-lookup"><span data-stu-id="3ea75-189">fileName</span></span>|<span data-ttu-id="3ea75-190">String</span><span class="sxs-lookup"><span data-stu-id="3ea75-190">String</span></span>|<span data-ttu-id="3ea75-191">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="3ea75-191">The name of the main Lob application file.</span></span> <span data-ttu-id="3ea75-192">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-192">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="3ea75-193">size</span><span class="sxs-lookup"><span data-stu-id="3ea75-193">size</span></span>|<span data-ttu-id="3ea75-194">Int64</span><span class="sxs-lookup"><span data-stu-id="3ea75-194">Int64</span></span>|<span data-ttu-id="3ea75-195">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="3ea75-195">The total size, including all uploaded files.</span></span> <span data-ttu-id="3ea75-196">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="3ea75-196">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="3ea75-197">packageId</span><span class="sxs-lookup"><span data-stu-id="3ea75-197">packageId</span></span>|<span data-ttu-id="3ea75-198">String</span><span class="sxs-lookup"><span data-stu-id="3ea75-198">String</span></span>|<span data-ttu-id="3ea75-199">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="3ea75-199">The package identifier.</span></span>|
|<span data-ttu-id="3ea75-200">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3ea75-200">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="3ea75-201">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3ea75-201">androidMinimumOperatingSystem</span></span>](../resources/intune_apps_androidminimumoperatingsystem.md)|<span data-ttu-id="3ea75-202">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="3ea75-202">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="3ea75-203">versionName</span><span class="sxs-lookup"><span data-stu-id="3ea75-203">versionName</span></span>|<span data-ttu-id="3ea75-204">String</span><span class="sxs-lookup"><span data-stu-id="3ea75-204">String</span></span>|<span data-ttu-id="3ea75-205">El nombre de la versión de la aplicación de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="3ea75-205">The version name of Android Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="3ea75-206">versionCode</span><span class="sxs-lookup"><span data-stu-id="3ea75-206">versionCode</span></span>|<span data-ttu-id="3ea75-207">String</span><span class="sxs-lookup"><span data-stu-id="3ea75-207">String</span></span>|<span data-ttu-id="3ea75-208">El código de versión de la aplicación de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="3ea75-208">The version code of Android Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="3ea75-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3ea75-209">Response</span></span>
<span data-ttu-id="3ea75-210">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidLobApp](../resources/intune_apps_androidlobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ea75-210">If successful, this method returns a `201 Created` response code and a [ListItemVersion](../resources/intune_apps_androidlobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3ea75-211">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3ea75-211">Example</span></span>
### <a name="request"></a><span data-ttu-id="3ea75-212">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3ea75-212">Request</span></span>
<span data-ttu-id="3ea75-213">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ea75-213">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1139

{
  "@odata.type": "#microsoft.graph.androidLobApp",
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

### <a name="response"></a><span data-ttu-id="3ea75-214">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3ea75-214">Response</span></span>
<span data-ttu-id="3ea75-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3ea75-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



