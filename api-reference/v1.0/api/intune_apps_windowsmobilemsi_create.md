# <a name="create-windowsmobilemsi"></a><span data-ttu-id="f41fa-101">Crear windowsMobileMSI</span><span class="sxs-lookup"><span data-stu-id="f41fa-101">Create windowsMobileMSI</span></span>

> <span data-ttu-id="f41fa-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f41fa-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f41fa-103">Crear un objeto [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-103">Create a new [plannerBucket](../resources/intune_apps_windowsmobilemsi.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f41fa-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f41fa-104">Prerequisites</span></span>
<span data-ttu-id="f41fa-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f41fa-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f41fa-107">Permission type</span></span>|<span data-ttu-id="f41fa-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f41fa-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f41fa-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f41fa-109">Delegated (work or school account)</span></span>|<span data-ttu-id="f41fa-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f41fa-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f41fa-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f41fa-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f41fa-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f41fa-112">Not supported.</span></span>|
|<span data-ttu-id="f41fa-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f41fa-113">Application</span></span>|<span data-ttu-id="f41fa-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="f41fa-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f41fa-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f41fa-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="f41fa-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f41fa-116">Request headers</span></span>
|<span data-ttu-id="f41fa-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f41fa-117">Header</span></span>|<span data-ttu-id="f41fa-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f41fa-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f41fa-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="f41fa-119">Authorization</span></span>|<span data-ttu-id="f41fa-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f41fa-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="f41fa-121">Accept</span><span class="sxs-lookup"><span data-stu-id="f41fa-121">Accept</span></span>|<span data-ttu-id="f41fa-122">application/json</span><span class="sxs-lookup"><span data-stu-id="f41fa-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f41fa-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f41fa-123">Request body</span></span>
<span data-ttu-id="f41fa-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsMobileMSI.</span><span class="sxs-lookup"><span data-stu-id="f41fa-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="f41fa-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsMobileMSI.</span><span class="sxs-lookup"><span data-stu-id="f41fa-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="f41fa-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f41fa-126">Property</span></span>|<span data-ttu-id="f41fa-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="f41fa-127">Type</span></span>|<span data-ttu-id="f41fa-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="f41fa-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f41fa-129">id</span><span class="sxs-lookup"><span data-stu-id="f41fa-129">id</span></span>|<span data-ttu-id="f41fa-130">String</span><span class="sxs-lookup"><span data-stu-id="f41fa-130">String</span></span>|<span data-ttu-id="f41fa-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f41fa-131">Key of the setting.</span></span> <span data-ttu-id="f41fa-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f41fa-133">displayName</span><span class="sxs-lookup"><span data-stu-id="f41fa-133">displayName</span></span>|<span data-ttu-id="f41fa-134">String</span><span class="sxs-lookup"><span data-stu-id="f41fa-134">String</span></span>|<span data-ttu-id="f41fa-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="f41fa-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="f41fa-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f41fa-137">description</span><span class="sxs-lookup"><span data-stu-id="f41fa-137">description</span></span>|<span data-ttu-id="f41fa-138">String</span><span class="sxs-lookup"><span data-stu-id="f41fa-138">String</span></span>|<span data-ttu-id="f41fa-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f41fa-139">The description of the app.</span></span> <span data-ttu-id="f41fa-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f41fa-141">publisher</span><span class="sxs-lookup"><span data-stu-id="f41fa-141">Publisher</span></span>|<span data-ttu-id="f41fa-142">String</span><span class="sxs-lookup"><span data-stu-id="f41fa-142">String</span></span>|<span data-ttu-id="f41fa-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f41fa-143">The name of the app.</span></span> <span data-ttu-id="f41fa-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f41fa-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="f41fa-145">largeIcon</span></span>|[<span data-ttu-id="f41fa-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="f41fa-146">mimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="f41fa-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="f41fa-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="f41fa-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f41fa-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f41fa-149">createdDateTime</span></span>|<span data-ttu-id="f41fa-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f41fa-150">DateTimeOffset</span></span>|<span data-ttu-id="f41fa-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f41fa-151">The date and time when the page was created.</span></span> <span data-ttu-id="f41fa-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f41fa-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f41fa-153">lastModifiedDateTime</span></span>|<span data-ttu-id="f41fa-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f41fa-154">DateTimeOffset</span></span>|<span data-ttu-id="f41fa-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f41fa-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="f41fa-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f41fa-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="f41fa-157">isFeatured</span></span>|<span data-ttu-id="f41fa-158">Boolean</span><span class="sxs-lookup"><span data-stu-id="f41fa-158">Boolean</span></span>|<span data-ttu-id="f41fa-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f41fa-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="f41fa-160">privacyInformationUrl</span></span>|<span data-ttu-id="f41fa-161">String</span><span class="sxs-lookup"><span data-stu-id="f41fa-161">String</span></span>|<span data-ttu-id="f41fa-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="f41fa-162">The privacy statement Url.</span></span> <span data-ttu-id="f41fa-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f41fa-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="f41fa-164">informationUrl</span></span>|<span data-ttu-id="f41fa-165">String</span><span class="sxs-lookup"><span data-stu-id="f41fa-165">String</span></span>|<span data-ttu-id="f41fa-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f41fa-166">The more information Url.</span></span> <span data-ttu-id="f41fa-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f41fa-168">owner</span><span class="sxs-lookup"><span data-stu-id="f41fa-168">owner</span></span>|<span data-ttu-id="f41fa-169">String</span><span class="sxs-lookup"><span data-stu-id="f41fa-169">String</span></span>|<span data-ttu-id="f41fa-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f41fa-170">The owner of the timesheet.</span></span> <span data-ttu-id="f41fa-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f41fa-172">developer</span><span class="sxs-lookup"><span data-stu-id="f41fa-172">developer</span></span>|<span data-ttu-id="f41fa-173">String</span><span class="sxs-lookup"><span data-stu-id="f41fa-173">String</span></span>|<span data-ttu-id="f41fa-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f41fa-174">The name of the app.</span></span> <span data-ttu-id="f41fa-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f41fa-176">notes</span><span class="sxs-lookup"><span data-stu-id="f41fa-176">Notes</span></span>|<span data-ttu-id="f41fa-177">String</span><span class="sxs-lookup"><span data-stu-id="f41fa-177">String</span></span>|<span data-ttu-id="f41fa-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f41fa-178">Notes for the app.</span></span> <span data-ttu-id="f41fa-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f41fa-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="f41fa-180">publishingState</span></span>|<span data-ttu-id="f41fa-181">String</span><span class="sxs-lookup"><span data-stu-id="f41fa-181">String</span></span>|<span data-ttu-id="f41fa-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f41fa-182">The publishing state for the app.</span></span> <span data-ttu-id="f41fa-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="f41fa-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="f41fa-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="f41fa-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="f41fa-185">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="f41fa-185">committedContentVersion</span></span>|<span data-ttu-id="f41fa-186">String</span><span class="sxs-lookup"><span data-stu-id="f41fa-186">String</span></span>|<span data-ttu-id="f41fa-187">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="f41fa-187">The internal committed content version.</span></span> <span data-ttu-id="f41fa-188">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-188">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="f41fa-189">fileName</span><span class="sxs-lookup"><span data-stu-id="f41fa-189">fileName</span></span>|<span data-ttu-id="f41fa-190">String</span><span class="sxs-lookup"><span data-stu-id="f41fa-190">String</span></span>|<span data-ttu-id="f41fa-191">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="f41fa-191">The name of the main Lob application file.</span></span> <span data-ttu-id="f41fa-192">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-192">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="f41fa-193">size</span><span class="sxs-lookup"><span data-stu-id="f41fa-193">size</span></span>|<span data-ttu-id="f41fa-194">Int64</span><span class="sxs-lookup"><span data-stu-id="f41fa-194">Int64</span></span>|<span data-ttu-id="f41fa-195">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="f41fa-195">The total size, including all uploaded files.</span></span> <span data-ttu-id="f41fa-196">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="f41fa-196">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="f41fa-197">commandLine</span><span class="sxs-lookup"><span data-stu-id="f41fa-197">Command-line:</span></span>|<span data-ttu-id="f41fa-198">String</span><span class="sxs-lookup"><span data-stu-id="f41fa-198">String</span></span>|<span data-ttu-id="f41fa-199">Línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="f41fa-199">The command line.</span></span>|
|<span data-ttu-id="f41fa-200">productCode</span><span class="sxs-lookup"><span data-stu-id="f41fa-200">ProductCode</span></span>|<span data-ttu-id="f41fa-201">String</span><span class="sxs-lookup"><span data-stu-id="f41fa-201">String</span></span>|<span data-ttu-id="f41fa-202">Código del producto.</span><span class="sxs-lookup"><span data-stu-id="f41fa-202">The product code.</span></span>|
|<span data-ttu-id="f41fa-203">productVersion</span><span class="sxs-lookup"><span data-stu-id="f41fa-203">productVersion</span></span>|<span data-ttu-id="f41fa-204">String</span><span class="sxs-lookup"><span data-stu-id="f41fa-204">String</span></span>|<span data-ttu-id="f41fa-205">Versión del producto de la aplicación de línea de negocio (LoB) de MSI para Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="f41fa-205">The product version of Windows Mobile MSI Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="f41fa-206">ignoreVersionDetection</span><span class="sxs-lookup"><span data-stu-id="f41fa-206">ignoreVersionDetection</span></span>|<span data-ttu-id="f41fa-207">Boolean</span><span class="sxs-lookup"><span data-stu-id="f41fa-207">Boolean</span></span>|<span data-ttu-id="f41fa-208">Valor booleano que controla si la versión de la aplicación se usará para detectar la aplicación después de instalarla en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f41fa-208">A boolean to control whether the app's version will be used to detect the app after it is installed on a device.</span></span> <span data-ttu-id="f41fa-209">Establézcalo en True para aplicaciones de línea de negocio (LoB) de MSI para Windows Mobile que usen la característica de actualización automática.</span><span class="sxs-lookup"><span data-stu-id="f41fa-209">Set this to true for Windows Mobile MSI Line of Business (LoB) apps that use a self update feature.</span></span>|



## <a name="response"></a><span data-ttu-id="f41fa-210">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f41fa-210">Response</span></span>
<span data-ttu-id="f41fa-211">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f41fa-211">If successful, this method returns a `201 Created` response code and a [DriveItemVersion](../resources/intune_apps_windowsmobilemsi.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f41fa-212">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f41fa-212">Example</span></span>
### <a name="request"></a><span data-ttu-id="f41fa-213">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f41fa-213">Request</span></span>
<span data-ttu-id="f41fa-214">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f41fa-214">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 919

{
  "@odata.type": "#microsoft.graph.windowsMobileMSI",
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
  "commandLine": "Command Line value",
  "productCode": "Product Code value",
  "productVersion": "Product Version value",
  "ignoreVersionDetection": true
}
```

### <a name="response"></a><span data-ttu-id="f41fa-215">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f41fa-215">Response</span></span>
<span data-ttu-id="f41fa-p119">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f41fa-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1027

{
  "@odata.type": "#microsoft.graph.windowsMobileMSI",
  "id": "aa453e5d-3e5d-aa45-5d3e-45aa5d3e45aa",
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
  "commandLine": "Command Line value",
  "productCode": "Product Code value",
  "productVersion": "Product Version value",
  "ignoreVersionDetection": true
}
```



