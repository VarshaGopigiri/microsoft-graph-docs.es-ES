# <a name="update-ioslobapp"></a><span data-ttu-id="8c988-101">Actualizar iosLobApp</span><span class="sxs-lookup"><span data-stu-id="8c988-101">Update iosLobApp</span></span>

> <span data-ttu-id="8c988-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8c988-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8c988-103">Actualice las propiedades de un objeto [iosLobApp](../resources/intune_apps_ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-103">Update the properties of a [calendar](../resources/intune_apps_ioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8c988-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8c988-104">Prerequisites</span></span>
<span data-ttu-id="8c988-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8c988-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8c988-107">Permission type</span></span>|<span data-ttu-id="8c988-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8c988-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8c988-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8c988-109">Delegated (work or school account)</span></span>|<span data-ttu-id="8c988-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8c988-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="8c988-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8c988-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8c988-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8c988-112">Not supported.</span></span>|
|<span data-ttu-id="8c988-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8c988-113">Application</span></span>|<span data-ttu-id="8c988-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8c988-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8c988-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8c988-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="8c988-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8c988-116">Request headers</span></span>
|<span data-ttu-id="8c988-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c988-117">Header</span></span>|<span data-ttu-id="8c988-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8c988-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8c988-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="8c988-119">Authorization</span></span>|<span data-ttu-id="8c988-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8c988-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="8c988-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8c988-121">Accept</span></span>|<span data-ttu-id="8c988-122">application/json</span><span class="sxs-lookup"><span data-stu-id="8c988-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8c988-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8c988-123">Request body</span></span>
<span data-ttu-id="8c988-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosLobApp](../resources/intune_apps_ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_apps_ioslobapp.md) object.</span></span>

<span data-ttu-id="8c988-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosLobApp](../resources/intune_apps_ioslobapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="8c988-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8c988-126">Property</span></span>|<span data-ttu-id="8c988-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c988-127">Type</span></span>|<span data-ttu-id="8c988-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c988-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8c988-129">id</span><span class="sxs-lookup"><span data-stu-id="8c988-129">id</span></span>|<span data-ttu-id="8c988-130">String</span><span class="sxs-lookup"><span data-stu-id="8c988-130">String</span></span>|<span data-ttu-id="8c988-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8c988-131">Key of the setting.</span></span> <span data-ttu-id="8c988-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8c988-133">displayName</span><span class="sxs-lookup"><span data-stu-id="8c988-133">displayName</span></span>|<span data-ttu-id="8c988-134">String</span><span class="sxs-lookup"><span data-stu-id="8c988-134">String</span></span>|<span data-ttu-id="8c988-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="8c988-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="8c988-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8c988-137">description</span><span class="sxs-lookup"><span data-stu-id="8c988-137">description</span></span>|<span data-ttu-id="8c988-138">String</span><span class="sxs-lookup"><span data-stu-id="8c988-138">String</span></span>|<span data-ttu-id="8c988-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c988-139">The description of the app.</span></span> <span data-ttu-id="8c988-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8c988-141">publicador</span><span class="sxs-lookup"><span data-stu-id="8c988-141">Publisher</span></span>|<span data-ttu-id="8c988-142">String</span><span class="sxs-lookup"><span data-stu-id="8c988-142">String</span></span>|<span data-ttu-id="8c988-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c988-143">The name of the app.</span></span> <span data-ttu-id="8c988-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8c988-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="8c988-145">largeIcon</span></span>|[<span data-ttu-id="8c988-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="8c988-146">mimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="8c988-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="8c988-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="8c988-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8c988-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8c988-149">createdDateTime</span></span>|<span data-ttu-id="8c988-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8c988-150">DateTimeOffset</span></span>|<span data-ttu-id="8c988-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c988-151">The date and time when the page was created.</span></span> <span data-ttu-id="8c988-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8c988-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8c988-153">lastModifiedDateTime</span></span>|<span data-ttu-id="8c988-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8c988-154">DateTimeOffset</span></span>|<span data-ttu-id="8c988-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c988-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="8c988-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8c988-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="8c988-157">isFeatured</span></span>|<span data-ttu-id="8c988-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="8c988-158">Boolean</span></span>|<span data-ttu-id="8c988-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8c988-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="8c988-160">privacyInformationUrl</span></span>|<span data-ttu-id="8c988-161">String</span><span class="sxs-lookup"><span data-stu-id="8c988-161">String</span></span>|<span data-ttu-id="8c988-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="8c988-162">The privacy statement Url.</span></span> <span data-ttu-id="8c988-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8c988-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="8c988-164">informationUrl</span></span>|<span data-ttu-id="8c988-165">String</span><span class="sxs-lookup"><span data-stu-id="8c988-165">String</span></span>|<span data-ttu-id="8c988-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8c988-166">The more information Url.</span></span> <span data-ttu-id="8c988-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8c988-168">owner</span><span class="sxs-lookup"><span data-stu-id="8c988-168">owner</span></span>|<span data-ttu-id="8c988-169">String</span><span class="sxs-lookup"><span data-stu-id="8c988-169">String</span></span>|<span data-ttu-id="8c988-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c988-170">The owner of the timesheet.</span></span> <span data-ttu-id="8c988-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8c988-172">developer</span><span class="sxs-lookup"><span data-stu-id="8c988-172">developer</span></span>|<span data-ttu-id="8c988-173">String</span><span class="sxs-lookup"><span data-stu-id="8c988-173">String</span></span>|<span data-ttu-id="8c988-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c988-174">The name of the app.</span></span> <span data-ttu-id="8c988-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8c988-176">notas</span><span class="sxs-lookup"><span data-stu-id="8c988-176">Notes</span></span>|<span data-ttu-id="8c988-177">String</span><span class="sxs-lookup"><span data-stu-id="8c988-177">String</span></span>|<span data-ttu-id="8c988-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c988-178">Notes for the app.</span></span> <span data-ttu-id="8c988-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8c988-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="8c988-180">publishingState</span></span>|<span data-ttu-id="8c988-181">String</span><span class="sxs-lookup"><span data-stu-id="8c988-181">String</span></span>|<span data-ttu-id="8c988-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c988-182">The publishing state for the app.</span></span> <span data-ttu-id="8c988-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="8c988-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="8c988-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="8c988-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="8c988-185">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="8c988-185">committedContentVersion</span></span>|<span data-ttu-id="8c988-186">String</span><span class="sxs-lookup"><span data-stu-id="8c988-186">String</span></span>|<span data-ttu-id="8c988-187">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="8c988-187">The internal committed content version.</span></span> <span data-ttu-id="8c988-188">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-188">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="8c988-189">fileName</span><span class="sxs-lookup"><span data-stu-id="8c988-189">fileName</span></span>|<span data-ttu-id="8c988-190">String</span><span class="sxs-lookup"><span data-stu-id="8c988-190">String</span></span>|<span data-ttu-id="8c988-191">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="8c988-191">The name of the main Lob application file.</span></span> <span data-ttu-id="8c988-192">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-192">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="8c988-193">size</span><span class="sxs-lookup"><span data-stu-id="8c988-193">size</span></span>|<span data-ttu-id="8c988-194">Int64</span><span class="sxs-lookup"><span data-stu-id="8c988-194">Int64</span></span>|<span data-ttu-id="8c988-195">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="8c988-195">The total size, including all uploaded files.</span></span> <span data-ttu-id="8c988-196">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="8c988-196">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="8c988-197">bundleId</span><span class="sxs-lookup"><span data-stu-id="8c988-197">bundleId</span></span>|<span data-ttu-id="8c988-198">String</span><span class="sxs-lookup"><span data-stu-id="8c988-198">String</span></span>|<span data-ttu-id="8c988-199">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="8c988-199">The Identity Name.</span></span>|
|<span data-ttu-id="8c988-200">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="8c988-200">applicableDeviceType</span></span>|[<span data-ttu-id="8c988-201">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="8c988-201">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="8c988-202">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c988-202">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="8c988-203">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="8c988-203">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="8c988-204">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="8c988-204">iosMinimumOperatingSystem</span></span>](../resources/intune_apps_iosminimumoperatingsystem.md)|<span data-ttu-id="8c988-205">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="8c988-205">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="8c988-206">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="8c988-206">expirationDateTime</span></span>|<span data-ttu-id="8c988-207">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8c988-207">DateTimeOffset</span></span>|<span data-ttu-id="8c988-208">Fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="8c988-208">: The expiration time for the subscription.</span></span>|
|<span data-ttu-id="8c988-209">versionNumber</span><span class="sxs-lookup"><span data-stu-id="8c988-209">versionNumber</span></span>|<span data-ttu-id="8c988-210">String</span><span class="sxs-lookup"><span data-stu-id="8c988-210">String</span></span>|<span data-ttu-id="8c988-211">El número de la versión de la aplicación de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="8c988-211">The version number of iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="8c988-212">buildNumber</span><span class="sxs-lookup"><span data-stu-id="8c988-212">buildNumber</span></span>|<span data-ttu-id="8c988-213">String</span><span class="sxs-lookup"><span data-stu-id="8c988-213">String</span></span>|<span data-ttu-id="8c988-214">El número de compilación de la aplicación de línea de negocio (LoB) de iOS.</span><span class="sxs-lookup"><span data-stu-id="8c988-214">The build number of iOS Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="8c988-215">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c988-215">Response</span></span>
<span data-ttu-id="8c988-216">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosLobApp](../resources/intune_apps_ioslobapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8c988-216">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_apps_ioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8c988-217">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8c988-217">Example</span></span>
### <a name="request"></a><span data-ttu-id="8c988-218">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8c988-218">Request</span></span>
<span data-ttu-id="8c988-219">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8c988-219">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="8c988-220">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c988-220">Response</span></span>
<span data-ttu-id="8c988-p118">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8c988-p118">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



