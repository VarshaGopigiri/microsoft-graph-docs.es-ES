# <a name="update-ioslobapp"></a><span data-ttu-id="56f0a-101">Actualizar iosLobApp</span><span class="sxs-lookup"><span data-stu-id="56f0a-101">Update iosLobApp</span></span>

> <span data-ttu-id="56f0a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="56f0a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="56f0a-103">Actualice las propiedades de un objeto [iosLobApp](../resources/intune_apps_ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-103">Update the properties of a [iosLobApp](../resources/intune_apps_ioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="56f0a-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="56f0a-104">Prerequisites</span></span>
<span data-ttu-id="56f0a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="56f0a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="56f0a-107">Permission type</span></span>|<span data-ttu-id="56f0a-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="56f0a-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="56f0a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="56f0a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="56f0a-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="56f0a-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="56f0a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="56f0a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="56f0a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56f0a-112">Not supported.</span></span>|
|<span data-ttu-id="56f0a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="56f0a-113">Application</span></span>|<span data-ttu-id="56f0a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="56f0a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="56f0a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="56f0a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="56f0a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="56f0a-116">Request headers</span></span>
|<span data-ttu-id="56f0a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56f0a-117">Header</span></span>|<span data-ttu-id="56f0a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="56f0a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="56f0a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="56f0a-119">Authorization</span></span>|<span data-ttu-id="56f0a-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="56f0a-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="56f0a-121">Accept</span><span class="sxs-lookup"><span data-stu-id="56f0a-121">Accept</span></span>|<span data-ttu-id="56f0a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="56f0a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="56f0a-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="56f0a-123">Request body</span></span>
<span data-ttu-id="56f0a-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosLobApp](../resources/intune_apps_ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-124">In the request body, supply a JSON representation for the [iosLobApp](../resources/intune_apps_ioslobapp.md) object.</span></span>

<span data-ttu-id="56f0a-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosLobApp](../resources/intune_apps_ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-125">The following table shows the properties that are required when you create the [iosLobApp](../resources/intune_apps_ioslobapp.md).</span></span>

|<span data-ttu-id="56f0a-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="56f0a-126">Property</span></span>|<span data-ttu-id="56f0a-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="56f0a-127">Type</span></span>|<span data-ttu-id="56f0a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="56f0a-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="56f0a-129">id</span><span class="sxs-lookup"><span data-stu-id="56f0a-129">id</span></span>|<span data-ttu-id="56f0a-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="56f0a-130">String</span></span>|<span data-ttu-id="56f0a-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="56f0a-131">Key of the entity.</span></span> <span data-ttu-id="56f0a-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="56f0a-133">displayName</span><span class="sxs-lookup"><span data-stu-id="56f0a-133">displayName</span></span>|<span data-ttu-id="56f0a-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="56f0a-134">String</span></span>|<span data-ttu-id="56f0a-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="56f0a-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="56f0a-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="56f0a-137">descripción</span><span class="sxs-lookup"><span data-stu-id="56f0a-137">description</span></span>|<span data-ttu-id="56f0a-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="56f0a-138">String</span></span>|<span data-ttu-id="56f0a-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56f0a-139">The description of the app.</span></span> <span data-ttu-id="56f0a-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="56f0a-141">publicador</span><span class="sxs-lookup"><span data-stu-id="56f0a-141">publisher</span></span>|<span data-ttu-id="56f0a-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="56f0a-142">String</span></span>|<span data-ttu-id="56f0a-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56f0a-143">The publisher of the app.</span></span> <span data-ttu-id="56f0a-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="56f0a-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="56f0a-145">largeIcon</span></span>|[<span data-ttu-id="56f0a-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="56f0a-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="56f0a-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="56f0a-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="56f0a-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="56f0a-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="56f0a-149">createdDateTime</span></span>|<span data-ttu-id="56f0a-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="56f0a-150">DateTimeOffset</span></span>|<span data-ttu-id="56f0a-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56f0a-151">The date and time the app was created.</span></span> <span data-ttu-id="56f0a-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="56f0a-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="56f0a-153">lastModifiedDateTime</span></span>|<span data-ttu-id="56f0a-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="56f0a-154">DateTimeOffset</span></span>|<span data-ttu-id="56f0a-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56f0a-155">The date and time the app was last modified.</span></span> <span data-ttu-id="56f0a-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="56f0a-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="56f0a-157">isFeatured</span></span>|<span data-ttu-id="56f0a-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="56f0a-158">Boolean</span></span>|<span data-ttu-id="56f0a-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="56f0a-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="56f0a-160">privacyInformationUrl</span></span>|<span data-ttu-id="56f0a-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="56f0a-161">String</span></span>|<span data-ttu-id="56f0a-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="56f0a-162">The privacy statement Url.</span></span> <span data-ttu-id="56f0a-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="56f0a-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="56f0a-164">informationUrl</span></span>|<span data-ttu-id="56f0a-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="56f0a-165">String</span></span>|<span data-ttu-id="56f0a-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="56f0a-166">The more information Url.</span></span> <span data-ttu-id="56f0a-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="56f0a-168">owner</span><span class="sxs-lookup"><span data-stu-id="56f0a-168">owner</span></span>|<span data-ttu-id="56f0a-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="56f0a-169">String</span></span>|<span data-ttu-id="56f0a-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56f0a-170">The owner of the app.</span></span> <span data-ttu-id="56f0a-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="56f0a-172">developer</span><span class="sxs-lookup"><span data-stu-id="56f0a-172">developer</span></span>|<span data-ttu-id="56f0a-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="56f0a-173">String</span></span>|<span data-ttu-id="56f0a-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56f0a-174">The developer of the app.</span></span> <span data-ttu-id="56f0a-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="56f0a-176">notes</span><span class="sxs-lookup"><span data-stu-id="56f0a-176">notes</span></span>|<span data-ttu-id="56f0a-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="56f0a-177">String</span></span>|<span data-ttu-id="56f0a-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="56f0a-178">Notes for the app.</span></span> <span data-ttu-id="56f0a-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="56f0a-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="56f0a-180">publishingState</span></span>|[<span data-ttu-id="56f0a-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="56f0a-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="56f0a-p114">El estado de publicación para la aplicación. La aplicación no se puede asignar a menos que se publique la aplicación. Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing`, `published`.</span><span class="sxs-lookup"><span data-stu-id="56f0a-p114">The publishing state for the app. The app cannot be assigned unless the app is published. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md). The possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="56f0a-186">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="56f0a-186">committedContentVersion</span></span>|<span data-ttu-id="56f0a-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="56f0a-187">String</span></span>|<span data-ttu-id="56f0a-188">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="56f0a-188">The internal committed content version.</span></span> <span data-ttu-id="56f0a-189">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-189">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="56f0a-190">fileName</span><span class="sxs-lookup"><span data-stu-id="56f0a-190">fileName</span></span>|<span data-ttu-id="56f0a-191">Cadena</span><span class="sxs-lookup"><span data-stu-id="56f0a-191">String</span></span>|<span data-ttu-id="56f0a-192">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="56f0a-192">The name of the main Lob application file.</span></span> <span data-ttu-id="56f0a-193">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-193">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="56f0a-194">size</span><span class="sxs-lookup"><span data-stu-id="56f0a-194">size</span></span>|<span data-ttu-id="56f0a-195">Int64</span><span class="sxs-lookup"><span data-stu-id="56f0a-195">Int64</span></span>|<span data-ttu-id="56f0a-196">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="56f0a-196">The total size, including all uploaded files.</span></span> <span data-ttu-id="56f0a-197">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="56f0a-197">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="56f0a-198">bundleId</span><span class="sxs-lookup"><span data-stu-id="56f0a-198">bundleId</span></span>|<span data-ttu-id="56f0a-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="56f0a-199">String</span></span>|<span data-ttu-id="56f0a-200">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="56f0a-200">The Identity Name.</span></span>|
|<span data-ttu-id="56f0a-201">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="56f0a-201">applicableDeviceType</span></span>|[<span data-ttu-id="56f0a-202">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="56f0a-202">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="56f0a-203">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="56f0a-203">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="56f0a-204">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="56f0a-204">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="56f0a-205">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="56f0a-205">iosMinimumOperatingSystem</span></span>](../resources/intune_apps_iosminimumoperatingsystem.md)|<span data-ttu-id="56f0a-206">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="56f0a-206">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="56f0a-207">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="56f0a-207">expirationDateTime</span></span>|<span data-ttu-id="56f0a-208">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="56f0a-208">DateTimeOffset</span></span>|<span data-ttu-id="56f0a-209">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="56f0a-209">The expiration time.</span></span>|
|<span data-ttu-id="56f0a-210">versionNumber</span><span class="sxs-lookup"><span data-stu-id="56f0a-210">versionNumber</span></span>|<span data-ttu-id="56f0a-211">Cadena</span><span class="sxs-lookup"><span data-stu-id="56f0a-211">String</span></span>|<span data-ttu-id="56f0a-212">El número de la versión de la aplicación de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="56f0a-212">The version number of iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="56f0a-213">buildNumber</span><span class="sxs-lookup"><span data-stu-id="56f0a-213">buildNumber</span></span>|<span data-ttu-id="56f0a-214">Cadena</span><span class="sxs-lookup"><span data-stu-id="56f0a-214">String</span></span>|<span data-ttu-id="56f0a-215">El número de compilación de la aplicación de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="56f0a-215">The build number of iOS Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="56f0a-216">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56f0a-216">Response</span></span>
<span data-ttu-id="56f0a-217">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosLobApp](../resources/intune_apps_ioslobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="56f0a-217">If successful, this method returns a `200 OK` response code and an updated [iosLobApp](../resources/intune_apps_ioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="56f0a-218">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="56f0a-218">Example</span></span>
### <a name="request"></a><span data-ttu-id="56f0a-219">Solicitud</span><span class="sxs-lookup"><span data-stu-id="56f0a-219">Request</span></span>
<span data-ttu-id="56f0a-220">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="56f0a-220">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="56f0a-221">Respuesta</span><span class="sxs-lookup"><span data-stu-id="56f0a-221">Response</span></span>
<span data-ttu-id="56f0a-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="56f0a-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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








