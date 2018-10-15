# <a name="update-managediosstoreapp"></a><span data-ttu-id="c8d4b-101">Actualizar managedIOSStoreApp</span><span class="sxs-lookup"><span data-stu-id="c8d4b-101">Update managedIOSStoreApp</span></span>

> <span data-ttu-id="c8d4b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c8d4b-103">Actualice las propiedades de un objeto [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-103">Update the properties of a [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c8d4b-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c8d4b-104">Prerequisites</span></span>
<span data-ttu-id="c8d4b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c8d4b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c8d4b-107">Permission type</span></span>|<span data-ttu-id="c8d4b-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c8d4b-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c8d4b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c8d4b-109">Delegated (work or school account)</span></span>|<span data-ttu-id="c8d4b-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c8d4b-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="c8d4b-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c8d4b-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c8d4b-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-112">Not supported.</span></span>|
|<span data-ttu-id="c8d4b-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c8d4b-113">Application</span></span>|<span data-ttu-id="c8d4b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c8d4b-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c8d4b-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="c8d4b-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c8d4b-116">Request headers</span></span>
|<span data-ttu-id="c8d4b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8d4b-117">Header</span></span>|<span data-ttu-id="c8d4b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c8d4b-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c8d4b-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="c8d4b-119">Authorization</span></span>|<span data-ttu-id="c8d4b-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c8d4b-121">Accept</span><span class="sxs-lookup"><span data-stu-id="c8d4b-121">Accept</span></span>|<span data-ttu-id="c8d4b-122">application/json</span><span class="sxs-lookup"><span data-stu-id="c8d4b-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c8d4b-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c8d4b-123">Request body</span></span>
<span data-ttu-id="c8d4b-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-124">In the request body, supply a JSON representation for the [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md) object.</span></span>

<span data-ttu-id="c8d4b-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-125">The following table shows the properties that are required when you create the [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md).</span></span>

|<span data-ttu-id="c8d4b-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c8d4b-126">Property</span></span>|<span data-ttu-id="c8d4b-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="c8d4b-127">Type</span></span>|<span data-ttu-id="c8d4b-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8d4b-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c8d4b-129">id</span><span class="sxs-lookup"><span data-stu-id="c8d4b-129">id</span></span>|<span data-ttu-id="c8d4b-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8d4b-130">String</span></span>|<span data-ttu-id="c8d4b-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-131">Key of the entity.</span></span> <span data-ttu-id="c8d4b-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c8d4b-133">displayName</span><span class="sxs-lookup"><span data-stu-id="c8d4b-133">displayName</span></span>|<span data-ttu-id="c8d4b-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8d4b-134">String</span></span>|<span data-ttu-id="c8d4b-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="c8d4b-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c8d4b-137">description</span><span class="sxs-lookup"><span data-stu-id="c8d4b-137">description</span></span>|<span data-ttu-id="c8d4b-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8d4b-138">String</span></span>|<span data-ttu-id="c8d4b-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-139">The description of the app.</span></span> <span data-ttu-id="c8d4b-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c8d4b-141">publicador</span><span class="sxs-lookup"><span data-stu-id="c8d4b-141">publisher</span></span>|<span data-ttu-id="c8d4b-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8d4b-142">String</span></span>|<span data-ttu-id="c8d4b-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-143">The publisher of the app.</span></span> <span data-ttu-id="c8d4b-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c8d4b-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="c8d4b-145">largeIcon</span></span>|[<span data-ttu-id="c8d4b-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="c8d4b-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="c8d4b-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="c8d4b-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c8d4b-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c8d4b-149">createdDateTime</span></span>|<span data-ttu-id="c8d4b-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c8d4b-150">DateTimeOffset</span></span>|<span data-ttu-id="c8d4b-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-151">The date and time the app was created.</span></span> <span data-ttu-id="c8d4b-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c8d4b-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c8d4b-153">lastModifiedDateTime</span></span>|<span data-ttu-id="c8d4b-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c8d4b-154">DateTimeOffset</span></span>|<span data-ttu-id="c8d4b-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-155">The date and time the app was last modified.</span></span> <span data-ttu-id="c8d4b-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c8d4b-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="c8d4b-157">isFeatured</span></span>|<span data-ttu-id="c8d4b-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="c8d4b-158">Boolean</span></span>|<span data-ttu-id="c8d4b-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c8d4b-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="c8d4b-160">privacyInformationUrl</span></span>|<span data-ttu-id="c8d4b-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8d4b-161">String</span></span>|<span data-ttu-id="c8d4b-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-162">The privacy statement Url.</span></span> <span data-ttu-id="c8d4b-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c8d4b-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="c8d4b-164">informationUrl</span></span>|<span data-ttu-id="c8d4b-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8d4b-165">String</span></span>|<span data-ttu-id="c8d4b-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-166">The more information Url.</span></span> <span data-ttu-id="c8d4b-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c8d4b-168">owner</span><span class="sxs-lookup"><span data-stu-id="c8d4b-168">owner</span></span>|<span data-ttu-id="c8d4b-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8d4b-169">String</span></span>|<span data-ttu-id="c8d4b-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-170">The owner of the app.</span></span> <span data-ttu-id="c8d4b-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c8d4b-172">developer</span><span class="sxs-lookup"><span data-stu-id="c8d4b-172">developer</span></span>|<span data-ttu-id="c8d4b-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8d4b-173">String</span></span>|<span data-ttu-id="c8d4b-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-174">The developer of the app.</span></span> <span data-ttu-id="c8d4b-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c8d4b-176">notes</span><span class="sxs-lookup"><span data-stu-id="c8d4b-176">notes</span></span>|<span data-ttu-id="c8d4b-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8d4b-177">String</span></span>|<span data-ttu-id="c8d4b-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-178">Notes for the app.</span></span> <span data-ttu-id="c8d4b-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="c8d4b-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="c8d4b-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="c8d4b-180">publishingState</span></span>|[<span data-ttu-id="c8d4b-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="c8d4b-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="c8d4b-p114">El estado de publicación para la aplicación. La aplicación no se puede asignar a menos que se publique la aplicación. Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing`, `published`.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-p114">The publishing state for the app. The app cannot be assigned unless the app is published. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md). The possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="c8d4b-186">appAvailability</span><span class="sxs-lookup"><span data-stu-id="c8d4b-186">appAvailability</span></span>|[<span data-ttu-id="c8d4b-187">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="c8d4b-187">managedAppAvailability</span></span>](../resources/intune_apps_managedappavailability.md)|<span data-ttu-id="c8d4b-p115">Disponibilidad de la aplicación. Se hereda de [managedApp](../resources/intune_apps_managedapp.md). Los valores posibles son: `global`, `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-p115">The Application's availability. Inherited from [managedApp](../resources/intune_apps_managedapp.md). The possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="c8d4b-191">version</span><span class="sxs-lookup"><span data-stu-id="c8d4b-191">version</span></span>|<span data-ttu-id="c8d4b-192">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8d4b-192">String</span></span>|<span data-ttu-id="c8d4b-193">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-193">The Application's version.</span></span> <span data-ttu-id="c8d4b-194">Heredado de [managedApp](../resources/intune_apps_managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="c8d4b-194">Inherited from [managedApp](../resources/intune_apps_managedapp.md)</span></span>|
|<span data-ttu-id="c8d4b-195">bundleId</span><span class="sxs-lookup"><span data-stu-id="c8d4b-195">bundleId</span></span>|<span data-ttu-id="c8d4b-196">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8d4b-196">String</span></span>|<span data-ttu-id="c8d4b-197">El identificador de lote de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-197">The app's Bundle ID.</span></span>|
|<span data-ttu-id="c8d4b-198">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="c8d4b-198">appStoreUrl</span></span>|<span data-ttu-id="c8d4b-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="c8d4b-199">String</span></span>|<span data-ttu-id="c8d4b-200">La AppStoreUrl de Apple.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-200">The Apple AppStoreUrl.</span></span>|
|<span data-ttu-id="c8d4b-201">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="c8d4b-201">applicableDeviceType</span></span>|[<span data-ttu-id="c8d4b-202">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="c8d4b-202">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="c8d4b-203">Arquitectura de iOS en la que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-203">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="c8d4b-204">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c8d4b-204">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="c8d4b-205">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c8d4b-205">iosMinimumOperatingSystem</span></span>](../resources/intune_apps_iosminimumoperatingsystem.md)|<span data-ttu-id="c8d4b-206">El valor para el sistema operativo mínimo compatible.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-206">The value for the minimum supported operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="c8d4b-207">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c8d4b-207">Response</span></span>
<span data-ttu-id="c8d4b-208">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-208">If successful, this method returns a `200 OK` response code and an updated [managedIOSStoreApp](../resources/intune_apps_managediosstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c8d4b-209">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c8d4b-209">Example</span></span>
### <a name="request"></a><span data-ttu-id="c8d4b-210">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c8d4b-210">Request</span></span>
<span data-ttu-id="c8d4b-211">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-211">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1071

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
    "v11_0": true
  }
}
```

### <a name="response"></a><span data-ttu-id="c8d4b-212">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c8d4b-212">Response</span></span>
<span data-ttu-id="c8d4b-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c8d4b-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1236

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
    "v11_0": true
  }
}
```








