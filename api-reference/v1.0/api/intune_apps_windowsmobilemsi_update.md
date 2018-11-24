# <a name="update-windowsmobilemsi"></a><span data-ttu-id="7dd21-101">Actualizar windowsMobileMSI</span><span class="sxs-lookup"><span data-stu-id="7dd21-101">Update windowsMobileMSI</span></span>

> <span data-ttu-id="7dd21-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7dd21-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7dd21-103">Actualice las propiedades de un objeto [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-103">Update the properties of a [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7dd21-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7dd21-104">Prerequisites</span></span>
<span data-ttu-id="7dd21-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7dd21-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7dd21-107">Permission type</span></span>|<span data-ttu-id="7dd21-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7dd21-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7dd21-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7dd21-109">Delegated (work or school account)</span></span>|<span data-ttu-id="7dd21-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7dd21-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="7dd21-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7dd21-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7dd21-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7dd21-112">Not supported.</span></span>|
|<span data-ttu-id="7dd21-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7dd21-113">Application</span></span>|<span data-ttu-id="7dd21-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7dd21-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7dd21-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7dd21-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="7dd21-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7dd21-116">Request headers</span></span>
|<span data-ttu-id="7dd21-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7dd21-117">Header</span></span>|<span data-ttu-id="7dd21-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7dd21-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7dd21-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="7dd21-119">Authorization</span></span>|<span data-ttu-id="7dd21-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7dd21-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7dd21-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7dd21-121">Accept</span></span>|<span data-ttu-id="7dd21-122">application/json</span><span class="sxs-lookup"><span data-stu-id="7dd21-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7dd21-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7dd21-123">Request body</span></span>
<span data-ttu-id="7dd21-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-124">In the request body, supply a JSON representation for the [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md) object.</span></span>

<span data-ttu-id="7dd21-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-125">The following table shows the properties that are required when you create the [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md).</span></span>

|<span data-ttu-id="7dd21-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7dd21-126">Property</span></span>|<span data-ttu-id="7dd21-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="7dd21-127">Type</span></span>|<span data-ttu-id="7dd21-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="7dd21-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7dd21-129">id</span><span class="sxs-lookup"><span data-stu-id="7dd21-129">id</span></span>|<span data-ttu-id="7dd21-130">String</span><span class="sxs-lookup"><span data-stu-id="7dd21-130">String</span></span>|<span data-ttu-id="7dd21-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7dd21-131">Key of the entity.</span></span> <span data-ttu-id="7dd21-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7dd21-133">displayName</span><span class="sxs-lookup"><span data-stu-id="7dd21-133">displayName</span></span>|<span data-ttu-id="7dd21-134">String</span><span class="sxs-lookup"><span data-stu-id="7dd21-134">String</span></span>|<span data-ttu-id="7dd21-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="7dd21-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="7dd21-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7dd21-137">description</span><span class="sxs-lookup"><span data-stu-id="7dd21-137">description</span></span>|<span data-ttu-id="7dd21-138">String</span><span class="sxs-lookup"><span data-stu-id="7dd21-138">String</span></span>|<span data-ttu-id="7dd21-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7dd21-139">The description of the app.</span></span> <span data-ttu-id="7dd21-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7dd21-141">publicador</span><span class="sxs-lookup"><span data-stu-id="7dd21-141">publisher</span></span>|<span data-ttu-id="7dd21-142">String</span><span class="sxs-lookup"><span data-stu-id="7dd21-142">String</span></span>|<span data-ttu-id="7dd21-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7dd21-143">The publisher of the app.</span></span> <span data-ttu-id="7dd21-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7dd21-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="7dd21-145">largeIcon</span></span>|[<span data-ttu-id="7dd21-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="7dd21-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="7dd21-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="7dd21-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="7dd21-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7dd21-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="7dd21-149">createdDateTime</span></span>|<span data-ttu-id="7dd21-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7dd21-150">DateTimeOffset</span></span>|<span data-ttu-id="7dd21-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7dd21-151">The date and time the app was created.</span></span> <span data-ttu-id="7dd21-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7dd21-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7dd21-153">lastModifiedDateTime</span></span>|<span data-ttu-id="7dd21-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7dd21-154">DateTimeOffset</span></span>|<span data-ttu-id="7dd21-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7dd21-155">The date and time the app was last modified.</span></span> <span data-ttu-id="7dd21-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7dd21-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="7dd21-157">isFeatured</span></span>|<span data-ttu-id="7dd21-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="7dd21-158">Boolean</span></span>|<span data-ttu-id="7dd21-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7dd21-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="7dd21-160">privacyInformationUrl</span></span>|<span data-ttu-id="7dd21-161">String</span><span class="sxs-lookup"><span data-stu-id="7dd21-161">String</span></span>|<span data-ttu-id="7dd21-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="7dd21-162">The privacy statement Url.</span></span> <span data-ttu-id="7dd21-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7dd21-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="7dd21-164">informationUrl</span></span>|<span data-ttu-id="7dd21-165">String</span><span class="sxs-lookup"><span data-stu-id="7dd21-165">String</span></span>|<span data-ttu-id="7dd21-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="7dd21-166">The more information Url.</span></span> <span data-ttu-id="7dd21-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7dd21-168">owner</span><span class="sxs-lookup"><span data-stu-id="7dd21-168">owner</span></span>|<span data-ttu-id="7dd21-169">String</span><span class="sxs-lookup"><span data-stu-id="7dd21-169">String</span></span>|<span data-ttu-id="7dd21-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7dd21-170">The owner of the app.</span></span> <span data-ttu-id="7dd21-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7dd21-172">developer</span><span class="sxs-lookup"><span data-stu-id="7dd21-172">developer</span></span>|<span data-ttu-id="7dd21-173">String</span><span class="sxs-lookup"><span data-stu-id="7dd21-173">String</span></span>|<span data-ttu-id="7dd21-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7dd21-174">The developer of the app.</span></span> <span data-ttu-id="7dd21-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7dd21-176">notas</span><span class="sxs-lookup"><span data-stu-id="7dd21-176">notes</span></span>|<span data-ttu-id="7dd21-177">String</span><span class="sxs-lookup"><span data-stu-id="7dd21-177">String</span></span>|<span data-ttu-id="7dd21-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7dd21-178">Notes for the app.</span></span> <span data-ttu-id="7dd21-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7dd21-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="7dd21-180">publishingState</span></span>|[<span data-ttu-id="7dd21-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="7dd21-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="7dd21-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7dd21-182">The publishing state for the app.</span></span> <span data-ttu-id="7dd21-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="7dd21-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="7dd21-184">Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md).</span></span> <span data-ttu-id="7dd21-185">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="7dd21-185">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="7dd21-186">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="7dd21-186">committedContentVersion</span></span>|<span data-ttu-id="7dd21-187">String</span><span class="sxs-lookup"><span data-stu-id="7dd21-187">String</span></span>|<span data-ttu-id="7dd21-188">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="7dd21-188">The internal committed content version.</span></span> <span data-ttu-id="7dd21-189">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-189">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="7dd21-190">fileName</span><span class="sxs-lookup"><span data-stu-id="7dd21-190">fileName</span></span>|<span data-ttu-id="7dd21-191">String</span><span class="sxs-lookup"><span data-stu-id="7dd21-191">String</span></span>|<span data-ttu-id="7dd21-192">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="7dd21-192">The name of the main Lob application file.</span></span> <span data-ttu-id="7dd21-193">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-193">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="7dd21-194">size</span><span class="sxs-lookup"><span data-stu-id="7dd21-194">size</span></span>|<span data-ttu-id="7dd21-195">Int64</span><span class="sxs-lookup"><span data-stu-id="7dd21-195">Int64</span></span>|<span data-ttu-id="7dd21-196">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="7dd21-196">The total size, including all uploaded files.</span></span> <span data-ttu-id="7dd21-197">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="7dd21-197">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="7dd21-198">commandLine</span><span class="sxs-lookup"><span data-stu-id="7dd21-198">commandLine</span></span>|<span data-ttu-id="7dd21-199">String</span><span class="sxs-lookup"><span data-stu-id="7dd21-199">String</span></span>|<span data-ttu-id="7dd21-200">Línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="7dd21-200">The command line.</span></span>|
|<span data-ttu-id="7dd21-201">productCode</span><span class="sxs-lookup"><span data-stu-id="7dd21-201">productCode</span></span>|<span data-ttu-id="7dd21-202">String</span><span class="sxs-lookup"><span data-stu-id="7dd21-202">String</span></span>|<span data-ttu-id="7dd21-203">Código del producto.</span><span class="sxs-lookup"><span data-stu-id="7dd21-203">The product code.</span></span>|
|<span data-ttu-id="7dd21-204">productVersion</span><span class="sxs-lookup"><span data-stu-id="7dd21-204">productVersion</span></span>|<span data-ttu-id="7dd21-205">String</span><span class="sxs-lookup"><span data-stu-id="7dd21-205">String</span></span>|<span data-ttu-id="7dd21-206">Versión del producto de la aplicación de línea de negocio (LoB) de MSI para Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="7dd21-206">The product version of Windows Mobile MSI Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="7dd21-207">ignoreVersionDetection</span><span class="sxs-lookup"><span data-stu-id="7dd21-207">ignoreVersionDetection</span></span>|<span data-ttu-id="7dd21-208">Booleano</span><span class="sxs-lookup"><span data-stu-id="7dd21-208">Boolean</span></span>|<span data-ttu-id="7dd21-209">Valor booleano que controla si la versión de la aplicación se usará para detectar la aplicación después de instalarla en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7dd21-209">A boolean to control whether the app's version will be used to detect the app after it is installed on a device.</span></span> <span data-ttu-id="7dd21-210">Establézcalo en True para aplicaciones de línea de negocio (LoB) de MSI para Windows Mobile que usen la característica de actualización automática.</span><span class="sxs-lookup"><span data-stu-id="7dd21-210">Set this to true for Windows Mobile MSI Line of Business (LoB) apps that use a self update feature.</span></span>|



## <a name="response"></a><span data-ttu-id="7dd21-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7dd21-211">Response</span></span>
<span data-ttu-id="7dd21-212">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7dd21-212">If successful, this method returns a `200 OK` response code and an updated [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7dd21-213">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7dd21-213">Example</span></span>
### <a name="request"></a><span data-ttu-id="7dd21-214">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7dd21-214">Request</span></span>
<span data-ttu-id="7dd21-215">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7dd21-215">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 855

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

### <a name="response"></a><span data-ttu-id="7dd21-216">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7dd21-216">Response</span></span>
<span data-ttu-id="7dd21-p119">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7dd21-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



