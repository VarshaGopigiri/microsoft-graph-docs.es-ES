# <a name="update-iosvppapp"></a><span data-ttu-id="46fc1-101">Actualizar iosVppApp</span><span class="sxs-lookup"><span data-stu-id="46fc1-101">Update iosVppApp</span></span>

> <span data-ttu-id="46fc1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="46fc1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="46fc1-103">Actualice las propiedades de un objeto [iosVppApp](../resources/intune_apps_iosvppapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-103">Update the properties of a [iosVppApp](../resources/intune_apps_iosvppapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="46fc1-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="46fc1-104">Prerequisites</span></span>
<span data-ttu-id="46fc1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="46fc1-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="46fc1-107">Permission type</span></span>|<span data-ttu-id="46fc1-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="46fc1-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="46fc1-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="46fc1-109">Delegated (work or school account)</span></span>|<span data-ttu-id="46fc1-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="46fc1-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="46fc1-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="46fc1-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="46fc1-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46fc1-112">Not supported.</span></span>|
|<span data-ttu-id="46fc1-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="46fc1-113">Application</span></span>|<span data-ttu-id="46fc1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46fc1-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="46fc1-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="46fc1-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="46fc1-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="46fc1-116">Request headers</span></span>
|<span data-ttu-id="46fc1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46fc1-117">Header</span></span>|<span data-ttu-id="46fc1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="46fc1-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="46fc1-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="46fc1-119">Authorization</span></span>|<span data-ttu-id="46fc1-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="46fc1-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="46fc1-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="46fc1-121">Accept</span></span>|<span data-ttu-id="46fc1-122">application/json</span><span class="sxs-lookup"><span data-stu-id="46fc1-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="46fc1-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="46fc1-123">Request body</span></span>
<span data-ttu-id="46fc1-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosVppApp](../resources/intune_apps_iosvppapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-124">In the request body, supply a JSON representation for the [iosVppApp](../resources/intune_apps_iosvppapp.md) object.</span></span>

<span data-ttu-id="46fc1-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosVppApp](../resources/intune_apps_iosvppapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-125">The following table shows the properties that are required when you create the [iosVppApp](../resources/intune_apps_iosvppapp.md).</span></span>

|<span data-ttu-id="46fc1-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="46fc1-126">Property</span></span>|<span data-ttu-id="46fc1-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="46fc1-127">Type</span></span>|<span data-ttu-id="46fc1-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="46fc1-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="46fc1-129">id</span><span class="sxs-lookup"><span data-stu-id="46fc1-129">id</span></span>|<span data-ttu-id="46fc1-130">String</span><span class="sxs-lookup"><span data-stu-id="46fc1-130">String</span></span>|<span data-ttu-id="46fc1-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="46fc1-131">Key of the entity.</span></span> <span data-ttu-id="46fc1-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="46fc1-133">displayName</span><span class="sxs-lookup"><span data-stu-id="46fc1-133">displayName</span></span>|<span data-ttu-id="46fc1-134">String</span><span class="sxs-lookup"><span data-stu-id="46fc1-134">String</span></span>|<span data-ttu-id="46fc1-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="46fc1-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="46fc1-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="46fc1-137">description</span><span class="sxs-lookup"><span data-stu-id="46fc1-137">description</span></span>|<span data-ttu-id="46fc1-138">String</span><span class="sxs-lookup"><span data-stu-id="46fc1-138">String</span></span>|<span data-ttu-id="46fc1-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46fc1-139">The description of the app.</span></span> <span data-ttu-id="46fc1-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="46fc1-141">publicador</span><span class="sxs-lookup"><span data-stu-id="46fc1-141">publisher</span></span>|<span data-ttu-id="46fc1-142">String</span><span class="sxs-lookup"><span data-stu-id="46fc1-142">String</span></span>|<span data-ttu-id="46fc1-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46fc1-143">The publisher of the app.</span></span> <span data-ttu-id="46fc1-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="46fc1-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="46fc1-145">largeIcon</span></span>|[<span data-ttu-id="46fc1-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="46fc1-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="46fc1-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="46fc1-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="46fc1-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="46fc1-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="46fc1-149">createdDateTime</span></span>|<span data-ttu-id="46fc1-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="46fc1-150">DateTimeOffset</span></span>|<span data-ttu-id="46fc1-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46fc1-151">The date and time the app was created.</span></span> <span data-ttu-id="46fc1-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="46fc1-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="46fc1-153">lastModifiedDateTime</span></span>|<span data-ttu-id="46fc1-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="46fc1-154">DateTimeOffset</span></span>|<span data-ttu-id="46fc1-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46fc1-155">The date and time the app was last modified.</span></span> <span data-ttu-id="46fc1-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="46fc1-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="46fc1-157">isFeatured</span></span>|<span data-ttu-id="46fc1-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="46fc1-158">Boolean</span></span>|<span data-ttu-id="46fc1-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="46fc1-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="46fc1-160">privacyInformationUrl</span></span>|<span data-ttu-id="46fc1-161">String</span><span class="sxs-lookup"><span data-stu-id="46fc1-161">String</span></span>|<span data-ttu-id="46fc1-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="46fc1-162">The privacy statement Url.</span></span> <span data-ttu-id="46fc1-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="46fc1-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="46fc1-164">informationUrl</span></span>|<span data-ttu-id="46fc1-165">String</span><span class="sxs-lookup"><span data-stu-id="46fc1-165">String</span></span>|<span data-ttu-id="46fc1-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="46fc1-166">The more information Url.</span></span> <span data-ttu-id="46fc1-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="46fc1-168">owner</span><span class="sxs-lookup"><span data-stu-id="46fc1-168">owner</span></span>|<span data-ttu-id="46fc1-169">String</span><span class="sxs-lookup"><span data-stu-id="46fc1-169">String</span></span>|<span data-ttu-id="46fc1-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46fc1-170">The owner of the app.</span></span> <span data-ttu-id="46fc1-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="46fc1-172">developer</span><span class="sxs-lookup"><span data-stu-id="46fc1-172">developer</span></span>|<span data-ttu-id="46fc1-173">String</span><span class="sxs-lookup"><span data-stu-id="46fc1-173">String</span></span>|<span data-ttu-id="46fc1-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46fc1-174">The developer of the app.</span></span> <span data-ttu-id="46fc1-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="46fc1-176">notas</span><span class="sxs-lookup"><span data-stu-id="46fc1-176">notes</span></span>|<span data-ttu-id="46fc1-177">String</span><span class="sxs-lookup"><span data-stu-id="46fc1-177">String</span></span>|<span data-ttu-id="46fc1-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46fc1-178">Notes for the app.</span></span> <span data-ttu-id="46fc1-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="46fc1-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="46fc1-180">publishingState</span></span>|[<span data-ttu-id="46fc1-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="46fc1-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="46fc1-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46fc1-182">The publishing state for the app.</span></span> <span data-ttu-id="46fc1-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="46fc1-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="46fc1-184">Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="46fc1-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md).</span></span> <span data-ttu-id="46fc1-185">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="46fc1-185">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="46fc1-186">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="46fc1-186">usedLicenseCount</span></span>|<span data-ttu-id="46fc1-187">Int32</span><span class="sxs-lookup"><span data-stu-id="46fc1-187">Int32</span></span>|<span data-ttu-id="46fc1-188">Número de licencias VPP en uso.</span><span class="sxs-lookup"><span data-stu-id="46fc1-188">The number of VPP licenses in use.</span></span>|
|<span data-ttu-id="46fc1-189">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="46fc1-189">totalLicenseCount</span></span>|<span data-ttu-id="46fc1-190">Int32</span><span class="sxs-lookup"><span data-stu-id="46fc1-190">Int32</span></span>|<span data-ttu-id="46fc1-191">Número total de licencias VPP.</span><span class="sxs-lookup"><span data-stu-id="46fc1-191">The total number of VPP licenses.</span></span>|
|<span data-ttu-id="46fc1-192">releaseDateTime</span><span class="sxs-lookup"><span data-stu-id="46fc1-192">releaseDateTime</span></span>|<span data-ttu-id="46fc1-193">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="46fc1-193">DateTimeOffset</span></span>|<span data-ttu-id="46fc1-194">Fecha y hora de publicación de la aplicación de VPP.</span><span class="sxs-lookup"><span data-stu-id="46fc1-194">The VPP application release date and time.</span></span>|
|<span data-ttu-id="46fc1-195">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="46fc1-195">appStoreUrl</span></span>|<span data-ttu-id="46fc1-196">String</span><span class="sxs-lookup"><span data-stu-id="46fc1-196">String</span></span>|<span data-ttu-id="46fc1-197">Dirección URL de la tienda.</span><span class="sxs-lookup"><span data-stu-id="46fc1-197">The store URL.</span></span>|
|<span data-ttu-id="46fc1-198">licensingType</span><span class="sxs-lookup"><span data-stu-id="46fc1-198">licensingType</span></span>|[<span data-ttu-id="46fc1-199">vppLicensingType</span><span class="sxs-lookup"><span data-stu-id="46fc1-199">vppLicensingType</span></span>](../resources/intune_apps_vpplicensingtype.md)|<span data-ttu-id="46fc1-200">Tipo de licencia compatible.</span><span class="sxs-lookup"><span data-stu-id="46fc1-200">The supported License Type.</span></span>|
|<span data-ttu-id="46fc1-201">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="46fc1-201">applicableDeviceType</span></span>|[<span data-ttu-id="46fc1-202">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="46fc1-202">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="46fc1-203">Tipo de dispositivo iOS aplicable.</span><span class="sxs-lookup"><span data-stu-id="46fc1-203">The applicable iOS Device Type.</span></span>|
|<span data-ttu-id="46fc1-204">vppTokenOrganizationName</span><span class="sxs-lookup"><span data-stu-id="46fc1-204">vppTokenOrganizationName</span></span>|<span data-ttu-id="46fc1-205">String</span><span class="sxs-lookup"><span data-stu-id="46fc1-205">String</span></span>|<span data-ttu-id="46fc1-206">Organización asociada al token del Programa de Compras por Volumen de Apple</span><span class="sxs-lookup"><span data-stu-id="46fc1-206">The organization associated with the Apple Volume Purchase Program Token</span></span>|
|<span data-ttu-id="46fc1-207">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="46fc1-207">vppTokenAccountType</span></span>|[<span data-ttu-id="46fc1-208">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="46fc1-208">vppTokenAccountType</span></span>](../resources/intune_shared_vpptokenaccounttype.md)|<span data-ttu-id="46fc1-209">Tipo de programa de compras por volumen al que está asociado el token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="46fc1-209">The type of volume purchase program which the given Apple Volume Purchase Program Token is associated with.</span></span> <span data-ttu-id="46fc1-210">Los valores posibles son: `business` y `education`.</span><span class="sxs-lookup"><span data-stu-id="46fc1-210">Possible values are: `business`, `education`.</span></span> <span data-ttu-id="46fc1-211">Los valores posibles son: `business` y `education`.</span><span class="sxs-lookup"><span data-stu-id="46fc1-211">Possible values are: `business`, `education`.</span></span>|
|<span data-ttu-id="46fc1-212">vppTokenAppleId</span><span class="sxs-lookup"><span data-stu-id="46fc1-212">vppTokenAppleId</span></span>|<span data-ttu-id="46fc1-213">String</span><span class="sxs-lookup"><span data-stu-id="46fc1-213">String</span></span>|<span data-ttu-id="46fc1-214">Identificador de Apple asociado al token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="46fc1-214">The Apple Id associated with the given Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="46fc1-215">bundleId</span><span class="sxs-lookup"><span data-stu-id="46fc1-215">bundleId</span></span>|<span data-ttu-id="46fc1-216">String</span><span class="sxs-lookup"><span data-stu-id="46fc1-216">String</span></span>|<span data-ttu-id="46fc1-217">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="46fc1-217">The Identity Name.</span></span>|



## <a name="response"></a><span data-ttu-id="46fc1-218">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46fc1-218">Response</span></span>
<span data-ttu-id="46fc1-219">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosVppApp](../resources/intune_apps_iosvppapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="46fc1-219">If successful, this method returns a `200 OK` response code and an updated [iosVppApp](../resources/intune_apps_iosvppapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="46fc1-220">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="46fc1-220">Example</span></span>
### <a name="request"></a><span data-ttu-id="46fc1-221">Solicitud</span><span class="sxs-lookup"><span data-stu-id="46fc1-221">Request</span></span>
<span data-ttu-id="46fc1-222">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="46fc1-222">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1222

{
  "@odata.type": "#microsoft.graph.iosVppApp",
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
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "releaseDateTime": "2017-01-01T00:01:34.7470482-08:00",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "licensingType": {
    "@odata.type": "microsoft.graph.vppLicensingType",
    "supportsUserLicensing": true,
    "supportsDeviceLicensing": true
  },
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "vppTokenOrganizationName": "Vpp Token Organization Name value",
  "vppTokenAccountType": "education",
  "vppTokenAppleId": "Vpp Token Apple Id value",
  "bundleId": "Bundle Id value"
}
```

### <a name="response"></a><span data-ttu-id="46fc1-223">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46fc1-223">Response</span></span>
<span data-ttu-id="46fc1-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="46fc1-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1394

{
  "@odata.type": "#microsoft.graph.iosVppApp",
  "id": "a0ac9b6f-9b6f-a0ac-6f9b-aca06f9baca0",
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
  "usedLicenseCount": 0,
  "totalLicenseCount": 1,
  "releaseDateTime": "2017-01-01T00:01:34.7470482-08:00",
  "appStoreUrl": "https://example.com/appStoreUrl/",
  "licensingType": {
    "@odata.type": "microsoft.graph.vppLicensingType",
    "supportsUserLicensing": true,
    "supportsDeviceLicensing": true
  },
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "vppTokenOrganizationName": "Vpp Token Organization Name value",
  "vppTokenAccountType": "education",
  "vppTokenAppleId": "Vpp Token Apple Id value",
  "bundleId": "Bundle Id value"
}
```



