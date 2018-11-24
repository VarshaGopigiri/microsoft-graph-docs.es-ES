# <a name="update-managediosstoreapp"></a><span data-ttu-id="463c9-101">Actualizar managedIOSStoreApp</span><span class="sxs-lookup"><span data-stu-id="463c9-101">Update managedIOSStoreApp</span></span>

> <span data-ttu-id="463c9-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="463c9-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="463c9-103">Actualice las propiedades de un objeto [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-103">Update the properties of a [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="463c9-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="463c9-104">Prerequisites</span></span>
<span data-ttu-id="463c9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="463c9-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="463c9-107">Permission type</span></span>|<span data-ttu-id="463c9-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="463c9-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="463c9-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="463c9-109">Delegated (work or school account)</span></span>|<span data-ttu-id="463c9-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="463c9-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="463c9-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="463c9-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="463c9-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="463c9-112">Not supported.</span></span>|
|<span data-ttu-id="463c9-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="463c9-113">Application</span></span>|<span data-ttu-id="463c9-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="463c9-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="463c9-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="463c9-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="463c9-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="463c9-116">Request headers</span></span>
|<span data-ttu-id="463c9-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="463c9-117">Header</span></span>|<span data-ttu-id="463c9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="463c9-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="463c9-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="463c9-119">Authorization</span></span>|<span data-ttu-id="463c9-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="463c9-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="463c9-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="463c9-121">Accept</span></span>|<span data-ttu-id="463c9-122">application/json</span><span class="sxs-lookup"><span data-stu-id="463c9-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="463c9-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="463c9-123">Request body</span></span>
<span data-ttu-id="463c9-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-124">In the request body, supply a JSON representation for the [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md) object.</span></span>

<span data-ttu-id="463c9-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-125">The following table shows the properties that are required when you create the [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md).</span></span>

|<span data-ttu-id="463c9-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="463c9-126">Property</span></span>|<span data-ttu-id="463c9-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="463c9-127">Type</span></span>|<span data-ttu-id="463c9-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="463c9-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="463c9-129">id</span><span class="sxs-lookup"><span data-stu-id="463c9-129">id</span></span>|<span data-ttu-id="463c9-130">String</span><span class="sxs-lookup"><span data-stu-id="463c9-130">String</span></span>|<span data-ttu-id="463c9-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="463c9-131">Key of the entity.</span></span> <span data-ttu-id="463c9-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="463c9-133">displayName</span><span class="sxs-lookup"><span data-stu-id="463c9-133">displayName</span></span>|<span data-ttu-id="463c9-134">String</span><span class="sxs-lookup"><span data-stu-id="463c9-134">String</span></span>|<span data-ttu-id="463c9-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="463c9-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="463c9-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="463c9-137">description</span><span class="sxs-lookup"><span data-stu-id="463c9-137">description</span></span>|<span data-ttu-id="463c9-138">String</span><span class="sxs-lookup"><span data-stu-id="463c9-138">String</span></span>|<span data-ttu-id="463c9-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="463c9-139">The description of the app.</span></span> <span data-ttu-id="463c9-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="463c9-141">publicador</span><span class="sxs-lookup"><span data-stu-id="463c9-141">publisher</span></span>|<span data-ttu-id="463c9-142">String</span><span class="sxs-lookup"><span data-stu-id="463c9-142">String</span></span>|<span data-ttu-id="463c9-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="463c9-143">The publisher of the app.</span></span> <span data-ttu-id="463c9-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="463c9-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="463c9-145">largeIcon</span></span>|[<span data-ttu-id="463c9-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="463c9-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="463c9-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="463c9-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="463c9-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="463c9-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="463c9-149">createdDateTime</span></span>|<span data-ttu-id="463c9-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="463c9-150">DateTimeOffset</span></span>|<span data-ttu-id="463c9-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="463c9-151">The date and time the app was created.</span></span> <span data-ttu-id="463c9-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="463c9-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="463c9-153">lastModifiedDateTime</span></span>|<span data-ttu-id="463c9-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="463c9-154">DateTimeOffset</span></span>|<span data-ttu-id="463c9-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="463c9-155">The date and time the app was last modified.</span></span> <span data-ttu-id="463c9-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="463c9-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="463c9-157">isFeatured</span></span>|<span data-ttu-id="463c9-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="463c9-158">Boolean</span></span>|<span data-ttu-id="463c9-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="463c9-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="463c9-160">privacyInformationUrl</span></span>|<span data-ttu-id="463c9-161">String</span><span class="sxs-lookup"><span data-stu-id="463c9-161">String</span></span>|<span data-ttu-id="463c9-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="463c9-162">The privacy statement Url.</span></span> <span data-ttu-id="463c9-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="463c9-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="463c9-164">informationUrl</span></span>|<span data-ttu-id="463c9-165">String</span><span class="sxs-lookup"><span data-stu-id="463c9-165">String</span></span>|<span data-ttu-id="463c9-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="463c9-166">The more information Url.</span></span> <span data-ttu-id="463c9-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="463c9-168">owner</span><span class="sxs-lookup"><span data-stu-id="463c9-168">owner</span></span>|<span data-ttu-id="463c9-169">String</span><span class="sxs-lookup"><span data-stu-id="463c9-169">String</span></span>|<span data-ttu-id="463c9-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="463c9-170">The owner of the app.</span></span> <span data-ttu-id="463c9-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="463c9-172">developer</span><span class="sxs-lookup"><span data-stu-id="463c9-172">developer</span></span>|<span data-ttu-id="463c9-173">String</span><span class="sxs-lookup"><span data-stu-id="463c9-173">String</span></span>|<span data-ttu-id="463c9-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="463c9-174">The developer of the app.</span></span> <span data-ttu-id="463c9-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="463c9-176">notas</span><span class="sxs-lookup"><span data-stu-id="463c9-176">notes</span></span>|<span data-ttu-id="463c9-177">String</span><span class="sxs-lookup"><span data-stu-id="463c9-177">String</span></span>|<span data-ttu-id="463c9-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="463c9-178">Notes for the app.</span></span> <span data-ttu-id="463c9-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="463c9-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="463c9-180">publishingState</span></span>|[<span data-ttu-id="463c9-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="463c9-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="463c9-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="463c9-182">The publishing state for the app.</span></span> <span data-ttu-id="463c9-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="463c9-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="463c9-184">Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md).</span></span> <span data-ttu-id="463c9-185">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="463c9-185">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="463c9-186">appAvailability</span><span class="sxs-lookup"><span data-stu-id="463c9-186">appAvailability</span></span>|[<span data-ttu-id="463c9-187">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="463c9-187">managedAppAvailability</span></span>](../resources/intune_apps_managedappavailability.md)|<span data-ttu-id="463c9-188">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="463c9-188">The Application's availability.</span></span> <span data-ttu-id="463c9-189">Se hereda de [managedApp](../resources/intune_apps_managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="463c9-189">Inherited from [managedApp](../resources/intune_apps_managedapp.md).</span></span> <span data-ttu-id="463c9-190">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="463c9-190">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="463c9-191">versión</span><span class="sxs-lookup"><span data-stu-id="463c9-191">version</span></span>|<span data-ttu-id="463c9-192">String</span><span class="sxs-lookup"><span data-stu-id="463c9-192">String</span></span>|<span data-ttu-id="463c9-193">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="463c9-193">The Application's version.</span></span> <span data-ttu-id="463c9-194">Heredado de [managedApp](../resources/intune_apps_managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="463c9-194">Inherited from [managedApp](../resources/intune_apps_managedapp.md)</span></span>|
|<span data-ttu-id="463c9-195">bundleId</span><span class="sxs-lookup"><span data-stu-id="463c9-195">bundleId</span></span>|<span data-ttu-id="463c9-196">String</span><span class="sxs-lookup"><span data-stu-id="463c9-196">String</span></span>|<span data-ttu-id="463c9-197">El identificador de lote de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="463c9-197">The app's Bundle ID.</span></span>|
|<span data-ttu-id="463c9-198">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="463c9-198">appStoreUrl</span></span>|<span data-ttu-id="463c9-199">String</span><span class="sxs-lookup"><span data-stu-id="463c9-199">String</span></span>|<span data-ttu-id="463c9-200">La AppStoreUrl de Apple.</span><span class="sxs-lookup"><span data-stu-id="463c9-200">The Apple AppStoreUrl.</span></span>|
|<span data-ttu-id="463c9-201">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="463c9-201">applicableDeviceType</span></span>|[<span data-ttu-id="463c9-202">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="463c9-202">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="463c9-203">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="463c9-203">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="463c9-204">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="463c9-204">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="463c9-205">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="463c9-205">iosMinimumOperatingSystem</span></span>](../resources/intune_apps_iosminimumoperatingsystem.md)|<span data-ttu-id="463c9-206">El valor para el sistema operativo mínimo compatible.</span><span class="sxs-lookup"><span data-stu-id="463c9-206">The value for the minimum supported operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="463c9-207">Respuesta</span><span class="sxs-lookup"><span data-stu-id="463c9-207">Response</span></span>
<span data-ttu-id="463c9-208">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="463c9-208">If successful, this method returns a `200 OK` response code and an updated [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="463c9-209">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="463c9-209">Example</span></span>
### <a name="request"></a><span data-ttu-id="463c9-210">Solicitud</span><span class="sxs-lookup"><span data-stu-id="463c9-210">Request</span></span>
<span data-ttu-id="463c9-211">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="463c9-211">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1084

{
  "@odata.type": "#microsoft.graph.managedIOSStoreApp",
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
  "bundleId": "Bundle Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
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
  }
}
```

### <a name="response"></a><span data-ttu-id="463c9-212">Respuesta</span><span class="sxs-lookup"><span data-stu-id="463c9-212">Response</span></span>
<span data-ttu-id="463c9-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="463c9-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1256

{
  "@odata.type": "#microsoft.graph.managedIOSStoreApp",
  "id": "51b9830f-830f-51b9-0f83-b9510f83b951",
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
  "bundleId": "Bundle Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
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
  }
}
```



