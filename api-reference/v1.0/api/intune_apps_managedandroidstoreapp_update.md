# <a name="update-managedandroidstoreapp"></a><span data-ttu-id="6c91b-101">Actualizar managedAndroidStoreApp</span><span class="sxs-lookup"><span data-stu-id="6c91b-101">Update managedAndroidStoreApp</span></span>

> <span data-ttu-id="6c91b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6c91b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6c91b-103">Actualice las propiedades de un objeto [managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-103">Update the properties of a [managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6c91b-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6c91b-104">Prerequisites</span></span>
<span data-ttu-id="6c91b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6c91b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6c91b-107">Permission type</span></span>|<span data-ttu-id="6c91b-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6c91b-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6c91b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6c91b-109">Delegated (work or school account)</span></span>|<span data-ttu-id="6c91b-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6c91b-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="6c91b-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6c91b-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6c91b-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6c91b-112">Not supported.</span></span>|
|<span data-ttu-id="6c91b-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6c91b-113">Application</span></span>|<span data-ttu-id="6c91b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6c91b-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6c91b-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6c91b-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="6c91b-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6c91b-116">Request headers</span></span>
|<span data-ttu-id="6c91b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c91b-117">Header</span></span>|<span data-ttu-id="6c91b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6c91b-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6c91b-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="6c91b-119">Authorization</span></span>|<span data-ttu-id="6c91b-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6c91b-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6c91b-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6c91b-121">Accept</span></span>|<span data-ttu-id="6c91b-122">application/json</span><span class="sxs-lookup"><span data-stu-id="6c91b-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6c91b-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6c91b-123">Request body</span></span>
<span data-ttu-id="6c91b-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-124">In the request body, supply a JSON representation for the [managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md) object.</span></span>

<span data-ttu-id="6c91b-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-125">The following table shows the properties that are required when you create the [managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md).</span></span>

|<span data-ttu-id="6c91b-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6c91b-126">Property</span></span>|<span data-ttu-id="6c91b-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c91b-127">Type</span></span>|<span data-ttu-id="6c91b-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c91b-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6c91b-129">id</span><span class="sxs-lookup"><span data-stu-id="6c91b-129">id</span></span>|<span data-ttu-id="6c91b-130">String</span><span class="sxs-lookup"><span data-stu-id="6c91b-130">String</span></span>|<span data-ttu-id="6c91b-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6c91b-131">Key of the entity.</span></span> <span data-ttu-id="6c91b-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="6c91b-133">displayName</span><span class="sxs-lookup"><span data-stu-id="6c91b-133">displayName</span></span>|<span data-ttu-id="6c91b-134">String</span><span class="sxs-lookup"><span data-stu-id="6c91b-134">String</span></span>|<span data-ttu-id="6c91b-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="6c91b-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="6c91b-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="6c91b-137">description</span><span class="sxs-lookup"><span data-stu-id="6c91b-137">description</span></span>|<span data-ttu-id="6c91b-138">String</span><span class="sxs-lookup"><span data-stu-id="6c91b-138">String</span></span>|<span data-ttu-id="6c91b-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6c91b-139">The description of the app.</span></span> <span data-ttu-id="6c91b-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="6c91b-141">publicador</span><span class="sxs-lookup"><span data-stu-id="6c91b-141">publisher</span></span>|<span data-ttu-id="6c91b-142">String</span><span class="sxs-lookup"><span data-stu-id="6c91b-142">String</span></span>|<span data-ttu-id="6c91b-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6c91b-143">The publisher of the app.</span></span> <span data-ttu-id="6c91b-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="6c91b-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="6c91b-145">largeIcon</span></span>|[<span data-ttu-id="6c91b-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="6c91b-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="6c91b-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="6c91b-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="6c91b-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="6c91b-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="6c91b-149">createdDateTime</span></span>|<span data-ttu-id="6c91b-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6c91b-150">DateTimeOffset</span></span>|<span data-ttu-id="6c91b-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6c91b-151">The date and time the app was created.</span></span> <span data-ttu-id="6c91b-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="6c91b-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="6c91b-153">lastModifiedDateTime</span></span>|<span data-ttu-id="6c91b-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6c91b-154">DateTimeOffset</span></span>|<span data-ttu-id="6c91b-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6c91b-155">The date and time the app was last modified.</span></span> <span data-ttu-id="6c91b-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="6c91b-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="6c91b-157">isFeatured</span></span>|<span data-ttu-id="6c91b-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="6c91b-158">Boolean</span></span>|<span data-ttu-id="6c91b-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="6c91b-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="6c91b-160">privacyInformationUrl</span></span>|<span data-ttu-id="6c91b-161">String</span><span class="sxs-lookup"><span data-stu-id="6c91b-161">String</span></span>|<span data-ttu-id="6c91b-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="6c91b-162">The privacy statement Url.</span></span> <span data-ttu-id="6c91b-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="6c91b-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="6c91b-164">informationUrl</span></span>|<span data-ttu-id="6c91b-165">String</span><span class="sxs-lookup"><span data-stu-id="6c91b-165">String</span></span>|<span data-ttu-id="6c91b-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="6c91b-166">The more information Url.</span></span> <span data-ttu-id="6c91b-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="6c91b-168">owner</span><span class="sxs-lookup"><span data-stu-id="6c91b-168">owner</span></span>|<span data-ttu-id="6c91b-169">String</span><span class="sxs-lookup"><span data-stu-id="6c91b-169">String</span></span>|<span data-ttu-id="6c91b-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6c91b-170">The owner of the app.</span></span> <span data-ttu-id="6c91b-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="6c91b-172">developer</span><span class="sxs-lookup"><span data-stu-id="6c91b-172">developer</span></span>|<span data-ttu-id="6c91b-173">String</span><span class="sxs-lookup"><span data-stu-id="6c91b-173">String</span></span>|<span data-ttu-id="6c91b-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6c91b-174">The developer of the app.</span></span> <span data-ttu-id="6c91b-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="6c91b-176">notas</span><span class="sxs-lookup"><span data-stu-id="6c91b-176">notes</span></span>|<span data-ttu-id="6c91b-177">String</span><span class="sxs-lookup"><span data-stu-id="6c91b-177">String</span></span>|<span data-ttu-id="6c91b-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6c91b-178">Notes for the app.</span></span> <span data-ttu-id="6c91b-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="6c91b-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="6c91b-180">publishingState</span></span>|[<span data-ttu-id="6c91b-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="6c91b-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="6c91b-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6c91b-182">The publishing state for the app.</span></span> <span data-ttu-id="6c91b-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="6c91b-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="6c91b-184">Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md).</span></span> <span data-ttu-id="6c91b-185">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="6c91b-185">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="6c91b-186">appAvailability</span><span class="sxs-lookup"><span data-stu-id="6c91b-186">appAvailability</span></span>|[<span data-ttu-id="6c91b-187">managedAppAvailability</span><span class="sxs-lookup"><span data-stu-id="6c91b-187">managedAppAvailability</span></span>](../resources/intune_apps_managedappavailability.md)|<span data-ttu-id="6c91b-188">Disponibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6c91b-188">The Application's availability.</span></span> <span data-ttu-id="6c91b-189">Se hereda de [managedApp](../resources/intune_apps_managedapp.md).</span><span class="sxs-lookup"><span data-stu-id="6c91b-189">Inherited from [managedApp](../resources/intune_apps_managedapp.md).</span></span> <span data-ttu-id="6c91b-190">Los valores posibles son: `global` y `lineOfBusiness`.</span><span class="sxs-lookup"><span data-stu-id="6c91b-190">Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="6c91b-191">versión</span><span class="sxs-lookup"><span data-stu-id="6c91b-191">version</span></span>|<span data-ttu-id="6c91b-192">String</span><span class="sxs-lookup"><span data-stu-id="6c91b-192">String</span></span>|<span data-ttu-id="6c91b-193">Versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6c91b-193">The Application's version.</span></span> <span data-ttu-id="6c91b-194">Heredado de [managedApp](../resources/intune_apps_managedapp.md)</span><span class="sxs-lookup"><span data-stu-id="6c91b-194">Inherited from [managedApp](../resources/intune_apps_managedapp.md)</span></span>|
|<span data-ttu-id="6c91b-195">packageId</span><span class="sxs-lookup"><span data-stu-id="6c91b-195">packageId</span></span>|<span data-ttu-id="6c91b-196">String</span><span class="sxs-lookup"><span data-stu-id="6c91b-196">String</span></span>|<span data-ttu-id="6c91b-197">El identificador de paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6c91b-197">The app's package ID.</span></span>|
|<span data-ttu-id="6c91b-198">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="6c91b-198">appStoreUrl</span></span>|<span data-ttu-id="6c91b-199">String</span><span class="sxs-lookup"><span data-stu-id="6c91b-199">String</span></span>|<span data-ttu-id="6c91b-200">La AppStoreUrl de Android.</span><span class="sxs-lookup"><span data-stu-id="6c91b-200">The Android AppStoreUrl.</span></span>|
|<span data-ttu-id="6c91b-201">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="6c91b-201">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="6c91b-202">androidMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="6c91b-202">androidMinimumOperatingSystem</span></span>](../resources/intune_apps_androidminimumoperatingsystem.md)|<span data-ttu-id="6c91b-203">El valor para el sistema operativo mínimo compatible.</span><span class="sxs-lookup"><span data-stu-id="6c91b-203">The value for the minimum supported operating system.</span></span>|



## <a name="response"></a><span data-ttu-id="6c91b-204">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c91b-204">Response</span></span>
<span data-ttu-id="6c91b-205">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6c91b-205">If successful, this method returns a `200 OK` response code and an updated [managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6c91b-206">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6c91b-206">Example</span></span>
### <a name="request"></a><span data-ttu-id="6c91b-207">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6c91b-207">Request</span></span>
<span data-ttu-id="6c91b-208">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6c91b-208">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1016

{
  "@odata.type": "#microsoft.graph.managedAndroidStoreApp",
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
  "packageId": "Package Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
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
  }
}
```

### <a name="response"></a><span data-ttu-id="6c91b-209">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c91b-209">Response</span></span>
<span data-ttu-id="6c91b-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6c91b-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1188

{
  "@odata.type": "#microsoft.graph.managedAndroidStoreApp",
  "id": "89e7e991-e991-89e7-91e9-e78991e9e789",
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
  "packageId": "Package Id value",
  "appStoreUrl": "https://example.com/appStoreUrl/",
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
  }
}
```



