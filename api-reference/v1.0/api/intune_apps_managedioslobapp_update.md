# <a name="update-managedioslobapp"></a><span data-ttu-id="aeb3b-101">Actualizar managedIOSLobApp</span><span class="sxs-lookup"><span data-stu-id="aeb3b-101">Update managedIOSLobApp</span></span>

> <span data-ttu-id="aeb3b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="aeb3b-103">Actualice las propiedades de un objeto [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-103">Update the properties of a [calendar](../resources/intune_apps_managedioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="aeb3b-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="aeb3b-104">Prerequisites</span></span>
<span data-ttu-id="aeb3b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="aeb3b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="aeb3b-107">Permission type</span></span>|<span data-ttu-id="aeb3b-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="aeb3b-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="aeb3b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="aeb3b-109">Delegated (work or school account)</span></span>|<span data-ttu-id="aeb3b-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="aeb3b-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="aeb3b-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="aeb3b-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="aeb3b-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-112">Not supported.</span></span>|
|<span data-ttu-id="aeb3b-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="aeb3b-113">Application</span></span>|<span data-ttu-id="aeb3b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="aeb3b-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aeb3b-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="aeb3b-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="aeb3b-116">Request headers</span></span>
|<span data-ttu-id="aeb3b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aeb3b-117">Header</span></span>|<span data-ttu-id="aeb3b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="aeb3b-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="aeb3b-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="aeb3b-119">Authorization</span></span>|<span data-ttu-id="aeb3b-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="aeb3b-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="aeb3b-121">Accept</span></span>|<span data-ttu-id="aeb3b-122">application/json</span><span class="sxs-lookup"><span data-stu-id="aeb3b-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="aeb3b-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aeb3b-123">Request body</span></span>
<span data-ttu-id="aeb3b-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-124">In the request body, supply a JSON representation of [directoryObject](../resources/intune_apps_managedioslobapp.md) object.</span></span>

<span data-ttu-id="aeb3b-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="aeb3b-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aeb3b-126">Property</span></span>|<span data-ttu-id="aeb3b-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeb3b-127">Type</span></span>|<span data-ttu-id="aeb3b-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeb3b-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="aeb3b-129">id</span><span class="sxs-lookup"><span data-stu-id="aeb3b-129">id</span></span>|<span data-ttu-id="aeb3b-130">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-130">String</span></span>|<span data-ttu-id="aeb3b-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-131">Key of the setting.</span></span> <span data-ttu-id="aeb3b-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="aeb3b-133">displayName</span><span class="sxs-lookup"><span data-stu-id="aeb3b-133">displayName</span></span>|<span data-ttu-id="aeb3b-134">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-134">String</span></span>|<span data-ttu-id="aeb3b-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="aeb3b-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="aeb3b-137">description</span><span class="sxs-lookup"><span data-stu-id="aeb3b-137">description</span></span>|<span data-ttu-id="aeb3b-138">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-138">String</span></span>|<span data-ttu-id="aeb3b-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-139">The description of the app.</span></span> <span data-ttu-id="aeb3b-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="aeb3b-141">publicador</span><span class="sxs-lookup"><span data-stu-id="aeb3b-141">Publisher</span></span>|<span data-ttu-id="aeb3b-142">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-142">String</span></span>|<span data-ttu-id="aeb3b-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-143">The name of the app.</span></span> <span data-ttu-id="aeb3b-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="aeb3b-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="aeb3b-145">largeIcon</span></span>|[<span data-ttu-id="aeb3b-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="aeb3b-146">mimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="aeb3b-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="aeb3b-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="aeb3b-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="aeb3b-149">createdDateTime</span></span>|<span data-ttu-id="aeb3b-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="aeb3b-150">DateTimeOffset</span></span>|<span data-ttu-id="aeb3b-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-151">The date and time when the page was created.</span></span> <span data-ttu-id="aeb3b-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="aeb3b-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="aeb3b-153">lastModifiedDateTime</span></span>|<span data-ttu-id="aeb3b-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="aeb3b-154">DateTimeOffset</span></span>|<span data-ttu-id="aeb3b-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="aeb3b-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="aeb3b-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="aeb3b-157">isFeatured</span></span>|<span data-ttu-id="aeb3b-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="aeb3b-158">Boolean</span></span>|<span data-ttu-id="aeb3b-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="aeb3b-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="aeb3b-160">privacyInformationUrl</span></span>|<span data-ttu-id="aeb3b-161">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-161">String</span></span>|<span data-ttu-id="aeb3b-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-162">The privacy statement Url.</span></span> <span data-ttu-id="aeb3b-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="aeb3b-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="aeb3b-164">informationUrl</span></span>|<span data-ttu-id="aeb3b-165">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-165">String</span></span>|<span data-ttu-id="aeb3b-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-166">The more information Url.</span></span> <span data-ttu-id="aeb3b-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="aeb3b-168">owner</span><span class="sxs-lookup"><span data-stu-id="aeb3b-168">owner</span></span>|<span data-ttu-id="aeb3b-169">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-169">String</span></span>|<span data-ttu-id="aeb3b-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-170">The owner of the timesheet.</span></span> <span data-ttu-id="aeb3b-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="aeb3b-172">developer</span><span class="sxs-lookup"><span data-stu-id="aeb3b-172">developer</span></span>|<span data-ttu-id="aeb3b-173">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-173">String</span></span>|<span data-ttu-id="aeb3b-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-174">The name of the app.</span></span> <span data-ttu-id="aeb3b-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="aeb3b-176">notas</span><span class="sxs-lookup"><span data-stu-id="aeb3b-176">Notes</span></span>|<span data-ttu-id="aeb3b-177">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-177">String</span></span>|<span data-ttu-id="aeb3b-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-178">Notes for the app.</span></span> <span data-ttu-id="aeb3b-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="aeb3b-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="aeb3b-180">publishingState</span></span>|<span data-ttu-id="aeb3b-181">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-181">String</span></span>|<span data-ttu-id="aeb3b-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-182">The publishing state for the app.</span></span> <span data-ttu-id="aeb3b-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="aeb3b-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="aeb3b-185">appAvailability</span><span class="sxs-lookup"><span data-stu-id="aeb3b-185">appAvailability</span></span>|<span data-ttu-id="aeb3b-186">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-186">String</span></span>|<span data-ttu-id="aeb3b-187">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-187">The Application's availability.</span></span> <span data-ttu-id="aeb3b-188">Heredado de [managedApp](../resources/intune_apps_managedapp.md). Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-188">Inherited from [managedApp](../resources/intune_apps_managedapp.md) Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="aeb3b-189">version</span><span class="sxs-lookup"><span data-stu-id="aeb3b-189">version</span></span>|<span data-ttu-id="aeb3b-190">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-190">String</span></span>|<span data-ttu-id="aeb3b-191">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-191">The Application's version.</span></span> <span data-ttu-id="aeb3b-192">Heredado de [managedApp](../resources/intune_apps_managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="aeb3b-192">Inherited from [managedApp](../resources/intune_apps_managedapp.md)</span></span>|
|<span data-ttu-id="aeb3b-193">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="aeb3b-193">committedContentVersion</span></span>|<span data-ttu-id="aeb3b-194">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-194">String</span></span>|<span data-ttu-id="aeb3b-195">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-195">The internal committed content version.</span></span> <span data-ttu-id="aeb3b-196">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-196">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="aeb3b-197">fileName</span><span class="sxs-lookup"><span data-stu-id="aeb3b-197">fileName</span></span>|<span data-ttu-id="aeb3b-198">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-198">String</span></span>|<span data-ttu-id="aeb3b-199">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-199">The name of the main Lob application file.</span></span> <span data-ttu-id="aeb3b-200">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-200">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="aeb3b-201">size</span><span class="sxs-lookup"><span data-stu-id="aeb3b-201">size</span></span>|<span data-ttu-id="aeb3b-202">Int64</span><span class="sxs-lookup"><span data-stu-id="aeb3b-202">Int64</span></span>|<span data-ttu-id="aeb3b-203">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-203">The total size, including all uploaded files.</span></span> <span data-ttu-id="aeb3b-204">Heredado de [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="aeb3b-204">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="aeb3b-205">bundleId</span><span class="sxs-lookup"><span data-stu-id="aeb3b-205">bundleId</span></span>|<span data-ttu-id="aeb3b-206">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-206">String</span></span>|<span data-ttu-id="aeb3b-207">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-207">The Identity Name.</span></span>|
|<span data-ttu-id="aeb3b-208">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="aeb3b-208">applicableDeviceType</span></span>|[<span data-ttu-id="aeb3b-209">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="aeb3b-209">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="aeb3b-210">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-210">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="aeb3b-211">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="aeb3b-211">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="aeb3b-212">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="aeb3b-212">iosMinimumOperatingSystem</span></span>](../resources/intune_apps_iosminimumoperatingsystem.md)|<span data-ttu-id="aeb3b-213">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-213">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="aeb3b-214">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="aeb3b-214">expirationDateTime</span></span>|<span data-ttu-id="aeb3b-215">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="aeb3b-215">DateTimeOffset</span></span>|<span data-ttu-id="aeb3b-216">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-216">: The expiration time for the subscription.</span></span>|
|<span data-ttu-id="aeb3b-217">versionNumber</span><span class="sxs-lookup"><span data-stu-id="aeb3b-217">versionNumber</span></span>|<span data-ttu-id="aeb3b-218">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-218">String</span></span>|<span data-ttu-id="aeb3b-219">Número de versión de la aplicación administrada de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-219">The version number of managed iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="aeb3b-220">buildNumber</span><span class="sxs-lookup"><span data-stu-id="aeb3b-220">buildNumber</span></span>|<span data-ttu-id="aeb3b-221">String</span><span class="sxs-lookup"><span data-stu-id="aeb3b-221">String</span></span>|<span data-ttu-id="aeb3b-222">Número de compilación de la aplicación administrada de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-222">The build number of managed iOS Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="aeb3b-223">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aeb3b-223">Response</span></span>
<span data-ttu-id="aeb3b-224">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-224">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_apps_managedioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="aeb3b-225">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aeb3b-225">Example</span></span>
### <a name="request"></a><span data-ttu-id="aeb3b-226">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aeb3b-226">Request</span></span>
<span data-ttu-id="aeb3b-227">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-227">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1276

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

### <a name="response"></a><span data-ttu-id="aeb3b-228">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aeb3b-228">Response</span></span>
<span data-ttu-id="aeb3b-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aeb3b-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



