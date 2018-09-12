# <a name="create-ioslobapp"></a><span data-ttu-id="a78fd-101">Crear iosLobApp</span><span class="sxs-lookup"><span data-stu-id="a78fd-101">Create iosLobApp</span></span>

> <span data-ttu-id="a78fd-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a78fd-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a78fd-103">Cree un objeto [iosLobApp](../resources/intune_apps_ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-103">Create a new [iosLobApp](../resources/intune_apps_ioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a78fd-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a78fd-104">Prerequisites</span></span>
<span data-ttu-id="a78fd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a78fd-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a78fd-107">Permission type</span></span>|<span data-ttu-id="a78fd-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a78fd-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a78fd-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a78fd-109">Delegated (work or school account)</span></span>|<span data-ttu-id="a78fd-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a78fd-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="a78fd-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a78fd-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a78fd-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a78fd-112">Not supported.</span></span>|
|<span data-ttu-id="a78fd-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a78fd-113">Application</span></span>|<span data-ttu-id="a78fd-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a78fd-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a78fd-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a78fd-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="a78fd-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a78fd-116">Request headers</span></span>
|<span data-ttu-id="a78fd-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a78fd-117">Header</span></span>|<span data-ttu-id="a78fd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a78fd-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a78fd-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="a78fd-119">Authorization</span></span>|<span data-ttu-id="a78fd-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a78fd-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a78fd-121">Accept</span><span class="sxs-lookup"><span data-stu-id="a78fd-121">Accept</span></span>|<span data-ttu-id="a78fd-122">application/json</span><span class="sxs-lookup"><span data-stu-id="a78fd-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a78fd-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a78fd-123">Request body</span></span>
<span data-ttu-id="a78fd-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosLobApp.</span><span class="sxs-lookup"><span data-stu-id="a78fd-124">In the request body, supply a JSON representation for the iosLobApp object.</span></span>

<span data-ttu-id="a78fd-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosLobApp.</span><span class="sxs-lookup"><span data-stu-id="a78fd-125">The following table shows the properties that are required when you create the iosLobApp.</span></span>

|<span data-ttu-id="a78fd-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a78fd-126">Property</span></span>|<span data-ttu-id="a78fd-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="a78fd-127">Type</span></span>|<span data-ttu-id="a78fd-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="a78fd-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a78fd-129">id</span><span class="sxs-lookup"><span data-stu-id="a78fd-129">id</span></span>|<span data-ttu-id="a78fd-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="a78fd-130">String</span></span>|<span data-ttu-id="a78fd-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a78fd-131">Key of the entity.</span></span> <span data-ttu-id="a78fd-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a78fd-133">displayName</span><span class="sxs-lookup"><span data-stu-id="a78fd-133">displayName</span></span>|<span data-ttu-id="a78fd-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="a78fd-134">String</span></span>|<span data-ttu-id="a78fd-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="a78fd-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="a78fd-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a78fd-137">description</span><span class="sxs-lookup"><span data-stu-id="a78fd-137">description</span></span>|<span data-ttu-id="a78fd-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="a78fd-138">String</span></span>|<span data-ttu-id="a78fd-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a78fd-139">The description of the app.</span></span> <span data-ttu-id="a78fd-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a78fd-141">publisher</span><span class="sxs-lookup"><span data-stu-id="a78fd-141">publisher</span></span>|<span data-ttu-id="a78fd-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="a78fd-142">String</span></span>|<span data-ttu-id="a78fd-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a78fd-143">The publisher of the app.</span></span> <span data-ttu-id="a78fd-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a78fd-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="a78fd-145">largeIcon</span></span>|[<span data-ttu-id="a78fd-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="a78fd-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="a78fd-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="a78fd-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="a78fd-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a78fd-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a78fd-149">createdDateTime</span></span>|<span data-ttu-id="a78fd-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a78fd-150">DateTimeOffset</span></span>|<span data-ttu-id="a78fd-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a78fd-151">The date and time the app was created.</span></span> <span data-ttu-id="a78fd-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a78fd-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a78fd-153">lastModifiedDateTime</span></span>|<span data-ttu-id="a78fd-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a78fd-154">DateTimeOffset</span></span>|<span data-ttu-id="a78fd-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a78fd-155">The date and time the app was last modified.</span></span> <span data-ttu-id="a78fd-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a78fd-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="a78fd-157">isFeatured</span></span>|<span data-ttu-id="a78fd-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="a78fd-158">Boolean</span></span>|<span data-ttu-id="a78fd-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a78fd-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="a78fd-160">privacyInformationUrl</span></span>|<span data-ttu-id="a78fd-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="a78fd-161">String</span></span>|<span data-ttu-id="a78fd-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="a78fd-162">The privacy statement Url.</span></span> <span data-ttu-id="a78fd-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a78fd-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="a78fd-164">informationUrl</span></span>|<span data-ttu-id="a78fd-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="a78fd-165">String</span></span>|<span data-ttu-id="a78fd-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a78fd-166">The more information Url.</span></span> <span data-ttu-id="a78fd-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a78fd-168">owner</span><span class="sxs-lookup"><span data-stu-id="a78fd-168">owner</span></span>|<span data-ttu-id="a78fd-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="a78fd-169">String</span></span>|<span data-ttu-id="a78fd-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a78fd-170">The owner of the app.</span></span> <span data-ttu-id="a78fd-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a78fd-172">developer</span><span class="sxs-lookup"><span data-stu-id="a78fd-172">developer</span></span>|<span data-ttu-id="a78fd-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="a78fd-173">String</span></span>|<span data-ttu-id="a78fd-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a78fd-174">The developer of the app.</span></span> <span data-ttu-id="a78fd-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a78fd-176">notas</span><span class="sxs-lookup"><span data-stu-id="a78fd-176">notes</span></span>|<span data-ttu-id="a78fd-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="a78fd-177">String</span></span>|<span data-ttu-id="a78fd-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a78fd-178">Notes for the app.</span></span> <span data-ttu-id="a78fd-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a78fd-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="a78fd-180">publishingState</span></span>|[<span data-ttu-id="a78fd-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="a78fd-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="a78fd-p114">El estado de publicación para la aplicación. La aplicación no se puede asignar a menos que se publique la aplicación. Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing`, `published`.</span><span class="sxs-lookup"><span data-stu-id="a78fd-p114">The publishing state for the app. The app cannot be assigned unless the app is published. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md). The possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="a78fd-186">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="a78fd-186">committedContentVersion</span></span>|<span data-ttu-id="a78fd-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="a78fd-187">String</span></span>|<span data-ttu-id="a78fd-188">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="a78fd-188">The internal committed content version.</span></span> <span data-ttu-id="a78fd-189">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-189">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="a78fd-190">fileName</span><span class="sxs-lookup"><span data-stu-id="a78fd-190">fileName</span></span>|<span data-ttu-id="a78fd-191">Cadena</span><span class="sxs-lookup"><span data-stu-id="a78fd-191">String</span></span>|<span data-ttu-id="a78fd-192">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="a78fd-192">The name of the main Lob application file.</span></span> <span data-ttu-id="a78fd-193">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-193">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="a78fd-194">size</span><span class="sxs-lookup"><span data-stu-id="a78fd-194">size</span></span>|<span data-ttu-id="a78fd-195">Int64</span><span class="sxs-lookup"><span data-stu-id="a78fd-195">Int64</span></span>|<span data-ttu-id="a78fd-196">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="a78fd-196">The total size, including all uploaded files.</span></span> <span data-ttu-id="a78fd-197">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="a78fd-197">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="a78fd-198">bundleId</span><span class="sxs-lookup"><span data-stu-id="a78fd-198">bundleId</span></span>|<span data-ttu-id="a78fd-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="a78fd-199">String</span></span>|<span data-ttu-id="a78fd-200">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="a78fd-200">The Identity Name.</span></span>|
|<span data-ttu-id="a78fd-201">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="a78fd-201">applicableDeviceType</span></span>|[<span data-ttu-id="a78fd-202">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="a78fd-202">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="a78fd-203">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="a78fd-203">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="a78fd-204">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a78fd-204">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="a78fd-205">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a78fd-205">iosMinimumOperatingSystem</span></span>](../resources/intune_apps_iosminimumoperatingsystem.md)|<span data-ttu-id="a78fd-206">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="a78fd-206">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="a78fd-207">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="a78fd-207">expirationDateTime</span></span>|<span data-ttu-id="a78fd-208">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a78fd-208">DateTimeOffset</span></span>|<span data-ttu-id="a78fd-209">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="a78fd-209">The expiration time.</span></span>|
|<span data-ttu-id="a78fd-210">versionNumber</span><span class="sxs-lookup"><span data-stu-id="a78fd-210">versionNumber</span></span>|<span data-ttu-id="a78fd-211">Cadena</span><span class="sxs-lookup"><span data-stu-id="a78fd-211">String</span></span>|<span data-ttu-id="a78fd-212">El número de la versión de la aplicación de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="a78fd-212">The version number of iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="a78fd-213">buildNumber</span><span class="sxs-lookup"><span data-stu-id="a78fd-213">buildNumber</span></span>|<span data-ttu-id="a78fd-214">Cadena</span><span class="sxs-lookup"><span data-stu-id="a78fd-214">String</span></span>|<span data-ttu-id="a78fd-215">El número de compilación de la aplicación de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="a78fd-215">The build number of iOS Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="a78fd-216">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a78fd-216">Response</span></span>
<span data-ttu-id="a78fd-217">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosLobApp](../resources/intune_apps_ioslobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a78fd-217">If successful, this method returns a `201 Created` response code and a [iosLobApp](../resources/intune_apps_ioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a78fd-218">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a78fd-218">Example</span></span>
### <a name="request"></a><span data-ttu-id="a78fd-219">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a78fd-219">Request</span></span>
<span data-ttu-id="a78fd-220">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a78fd-220">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1253

{
  "@odata.type": "#microsoft.graph.iosLobApp",
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
  "bundleId": "Bundle Id value",
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
  },
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "versionNumber": "Version Number value",
  "buildNumber": "Build Number value"
}
```

### <a name="response"></a><span data-ttu-id="a78fd-221">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a78fd-221">Response</span></span>
<span data-ttu-id="a78fd-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a78fd-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1361

{
  "@odata.type": "#microsoft.graph.iosLobApp",
  "id": "b34052ea-52ea-b340-ea52-40b3ea5240b3",
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
  "bundleId": "Bundle Id value",
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
  },
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "versionNumber": "Version Number value",
  "buildNumber": "Build Number value"
}
```








