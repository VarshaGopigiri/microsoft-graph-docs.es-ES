# <a name="update-managedandroidlobapp"></a><span data-ttu-id="00a49-101">Actualizar managedAndroidLobApp</span><span class="sxs-lookup"><span data-stu-id="00a49-101">Update managedAndroidLobApp</span></span>

> <span data-ttu-id="00a49-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="00a49-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="00a49-103">Actualice las propiedades de un objeto [managedAndroidLobApp](../resources/intune_apps_managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-103">Update the properties of a [managedAndroidLobApp](../resources/intune_apps_managedandroidlobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="00a49-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="00a49-104">Prerequisites</span></span>
<span data-ttu-id="00a49-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="00a49-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="00a49-107">Permission type</span></span>|<span data-ttu-id="00a49-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="00a49-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="00a49-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="00a49-109">Delegated (work or school account)</span></span>|<span data-ttu-id="00a49-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="00a49-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="00a49-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="00a49-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="00a49-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="00a49-112">Not supported.</span></span>|
|<span data-ttu-id="00a49-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="00a49-113">Application</span></span>|<span data-ttu-id="00a49-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="00a49-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="00a49-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="00a49-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="00a49-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="00a49-116">Request headers</span></span>
|<span data-ttu-id="00a49-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00a49-117">Header</span></span>|<span data-ttu-id="00a49-118">Valor</span><span class="sxs-lookup"><span data-stu-id="00a49-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="00a49-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="00a49-119">Authorization</span></span>|<span data-ttu-id="00a49-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="00a49-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="00a49-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="00a49-121">Accept</span></span>|<span data-ttu-id="00a49-122">application/json</span><span class="sxs-lookup"><span data-stu-id="00a49-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="00a49-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="00a49-123">Request body</span></span>
<span data-ttu-id="00a49-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedAndroidLobApp](../resources/intune_apps_managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-124">In the request body, supply a JSON representation for the [managedAndroidLobApp](../resources/intune_apps_managedandroidlobapp.md) object.</span></span>

<span data-ttu-id="00a49-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedAndroidLobApp](../resources/intune_apps_managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-125">The following table shows the properties that are required when you create the [managedAndroidLobApp](../resources/intune_apps_managedandroidlobapp.md).</span></span>

|<span data-ttu-id="00a49-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="00a49-126">Property</span></span>|<span data-ttu-id="00a49-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="00a49-127">Type</span></span>|<span data-ttu-id="00a49-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="00a49-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="00a49-129">id</span><span class="sxs-lookup"><span data-stu-id="00a49-129">id</span></span>|<span data-ttu-id="00a49-130">String</span><span class="sxs-lookup"><span data-stu-id="00a49-130">String</span></span>|<span data-ttu-id="00a49-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="00a49-131">Key of the entity.</span></span> <span data-ttu-id="00a49-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="00a49-133">displayName</span><span class="sxs-lookup"><span data-stu-id="00a49-133">displayName</span></span>|<span data-ttu-id="00a49-134">String</span><span class="sxs-lookup"><span data-stu-id="00a49-134">String</span></span>|<span data-ttu-id="00a49-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="00a49-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="00a49-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="00a49-137">description</span><span class="sxs-lookup"><span data-stu-id="00a49-137">description</span></span>|<span data-ttu-id="00a49-138">String</span><span class="sxs-lookup"><span data-stu-id="00a49-138">String</span></span>|<span data-ttu-id="00a49-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="00a49-139">The description of the app.</span></span> <span data-ttu-id="00a49-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="00a49-141">publicador</span><span class="sxs-lookup"><span data-stu-id="00a49-141">publisher</span></span>|<span data-ttu-id="00a49-142">String</span><span class="sxs-lookup"><span data-stu-id="00a49-142">String</span></span>|<span data-ttu-id="00a49-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="00a49-143">The publisher of the app.</span></span> <span data-ttu-id="00a49-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="00a49-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="00a49-145">largeIcon</span></span>|[<span data-ttu-id="00a49-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="00a49-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="00a49-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="00a49-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="00a49-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="00a49-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="00a49-149">createdDateTime</span></span>|<span data-ttu-id="00a49-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="00a49-150">DateTimeOffset</span></span>|<span data-ttu-id="00a49-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="00a49-151">The date and time the app was created.</span></span> <span data-ttu-id="00a49-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="00a49-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="00a49-153">lastModifiedDateTime</span></span>|<span data-ttu-id="00a49-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="00a49-154">DateTimeOffset</span></span>|<span data-ttu-id="00a49-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="00a49-155">The date and time the app was last modified.</span></span> <span data-ttu-id="00a49-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="00a49-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="00a49-157">isFeatured</span></span>|<span data-ttu-id="00a49-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="00a49-158">Boolean</span></span>|<span data-ttu-id="00a49-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="00a49-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="00a49-160">privacyInformationUrl</span></span>|<span data-ttu-id="00a49-161">String</span><span class="sxs-lookup"><span data-stu-id="00a49-161">String</span></span>|<span data-ttu-id="00a49-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="00a49-162">The privacy statement Url.</span></span> <span data-ttu-id="00a49-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="00a49-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="00a49-164">informationUrl</span></span>|<span data-ttu-id="00a49-165">String</span><span class="sxs-lookup"><span data-stu-id="00a49-165">String</span></span>|<span data-ttu-id="00a49-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="00a49-166">The more information Url.</span></span> <span data-ttu-id="00a49-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="00a49-168">owner</span><span class="sxs-lookup"><span data-stu-id="00a49-168">owner</span></span>|<span data-ttu-id="00a49-169">String</span><span class="sxs-lookup"><span data-stu-id="00a49-169">String</span></span>|<span data-ttu-id="00a49-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="00a49-170">The owner of the app.</span></span> <span data-ttu-id="00a49-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="00a49-172">developer</span><span class="sxs-lookup"><span data-stu-id="00a49-172">developer</span></span>|<span data-ttu-id="00a49-173">String</span><span class="sxs-lookup"><span data-stu-id="00a49-173">String</span></span>|<span data-ttu-id="00a49-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="00a49-174">The developer of the app.</span></span> <span data-ttu-id="00a49-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="00a49-176">notas</span><span class="sxs-lookup"><span data-stu-id="00a49-176">notes</span></span>|<span data-ttu-id="00a49-177">String</span><span class="sxs-lookup"><span data-stu-id="00a49-177">String</span></span>|<span data-ttu-id="00a49-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="00a49-178">Notes for the app.</span></span> <span data-ttu-id="00a49-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="00a49-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="00a49-180">publishingState</span></span>|[<span data-ttu-id="00a49-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="00a49-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="00a49-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="00a49-182">The publishing state for the app.</span></span> <span data-ttu-id="00a49-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="00a49-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="00a49-184">Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md).</span></span> <span data-ttu-id="00a49-185">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="00a49-185">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="00a49-186">appAvailability</span><span class="sxs-lookup"><span data-stu-id="00a49-186">appAvailability</span></span>|[<span data-ttu-id="00a49-187">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="00a49-187">managedAppAvailability</span></span>](../resources/intune_apps_managedappavailability.md)|<span data-ttu-id="00a49-188">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="00a49-188">The Application's availability.</span></span> <span data-ttu-id="00a49-189">Se hereda de [managedApp](../resources/intune_apps_managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-189">Inherited from [managedApp](../resources/intune_apps_managedapp.md).</span></span> <span data-ttu-id="00a49-190">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="00a49-190">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="00a49-191">versión</span><span class="sxs-lookup"><span data-stu-id="00a49-191">version</span></span>|<span data-ttu-id="00a49-192">String</span><span class="sxs-lookup"><span data-stu-id="00a49-192">String</span></span>|<span data-ttu-id="00a49-193">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="00a49-193">The Application's version.</span></span> <span data-ttu-id="00a49-194">Heredado de [managedApp](../resources/intune_apps_managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="00a49-194">Inherited from [managedApp](../resources/intune_apps_managedapp.md)</span></span>|
|<span data-ttu-id="00a49-195">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="00a49-195">committedContentVersion</span></span>|<span data-ttu-id="00a49-196">String</span><span class="sxs-lookup"><span data-stu-id="00a49-196">String</span></span>|<span data-ttu-id="00a49-197">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="00a49-197">The internal committed content version.</span></span> <span data-ttu-id="00a49-198">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-198">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="00a49-199">fileName</span><span class="sxs-lookup"><span data-stu-id="00a49-199">fileName</span></span>|<span data-ttu-id="00a49-200">String</span><span class="sxs-lookup"><span data-stu-id="00a49-200">String</span></span>|<span data-ttu-id="00a49-201">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="00a49-201">The name of the main Lob application file.</span></span> <span data-ttu-id="00a49-202">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-202">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="00a49-203">size</span><span class="sxs-lookup"><span data-stu-id="00a49-203">size</span></span>|<span data-ttu-id="00a49-204">Int64</span><span class="sxs-lookup"><span data-stu-id="00a49-204">Int64</span></span>|<span data-ttu-id="00a49-205">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="00a49-205">The total size, including all uploaded files.</span></span> <span data-ttu-id="00a49-206">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="00a49-206">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="00a49-207">packageId</span><span class="sxs-lookup"><span data-stu-id="00a49-207">packageId</span></span>|<span data-ttu-id="00a49-208">String</span><span class="sxs-lookup"><span data-stu-id="00a49-208">String</span></span>|<span data-ttu-id="00a49-209">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="00a49-209">The package identifier.</span></span>|
|<span data-ttu-id="00a49-210">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="00a49-210">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="00a49-211">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="00a49-211">androidMinimumOperatingSystem</span></span>](../resources/intune_apps_androidminimumoperatingsystem.md)|<span data-ttu-id="00a49-212">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="00a49-212">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="00a49-213">versionName</span><span class="sxs-lookup"><span data-stu-id="00a49-213">versionName</span></span>|<span data-ttu-id="00a49-214">String</span><span class="sxs-lookup"><span data-stu-id="00a49-214">String</span></span>|<span data-ttu-id="00a49-215">Nombre de versión de la aplicación administrada de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="00a49-215">The version name of managed Android Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="00a49-216">versionCode</span><span class="sxs-lookup"><span data-stu-id="00a49-216">versionCode</span></span>|<span data-ttu-id="00a49-217">String</span><span class="sxs-lookup"><span data-stu-id="00a49-217">String</span></span>|<span data-ttu-id="00a49-218">Código de versión de la aplicación administrada de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="00a49-218">The version code of managed Android Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="00a49-219">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00a49-219">Response</span></span>
<span data-ttu-id="00a49-220">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAndroidLobApp](../resources/intune_apps_managedandroidlobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="00a49-220">If successful, this method returns a `200 OK` response code and an updated [managedAndroidLobApp](../resources/intune_apps_managedandroidlobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="00a49-221">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="00a49-221">Example</span></span>
### <a name="request"></a><span data-ttu-id="00a49-222">Solicitud</span><span class="sxs-lookup"><span data-stu-id="00a49-222">Request</span></span>
<span data-ttu-id="00a49-223">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="00a49-223">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1153

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

### <a name="response"></a><span data-ttu-id="00a49-224">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00a49-224">Response</span></span>
<span data-ttu-id="00a49-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="00a49-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



