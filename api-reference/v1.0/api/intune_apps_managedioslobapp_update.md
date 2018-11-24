# <a name="update-managedioslobapp"></a><span data-ttu-id="0a2a4-101">Actualizar managedIOSLobApp</span><span class="sxs-lookup"><span data-stu-id="0a2a4-101">Update managedIOSLobApp</span></span>

> <span data-ttu-id="0a2a4-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0a2a4-103">Actualice las propiedades de un objeto [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-103">Update the properties of a [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0a2a4-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0a2a4-104">Prerequisites</span></span>
<span data-ttu-id="0a2a4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0a2a4-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0a2a4-107">Permission type</span></span>|<span data-ttu-id="0a2a4-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0a2a4-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0a2a4-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0a2a4-109">Delegated (work or school account)</span></span>|<span data-ttu-id="0a2a4-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0a2a4-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="0a2a4-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0a2a4-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0a2a4-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-112">Not supported.</span></span>|
|<span data-ttu-id="0a2a4-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0a2a4-113">Application</span></span>|<span data-ttu-id="0a2a4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0a2a4-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0a2a4-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="0a2a4-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0a2a4-116">Request headers</span></span>
|<span data-ttu-id="0a2a4-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a2a4-117">Header</span></span>|<span data-ttu-id="0a2a4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0a2a4-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0a2a4-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="0a2a4-119">Authorization</span></span>|<span data-ttu-id="0a2a4-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0a2a4-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0a2a4-121">Accept</span></span>|<span data-ttu-id="0a2a4-122">application/json</span><span class="sxs-lookup"><span data-stu-id="0a2a4-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0a2a4-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0a2a4-123">Request body</span></span>
<span data-ttu-id="0a2a4-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-124">In the request body, supply a JSON representation for the [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md) object.</span></span>

<span data-ttu-id="0a2a4-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-125">The following table shows the properties that are required when you create the [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md).</span></span>

|<span data-ttu-id="0a2a4-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0a2a4-126">Property</span></span>|<span data-ttu-id="0a2a4-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a2a4-127">Type</span></span>|<span data-ttu-id="0a2a4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a2a4-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0a2a4-129">id</span><span class="sxs-lookup"><span data-stu-id="0a2a4-129">id</span></span>|<span data-ttu-id="0a2a4-130">String</span><span class="sxs-lookup"><span data-stu-id="0a2a4-130">String</span></span>|<span data-ttu-id="0a2a4-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-131">Key of the entity.</span></span> <span data-ttu-id="0a2a4-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="0a2a4-133">displayName</span><span class="sxs-lookup"><span data-stu-id="0a2a4-133">displayName</span></span>|<span data-ttu-id="0a2a4-134">String</span><span class="sxs-lookup"><span data-stu-id="0a2a4-134">String</span></span>|<span data-ttu-id="0a2a4-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="0a2a4-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="0a2a4-137">description</span><span class="sxs-lookup"><span data-stu-id="0a2a4-137">description</span></span>|<span data-ttu-id="0a2a4-138">String</span><span class="sxs-lookup"><span data-stu-id="0a2a4-138">String</span></span>|<span data-ttu-id="0a2a4-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-139">The description of the app.</span></span> <span data-ttu-id="0a2a4-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="0a2a4-141">publicador</span><span class="sxs-lookup"><span data-stu-id="0a2a4-141">publisher</span></span>|<span data-ttu-id="0a2a4-142">String</span><span class="sxs-lookup"><span data-stu-id="0a2a4-142">String</span></span>|<span data-ttu-id="0a2a4-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-143">The publisher of the app.</span></span> <span data-ttu-id="0a2a4-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="0a2a4-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="0a2a4-145">largeIcon</span></span>|[<span data-ttu-id="0a2a4-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="0a2a4-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="0a2a4-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="0a2a4-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="0a2a4-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="0a2a4-149">createdDateTime</span></span>|<span data-ttu-id="0a2a4-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0a2a4-150">DateTimeOffset</span></span>|<span data-ttu-id="0a2a4-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-151">The date and time the app was created.</span></span> <span data-ttu-id="0a2a4-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="0a2a4-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0a2a4-153">lastModifiedDateTime</span></span>|<span data-ttu-id="0a2a4-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0a2a4-154">DateTimeOffset</span></span>|<span data-ttu-id="0a2a4-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-155">The date and time the app was last modified.</span></span> <span data-ttu-id="0a2a4-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="0a2a4-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="0a2a4-157">isFeatured</span></span>|<span data-ttu-id="0a2a4-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="0a2a4-158">Boolean</span></span>|<span data-ttu-id="0a2a4-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="0a2a4-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="0a2a4-160">privacyInformationUrl</span></span>|<span data-ttu-id="0a2a4-161">String</span><span class="sxs-lookup"><span data-stu-id="0a2a4-161">String</span></span>|<span data-ttu-id="0a2a4-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-162">The privacy statement Url.</span></span> <span data-ttu-id="0a2a4-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="0a2a4-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="0a2a4-164">informationUrl</span></span>|<span data-ttu-id="0a2a4-165">String</span><span class="sxs-lookup"><span data-stu-id="0a2a4-165">String</span></span>|<span data-ttu-id="0a2a4-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-166">The more information Url.</span></span> <span data-ttu-id="0a2a4-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="0a2a4-168">owner</span><span class="sxs-lookup"><span data-stu-id="0a2a4-168">owner</span></span>|<span data-ttu-id="0a2a4-169">String</span><span class="sxs-lookup"><span data-stu-id="0a2a4-169">String</span></span>|<span data-ttu-id="0a2a4-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-170">The owner of the app.</span></span> <span data-ttu-id="0a2a4-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="0a2a4-172">developer</span><span class="sxs-lookup"><span data-stu-id="0a2a4-172">developer</span></span>|<span data-ttu-id="0a2a4-173">String</span><span class="sxs-lookup"><span data-stu-id="0a2a4-173">String</span></span>|<span data-ttu-id="0a2a4-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-174">The developer of the app.</span></span> <span data-ttu-id="0a2a4-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="0a2a4-176">notas</span><span class="sxs-lookup"><span data-stu-id="0a2a4-176">notes</span></span>|<span data-ttu-id="0a2a4-177">String</span><span class="sxs-lookup"><span data-stu-id="0a2a4-177">String</span></span>|<span data-ttu-id="0a2a4-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-178">Notes for the app.</span></span> <span data-ttu-id="0a2a4-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="0a2a4-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="0a2a4-180">publishingState</span></span>|[<span data-ttu-id="0a2a4-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="0a2a4-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="0a2a4-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-182">The publishing state for the app.</span></span> <span data-ttu-id="0a2a4-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="0a2a4-184">Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md).</span></span> <span data-ttu-id="0a2a4-185">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-185">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="0a2a4-186">appAvailability</span><span class="sxs-lookup"><span data-stu-id="0a2a4-186">appAvailability</span></span>|[<span data-ttu-id="0a2a4-187">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="0a2a4-187">managedAppAvailability</span></span>](../resources/intune_apps_managedappavailability.md)|<span data-ttu-id="0a2a4-188">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-188">The Application's availability.</span></span> <span data-ttu-id="0a2a4-189">Se hereda de [managedApp](../resources/intune_apps_managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-189">Inherited from [managedApp](../resources/intune_apps_managedapp.md).</span></span> <span data-ttu-id="0a2a4-190">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-190">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="0a2a4-191">versión</span><span class="sxs-lookup"><span data-stu-id="0a2a4-191">version</span></span>|<span data-ttu-id="0a2a4-192">String</span><span class="sxs-lookup"><span data-stu-id="0a2a4-192">String</span></span>|<span data-ttu-id="0a2a4-193">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-193">The Application's version.</span></span> <span data-ttu-id="0a2a4-194">Heredado de [managedApp](../resources/intune_apps_managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="0a2a4-194">Inherited from [managedApp](../resources/intune_apps_managedapp.md)</span></span>|
|<span data-ttu-id="0a2a4-195">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="0a2a4-195">committedContentVersion</span></span>|<span data-ttu-id="0a2a4-196">String</span><span class="sxs-lookup"><span data-stu-id="0a2a4-196">String</span></span>|<span data-ttu-id="0a2a4-197">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-197">The internal committed content version.</span></span> <span data-ttu-id="0a2a4-198">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-198">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="0a2a4-199">fileName</span><span class="sxs-lookup"><span data-stu-id="0a2a4-199">fileName</span></span>|<span data-ttu-id="0a2a4-200">String</span><span class="sxs-lookup"><span data-stu-id="0a2a4-200">String</span></span>|<span data-ttu-id="0a2a4-201">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-201">The name of the main Lob application file.</span></span> <span data-ttu-id="0a2a4-202">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-202">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="0a2a4-203">size</span><span class="sxs-lookup"><span data-stu-id="0a2a4-203">size</span></span>|<span data-ttu-id="0a2a4-204">Int64</span><span class="sxs-lookup"><span data-stu-id="0a2a4-204">Int64</span></span>|<span data-ttu-id="0a2a4-205">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-205">The total size, including all uploaded files.</span></span> <span data-ttu-id="0a2a4-206">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="0a2a4-206">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="0a2a4-207">bundleId</span><span class="sxs-lookup"><span data-stu-id="0a2a4-207">bundleId</span></span>|<span data-ttu-id="0a2a4-208">String</span><span class="sxs-lookup"><span data-stu-id="0a2a4-208">String</span></span>|<span data-ttu-id="0a2a4-209">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-209">The Identity Name.</span></span>|
|<span data-ttu-id="0a2a4-210">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="0a2a4-210">applicableDeviceType</span></span>|[<span data-ttu-id="0a2a4-211">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="0a2a4-211">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="0a2a4-212">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-212">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="0a2a4-213">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="0a2a4-213">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="0a2a4-214">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="0a2a4-214">iosMinimumOperatingSystem</span></span>](../resources/intune_apps_iosminimumoperatingsystem.md)|<span data-ttu-id="0a2a4-215">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-215">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="0a2a4-216">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="0a2a4-216">expirationDateTime</span></span>|<span data-ttu-id="0a2a4-217">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0a2a4-217">DateTimeOffset</span></span>|<span data-ttu-id="0a2a4-218">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-218">The expiration time.</span></span>|
|<span data-ttu-id="0a2a4-219">versionNumber</span><span class="sxs-lookup"><span data-stu-id="0a2a4-219">versionNumber</span></span>|<span data-ttu-id="0a2a4-220">String</span><span class="sxs-lookup"><span data-stu-id="0a2a4-220">String</span></span>|<span data-ttu-id="0a2a4-221">Número de versión de la aplicación administrada de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-221">The version number of managed iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="0a2a4-222">buildNumber</span><span class="sxs-lookup"><span data-stu-id="0a2a4-222">buildNumber</span></span>|<span data-ttu-id="0a2a4-223">String</span><span class="sxs-lookup"><span data-stu-id="0a2a4-223">String</span></span>|<span data-ttu-id="0a2a4-224">Número de compilación de la aplicación administrada de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-224">The build number of managed iOS Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="0a2a4-225">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a2a4-225">Response</span></span>
<span data-ttu-id="0a2a4-226">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-226">If successful, this method returns a `200 OK` response code and an updated [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0a2a4-227">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a2a4-227">Example</span></span>
### <a name="request"></a><span data-ttu-id="0a2a4-228">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0a2a4-228">Request</span></span>
<span data-ttu-id="0a2a4-229">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-229">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
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

### <a name="response"></a><span data-ttu-id="0a2a4-230">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a2a4-230">Response</span></span>
<span data-ttu-id="0a2a4-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0a2a4-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



