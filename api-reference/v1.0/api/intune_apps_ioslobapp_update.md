# <a name="update-ioslobapp"></a><span data-ttu-id="4dbe8-101">Actualizar iosLobApp</span><span class="sxs-lookup"><span data-stu-id="4dbe8-101">Update iosLobApp</span></span>

> <span data-ttu-id="4dbe8-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4dbe8-103">Actualice las propiedades de un objeto [iosLobApp](../resources/intune_apps_ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-103">Update the properties of a [iosLobApp](../resources/intune_apps_ioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4dbe8-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4dbe8-104">Prerequisites</span></span>
<span data-ttu-id="4dbe8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4dbe8-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4dbe8-107">Permission type</span></span>|<span data-ttu-id="4dbe8-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4dbe8-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4dbe8-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4dbe8-109">Delegated (work or school account)</span></span>|<span data-ttu-id="4dbe8-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4dbe8-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="4dbe8-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4dbe8-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4dbe8-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-112">Not supported.</span></span>|
|<span data-ttu-id="4dbe8-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4dbe8-113">Application</span></span>|<span data-ttu-id="4dbe8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4dbe8-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4dbe8-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="4dbe8-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4dbe8-116">Request headers</span></span>
|<span data-ttu-id="4dbe8-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4dbe8-117">Header</span></span>|<span data-ttu-id="4dbe8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4dbe8-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4dbe8-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="4dbe8-119">Authorization</span></span>|<span data-ttu-id="4dbe8-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4dbe8-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4dbe8-121">Accept</span></span>|<span data-ttu-id="4dbe8-122">application/json</span><span class="sxs-lookup"><span data-stu-id="4dbe8-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4dbe8-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4dbe8-123">Request body</span></span>
<span data-ttu-id="4dbe8-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosLobApp](../resources/intune_apps_ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-124">In the request body, supply a JSON representation for the [iosLobApp](../resources/intune_apps_ioslobapp.md) object.</span></span>

<span data-ttu-id="4dbe8-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosLobApp](../resources/intune_apps_ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-125">The following table shows the properties that are required when you create the [iosLobApp](../resources/intune_apps_ioslobapp.md).</span></span>

|<span data-ttu-id="4dbe8-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4dbe8-126">Property</span></span>|<span data-ttu-id="4dbe8-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="4dbe8-127">Type</span></span>|<span data-ttu-id="4dbe8-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="4dbe8-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4dbe8-129">id</span><span class="sxs-lookup"><span data-stu-id="4dbe8-129">id</span></span>|<span data-ttu-id="4dbe8-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="4dbe8-130">String</span></span>|<span data-ttu-id="4dbe8-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-131">Key of the entity.</span></span> <span data-ttu-id="4dbe8-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="4dbe8-133">displayName</span><span class="sxs-lookup"><span data-stu-id="4dbe8-133">displayName</span></span>|<span data-ttu-id="4dbe8-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="4dbe8-134">String</span></span>|<span data-ttu-id="4dbe8-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="4dbe8-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="4dbe8-137">descripción</span><span class="sxs-lookup"><span data-stu-id="4dbe8-137">description</span></span>|<span data-ttu-id="4dbe8-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="4dbe8-138">String</span></span>|<span data-ttu-id="4dbe8-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-139">The description of the app.</span></span> <span data-ttu-id="4dbe8-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="4dbe8-141">publicador</span><span class="sxs-lookup"><span data-stu-id="4dbe8-141">publisher</span></span>|<span data-ttu-id="4dbe8-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="4dbe8-142">String</span></span>|<span data-ttu-id="4dbe8-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-143">The publisher of the app.</span></span> <span data-ttu-id="4dbe8-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="4dbe8-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="4dbe8-145">largeIcon</span></span>|[<span data-ttu-id="4dbe8-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="4dbe8-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="4dbe8-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="4dbe8-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="4dbe8-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4dbe8-149">createdDateTime</span></span>|<span data-ttu-id="4dbe8-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4dbe8-150">DateTimeOffset</span></span>|<span data-ttu-id="4dbe8-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-151">The date and time the app was created.</span></span> <span data-ttu-id="4dbe8-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="4dbe8-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4dbe8-153">lastModifiedDateTime</span></span>|<span data-ttu-id="4dbe8-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4dbe8-154">DateTimeOffset</span></span>|<span data-ttu-id="4dbe8-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-155">The date and time the app was last modified.</span></span> <span data-ttu-id="4dbe8-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="4dbe8-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="4dbe8-157">isFeatured</span></span>|<span data-ttu-id="4dbe8-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="4dbe8-158">Boolean</span></span>|<span data-ttu-id="4dbe8-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="4dbe8-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="4dbe8-160">privacyInformationUrl</span></span>|<span data-ttu-id="4dbe8-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="4dbe8-161">String</span></span>|<span data-ttu-id="4dbe8-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-162">The privacy statement Url.</span></span> <span data-ttu-id="4dbe8-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="4dbe8-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="4dbe8-164">informationUrl</span></span>|<span data-ttu-id="4dbe8-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="4dbe8-165">String</span></span>|<span data-ttu-id="4dbe8-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-166">The more information Url.</span></span> <span data-ttu-id="4dbe8-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="4dbe8-168">owner</span><span class="sxs-lookup"><span data-stu-id="4dbe8-168">owner</span></span>|<span data-ttu-id="4dbe8-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="4dbe8-169">String</span></span>|<span data-ttu-id="4dbe8-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-170">The owner of the app.</span></span> <span data-ttu-id="4dbe8-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="4dbe8-172">developer</span><span class="sxs-lookup"><span data-stu-id="4dbe8-172">developer</span></span>|<span data-ttu-id="4dbe8-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="4dbe8-173">String</span></span>|<span data-ttu-id="4dbe8-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-174">The developer of the app.</span></span> <span data-ttu-id="4dbe8-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="4dbe8-176">notas</span><span class="sxs-lookup"><span data-stu-id="4dbe8-176">notes</span></span>|<span data-ttu-id="4dbe8-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="4dbe8-177">String</span></span>|<span data-ttu-id="4dbe8-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-178">Notes for the app.</span></span> <span data-ttu-id="4dbe8-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="4dbe8-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="4dbe8-180">publishingState</span></span>|[<span data-ttu-id="4dbe8-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="4dbe8-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="4dbe8-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-182">The publishing state for the app.</span></span> <span data-ttu-id="4dbe8-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="4dbe8-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span> <span data-ttu-id="4dbe8-185">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-185">The possible values are `notPublished`, `processing`, `published`, , , , , , , , , or .</span></span>|
|<span data-ttu-id="4dbe8-186">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="4dbe8-186">committedContentVersion</span></span>|<span data-ttu-id="4dbe8-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="4dbe8-187">String</span></span>|<span data-ttu-id="4dbe8-188">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-188">The internal committed content version.</span></span> <span data-ttu-id="4dbe8-189">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-189">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="4dbe8-190">fileName</span><span class="sxs-lookup"><span data-stu-id="4dbe8-190">fileName</span></span>|<span data-ttu-id="4dbe8-191">Cadena</span><span class="sxs-lookup"><span data-stu-id="4dbe8-191">String</span></span>|<span data-ttu-id="4dbe8-192">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-192">The name of the main Lob application file.</span></span> <span data-ttu-id="4dbe8-193">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-193">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="4dbe8-194">size</span><span class="sxs-lookup"><span data-stu-id="4dbe8-194">size</span></span>|<span data-ttu-id="4dbe8-195">Int64</span><span class="sxs-lookup"><span data-stu-id="4dbe8-195">Int64</span></span>|<span data-ttu-id="4dbe8-196">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-196">The total size, including all uploaded files.</span></span> <span data-ttu-id="4dbe8-197">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="4dbe8-197">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="4dbe8-198">bundleId</span><span class="sxs-lookup"><span data-stu-id="4dbe8-198">bundleId</span></span>|<span data-ttu-id="4dbe8-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="4dbe8-199">String</span></span>|<span data-ttu-id="4dbe8-200">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-200">The Identity Name.</span></span>|
|<span data-ttu-id="4dbe8-201">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="4dbe8-201">applicableDeviceType</span></span>|[<span data-ttu-id="4dbe8-202">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="4dbe8-202">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="4dbe8-203">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-203">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="4dbe8-204">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4dbe8-204">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="4dbe8-205">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4dbe8-205">iosMinimumOperatingSystem</span></span>](../resources/intune_apps_iosminimumoperatingsystem.md)|<span data-ttu-id="4dbe8-206">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-206">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="4dbe8-207">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="4dbe8-207">expirationDateTime</span></span>|<span data-ttu-id="4dbe8-208">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4dbe8-208">DateTimeOffset</span></span>|<span data-ttu-id="4dbe8-209">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-209">The expiration time.</span></span>|
|<span data-ttu-id="4dbe8-210">versionNumber</span><span class="sxs-lookup"><span data-stu-id="4dbe8-210">versionNumber</span></span>|<span data-ttu-id="4dbe8-211">Cadena</span><span class="sxs-lookup"><span data-stu-id="4dbe8-211">String</span></span>|<span data-ttu-id="4dbe8-212">El número de la versión de la aplicación de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-212">The version number of iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="4dbe8-213">buildNumber</span><span class="sxs-lookup"><span data-stu-id="4dbe8-213">buildNumber</span></span>|<span data-ttu-id="4dbe8-214">Cadena</span><span class="sxs-lookup"><span data-stu-id="4dbe8-214">String</span></span>|<span data-ttu-id="4dbe8-215">El número de compilación de la aplicación de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-215">The build number of iOS Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="4dbe8-216">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4dbe8-216">Response</span></span>
<span data-ttu-id="4dbe8-217">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosLobApp](../resources/intune_apps_ioslobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-217">If successful, this method returns a `200 OK` response code and an updated [iosLobApp](../resources/intune_apps_ioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4dbe8-218">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4dbe8-218">Example</span></span>
### <a name="request"></a><span data-ttu-id="4dbe8-219">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4dbe8-219">Request</span></span>
<span data-ttu-id="4dbe8-220">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-220">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1205

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

### <a name="response"></a><span data-ttu-id="4dbe8-221">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4dbe8-221">Response</span></span>
<span data-ttu-id="4dbe8-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4dbe8-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



