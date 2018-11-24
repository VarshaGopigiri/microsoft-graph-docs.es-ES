# <a name="update-windowsuniversalappx"></a><span data-ttu-id="d0f74-101">Actualizar windowsUniversalAppX</span><span class="sxs-lookup"><span data-stu-id="d0f74-101">Update windowsUniversalAppX</span></span>

> <span data-ttu-id="d0f74-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d0f74-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d0f74-103">Actualice las propiedades de un objeto [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-103">Update the properties of a [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d0f74-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d0f74-104">Prerequisites</span></span>
<span data-ttu-id="d0f74-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d0f74-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d0f74-107">Permission type</span></span>|<span data-ttu-id="d0f74-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d0f74-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d0f74-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d0f74-109">Delegated (work or school account)</span></span>|<span data-ttu-id="d0f74-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0f74-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="d0f74-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d0f74-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d0f74-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0f74-112">Not supported.</span></span>|
|<span data-ttu-id="d0f74-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d0f74-113">Application</span></span>|<span data-ttu-id="d0f74-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0f74-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d0f74-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d0f74-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="d0f74-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d0f74-116">Request headers</span></span>
|<span data-ttu-id="d0f74-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0f74-117">Header</span></span>|<span data-ttu-id="d0f74-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d0f74-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d0f74-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="d0f74-119">Authorization</span></span>|<span data-ttu-id="d0f74-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d0f74-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d0f74-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d0f74-121">Accept</span></span>|<span data-ttu-id="d0f74-122">application/json</span><span class="sxs-lookup"><span data-stu-id="d0f74-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d0f74-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d0f74-123">Request body</span></span>
<span data-ttu-id="d0f74-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-124">In the request body, supply a JSON representation for the [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) object.</span></span>

<span data-ttu-id="d0f74-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-125">The following table shows the properties that are required when you create the [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md).</span></span>

|<span data-ttu-id="d0f74-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d0f74-126">Property</span></span>|<span data-ttu-id="d0f74-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0f74-127">Type</span></span>|<span data-ttu-id="d0f74-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0f74-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d0f74-129">id</span><span class="sxs-lookup"><span data-stu-id="d0f74-129">id</span></span>|<span data-ttu-id="d0f74-130">String</span><span class="sxs-lookup"><span data-stu-id="d0f74-130">String</span></span>|<span data-ttu-id="d0f74-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d0f74-131">Key of the entity.</span></span> <span data-ttu-id="d0f74-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d0f74-133">displayName</span><span class="sxs-lookup"><span data-stu-id="d0f74-133">displayName</span></span>|<span data-ttu-id="d0f74-134">String</span><span class="sxs-lookup"><span data-stu-id="d0f74-134">String</span></span>|<span data-ttu-id="d0f74-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="d0f74-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="d0f74-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d0f74-137">description</span><span class="sxs-lookup"><span data-stu-id="d0f74-137">description</span></span>|<span data-ttu-id="d0f74-138">String</span><span class="sxs-lookup"><span data-stu-id="d0f74-138">String</span></span>|<span data-ttu-id="d0f74-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d0f74-139">The description of the app.</span></span> <span data-ttu-id="d0f74-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d0f74-141">publicador</span><span class="sxs-lookup"><span data-stu-id="d0f74-141">publisher</span></span>|<span data-ttu-id="d0f74-142">String</span><span class="sxs-lookup"><span data-stu-id="d0f74-142">String</span></span>|<span data-ttu-id="d0f74-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d0f74-143">The publisher of the app.</span></span> <span data-ttu-id="d0f74-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d0f74-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="d0f74-145">largeIcon</span></span>|[<span data-ttu-id="d0f74-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="d0f74-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="d0f74-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="d0f74-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="d0f74-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d0f74-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d0f74-149">createdDateTime</span></span>|<span data-ttu-id="d0f74-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d0f74-150">DateTimeOffset</span></span>|<span data-ttu-id="d0f74-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d0f74-151">The date and time the app was created.</span></span> <span data-ttu-id="d0f74-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d0f74-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d0f74-153">lastModifiedDateTime</span></span>|<span data-ttu-id="d0f74-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d0f74-154">DateTimeOffset</span></span>|<span data-ttu-id="d0f74-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d0f74-155">The date and time the app was last modified.</span></span> <span data-ttu-id="d0f74-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d0f74-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="d0f74-157">isFeatured</span></span>|<span data-ttu-id="d0f74-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="d0f74-158">Boolean</span></span>|<span data-ttu-id="d0f74-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d0f74-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="d0f74-160">privacyInformationUrl</span></span>|<span data-ttu-id="d0f74-161">String</span><span class="sxs-lookup"><span data-stu-id="d0f74-161">String</span></span>|<span data-ttu-id="d0f74-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="d0f74-162">The privacy statement Url.</span></span> <span data-ttu-id="d0f74-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d0f74-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="d0f74-164">informationUrl</span></span>|<span data-ttu-id="d0f74-165">String</span><span class="sxs-lookup"><span data-stu-id="d0f74-165">String</span></span>|<span data-ttu-id="d0f74-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="d0f74-166">The more information Url.</span></span> <span data-ttu-id="d0f74-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d0f74-168">owner</span><span class="sxs-lookup"><span data-stu-id="d0f74-168">owner</span></span>|<span data-ttu-id="d0f74-169">String</span><span class="sxs-lookup"><span data-stu-id="d0f74-169">String</span></span>|<span data-ttu-id="d0f74-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d0f74-170">The owner of the app.</span></span> <span data-ttu-id="d0f74-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d0f74-172">developer</span><span class="sxs-lookup"><span data-stu-id="d0f74-172">developer</span></span>|<span data-ttu-id="d0f74-173">String</span><span class="sxs-lookup"><span data-stu-id="d0f74-173">String</span></span>|<span data-ttu-id="d0f74-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d0f74-174">The developer of the app.</span></span> <span data-ttu-id="d0f74-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d0f74-176">notas</span><span class="sxs-lookup"><span data-stu-id="d0f74-176">notes</span></span>|<span data-ttu-id="d0f74-177">String</span><span class="sxs-lookup"><span data-stu-id="d0f74-177">String</span></span>|<span data-ttu-id="d0f74-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d0f74-178">Notes for the app.</span></span> <span data-ttu-id="d0f74-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d0f74-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="d0f74-180">publishingState</span></span>|[<span data-ttu-id="d0f74-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="d0f74-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="d0f74-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d0f74-182">The publishing state for the app.</span></span> <span data-ttu-id="d0f74-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="d0f74-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="d0f74-184">Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md).</span></span> <span data-ttu-id="d0f74-185">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="d0f74-185">Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="d0f74-186">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="d0f74-186">committedContentVersion</span></span>|<span data-ttu-id="d0f74-187">String</span><span class="sxs-lookup"><span data-stu-id="d0f74-187">String</span></span>|<span data-ttu-id="d0f74-188">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="d0f74-188">The internal committed content version.</span></span> <span data-ttu-id="d0f74-189">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-189">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="d0f74-190">fileName</span><span class="sxs-lookup"><span data-stu-id="d0f74-190">fileName</span></span>|<span data-ttu-id="d0f74-191">String</span><span class="sxs-lookup"><span data-stu-id="d0f74-191">String</span></span>|<span data-ttu-id="d0f74-192">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="d0f74-192">The name of the main Lob application file.</span></span> <span data-ttu-id="d0f74-193">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-193">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="d0f74-194">size</span><span class="sxs-lookup"><span data-stu-id="d0f74-194">size</span></span>|<span data-ttu-id="d0f74-195">Int64</span><span class="sxs-lookup"><span data-stu-id="d0f74-195">Int64</span></span>|<span data-ttu-id="d0f74-196">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="d0f74-196">The total size, including all uploaded files.</span></span> <span data-ttu-id="d0f74-197">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="d0f74-197">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="d0f74-198">applicableArchitectures</span><span class="sxs-lookup"><span data-stu-id="d0f74-198">applicableArchitectures</span></span>|[<span data-ttu-id="d0f74-199">windowsArchitecture</span><span class="sxs-lookup"><span data-stu-id="d0f74-199">windowsArchitecture</span></span>](../resources/intune_apps_windowsarchitecture.md)|<span data-ttu-id="d0f74-200">Arquitecturas de Windows en las que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="d0f74-200">The Windows architecture(s) for which this app can run on.</span></span> <span data-ttu-id="d0f74-201">Los valores posibles son: `none`, `x86`, `x64`, `arm` y `neutral`.</span><span class="sxs-lookup"><span data-stu-id="d0f74-201">Possible values are: `none`, `x86`, `x64`, `arm`, `neutral`.</span></span>|
|<span data-ttu-id="d0f74-202">applicableDeviceTypes</span><span class="sxs-lookup"><span data-stu-id="d0f74-202">applicableDeviceTypes</span></span>|[<span data-ttu-id="d0f74-203">windowsDeviceType</span><span class="sxs-lookup"><span data-stu-id="d0f74-203">windowsDeviceType</span></span>](../resources/intune_apps_windowsdevicetype.md)|<span data-ttu-id="d0f74-204">Tipos de dispositivos Windows en los que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="d0f74-204">The Windows device type(s) for which this app can run on.</span></span> <span data-ttu-id="d0f74-205">Los valores posibles son: `none`, `desktop`, `mobile`, `holographic` y `team`.</span><span class="sxs-lookup"><span data-stu-id="d0f74-205">Possible values are: `none`, `desktop`, `mobile`, `holographic`, `team`.</span></span>|
|<span data-ttu-id="d0f74-206">identityName</span><span class="sxs-lookup"><span data-stu-id="d0f74-206">identityName</span></span>|<span data-ttu-id="d0f74-207">String</span><span class="sxs-lookup"><span data-stu-id="d0f74-207">String</span></span>|<span data-ttu-id="d0f74-208">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="d0f74-208">The Identity Name.</span></span>|
|<span data-ttu-id="d0f74-209">identityPublisherHash</span><span class="sxs-lookup"><span data-stu-id="d0f74-209">identityPublisherHash</span></span>|<span data-ttu-id="d0f74-210">String</span><span class="sxs-lookup"><span data-stu-id="d0f74-210">String</span></span>|<span data-ttu-id="d0f74-211">Hash del publicador de identidad.</span><span class="sxs-lookup"><span data-stu-id="d0f74-211">The Identity Publisher Hash.</span></span>|
|<span data-ttu-id="d0f74-212">identityResourceIdentifier</span><span class="sxs-lookup"><span data-stu-id="d0f74-212">identityResourceIdentifier</span></span>|<span data-ttu-id="d0f74-213">String</span><span class="sxs-lookup"><span data-stu-id="d0f74-213">String</span></span>|<span data-ttu-id="d0f74-214">Identificador del recurso de identidad.</span><span class="sxs-lookup"><span data-stu-id="d0f74-214">The Identity Resource Identifier.</span></span>|
|<span data-ttu-id="d0f74-215">isBundle</span><span class="sxs-lookup"><span data-stu-id="d0f74-215">isBundle</span></span>|<span data-ttu-id="d0f74-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="d0f74-216">Boolean</span></span>|<span data-ttu-id="d0f74-217">Indica si la aplicación es una agrupación.</span><span class="sxs-lookup"><span data-stu-id="d0f74-217">Whether or not the app is a bundle.</span></span>|
|<span data-ttu-id="d0f74-218">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="d0f74-218">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="d0f74-219">windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="d0f74-219">windowsMinimumOperatingSystem</span></span>](../resources/intune_apps_windowsminimumoperatingsystem.md)|<span data-ttu-id="d0f74-220">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="d0f74-220">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="d0f74-221">identityVersion</span><span class="sxs-lookup"><span data-stu-id="d0f74-221">identityVersion</span></span>|<span data-ttu-id="d0f74-222">String</span><span class="sxs-lookup"><span data-stu-id="d0f74-222">String</span></span>|<span data-ttu-id="d0f74-223">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="d0f74-223">The identity version.</span></span>|



