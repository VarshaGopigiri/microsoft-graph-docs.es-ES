# <a name="update-managedandroidlobapp"></a><span data-ttu-id="9f0cb-101">Actualizar managedAndroidLobApp</span><span class="sxs-lookup"><span data-stu-id="9f0cb-101">Update managedAndroidLobApp</span></span>

> <span data-ttu-id="9f0cb-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9f0cb-103">Actualice las propiedades de un objeto [managedAndroidLobApp](../resources/intune_apps_managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-103">Update the properties of a [calendar](../resources/intune_apps_managedandroidlobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9f0cb-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9f0cb-104">Prerequisites</span></span>
<span data-ttu-id="9f0cb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9f0cb-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9f0cb-107">Permission type</span></span>|<span data-ttu-id="9f0cb-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9f0cb-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9f0cb-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9f0cb-109">Delegated (work or school account)</span></span>|<span data-ttu-id="9f0cb-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9f0cb-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="9f0cb-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9f0cb-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9f0cb-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-112">Not supported.</span></span>|
|<span data-ttu-id="9f0cb-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9f0cb-113">Application</span></span>|<span data-ttu-id="9f0cb-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9f0cb-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9f0cb-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="9f0cb-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9f0cb-116">Request headers</span></span>
|<span data-ttu-id="9f0cb-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f0cb-117">Header</span></span>|<span data-ttu-id="9f0cb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9f0cb-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9f0cb-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="9f0cb-119">Authorization</span></span>|<span data-ttu-id="9f0cb-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="9f0cb-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9f0cb-121">Accept</span></span>|<span data-ttu-id="9f0cb-122">application/json</span><span class="sxs-lookup"><span data-stu-id="9f0cb-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9f0cb-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9f0cb-123">Request body</span></span>
<span data-ttu-id="9f0cb-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedAndroidLobApp](../resources/intune_apps_managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-124">In the request body, supply a JSON representation of [message](../resources/intune_apps_managedandroidlobapp.md) object.</span></span>

<span data-ttu-id="9f0cb-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedAndroidLobApp](../resources/intune_apps_managedandroidlobapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="9f0cb-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9f0cb-126">Property</span></span>|<span data-ttu-id="9f0cb-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="9f0cb-127">Type</span></span>|<span data-ttu-id="9f0cb-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f0cb-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9f0cb-129">id</span><span class="sxs-lookup"><span data-stu-id="9f0cb-129">id</span></span>|<span data-ttu-id="9f0cb-130">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-130">String</span></span>|<span data-ttu-id="9f0cb-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-131">Key of the setting.</span></span> <span data-ttu-id="9f0cb-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="9f0cb-133">displayName</span><span class="sxs-lookup"><span data-stu-id="9f0cb-133">displayName</span></span>|<span data-ttu-id="9f0cb-134">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-134">String</span></span>|<span data-ttu-id="9f0cb-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="9f0cb-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="9f0cb-137">description</span><span class="sxs-lookup"><span data-stu-id="9f0cb-137">description</span></span>|<span data-ttu-id="9f0cb-138">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-138">String</span></span>|<span data-ttu-id="9f0cb-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-139">The description of the app.</span></span> <span data-ttu-id="9f0cb-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="9f0cb-141">publicador</span><span class="sxs-lookup"><span data-stu-id="9f0cb-141">Publisher</span></span>|<span data-ttu-id="9f0cb-142">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-142">String</span></span>|<span data-ttu-id="9f0cb-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-143">The name of the app.</span></span> <span data-ttu-id="9f0cb-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="9f0cb-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="9f0cb-145">largeIcon</span></span>|[<span data-ttu-id="9f0cb-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="9f0cb-146">mimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="9f0cb-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="9f0cb-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="9f0cb-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="9f0cb-149">createdDateTime</span></span>|<span data-ttu-id="9f0cb-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9f0cb-150">DateTimeOffset</span></span>|<span data-ttu-id="9f0cb-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-151">The date and time when the page was created.</span></span> <span data-ttu-id="9f0cb-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="9f0cb-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9f0cb-153">lastModifiedDateTime</span></span>|<span data-ttu-id="9f0cb-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9f0cb-154">DateTimeOffset</span></span>|<span data-ttu-id="9f0cb-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="9f0cb-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="9f0cb-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="9f0cb-157">isFeatured</span></span>|<span data-ttu-id="9f0cb-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="9f0cb-158">Boolean</span></span>|<span data-ttu-id="9f0cb-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="9f0cb-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="9f0cb-160">privacyInformationUrl</span></span>|<span data-ttu-id="9f0cb-161">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-161">String</span></span>|<span data-ttu-id="9f0cb-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-162">The privacy statement Url.</span></span> <span data-ttu-id="9f0cb-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="9f0cb-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="9f0cb-164">informationUrl</span></span>|<span data-ttu-id="9f0cb-165">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-165">String</span></span>|<span data-ttu-id="9f0cb-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-166">The more information Url.</span></span> <span data-ttu-id="9f0cb-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="9f0cb-168">owner</span><span class="sxs-lookup"><span data-stu-id="9f0cb-168">owner</span></span>|<span data-ttu-id="9f0cb-169">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-169">String</span></span>|<span data-ttu-id="9f0cb-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-170">The owner of the timesheet.</span></span> <span data-ttu-id="9f0cb-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="9f0cb-172">developer</span><span class="sxs-lookup"><span data-stu-id="9f0cb-172">developer</span></span>|<span data-ttu-id="9f0cb-173">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-173">String</span></span>|<span data-ttu-id="9f0cb-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-174">The name of the app.</span></span> <span data-ttu-id="9f0cb-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="9f0cb-176">notas</span><span class="sxs-lookup"><span data-stu-id="9f0cb-176">Notes</span></span>|<span data-ttu-id="9f0cb-177">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-177">String</span></span>|<span data-ttu-id="9f0cb-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-178">Notes for the app.</span></span> <span data-ttu-id="9f0cb-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="9f0cb-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="9f0cb-180">publishingState</span></span>|<span data-ttu-id="9f0cb-181">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-181">String</span></span>|<span data-ttu-id="9f0cb-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-182">The publishing state for the app.</span></span> <span data-ttu-id="9f0cb-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="9f0cb-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="9f0cb-185">appAvailability</span><span class="sxs-lookup"><span data-stu-id="9f0cb-185">appAvailability</span></span>|<span data-ttu-id="9f0cb-186">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-186">String</span></span>|<span data-ttu-id="9f0cb-187">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-187">The Application's availability.</span></span> <span data-ttu-id="9f0cb-188">Heredado de [managedApp](../resources/intune_apps_managedapp.md). Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-188">Inherited from [managedApp](../resources/intune_apps_managedapp.md) Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="9f0cb-189">version</span><span class="sxs-lookup"><span data-stu-id="9f0cb-189">version</span></span>|<span data-ttu-id="9f0cb-190">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-190">String</span></span>|<span data-ttu-id="9f0cb-191">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-191">The Application's version.</span></span> <span data-ttu-id="9f0cb-192">Heredado de [managedApp](../resources/intune_apps_managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="9f0cb-192">Inherited from [managedApp](../resources/intune_apps_managedapp.md)</span></span>|
|<span data-ttu-id="9f0cb-193">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="9f0cb-193">committedContentVersion</span></span>|<span data-ttu-id="9f0cb-194">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-194">String</span></span>|<span data-ttu-id="9f0cb-195">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-195">The internal committed content version.</span></span> <span data-ttu-id="9f0cb-196">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-196">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="9f0cb-197">fileName</span><span class="sxs-lookup"><span data-stu-id="9f0cb-197">fileName</span></span>|<span data-ttu-id="9f0cb-198">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-198">String</span></span>|<span data-ttu-id="9f0cb-199">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-199">The name of the main Lob application file.</span></span> <span data-ttu-id="9f0cb-200">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-200">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="9f0cb-201">size</span><span class="sxs-lookup"><span data-stu-id="9f0cb-201">size</span></span>|<span data-ttu-id="9f0cb-202">Int64</span><span class="sxs-lookup"><span data-stu-id="9f0cb-202">Int64</span></span>|<span data-ttu-id="9f0cb-203">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-203">The total size, including all uploaded files.</span></span> <span data-ttu-id="9f0cb-204">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="9f0cb-204">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="9f0cb-205">packageId</span><span class="sxs-lookup"><span data-stu-id="9f0cb-205">packageId</span></span>|<span data-ttu-id="9f0cb-206">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-206">String</span></span>|<span data-ttu-id="9f0cb-207">El identificador del paquete.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-207">The package identifier.</span></span>|
|<span data-ttu-id="9f0cb-208">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="9f0cb-208">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="9f0cb-209">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="9f0cb-209">androidMinimumOperatingSystem</span></span>](../resources/intune_apps_androidminimumoperatingsystem.md)|<span data-ttu-id="9f0cb-210">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-210">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="9f0cb-211">versionName</span><span class="sxs-lookup"><span data-stu-id="9f0cb-211">versionName</span></span>|<span data-ttu-id="9f0cb-212">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-212">String</span></span>|<span data-ttu-id="9f0cb-213">Nombre de versión de la aplicación administrada de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-213">The version name of managed Android Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="9f0cb-214">versionCode</span><span class="sxs-lookup"><span data-stu-id="9f0cb-214">versionCode</span></span>|<span data-ttu-id="9f0cb-215">String</span><span class="sxs-lookup"><span data-stu-id="9f0cb-215">String</span></span>|<span data-ttu-id="9f0cb-216">Código de versión de la aplicación administrada de línea de negocio (LoB) de Android.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-216">The version code of managed Android Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="9f0cb-217">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f0cb-217">Response</span></span>
<span data-ttu-id="9f0cb-218">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAndroidLobApp](../resources/intune_apps_managedandroidlobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-218">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_apps_managedandroidlobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9f0cb-219">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f0cb-219">Example</span></span>
### <a name="request"></a><span data-ttu-id="9f0cb-220">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9f0cb-220">Request</span></span>
<span data-ttu-id="9f0cb-221">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-221">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1158

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

### <a name="response"></a><span data-ttu-id="9f0cb-222">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f0cb-222">Response</span></span>
<span data-ttu-id="9f0cb-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9f0cb-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



