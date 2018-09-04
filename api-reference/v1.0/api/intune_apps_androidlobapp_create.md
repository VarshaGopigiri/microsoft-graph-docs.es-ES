# <a name="create-androidlobapp"></a><span data-ttu-id="f8bb1-101">Crear androidLobApp</span><span class="sxs-lookup"><span data-stu-id="f8bb1-101">Create androidLobApp</span></span>

> <span data-ttu-id="f8bb1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f8bb1-103">Cree un objeto [androidLobApp](../resources/intune_apps_androidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-103">Create a new [androidLobApp](../resources/intune_apps_androidlobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f8bb1-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f8bb1-104">Prerequisites</span></span>
<span data-ttu-id="f8bb1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f8bb1-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f8bb1-107">Permission type</span></span>|<span data-ttu-id="f8bb1-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f8bb1-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f8bb1-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f8bb1-109">Delegated (work or school account)</span></span>|<span data-ttu-id="f8bb1-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f8bb1-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f8bb1-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f8bb1-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f8bb1-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-112">Not supported.</span></span>|
|<span data-ttu-id="f8bb1-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f8bb1-113">Application</span></span>|<span data-ttu-id="f8bb1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f8bb1-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f8bb1-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="f8bb1-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f8bb1-116">Request headers</span></span>
|<span data-ttu-id="f8bb1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8bb1-117">Header</span></span>|<span data-ttu-id="f8bb1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f8bb1-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f8bb1-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="f8bb1-119">Authorization</span></span>|<span data-ttu-id="f8bb1-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f8bb1-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f8bb1-121">Accept</span></span>|<span data-ttu-id="f8bb1-122">aplicación/json</span><span class="sxs-lookup"><span data-stu-id="f8bb1-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f8bb1-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f8bb1-123">Request body</span></span>
<span data-ttu-id="f8bb1-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidLobApp.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-124">In the request body, supply a JSON representation for the androidLobApp object.</span></span>

<span data-ttu-id="f8bb1-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidLobApp.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-125">The following table shows the properties that are required when you create the androidLobApp.</span></span>

|<span data-ttu-id="f8bb1-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f8bb1-126">Property</span></span>|<span data-ttu-id="f8bb1-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="f8bb1-127">Type</span></span>|<span data-ttu-id="f8bb1-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8bb1-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f8bb1-129">id</span><span class="sxs-lookup"><span data-stu-id="f8bb1-129">id</span></span>|<span data-ttu-id="f8bb1-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8bb1-130">String</span></span>|<span data-ttu-id="f8bb1-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-131">Key of the entity.</span></span> <span data-ttu-id="f8bb1-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f8bb1-133">displayName</span><span class="sxs-lookup"><span data-stu-id="f8bb1-133">displayName</span></span>|<span data-ttu-id="f8bb1-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8bb1-134">String</span></span>|<span data-ttu-id="f8bb1-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="f8bb1-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f8bb1-137">descripción</span><span class="sxs-lookup"><span data-stu-id="f8bb1-137">description</span></span>|<span data-ttu-id="f8bb1-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8bb1-138">String</span></span>|<span data-ttu-id="f8bb1-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-139">The description of the app.</span></span> <span data-ttu-id="f8bb1-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f8bb1-141">publicador</span><span class="sxs-lookup"><span data-stu-id="f8bb1-141">publisher</span></span>|<span data-ttu-id="f8bb1-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8bb1-142">String</span></span>|<span data-ttu-id="f8bb1-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-143">The publisher of the app.</span></span> <span data-ttu-id="f8bb1-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f8bb1-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="f8bb1-145">largeIcon</span></span>|[<span data-ttu-id="f8bb1-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="f8bb1-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="f8bb1-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="f8bb1-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f8bb1-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f8bb1-149">createdDateTime</span></span>|<span data-ttu-id="f8bb1-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f8bb1-150">DateTimeOffset</span></span>|<span data-ttu-id="f8bb1-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-151">The date and time the app was created.</span></span> <span data-ttu-id="f8bb1-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f8bb1-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f8bb1-153">lastModifiedDateTime</span></span>|<span data-ttu-id="f8bb1-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f8bb1-154">DateTimeOffset</span></span>|<span data-ttu-id="f8bb1-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-155">The date and time the app was last modified.</span></span> <span data-ttu-id="f8bb1-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f8bb1-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="f8bb1-157">isFeatured</span></span>|<span data-ttu-id="f8bb1-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="f8bb1-158">Boolean</span></span>|<span data-ttu-id="f8bb1-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f8bb1-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="f8bb1-160">privacyInformationUrl</span></span>|<span data-ttu-id="f8bb1-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8bb1-161">String</span></span>|<span data-ttu-id="f8bb1-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-162">The privacy statement Url.</span></span> <span data-ttu-id="f8bb1-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f8bb1-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="f8bb1-164">informationUrl</span></span>|<span data-ttu-id="f8bb1-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8bb1-165">String</span></span>|<span data-ttu-id="f8bb1-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-166">The more information Url.</span></span> <span data-ttu-id="f8bb1-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f8bb1-168">owner</span><span class="sxs-lookup"><span data-stu-id="f8bb1-168">owner</span></span>|<span data-ttu-id="f8bb1-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8bb1-169">String</span></span>|<span data-ttu-id="f8bb1-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-170">The owner of the app.</span></span> <span data-ttu-id="f8bb1-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f8bb1-172">developer</span><span class="sxs-lookup"><span data-stu-id="f8bb1-172">developer</span></span>|<span data-ttu-id="f8bb1-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8bb1-173">String</span></span>|<span data-ttu-id="f8bb1-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-174">The developer of the app.</span></span> <span data-ttu-id="f8bb1-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f8bb1-176">notas</span><span class="sxs-lookup"><span data-stu-id="f8bb1-176">notes</span></span>|<span data-ttu-id="f8bb1-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8bb1-177">String</span></span>|<span data-ttu-id="f8bb1-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-178">Notes for the app.</span></span> <span data-ttu-id="f8bb1-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="f8bb1-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="f8bb1-180">publishingState</span></span>|[<span data-ttu-id="f8bb1-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="f8bb1-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="f8bb1-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-182">The publishing state for the app.</span></span> <span data-ttu-id="f8bb1-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="f8bb1-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span> <span data-ttu-id="f8bb1-185">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-185">The possible values are `notPublished`, `processing`, `published`, , , , , , , , , or .</span></span>|
|<span data-ttu-id="f8bb1-186">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="f8bb1-186">committedContentVersion</span></span>|<span data-ttu-id="f8bb1-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8bb1-187">String</span></span>|<span data-ttu-id="f8bb1-188">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-188">The internal committed content version.</span></span> <span data-ttu-id="f8bb1-189">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-189">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="f8bb1-190">fileName</span><span class="sxs-lookup"><span data-stu-id="f8bb1-190">fileName</span></span>|<span data-ttu-id="f8bb1-191">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8bb1-191">String</span></span>|<span data-ttu-id="f8bb1-192">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-192">The name of the main Lob application file.</span></span> <span data-ttu-id="f8bb1-193">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-193">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="f8bb1-194">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8bb1-194">size</span></span>|<span data-ttu-id="f8bb1-195">Int64</span><span class="sxs-lookup"><span data-stu-id="f8bb1-195">Int64</span></span>|<span data-ttu-id="f8bb1-196">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-196">The total size, including all uploaded files.</span></span> <span data-ttu-id="f8bb1-197">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb1-197">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="f8bb1-198">packageId</span><span class="sxs-lookup"><span data-stu-id="f8bb1-198">packageId</span></span>|<span data-ttu-id="f8bb1-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8bb1-199">String</span></span>|<span data-ttu-id="f8bb1-200">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-200">The package identifier.</span></span>|
|<span data-ttu-id="f8bb1-201">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="f8bb1-201">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="f8bb1-202">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="f8bb1-202">androidMinimumOperatingSystem</span></span>](../resources/intune_apps_androidminimumoperatingsystem.md)|<span data-ttu-id="f8bb1-203">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-203">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="f8bb1-204">versionName</span><span class="sxs-lookup"><span data-stu-id="f8bb1-204">versionName</span></span>|<span data-ttu-id="f8bb1-205">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8bb1-205">String</span></span>|<span data-ttu-id="f8bb1-206">El nombre de la versión de la aplicación de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-206">The version name of Android Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="f8bb1-207">versionCode</span><span class="sxs-lookup"><span data-stu-id="f8bb1-207">versionCode</span></span>|<span data-ttu-id="f8bb1-208">Cadena</span><span class="sxs-lookup"><span data-stu-id="f8bb1-208">String</span></span>|<span data-ttu-id="f8bb1-209">El código de versión de la aplicación de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-209">The version code of Android Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="f8bb1-210">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8bb1-210">Response</span></span>
<span data-ttu-id="f8bb1-211">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidLobApp](../resources/intune_apps_androidlobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-211">If successful, this method returns a `201 Created` response code and a [androidLobApp](../resources/intune_apps_androidlobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f8bb1-212">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f8bb1-212">Example</span></span>
### <a name="request"></a><span data-ttu-id="f8bb1-213">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f8bb1-213">Request</span></span>
<span data-ttu-id="f8bb1-214">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-214">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="f8bb1-215">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8bb1-215">Response</span></span>
<span data-ttu-id="f8bb1-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f8bb1-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



