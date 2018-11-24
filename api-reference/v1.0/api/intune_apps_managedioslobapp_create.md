# <a name="create-managedioslobapp"></a><span data-ttu-id="a0d84-101">Crear managedIOSLobApp</span><span class="sxs-lookup"><span data-stu-id="a0d84-101">Create managedIOSLobApp</span></span>

> <span data-ttu-id="a0d84-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a0d84-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a0d84-103">Crear un objeto [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-103">Create a new [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a0d84-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a0d84-104">Prerequisites</span></span>
<span data-ttu-id="a0d84-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a0d84-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a0d84-107">Permission type</span></span>|<span data-ttu-id="a0d84-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a0d84-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a0d84-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a0d84-109">Delegated (work or school account)</span></span>|<span data-ttu-id="a0d84-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a0d84-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="a0d84-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a0d84-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a0d84-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a0d84-112">Not supported.</span></span>|
|<span data-ttu-id="a0d84-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a0d84-113">Application</span></span>|<span data-ttu-id="a0d84-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="a0d84-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a0d84-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a0d84-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="a0d84-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a0d84-116">Request headers</span></span>
|<span data-ttu-id="a0d84-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0d84-117">Header</span></span>|<span data-ttu-id="a0d84-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a0d84-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a0d84-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="a0d84-119">Authorization</span></span>|<span data-ttu-id="a0d84-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a0d84-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a0d84-121">Accept</span><span class="sxs-lookup"><span data-stu-id="a0d84-121">Accept</span></span>|<span data-ttu-id="a0d84-122">application/json</span><span class="sxs-lookup"><span data-stu-id="a0d84-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a0d84-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a0d84-123">Request body</span></span>
<span data-ttu-id="a0d84-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedIOSLobApp.</span><span class="sxs-lookup"><span data-stu-id="a0d84-124">In the request body, supply a JSON representation for the managedIOSLobApp object.</span></span>

<span data-ttu-id="a0d84-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedIOSLobApp.</span><span class="sxs-lookup"><span data-stu-id="a0d84-125">The following table shows the properties that are required when you create the managedIOSLobApp.</span></span>

|<span data-ttu-id="a0d84-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a0d84-126">Property</span></span>|<span data-ttu-id="a0d84-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0d84-127">Type</span></span>|<span data-ttu-id="a0d84-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0d84-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a0d84-129">id</span><span class="sxs-lookup"><span data-stu-id="a0d84-129">id</span></span>|<span data-ttu-id="a0d84-130">String</span><span class="sxs-lookup"><span data-stu-id="a0d84-130">String</span></span>|<span data-ttu-id="a0d84-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a0d84-131">Key of the entity.</span></span> <span data-ttu-id="a0d84-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a0d84-133">displayName</span><span class="sxs-lookup"><span data-stu-id="a0d84-133">displayName</span></span>|<span data-ttu-id="a0d84-134">String</span><span class="sxs-lookup"><span data-stu-id="a0d84-134">String</span></span>|<span data-ttu-id="a0d84-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="a0d84-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="a0d84-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a0d84-137">description</span><span class="sxs-lookup"><span data-stu-id="a0d84-137">description</span></span>|<span data-ttu-id="a0d84-138">String</span><span class="sxs-lookup"><span data-stu-id="a0d84-138">String</span></span>|<span data-ttu-id="a0d84-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a0d84-139">The description of the app.</span></span> <span data-ttu-id="a0d84-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a0d84-141">publisher</span><span class="sxs-lookup"><span data-stu-id="a0d84-141">publisher</span></span>|<span data-ttu-id="a0d84-142">String</span><span class="sxs-lookup"><span data-stu-id="a0d84-142">String</span></span>|<span data-ttu-id="a0d84-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a0d84-143">The publisher of the app.</span></span> <span data-ttu-id="a0d84-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a0d84-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="a0d84-145">largeIcon</span></span>|[<span data-ttu-id="a0d84-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="a0d84-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="a0d84-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="a0d84-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="a0d84-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a0d84-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a0d84-149">createdDateTime</span></span>|<span data-ttu-id="a0d84-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a0d84-150">DateTimeOffset</span></span>|<span data-ttu-id="a0d84-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a0d84-151">The date and time the app was created.</span></span> <span data-ttu-id="a0d84-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a0d84-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a0d84-153">lastModifiedDateTime</span></span>|<span data-ttu-id="a0d84-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a0d84-154">DateTimeOffset</span></span>|<span data-ttu-id="a0d84-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a0d84-155">The date and time the app was last modified.</span></span> <span data-ttu-id="a0d84-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a0d84-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="a0d84-157">isFeatured</span></span>|<span data-ttu-id="a0d84-158">Boolean</span><span class="sxs-lookup"><span data-stu-id="a0d84-158">Boolean</span></span>|<span data-ttu-id="a0d84-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a0d84-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="a0d84-160">privacyInformationUrl</span></span>|<span data-ttu-id="a0d84-161">String</span><span class="sxs-lookup"><span data-stu-id="a0d84-161">String</span></span>|<span data-ttu-id="a0d84-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="a0d84-162">The privacy statement Url.</span></span> <span data-ttu-id="a0d84-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a0d84-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="a0d84-164">informationUrl</span></span>|<span data-ttu-id="a0d84-165">String</span><span class="sxs-lookup"><span data-stu-id="a0d84-165">String</span></span>|<span data-ttu-id="a0d84-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a0d84-166">The more information Url.</span></span> <span data-ttu-id="a0d84-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a0d84-168">owner</span><span class="sxs-lookup"><span data-stu-id="a0d84-168">owner</span></span>|<span data-ttu-id="a0d84-169">String</span><span class="sxs-lookup"><span data-stu-id="a0d84-169">String</span></span>|<span data-ttu-id="a0d84-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a0d84-170">The owner of the app.</span></span> <span data-ttu-id="a0d84-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a0d84-172">developer</span><span class="sxs-lookup"><span data-stu-id="a0d84-172">developer</span></span>|<span data-ttu-id="a0d84-173">String</span><span class="sxs-lookup"><span data-stu-id="a0d84-173">String</span></span>|<span data-ttu-id="a0d84-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a0d84-174">The developer of the app.</span></span> <span data-ttu-id="a0d84-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a0d84-176">notes</span><span class="sxs-lookup"><span data-stu-id="a0d84-176">notes</span></span>|<span data-ttu-id="a0d84-177">String</span><span class="sxs-lookup"><span data-stu-id="a0d84-177">String</span></span>|<span data-ttu-id="a0d84-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a0d84-178">Notes for the app.</span></span> <span data-ttu-id="a0d84-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="a0d84-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="a0d84-180">publishingState</span></span>|[<span data-ttu-id="a0d84-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="a0d84-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="a0d84-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a0d84-182">The publishing state for the app.</span></span> <span data-ttu-id="a0d84-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="a0d84-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="a0d84-184">Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md).</span></span> <span data-ttu-id="a0d84-185">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="a0d84-185">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="a0d84-186">appAvailability</span><span class="sxs-lookup"><span data-stu-id="a0d84-186">appAvailability</span></span>|[<span data-ttu-id="a0d84-187">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="a0d84-187">managedAppAvailability</span></span>](../resources/intune_apps_managedappavailability.md)|<span data-ttu-id="a0d84-188">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a0d84-188">The Application's availability.</span></span> <span data-ttu-id="a0d84-189">Se hereda de [managedApp](../resources/intune_apps_managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-189">Inherited from [managedApp](../resources/intune_apps_managedapp.md).</span></span> <span data-ttu-id="a0d84-190">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="a0d84-190">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="a0d84-191">versión</span><span class="sxs-lookup"><span data-stu-id="a0d84-191">version</span></span>|<span data-ttu-id="a0d84-192">String</span><span class="sxs-lookup"><span data-stu-id="a0d84-192">String</span></span>|<span data-ttu-id="a0d84-193">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a0d84-193">The Application's version.</span></span> <span data-ttu-id="a0d84-194">Heredado de [managedApp](../resources/intune_apps_managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="a0d84-194">Inherited from [managedApp](../resources/intune_apps_managedapp.md)</span></span>|
|<span data-ttu-id="a0d84-195">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="a0d84-195">committedContentVersion</span></span>|<span data-ttu-id="a0d84-196">String</span><span class="sxs-lookup"><span data-stu-id="a0d84-196">String</span></span>|<span data-ttu-id="a0d84-197">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="a0d84-197">The internal committed content version.</span></span> <span data-ttu-id="a0d84-198">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-198">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="a0d84-199">fileName</span><span class="sxs-lookup"><span data-stu-id="a0d84-199">fileName</span></span>|<span data-ttu-id="a0d84-200">String</span><span class="sxs-lookup"><span data-stu-id="a0d84-200">String</span></span>|<span data-ttu-id="a0d84-201">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="a0d84-201">The name of the main Lob application file.</span></span> <span data-ttu-id="a0d84-202">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-202">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="a0d84-203">size</span><span class="sxs-lookup"><span data-stu-id="a0d84-203">size</span></span>|<span data-ttu-id="a0d84-204">Int64</span><span class="sxs-lookup"><span data-stu-id="a0d84-204">Int64</span></span>|<span data-ttu-id="a0d84-205">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="a0d84-205">The total size, including all uploaded files.</span></span> <span data-ttu-id="a0d84-206">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="a0d84-206">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="a0d84-207">bundleId</span><span class="sxs-lookup"><span data-stu-id="a0d84-207">bundleId</span></span>|<span data-ttu-id="a0d84-208">String</span><span class="sxs-lookup"><span data-stu-id="a0d84-208">String</span></span>|<span data-ttu-id="a0d84-209">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="a0d84-209">The Identity Name.</span></span>|
|<span data-ttu-id="a0d84-210">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="a0d84-210">applicableDeviceType</span></span>|[<span data-ttu-id="a0d84-211">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="a0d84-211">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="a0d84-212">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="a0d84-212">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="a0d84-213">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a0d84-213">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="a0d84-214">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a0d84-214">iosMinimumOperatingSystem</span></span>](../resources/intune_apps_iosminimumoperatingsystem.md)|<span data-ttu-id="a0d84-215">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="a0d84-215">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="a0d84-216">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="a0d84-216">expirationDateTime</span></span>|<span data-ttu-id="a0d84-217">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a0d84-217">DateTimeOffset</span></span>|<span data-ttu-id="a0d84-218">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="a0d84-218">The expiration time.</span></span>|
|<span data-ttu-id="a0d84-219">versionNumber</span><span class="sxs-lookup"><span data-stu-id="a0d84-219">versionNumber</span></span>|<span data-ttu-id="a0d84-220">String</span><span class="sxs-lookup"><span data-stu-id="a0d84-220">String</span></span>|<span data-ttu-id="a0d84-221">Número de versión de la aplicación administrada de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="a0d84-221">The version number of managed iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="a0d84-222">buildNumber</span><span class="sxs-lookup"><span data-stu-id="a0d84-222">buildNumber</span></span>|<span data-ttu-id="a0d84-223">String</span><span class="sxs-lookup"><span data-stu-id="a0d84-223">String</span></span>|<span data-ttu-id="a0d84-224">Número de compilación de la aplicación administrada de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="a0d84-224">The build number of managed iOS Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="a0d84-225">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0d84-225">Response</span></span>
<span data-ttu-id="a0d84-226">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0d84-226">If successful, this method returns a `201 Created` response code and a [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a0d84-227">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0d84-227">Example</span></span>
### <a name="request"></a><span data-ttu-id="a0d84-228">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a0d84-228">Request</span></span>
<span data-ttu-id="a0d84-229">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a0d84-229">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1287

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
    "v11_0": true,
    "v12_0": true
  },
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "versionNumber": "Version Number value",
  "buildNumber": "Build Number value"
}
```

### <a name="response"></a><span data-ttu-id="a0d84-230">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0d84-230">Response</span></span>
<span data-ttu-id="a0d84-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a0d84-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1459

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
    "v11_0": true,
    "v12_0": true
  },
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "versionNumber": "Version Number value",
  "buildNumber": "Build Number value"
}
```



