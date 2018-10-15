# <a name="update-windowsmobilemsi"></a><span data-ttu-id="5fe70-101">Actualizar windowsMobileMSI</span><span class="sxs-lookup"><span data-stu-id="5fe70-101">Update windowsMobileMSI</span></span>

> <span data-ttu-id="5fe70-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5fe70-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5fe70-103">Actualice las propiedades de un objeto [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-103">Update the properties of a [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5fe70-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5fe70-104">Prerequisites</span></span>
<span data-ttu-id="5fe70-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5fe70-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5fe70-107">Permission type</span></span>|<span data-ttu-id="5fe70-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5fe70-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5fe70-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5fe70-109">Delegated (work or school account)</span></span>|<span data-ttu-id="5fe70-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5fe70-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="5fe70-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5fe70-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5fe70-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5fe70-112">Not supported.</span></span>|
|<span data-ttu-id="5fe70-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5fe70-113">Application</span></span>|<span data-ttu-id="5fe70-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5fe70-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5fe70-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5fe70-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="5fe70-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5fe70-116">Request headers</span></span>
|<span data-ttu-id="5fe70-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fe70-117">Header</span></span>|<span data-ttu-id="5fe70-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5fe70-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5fe70-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="5fe70-119">Authorization</span></span>|<span data-ttu-id="5fe70-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5fe70-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5fe70-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5fe70-121">Accept</span></span>|<span data-ttu-id="5fe70-122">application/json</span><span class="sxs-lookup"><span data-stu-id="5fe70-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5fe70-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5fe70-123">Request body</span></span>
<span data-ttu-id="5fe70-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-124">In the request body, supply a JSON representation for the [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md) object.</span></span>

<span data-ttu-id="5fe70-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-125">The following table shows the properties that are required when you create the [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md).</span></span>

|<span data-ttu-id="5fe70-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5fe70-126">Property</span></span>|<span data-ttu-id="5fe70-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="5fe70-127">Type</span></span>|<span data-ttu-id="5fe70-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fe70-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5fe70-129">id.</span><span class="sxs-lookup"><span data-stu-id="5fe70-129">id</span></span>|<span data-ttu-id="5fe70-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fe70-130">String</span></span>|<span data-ttu-id="5fe70-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5fe70-131">Key of the entity.</span></span> <span data-ttu-id="5fe70-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5fe70-133">displayName</span><span class="sxs-lookup"><span data-stu-id="5fe70-133">displayName</span></span>|<span data-ttu-id="5fe70-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fe70-134">String</span></span>|<span data-ttu-id="5fe70-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="5fe70-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="5fe70-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5fe70-137">descripción</span><span class="sxs-lookup"><span data-stu-id="5fe70-137">description</span></span>|<span data-ttu-id="5fe70-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fe70-138">String</span></span>|<span data-ttu-id="5fe70-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5fe70-139">The description of the app.</span></span> <span data-ttu-id="5fe70-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5fe70-141">publicador</span><span class="sxs-lookup"><span data-stu-id="5fe70-141">publisher</span></span>|<span data-ttu-id="5fe70-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fe70-142">String</span></span>|<span data-ttu-id="5fe70-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5fe70-143">The publisher of the app.</span></span> <span data-ttu-id="5fe70-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5fe70-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="5fe70-145">largeIcon</span></span>|[<span data-ttu-id="5fe70-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="5fe70-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="5fe70-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="5fe70-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="5fe70-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5fe70-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5fe70-149">createdDateTime</span></span>|<span data-ttu-id="5fe70-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5fe70-150">DateTimeOffset</span></span>|<span data-ttu-id="5fe70-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5fe70-151">The date and time the app was created.</span></span> <span data-ttu-id="5fe70-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5fe70-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="5fe70-153">lastModifiedDateTime</span></span>|<span data-ttu-id="5fe70-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5fe70-154">DateTimeOffset</span></span>|<span data-ttu-id="5fe70-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5fe70-155">The date and time the app was last modified.</span></span> <span data-ttu-id="5fe70-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5fe70-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="5fe70-157">isFeatured</span></span>|<span data-ttu-id="5fe70-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="5fe70-158">Boolean</span></span>|<span data-ttu-id="5fe70-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5fe70-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="5fe70-160">privacyInformationUrl</span></span>|<span data-ttu-id="5fe70-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fe70-161">String</span></span>|<span data-ttu-id="5fe70-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="5fe70-162">The privacy statement Url.</span></span> <span data-ttu-id="5fe70-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5fe70-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="5fe70-164">informationUrl</span></span>|<span data-ttu-id="5fe70-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fe70-165">String</span></span>|<span data-ttu-id="5fe70-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="5fe70-166">The more information Url.</span></span> <span data-ttu-id="5fe70-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5fe70-168">propietario/a</span><span class="sxs-lookup"><span data-stu-id="5fe70-168">owner</span></span>|<span data-ttu-id="5fe70-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fe70-169">String</span></span>|<span data-ttu-id="5fe70-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5fe70-170">The owner of the app.</span></span> <span data-ttu-id="5fe70-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5fe70-172">programador</span><span class="sxs-lookup"><span data-stu-id="5fe70-172">developer</span></span>|<span data-ttu-id="5fe70-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fe70-173">String</span></span>|<span data-ttu-id="5fe70-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5fe70-174">The developer of the app.</span></span> <span data-ttu-id="5fe70-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5fe70-176">notas</span><span class="sxs-lookup"><span data-stu-id="5fe70-176">notes</span></span>|<span data-ttu-id="5fe70-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fe70-177">String</span></span>|<span data-ttu-id="5fe70-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5fe70-178">Notes for the app.</span></span> <span data-ttu-id="5fe70-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5fe70-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="5fe70-180">publishingState</span></span>|[<span data-ttu-id="5fe70-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="5fe70-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="5fe70-p114">El estado de publicación para la aplicación. La aplicación no se puede asignar a menos que se publique la aplicación. Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing`, `published`.</span><span class="sxs-lookup"><span data-stu-id="5fe70-p114">The publishing state for the app. The app cannot be assigned unless the app is published. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md). The possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="5fe70-186">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="5fe70-186">committedContentVersion</span></span>|<span data-ttu-id="5fe70-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fe70-187">String</span></span>|<span data-ttu-id="5fe70-188">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="5fe70-188">The internal committed content version.</span></span> <span data-ttu-id="5fe70-189">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-189">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="5fe70-190">fileName</span><span class="sxs-lookup"><span data-stu-id="5fe70-190">fileName</span></span>|<span data-ttu-id="5fe70-191">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fe70-191">String</span></span>|<span data-ttu-id="5fe70-192">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="5fe70-192">The name of the main Lob application file.</span></span> <span data-ttu-id="5fe70-193">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-193">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="5fe70-194">tamaño</span><span class="sxs-lookup"><span data-stu-id="5fe70-194">size</span></span>|<span data-ttu-id="5fe70-195">Int64</span><span class="sxs-lookup"><span data-stu-id="5fe70-195">Int64</span></span>|<span data-ttu-id="5fe70-196">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="5fe70-196">The total size, including all uploaded files.</span></span> <span data-ttu-id="5fe70-197">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="5fe70-197">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="5fe70-198">commandLine</span><span class="sxs-lookup"><span data-stu-id="5fe70-198">commandLine</span></span>|<span data-ttu-id="5fe70-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fe70-199">String</span></span>|<span data-ttu-id="5fe70-200">Línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="5fe70-200">The command line.</span></span>|
|<span data-ttu-id="5fe70-201">productCode</span><span class="sxs-lookup"><span data-stu-id="5fe70-201">productCode</span></span>|<span data-ttu-id="5fe70-202">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fe70-202">String</span></span>|<span data-ttu-id="5fe70-203">Código del producto.</span><span class="sxs-lookup"><span data-stu-id="5fe70-203">The product code.</span></span>|
|<span data-ttu-id="5fe70-204">productVersion</span><span class="sxs-lookup"><span data-stu-id="5fe70-204">productVersion</span></span>|<span data-ttu-id="5fe70-205">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fe70-205">String</span></span>|<span data-ttu-id="5fe70-206">Versión del producto de la aplicación de línea de negocio (LoB) de MSI para Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="5fe70-206">The product version of Windows Mobile MSI Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="5fe70-207">ignoreVersionDetection</span><span class="sxs-lookup"><span data-stu-id="5fe70-207">ignoreVersionDetection</span></span>|<span data-ttu-id="5fe70-208">Booleano</span><span class="sxs-lookup"><span data-stu-id="5fe70-208">Boolean</span></span>|<span data-ttu-id="5fe70-209">Valor booleano que controla si la versión de la aplicación se usará para detectar la aplicación después de instalarla en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5fe70-209">A boolean to control whether the app's version will be used to detect the app after it is installed on a device.</span></span> <span data-ttu-id="5fe70-210">Establézcalo en True para aplicaciones de línea de negocio (LoB) de MSI para Windows Mobile que usen la característica de actualización automática.</span><span class="sxs-lookup"><span data-stu-id="5fe70-210">Set this to true for Windows Mobile MSI Line of Business (LoB) apps that use a self update feature.</span></span>|



## <a name="response"></a><span data-ttu-id="5fe70-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5fe70-211">Response</span></span>
<span data-ttu-id="5fe70-212">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5fe70-212">If successful, this method returns a `200 OK` response code and an updated [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5fe70-213">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5fe70-213">Example</span></span>
### <a name="request"></a><span data-ttu-id="5fe70-214">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5fe70-214">Request</span></span>
<span data-ttu-id="5fe70-215">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5fe70-215">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 864

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
  "commandLine": "Command Line value",
  "productCode": "Product Code value",
  "productVersion": "Product Version value",
  "ignoreVersionDetection": true
}
```

### <a name="response"></a><span data-ttu-id="5fe70-216">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5fe70-216">Response</span></span>
<span data-ttu-id="5fe70-p119">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5fe70-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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








