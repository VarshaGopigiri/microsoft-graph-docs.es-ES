# <a name="update-iosvppapp"></a><span data-ttu-id="5d50d-101">Actualizar iosVppApp</span><span class="sxs-lookup"><span data-stu-id="5d50d-101">Update iosVppApp</span></span>

> <span data-ttu-id="5d50d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5d50d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5d50d-103">Actualice las propiedades de un objeto [iosVppApp](../resources/intune_apps_iosvppapp.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-103">Update the properties of a [iosVppApp](../resources/intune_apps_iosvppapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5d50d-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5d50d-104">Prerequisites</span></span>
<span data-ttu-id="5d50d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5d50d-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5d50d-107">Permission type</span></span>|<span data-ttu-id="5d50d-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5d50d-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5d50d-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5d50d-109">Delegated (work or school account)</span></span>|<span data-ttu-id="5d50d-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5d50d-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="5d50d-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5d50d-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5d50d-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d50d-112">Not supported.</span></span>|
|<span data-ttu-id="5d50d-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5d50d-113">Application</span></span>|<span data-ttu-id="5d50d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d50d-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5d50d-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5d50d-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="5d50d-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5d50d-116">Request headers</span></span>
|<span data-ttu-id="5d50d-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d50d-117">Header</span></span>|<span data-ttu-id="5d50d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5d50d-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5d50d-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="5d50d-119">Authorization</span></span>|<span data-ttu-id="5d50d-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5d50d-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5d50d-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5d50d-121">Accept</span></span>|<span data-ttu-id="5d50d-122">application/json</span><span class="sxs-lookup"><span data-stu-id="5d50d-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5d50d-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5d50d-123">Request body</span></span>
<span data-ttu-id="5d50d-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosVppApp](../resources/intune_apps_iosvppapp.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-124">In the request body, supply a JSON representation for the [iosVppApp](../resources/intune_apps_iosvppapp.md) object.</span></span>

<span data-ttu-id="5d50d-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosVppApp](../resources/intune_apps_iosvppapp.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-125">The following table shows the properties that are required when you create the [iosVppApp](../resources/intune_apps_iosvppapp.md).</span></span>

|<span data-ttu-id="5d50d-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5d50d-126">Property</span></span>|<span data-ttu-id="5d50d-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="5d50d-127">Type</span></span>|<span data-ttu-id="5d50d-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d50d-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5d50d-129">id.</span><span class="sxs-lookup"><span data-stu-id="5d50d-129">id</span></span>|<span data-ttu-id="5d50d-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="5d50d-130">String</span></span>|<span data-ttu-id="5d50d-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5d50d-131">Key of the entity.</span></span> <span data-ttu-id="5d50d-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5d50d-133">displayName</span><span class="sxs-lookup"><span data-stu-id="5d50d-133">displayName</span></span>|<span data-ttu-id="5d50d-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="5d50d-134">String</span></span>|<span data-ttu-id="5d50d-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="5d50d-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="5d50d-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5d50d-137">descripción</span><span class="sxs-lookup"><span data-stu-id="5d50d-137">description</span></span>|<span data-ttu-id="5d50d-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="5d50d-138">String</span></span>|<span data-ttu-id="5d50d-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d50d-139">The description of the app.</span></span> <span data-ttu-id="5d50d-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5d50d-141">publicador</span><span class="sxs-lookup"><span data-stu-id="5d50d-141">publisher</span></span>|<span data-ttu-id="5d50d-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="5d50d-142">String</span></span>|<span data-ttu-id="5d50d-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d50d-143">The publisher of the app.</span></span> <span data-ttu-id="5d50d-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5d50d-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="5d50d-145">largeIcon</span></span>|[<span data-ttu-id="5d50d-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="5d50d-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="5d50d-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="5d50d-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="5d50d-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5d50d-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5d50d-149">createdDateTime</span></span>|<span data-ttu-id="5d50d-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5d50d-150">DateTimeOffset</span></span>|<span data-ttu-id="5d50d-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d50d-151">The date and time the app was created.</span></span> <span data-ttu-id="5d50d-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5d50d-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="5d50d-153">lastModifiedDateTime</span></span>|<span data-ttu-id="5d50d-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5d50d-154">DateTimeOffset</span></span>|<span data-ttu-id="5d50d-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d50d-155">The date and time the app was last modified.</span></span> <span data-ttu-id="5d50d-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5d50d-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="5d50d-157">isFeatured</span></span>|<span data-ttu-id="5d50d-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="5d50d-158">Boolean</span></span>|<span data-ttu-id="5d50d-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5d50d-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="5d50d-160">privacyInformationUrl</span></span>|<span data-ttu-id="5d50d-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="5d50d-161">String</span></span>|<span data-ttu-id="5d50d-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="5d50d-162">The privacy statement Url.</span></span> <span data-ttu-id="5d50d-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5d50d-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="5d50d-164">informationUrl</span></span>|<span data-ttu-id="5d50d-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="5d50d-165">String</span></span>|<span data-ttu-id="5d50d-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="5d50d-166">The more information Url.</span></span> <span data-ttu-id="5d50d-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5d50d-168">propietario/a</span><span class="sxs-lookup"><span data-stu-id="5d50d-168">owner</span></span>|<span data-ttu-id="5d50d-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="5d50d-169">String</span></span>|<span data-ttu-id="5d50d-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d50d-170">The owner of the app.</span></span> <span data-ttu-id="5d50d-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5d50d-172">programador</span><span class="sxs-lookup"><span data-stu-id="5d50d-172">developer</span></span>|<span data-ttu-id="5d50d-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="5d50d-173">String</span></span>|<span data-ttu-id="5d50d-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d50d-174">The developer of the app.</span></span> <span data-ttu-id="5d50d-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5d50d-176">notas</span><span class="sxs-lookup"><span data-stu-id="5d50d-176">notes</span></span>|<span data-ttu-id="5d50d-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="5d50d-177">String</span></span>|<span data-ttu-id="5d50d-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d50d-178">Notes for the app.</span></span> <span data-ttu-id="5d50d-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5d50d-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5d50d-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="5d50d-180">publishingState</span></span>|[<span data-ttu-id="5d50d-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="5d50d-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="5d50d-p114">El estado de publicación para la aplicación. La aplicación no se puede asignar a menos que se publique la aplicación. Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing`, `published`.</span><span class="sxs-lookup"><span data-stu-id="5d50d-p114">The publishing state for the app. The app cannot be assigned unless the app is published. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md). The possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="5d50d-186">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="5d50d-186">usedLicenseCount</span></span>|<span data-ttu-id="5d50d-187">Int32</span><span class="sxs-lookup"><span data-stu-id="5d50d-187">Int32</span></span>|<span data-ttu-id="5d50d-188">Número de licencias VPP en uso.</span><span class="sxs-lookup"><span data-stu-id="5d50d-188">The number of VPP licenses in use.</span></span>|
|<span data-ttu-id="5d50d-189">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="5d50d-189">totalLicenseCount</span></span>|<span data-ttu-id="5d50d-190">Int32</span><span class="sxs-lookup"><span data-stu-id="5d50d-190">Int32</span></span>|<span data-ttu-id="5d50d-191">Número total de licencias VPP.</span><span class="sxs-lookup"><span data-stu-id="5d50d-191">The total number of VPP licenses.</span></span>|
|<span data-ttu-id="5d50d-192">releaseDateTime</span><span class="sxs-lookup"><span data-stu-id="5d50d-192">releaseDateTime</span></span>|<span data-ttu-id="5d50d-193">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5d50d-193">DateTimeOffset</span></span>|<span data-ttu-id="5d50d-194">Fecha y hora de publicación de la aplicación de VPP.</span><span class="sxs-lookup"><span data-stu-id="5d50d-194">The VPP application release date and time.</span></span>|
|<span data-ttu-id="5d50d-195">appStoreUrl</span><span class="sxs-lookup"><span data-stu-id="5d50d-195">appStoreUrl</span></span>|<span data-ttu-id="5d50d-196">Cadena</span><span class="sxs-lookup"><span data-stu-id="5d50d-196">String</span></span>|<span data-ttu-id="5d50d-197">Dirección URL de la tienda.</span><span class="sxs-lookup"><span data-stu-id="5d50d-197">The store URL.</span></span>|
|<span data-ttu-id="5d50d-198">licensingType</span><span class="sxs-lookup"><span data-stu-id="5d50d-198">licensingType</span></span>|[<span data-ttu-id="5d50d-199">vppLicensingType</span><span class="sxs-lookup"><span data-stu-id="5d50d-199">vppLicensingType</span></span>](../resources/intune_apps_vpplicensingtype.md)|<span data-ttu-id="5d50d-200">Tipo de licencia compatible.</span><span class="sxs-lookup"><span data-stu-id="5d50d-200">The supported License Type.</span></span>|
|<span data-ttu-id="5d50d-201">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="5d50d-201">applicableDeviceType</span></span>|[<span data-ttu-id="5d50d-202">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="5d50d-202">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="5d50d-203">Tipo de dispositivo iOS aplicable.</span><span class="sxs-lookup"><span data-stu-id="5d50d-203">The applicable iOS Device Type.</span></span>|
|<span data-ttu-id="5d50d-204">vppTokenOrganizationName</span><span class="sxs-lookup"><span data-stu-id="5d50d-204">vppTokenOrganizationName</span></span>|<span data-ttu-id="5d50d-205">Cadena</span><span class="sxs-lookup"><span data-stu-id="5d50d-205">String</span></span>|<span data-ttu-id="5d50d-206">Organización asociada al token del Programa de Compras por Volumen de Apple</span><span class="sxs-lookup"><span data-stu-id="5d50d-206">The organization associated with the Apple Volume Purchase Program Token</span></span>|
|<span data-ttu-id="5d50d-207">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="5d50d-207">vppTokenAccountType</span></span>|[<span data-ttu-id="5d50d-208">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="5d50d-208">vppTokenAccountType</span></span>](../resources/intune_shared_vpptokenaccounttype.md)|<span data-ttu-id="5d50d-p115">El tipo de programa de compra de volumen al que está asociado el Token de programa de compra de volumen de Apple determinado. Los valores posibles son: `business`, `education`. Los valores posibles son: `business`, `education`.</span><span class="sxs-lookup"><span data-stu-id="5d50d-p115">The type of volume purchase program which the given Apple Volume Purchase Program Token is associated with. The possible values are: `business`, `education`. The possible values are: `business`, `education`.</span></span>|
|<span data-ttu-id="5d50d-212">vppTokenAppleId</span><span class="sxs-lookup"><span data-stu-id="5d50d-212">vppTokenAppleId</span></span>|<span data-ttu-id="5d50d-213">Cadena</span><span class="sxs-lookup"><span data-stu-id="5d50d-213">String</span></span>|<span data-ttu-id="5d50d-214">Identificador de Apple asociado al token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="5d50d-214">The Apple Id associated with the given Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="5d50d-215">bundleId</span><span class="sxs-lookup"><span data-stu-id="5d50d-215">bundleId</span></span>|<span data-ttu-id="5d50d-216">Cadena</span><span class="sxs-lookup"><span data-stu-id="5d50d-216">String</span></span>|<span data-ttu-id="5d50d-217">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="5d50d-217">The Identity Name.</span></span>|



## <a name="response"></a><span data-ttu-id="5d50d-218">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d50d-218">Response</span></span>
<span data-ttu-id="5d50d-219">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosVppApp](../resources/intune_apps_iosvppapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5d50d-219">If successful, this method returns a `200 OK` response code and an updated [iosVppApp](../resources/intune_apps_iosvppapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5d50d-220">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5d50d-220">Example</span></span>
### <a name="request"></a><span data-ttu-id="5d50d-221">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5d50d-221">Request</span></span>
<span data-ttu-id="5d50d-222">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5d50d-222">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1238

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

### <a name="response"></a><span data-ttu-id="5d50d-223">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d50d-223">Response</span></span>
<span data-ttu-id="5d50d-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5d50d-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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








