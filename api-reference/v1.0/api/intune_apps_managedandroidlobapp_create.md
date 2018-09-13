# <a name="create-managedandroidlobapp"></a><span data-ttu-id="ac2ed-101">Crear managedAndroidLobApp</span><span class="sxs-lookup"><span data-stu-id="ac2ed-101">Create managedAndroidLobApp</span></span>

> <span data-ttu-id="ac2ed-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ac2ed-103">Cree un objeto [managedAndroidLobApp](../resources/intune_apps_managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-103">Create a new [managedAndroidLobApp](../resources/intune_apps_managedandroidlobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ac2ed-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ac2ed-104">Prerequisites</span></span>
<span data-ttu-id="ac2ed-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ac2ed-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ac2ed-107">Permission type</span></span>|<span data-ttu-id="ac2ed-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ac2ed-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ac2ed-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ac2ed-109">Delegated (work or school account)</span></span>|<span data-ttu-id="ac2ed-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ac2ed-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="ac2ed-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ac2ed-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ac2ed-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-112">Not supported.</span></span>|
|<span data-ttu-id="ac2ed-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ac2ed-113">Application</span></span>|<span data-ttu-id="ac2ed-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ac2ed-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ac2ed-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="ac2ed-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ac2ed-116">Request headers</span></span>
|<span data-ttu-id="ac2ed-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac2ed-117">Header</span></span>|<span data-ttu-id="ac2ed-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ac2ed-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ac2ed-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="ac2ed-119">Authorization</span></span>|<span data-ttu-id="ac2ed-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ac2ed-121">Accept</span><span class="sxs-lookup"><span data-stu-id="ac2ed-121">Accept</span></span>|<span data-ttu-id="ac2ed-122">application/json</span><span class="sxs-lookup"><span data-stu-id="ac2ed-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ac2ed-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ac2ed-123">Request body</span></span>
<span data-ttu-id="ac2ed-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedAndroidLobApp.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-124">In the request body, supply a JSON representation for the managedAndroidLobApp object.</span></span>

<span data-ttu-id="ac2ed-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedAndroidLobApp.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-125">The following table shows the properties that are required when you create the managedAndroidLobApp.</span></span>

|<span data-ttu-id="ac2ed-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac2ed-126">Property</span></span>|<span data-ttu-id="ac2ed-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac2ed-127">Type</span></span>|<span data-ttu-id="ac2ed-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac2ed-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ac2ed-129">id</span><span class="sxs-lookup"><span data-stu-id="ac2ed-129">id</span></span>|<span data-ttu-id="ac2ed-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac2ed-130">String</span></span>|<span data-ttu-id="ac2ed-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-131">Key of the entity.</span></span> <span data-ttu-id="ac2ed-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="ac2ed-133">displayName</span><span class="sxs-lookup"><span data-stu-id="ac2ed-133">displayName</span></span>|<span data-ttu-id="ac2ed-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac2ed-134">String</span></span>|<span data-ttu-id="ac2ed-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="ac2ed-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="ac2ed-137">description</span><span class="sxs-lookup"><span data-stu-id="ac2ed-137">description</span></span>|<span data-ttu-id="ac2ed-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac2ed-138">String</span></span>|<span data-ttu-id="ac2ed-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-139">The description of the app.</span></span> <span data-ttu-id="ac2ed-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="ac2ed-141">publisher</span><span class="sxs-lookup"><span data-stu-id="ac2ed-141">publisher</span></span>|<span data-ttu-id="ac2ed-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac2ed-142">String</span></span>|<span data-ttu-id="ac2ed-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-143">The publisher of the app.</span></span> <span data-ttu-id="ac2ed-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="ac2ed-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="ac2ed-145">largeIcon</span></span>|[<span data-ttu-id="ac2ed-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="ac2ed-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="ac2ed-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="ac2ed-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="ac2ed-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ac2ed-149">createdDateTime</span></span>|<span data-ttu-id="ac2ed-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ac2ed-150">DateTimeOffset</span></span>|<span data-ttu-id="ac2ed-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-151">The date and time the app was created.</span></span> <span data-ttu-id="ac2ed-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="ac2ed-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ac2ed-153">lastModifiedDateTime</span></span>|<span data-ttu-id="ac2ed-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ac2ed-154">DateTimeOffset</span></span>|<span data-ttu-id="ac2ed-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-155">The date and time the app was last modified.</span></span> <span data-ttu-id="ac2ed-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="ac2ed-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="ac2ed-157">isFeatured</span></span>|<span data-ttu-id="ac2ed-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="ac2ed-158">Boolean</span></span>|<span data-ttu-id="ac2ed-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="ac2ed-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="ac2ed-160">privacyInformationUrl</span></span>|<span data-ttu-id="ac2ed-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac2ed-161">String</span></span>|<span data-ttu-id="ac2ed-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-162">The privacy statement Url.</span></span> <span data-ttu-id="ac2ed-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="ac2ed-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="ac2ed-164">informationUrl</span></span>|<span data-ttu-id="ac2ed-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac2ed-165">String</span></span>|<span data-ttu-id="ac2ed-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-166">The more information Url.</span></span> <span data-ttu-id="ac2ed-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="ac2ed-168">owner</span><span class="sxs-lookup"><span data-stu-id="ac2ed-168">owner</span></span>|<span data-ttu-id="ac2ed-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac2ed-169">String</span></span>|<span data-ttu-id="ac2ed-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-170">The owner of the app.</span></span> <span data-ttu-id="ac2ed-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="ac2ed-172">developer</span><span class="sxs-lookup"><span data-stu-id="ac2ed-172">developer</span></span>|<span data-ttu-id="ac2ed-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac2ed-173">String</span></span>|<span data-ttu-id="ac2ed-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-174">The developer of the app.</span></span> <span data-ttu-id="ac2ed-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="ac2ed-176">notes</span><span class="sxs-lookup"><span data-stu-id="ac2ed-176">notes</span></span>|<span data-ttu-id="ac2ed-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac2ed-177">String</span></span>|<span data-ttu-id="ac2ed-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-178">Notes for the app.</span></span> <span data-ttu-id="ac2ed-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="ac2ed-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="ac2ed-180">publishingState</span></span>|[<span data-ttu-id="ac2ed-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="ac2ed-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="ac2ed-p114">El estado de publicación para la aplicación. La aplicación no se puede asignar a menos que se publique la aplicación. Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing`, `published`.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-p114">The publishing state for the app. The app cannot be assigned unless the app is published. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md). The possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="ac2ed-186">appAvailability</span><span class="sxs-lookup"><span data-stu-id="ac2ed-186">appAvailability</span></span>|[<span data-ttu-id="ac2ed-187">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="ac2ed-187">managedAppAvailability</span></span>](../resources/intune_apps_managedappavailability.md)|<span data-ttu-id="ac2ed-p115">Disponibilidad de la aplicación. Se hereda de [managedApp](../resources/intune_apps_managedapp.md). Los valores posibles son: `global`, `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-p115">The Application's availability. Inherited from [managedApp](../resources/intune_apps_managedapp.md). The possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="ac2ed-191">version</span><span class="sxs-lookup"><span data-stu-id="ac2ed-191">version</span></span>|<span data-ttu-id="ac2ed-192">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac2ed-192">String</span></span>|<span data-ttu-id="ac2ed-193">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-193">The Application's version.</span></span> <span data-ttu-id="ac2ed-194">Heredado de [managedApp](../resources/intune_apps_managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="ac2ed-194">Inherited from [managedApp](../resources/intune_apps_managedapp.md)</span></span>|
|<span data-ttu-id="ac2ed-195">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="ac2ed-195">committedContentVersion</span></span>|<span data-ttu-id="ac2ed-196">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac2ed-196">String</span></span>|<span data-ttu-id="ac2ed-197">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-197">The internal committed content version.</span></span> <span data-ttu-id="ac2ed-198">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-198">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="ac2ed-199">fileName</span><span class="sxs-lookup"><span data-stu-id="ac2ed-199">fileName</span></span>|<span data-ttu-id="ac2ed-200">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac2ed-200">String</span></span>|<span data-ttu-id="ac2ed-201">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-201">The name of the main Lob application file.</span></span> <span data-ttu-id="ac2ed-202">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-202">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="ac2ed-203">size</span><span class="sxs-lookup"><span data-stu-id="ac2ed-203">size</span></span>|<span data-ttu-id="ac2ed-204">Int64</span><span class="sxs-lookup"><span data-stu-id="ac2ed-204">Int64</span></span>|<span data-ttu-id="ac2ed-205">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-205">The total size, including all uploaded files.</span></span> <span data-ttu-id="ac2ed-206">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="ac2ed-206">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="ac2ed-207">packageId</span><span class="sxs-lookup"><span data-stu-id="ac2ed-207">packageId</span></span>|<span data-ttu-id="ac2ed-208">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac2ed-208">String</span></span>|<span data-ttu-id="ac2ed-209">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-209">The package identifier.</span></span>|
|<span data-ttu-id="ac2ed-210">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="ac2ed-210">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="ac2ed-211">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="ac2ed-211">androidMinimumOperatingSystem</span></span>](../resources/intune_apps_androidminimumoperatingsystem.md)|<span data-ttu-id="ac2ed-212">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-212">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="ac2ed-213">versionName</span><span class="sxs-lookup"><span data-stu-id="ac2ed-213">versionName</span></span>|<span data-ttu-id="ac2ed-214">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac2ed-214">String</span></span>|<span data-ttu-id="ac2ed-215">Nombre de versión de la aplicación administrada de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-215">The version name of managed Android Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="ac2ed-216">versionCode</span><span class="sxs-lookup"><span data-stu-id="ac2ed-216">versionCode</span></span>|<span data-ttu-id="ac2ed-217">Cadena</span><span class="sxs-lookup"><span data-stu-id="ac2ed-217">String</span></span>|<span data-ttu-id="ac2ed-218">Código de versión de la aplicación administrada de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-218">The version code of managed Android Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="ac2ed-219">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac2ed-219">Response</span></span>
<span data-ttu-id="ac2ed-220">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedAndroidLobApp](../resources/intune_apps_managedandroidlobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-220">If successful, this method returns a `201 Created` response code and a [managedAndroidLobApp](../resources/intune_apps_managedandroidlobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ac2ed-221">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac2ed-221">Example</span></span>
### <a name="request"></a><span data-ttu-id="ac2ed-222">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ac2ed-222">Request</span></span>
<span data-ttu-id="ac2ed-223">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-223">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1217

{
  "@odata.type": "#microsoft.graph.managedAndroidLobApp",
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
  "appAvailability": "lineOfBusiness",
  "version": "Version value",
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

### <a name="response"></a><span data-ttu-id="ac2ed-224">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac2ed-224">Response</span></span>
<span data-ttu-id="ac2ed-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ac2ed-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1325

{
  "@odata.type": "#microsoft.graph.managedAndroidLobApp",
  "id": "802b7ed3-7ed3-802b-d37e-2b80d37e2b80",
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
  "appAvailability": "lineOfBusiness",
  "version": "Version value",
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