## <a name="response"></a><span data-ttu-id="d0f74-224">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0f74-224">Response</span></span>
<span data-ttu-id="d0f74-225">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0f74-225">If successful, this method returns a `200 OK` response code and an updated [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d0f74-226">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0f74-226">Example</span></span>
### <a name="request"></a><span data-ttu-id="d0f74-227">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d0f74-227">Request</span></span>
<span data-ttu-id="d0f74-228">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d0f74-228">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1189

{
  "@odata.type": "#microsoft.graph.windowsUniversalAppX",
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
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "applicableArchitectures": "x86",
  "applicableDeviceTypes": "desktop",
  "identityName": "Identity Name value",
  "identityPublisherHash": "Identity Publisher Hash value",
  "identityResourceIdentifier": "Identity Resource Identifier value",
  "isBundle": true,
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true
  },
  "identityVersion": "Identity Version value"
}
```

### <a name="response"></a><span data-ttu-id="d0f74-229">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0f74-229">Response</span></span>
<span data-ttu-id="d0f74-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d0f74-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1361

{
  "@odata.type": "#microsoft.graph.windowsUniversalAppX",
  "id": "4bc47eba-7eba-4bc4-ba7e-c44bba7ec44b",
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
  "applicableArchitectures": "x86",
  "applicableDeviceTypes": "desktop",
  "identityName": "Identity Name value",
  "identityPublisherHash": "Identity Publisher Hash value",
  "identityResourceIdentifier": "Identity Resource Identifier value",
  "isBundle": true,
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true
  },
  "identityVersion": "Identity Version value"
}
```



