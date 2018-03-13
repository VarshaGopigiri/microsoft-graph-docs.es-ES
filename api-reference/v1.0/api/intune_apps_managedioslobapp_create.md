# <a name="create-managedioslobapp"></a><span data-ttu-id="edc09-101">Crear managedIOSLobApp</span><span class="sxs-lookup"><span data-stu-id="edc09-101">Create managedIOSLobApp</span></span>

> <span data-ttu-id="edc09-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="edc09-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="edc09-103">Crear un objeto [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-103">Create a new [plannerBucket](../resources/intune_apps_managedioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="edc09-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="edc09-104">Prerequisites</span></span>
<span data-ttu-id="edc09-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="edc09-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="edc09-107">Permission type</span></span>|<span data-ttu-id="edc09-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="edc09-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="edc09-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="edc09-109">Delegated (work or school account)</span></span>|<span data-ttu-id="edc09-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="edc09-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="edc09-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="edc09-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="edc09-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="edc09-112">Not supported.</span></span>|
|<span data-ttu-id="edc09-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="edc09-113">Application</span></span>|<span data-ttu-id="edc09-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="edc09-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="edc09-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="edc09-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="edc09-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="edc09-116">Request headers</span></span>
|<span data-ttu-id="edc09-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edc09-117">Header</span></span>|<span data-ttu-id="edc09-118">Valor</span><span class="sxs-lookup"><span data-stu-id="edc09-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="edc09-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="edc09-119">Authorization</span></span>|<span data-ttu-id="edc09-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="edc09-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="edc09-121">Accept</span><span class="sxs-lookup"><span data-stu-id="edc09-121">Accept</span></span>|<span data-ttu-id="edc09-122">application/json</span><span class="sxs-lookup"><span data-stu-id="edc09-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="edc09-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="edc09-123">Request body</span></span>
<span data-ttu-id="edc09-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedIOSLobApp.</span><span class="sxs-lookup"><span data-stu-id="edc09-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="edc09-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedIOSLobApp.</span><span class="sxs-lookup"><span data-stu-id="edc09-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="edc09-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="edc09-126">Property</span></span>|<span data-ttu-id="edc09-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="edc09-127">Type</span></span>|<span data-ttu-id="edc09-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="edc09-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="edc09-129">id</span><span class="sxs-lookup"><span data-stu-id="edc09-129">id</span></span>|<span data-ttu-id="edc09-130">String</span><span class="sxs-lookup"><span data-stu-id="edc09-130">String</span></span>|<span data-ttu-id="edc09-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="edc09-131">Key of the setting.</span></span> <span data-ttu-id="edc09-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="edc09-133">displayName</span><span class="sxs-lookup"><span data-stu-id="edc09-133">displayName</span></span>|<span data-ttu-id="edc09-134">String</span><span class="sxs-lookup"><span data-stu-id="edc09-134">String</span></span>|<span data-ttu-id="edc09-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="edc09-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="edc09-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="edc09-137">description</span><span class="sxs-lookup"><span data-stu-id="edc09-137">description</span></span>|<span data-ttu-id="edc09-138">String</span><span class="sxs-lookup"><span data-stu-id="edc09-138">String</span></span>|<span data-ttu-id="edc09-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="edc09-139">The description of the app.</span></span> <span data-ttu-id="edc09-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="edc09-141">publisher</span><span class="sxs-lookup"><span data-stu-id="edc09-141">Publisher</span></span>|<span data-ttu-id="edc09-142">String</span><span class="sxs-lookup"><span data-stu-id="edc09-142">String</span></span>|<span data-ttu-id="edc09-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="edc09-143">The name of the app.</span></span> <span data-ttu-id="edc09-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="edc09-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="edc09-145">largeIcon</span></span>|[<span data-ttu-id="edc09-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="edc09-146">mimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="edc09-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="edc09-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="edc09-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="edc09-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="edc09-149">createdDateTime</span></span>|<span data-ttu-id="edc09-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="edc09-150">DateTimeOffset</span></span>|<span data-ttu-id="edc09-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="edc09-151">The date and time when the page was created.</span></span> <span data-ttu-id="edc09-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="edc09-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="edc09-153">lastModifiedDateTime</span></span>|<span data-ttu-id="edc09-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="edc09-154">DateTimeOffset</span></span>|<span data-ttu-id="edc09-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="edc09-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="edc09-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="edc09-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="edc09-157">isFeatured</span></span>|<span data-ttu-id="edc09-158">Boolean</span><span class="sxs-lookup"><span data-stu-id="edc09-158">Boolean</span></span>|<span data-ttu-id="edc09-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="edc09-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="edc09-160">privacyInformationUrl</span></span>|<span data-ttu-id="edc09-161">String</span><span class="sxs-lookup"><span data-stu-id="edc09-161">String</span></span>|<span data-ttu-id="edc09-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="edc09-162">The privacy statement Url.</span></span> <span data-ttu-id="edc09-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="edc09-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="edc09-164">informationUrl</span></span>|<span data-ttu-id="edc09-165">String</span><span class="sxs-lookup"><span data-stu-id="edc09-165">String</span></span>|<span data-ttu-id="edc09-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="edc09-166">The more information Url.</span></span> <span data-ttu-id="edc09-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="edc09-168">owner</span><span class="sxs-lookup"><span data-stu-id="edc09-168">owner</span></span>|<span data-ttu-id="edc09-169">String</span><span class="sxs-lookup"><span data-stu-id="edc09-169">String</span></span>|<span data-ttu-id="edc09-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="edc09-170">The owner of the timesheet.</span></span> <span data-ttu-id="edc09-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="edc09-172">developer</span><span class="sxs-lookup"><span data-stu-id="edc09-172">developer</span></span>|<span data-ttu-id="edc09-173">String</span><span class="sxs-lookup"><span data-stu-id="edc09-173">String</span></span>|<span data-ttu-id="edc09-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="edc09-174">The name of the app.</span></span> <span data-ttu-id="edc09-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="edc09-176">notes</span><span class="sxs-lookup"><span data-stu-id="edc09-176">Notes</span></span>|<span data-ttu-id="edc09-177">String</span><span class="sxs-lookup"><span data-stu-id="edc09-177">String</span></span>|<span data-ttu-id="edc09-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="edc09-178">Notes for the app.</span></span> <span data-ttu-id="edc09-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="edc09-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="edc09-180">publishingState</span></span>|<span data-ttu-id="edc09-181">String</span><span class="sxs-lookup"><span data-stu-id="edc09-181">String</span></span>|<span data-ttu-id="edc09-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="edc09-182">The publishing state for the app.</span></span> <span data-ttu-id="edc09-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="edc09-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="edc09-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="edc09-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="edc09-185">appAvailability</span><span class="sxs-lookup"><span data-stu-id="edc09-185">appAvailability</span></span>|<span data-ttu-id="edc09-186">String</span><span class="sxs-lookup"><span data-stu-id="edc09-186">String</span></span>|<span data-ttu-id="edc09-187">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="edc09-187">The Application's availability.</span></span> <span data-ttu-id="edc09-188">Heredado de [managedApp](../resources/intune_apps_managedapp.md). Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="edc09-188">Inherited from [managedApp](../resources/intune_apps_managedapp.md) Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="edc09-189">version</span><span class="sxs-lookup"><span data-stu-id="edc09-189">version</span></span>|<span data-ttu-id="edc09-190">String</span><span class="sxs-lookup"><span data-stu-id="edc09-190">String</span></span>|<span data-ttu-id="edc09-191">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="edc09-191">The Application's version.</span></span> <span data-ttu-id="edc09-192">Heredado de [managedApp](../resources/intune_apps_managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="edc09-192">Inherited from [managedApp](../resources/intune_apps_managedapp.md)</span></span>|
|<span data-ttu-id="edc09-193">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="edc09-193">committedContentVersion</span></span>|<span data-ttu-id="edc09-194">String</span><span class="sxs-lookup"><span data-stu-id="edc09-194">String</span></span>|<span data-ttu-id="edc09-195">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="edc09-195">The internal committed content version.</span></span> <span data-ttu-id="edc09-196">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-196">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="edc09-197">fileName</span><span class="sxs-lookup"><span data-stu-id="edc09-197">fileName</span></span>|<span data-ttu-id="edc09-198">String</span><span class="sxs-lookup"><span data-stu-id="edc09-198">String</span></span>|<span data-ttu-id="edc09-199">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="edc09-199">The name of the main Lob application file.</span></span> <span data-ttu-id="edc09-200">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-200">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="edc09-201">size</span><span class="sxs-lookup"><span data-stu-id="edc09-201">size</span></span>|<span data-ttu-id="edc09-202">Int64</span><span class="sxs-lookup"><span data-stu-id="edc09-202">Int64</span></span>|<span data-ttu-id="edc09-203">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="edc09-203">The total size, including all uploaded files.</span></span> <span data-ttu-id="edc09-204">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="edc09-204">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="edc09-205">bundleId</span><span class="sxs-lookup"><span data-stu-id="edc09-205">bundleId</span></span>|<span data-ttu-id="edc09-206">String</span><span class="sxs-lookup"><span data-stu-id="edc09-206">String</span></span>|<span data-ttu-id="edc09-207">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="edc09-207">The Identity Name.</span></span>|
|<span data-ttu-id="edc09-208">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="edc09-208">applicableDeviceType</span></span>|[<span data-ttu-id="edc09-209">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="edc09-209">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="edc09-210">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="edc09-210">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="edc09-211">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="edc09-211">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="edc09-212">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="edc09-212">iosMinimumOperatingSystem</span></span>](../resources/intune_apps_iosminimumoperatingsystem.md)|<span data-ttu-id="edc09-213">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="edc09-213">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="edc09-214">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="edc09-214">expirationDateTime</span></span>|<span data-ttu-id="edc09-215">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="edc09-215">DateTimeOffset</span></span>|<span data-ttu-id="edc09-216">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="edc09-216">: The expiration time for the subscription.</span></span>|
|<span data-ttu-id="edc09-217">versionNumber</span><span class="sxs-lookup"><span data-stu-id="edc09-217">versionNumber</span></span>|<span data-ttu-id="edc09-218">String</span><span class="sxs-lookup"><span data-stu-id="edc09-218">String</span></span>|<span data-ttu-id="edc09-219">Número de versión de la aplicación administrada de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="edc09-219">The version number of managed iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="edc09-220">buildNumber</span><span class="sxs-lookup"><span data-stu-id="edc09-220">buildNumber</span></span>|<span data-ttu-id="edc09-221">String</span><span class="sxs-lookup"><span data-stu-id="edc09-221">String</span></span>|<span data-ttu-id="edc09-222">Número de compilación de la aplicación administrada de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="edc09-222">The build number of managed iOS Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="edc09-223">Respuesta</span><span class="sxs-lookup"><span data-stu-id="edc09-223">Response</span></span>
<span data-ttu-id="edc09-224">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="edc09-224">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_apps_managedioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="edc09-225">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="edc09-225">Example</span></span>
### <a name="request"></a><span data-ttu-id="edc09-226">Solicitud</span><span class="sxs-lookup"><span data-stu-id="edc09-226">Request</span></span>
<span data-ttu-id="edc09-227">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="edc09-227">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1331

{
  "@odata.type": "#microsoft.graph.managedIOSLobApp",
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

### <a name="response"></a><span data-ttu-id="edc09-228">Respuesta</span><span class="sxs-lookup"><span data-stu-id="edc09-228">Response</span></span>
<span data-ttu-id="edc09-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="edc09-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1439

{
  "@odata.type": "#microsoft.graph.managedIOSLobApp",
  "id": "8f59792d-792d-8f59-2d79-598f2d79598f",
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



