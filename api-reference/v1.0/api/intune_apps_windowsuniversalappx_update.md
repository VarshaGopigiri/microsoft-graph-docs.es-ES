# <a name="update-windowsuniversalappx"></a><span data-ttu-id="88f17-101">Actualizar windowsUniversalAppX</span><span class="sxs-lookup"><span data-stu-id="88f17-101">Update windowsUniversalAppX</span></span>

> <span data-ttu-id="88f17-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="88f17-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="88f17-103">Actualice las propiedades de un objeto [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-103">Update the properties of a [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="88f17-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="88f17-104">Prerequisites</span></span>
<span data-ttu-id="88f17-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="88f17-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="88f17-107">Permission type</span></span>|<span data-ttu-id="88f17-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="88f17-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="88f17-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="88f17-109">Delegated (work or school account)</span></span>|<span data-ttu-id="88f17-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="88f17-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="88f17-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="88f17-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="88f17-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88f17-112">Not supported.</span></span>|
|<span data-ttu-id="88f17-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="88f17-113">Application</span></span>|<span data-ttu-id="88f17-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88f17-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="88f17-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="88f17-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="88f17-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="88f17-116">Request headers</span></span>
|<span data-ttu-id="88f17-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88f17-117">Header</span></span>|<span data-ttu-id="88f17-118">Valor</span><span class="sxs-lookup"><span data-stu-id="88f17-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="88f17-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="88f17-119">Authorization</span></span>|<span data-ttu-id="88f17-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="88f17-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="88f17-121">Accept</span><span class="sxs-lookup"><span data-stu-id="88f17-121">Accept</span></span>|<span data-ttu-id="88f17-122">application/json</span><span class="sxs-lookup"><span data-stu-id="88f17-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="88f17-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="88f17-123">Request body</span></span>
<span data-ttu-id="88f17-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-124">In the request body, supply a JSON representation for the [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) object.</span></span>

<span data-ttu-id="88f17-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-125">The following table shows the properties that are required when you create the [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md).</span></span>

|<span data-ttu-id="88f17-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="88f17-126">Property</span></span>|<span data-ttu-id="88f17-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="88f17-127">Type</span></span>|<span data-ttu-id="88f17-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="88f17-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="88f17-129">id</span><span class="sxs-lookup"><span data-stu-id="88f17-129">id</span></span>|<span data-ttu-id="88f17-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="88f17-130">String</span></span>|<span data-ttu-id="88f17-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="88f17-131">Key of the entity.</span></span> <span data-ttu-id="88f17-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="88f17-133">displayName</span><span class="sxs-lookup"><span data-stu-id="88f17-133">displayName</span></span>|<span data-ttu-id="88f17-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="88f17-134">String</span></span>|<span data-ttu-id="88f17-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="88f17-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="88f17-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="88f17-137">descripción</span><span class="sxs-lookup"><span data-stu-id="88f17-137">description</span></span>|<span data-ttu-id="88f17-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="88f17-138">String</span></span>|<span data-ttu-id="88f17-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88f17-139">The description of the app.</span></span> <span data-ttu-id="88f17-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="88f17-141">publicador</span><span class="sxs-lookup"><span data-stu-id="88f17-141">publisher</span></span>|<span data-ttu-id="88f17-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="88f17-142">String</span></span>|<span data-ttu-id="88f17-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88f17-143">The publisher of the app.</span></span> <span data-ttu-id="88f17-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="88f17-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="88f17-145">largeIcon</span></span>|[<span data-ttu-id="88f17-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="88f17-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="88f17-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="88f17-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="88f17-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="88f17-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="88f17-149">createdDateTime</span></span>|<span data-ttu-id="88f17-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="88f17-150">DateTimeOffset</span></span>|<span data-ttu-id="88f17-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88f17-151">The date and time the app was created.</span></span> <span data-ttu-id="88f17-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="88f17-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="88f17-153">lastModifiedDateTime</span></span>|<span data-ttu-id="88f17-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="88f17-154">DateTimeOffset</span></span>|<span data-ttu-id="88f17-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88f17-155">The date and time the app was last modified.</span></span> <span data-ttu-id="88f17-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="88f17-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="88f17-157">isFeatured</span></span>|<span data-ttu-id="88f17-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="88f17-158">Boolean</span></span>|<span data-ttu-id="88f17-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="88f17-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="88f17-160">privacyInformationUrl</span></span>|<span data-ttu-id="88f17-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="88f17-161">String</span></span>|<span data-ttu-id="88f17-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="88f17-162">The privacy statement Url.</span></span> <span data-ttu-id="88f17-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="88f17-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="88f17-164">informationUrl</span></span>|<span data-ttu-id="88f17-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="88f17-165">String</span></span>|<span data-ttu-id="88f17-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="88f17-166">The more information Url.</span></span> <span data-ttu-id="88f17-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="88f17-168">owner</span><span class="sxs-lookup"><span data-stu-id="88f17-168">owner</span></span>|<span data-ttu-id="88f17-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="88f17-169">String</span></span>|<span data-ttu-id="88f17-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88f17-170">The owner of the app.</span></span> <span data-ttu-id="88f17-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="88f17-172">developer</span><span class="sxs-lookup"><span data-stu-id="88f17-172">developer</span></span>|<span data-ttu-id="88f17-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="88f17-173">String</span></span>|<span data-ttu-id="88f17-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88f17-174">The developer of the app.</span></span> <span data-ttu-id="88f17-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="88f17-176">notas</span><span class="sxs-lookup"><span data-stu-id="88f17-176">notes</span></span>|<span data-ttu-id="88f17-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="88f17-177">String</span></span>|<span data-ttu-id="88f17-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88f17-178">Notes for the app.</span></span> <span data-ttu-id="88f17-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="88f17-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="88f17-180">publishingState</span></span>|[<span data-ttu-id="88f17-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="88f17-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="88f17-p114">El estado de publicación para la aplicación. La aplicación no se puede asignar a menos que se publique la aplicación. Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing`, `published`.</span><span class="sxs-lookup"><span data-stu-id="88f17-p114">The publishing state for the app. The app cannot be assigned unless the app is published. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md). The possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="88f17-186">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="88f17-186">committedContentVersion</span></span>|<span data-ttu-id="88f17-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="88f17-187">String</span></span>|<span data-ttu-id="88f17-188">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="88f17-188">The internal committed content version.</span></span> <span data-ttu-id="88f17-189">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-189">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="88f17-190">fileName</span><span class="sxs-lookup"><span data-stu-id="88f17-190">fileName</span></span>|<span data-ttu-id="88f17-191">Cadena</span><span class="sxs-lookup"><span data-stu-id="88f17-191">String</span></span>|<span data-ttu-id="88f17-192">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="88f17-192">The name of the main Lob application file.</span></span> <span data-ttu-id="88f17-193">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-193">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="88f17-194">size</span><span class="sxs-lookup"><span data-stu-id="88f17-194">size</span></span>|<span data-ttu-id="88f17-195">Int64</span><span class="sxs-lookup"><span data-stu-id="88f17-195">Int64</span></span>|<span data-ttu-id="88f17-196">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="88f17-196">The total size, including all uploaded files.</span></span> <span data-ttu-id="88f17-197">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="88f17-197">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="88f17-198">applicableArchitectures</span><span class="sxs-lookup"><span data-stu-id="88f17-198">applicableArchitectures</span></span>|[<span data-ttu-id="88f17-199">windowsArchitecture</span><span class="sxs-lookup"><span data-stu-id="88f17-199">windowsArchitecture</span></span>](../resources/intune_apps_windowsarchitecture.md)|<span data-ttu-id="88f17-p118">La(s) arquitectura(s) de Windows en que se puede ejecutar esta aplicación. Los valores posibles son: `none`, `x86`, `x64`, `arm`, `neutral`.</span><span class="sxs-lookup"><span data-stu-id="88f17-p118">The Windows architecture(s) for which this app can run on. The possible values are: `none`, `x86`, `x64`, `arm`, `neutral`.</span></span>|
|<span data-ttu-id="88f17-202">applicableDeviceTypes</span><span class="sxs-lookup"><span data-stu-id="88f17-202">applicableDeviceTypes</span></span>|[<span data-ttu-id="88f17-203">windowsDeviceType</span><span class="sxs-lookup"><span data-stu-id="88f17-203">windowsDeviceType</span></span>](../resources/intune_apps_windowsdevicetype.md)|<span data-ttu-id="88f17-p119">El/los tipo(s) de dispositivos de Windows en que se puede ejecutar esta aplicación. Los valores posibles son: `none`, `desktop`, `mobile`, `holographic`, `team`.</span><span class="sxs-lookup"><span data-stu-id="88f17-p119">The Windows device type(s) for which this app can run on. The possible values are: `none`, `desktop`, `mobile`, `holographic`, `team`.</span></span>|
|<span data-ttu-id="88f17-206">identityName</span><span class="sxs-lookup"><span data-stu-id="88f17-206">identityName</span></span>|<span data-ttu-id="88f17-207">Cadena</span><span class="sxs-lookup"><span data-stu-id="88f17-207">String</span></span>|<span data-ttu-id="88f17-208">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="88f17-208">The Identity Name.</span></span>|
|<span data-ttu-id="88f17-209">identityPublisherHash</span><span class="sxs-lookup"><span data-stu-id="88f17-209">identityPublisherHash</span></span>|<span data-ttu-id="88f17-210">Cadena</span><span class="sxs-lookup"><span data-stu-id="88f17-210">String</span></span>|<span data-ttu-id="88f17-211">Hash del publicador de identidad.</span><span class="sxs-lookup"><span data-stu-id="88f17-211">The Identity Publisher Hash.</span></span>|
|<span data-ttu-id="88f17-212">identityResourceIdentifier</span><span class="sxs-lookup"><span data-stu-id="88f17-212">identityResourceIdentifier</span></span>|<span data-ttu-id="88f17-213">Cadena</span><span class="sxs-lookup"><span data-stu-id="88f17-213">String</span></span>|<span data-ttu-id="88f17-214">Identificador del recurso de identidad.</span><span class="sxs-lookup"><span data-stu-id="88f17-214">The Identity Resource Identifier.</span></span>|
|<span data-ttu-id="88f17-215">isBundle</span><span class="sxs-lookup"><span data-stu-id="88f17-215">isBundle</span></span>|<span data-ttu-id="88f17-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="88f17-216">Boolean</span></span>|<span data-ttu-id="88f17-217">Indica si la aplicación es una agrupación.</span><span class="sxs-lookup"><span data-stu-id="88f17-217">Whether or not the app is a bundle.</span></span>|
|<span data-ttu-id="88f17-218">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="88f17-218">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="88f17-219">windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="88f17-219">windowsMinimumOperatingSystem</span></span>](../resources/intune_apps_windowsminimumoperatingsystem.md)|<span data-ttu-id="88f17-220">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="88f17-220">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="88f17-221">identityVersion</span><span class="sxs-lookup"><span data-stu-id="88f17-221">identityVersion</span></span>|<span data-ttu-id="88f17-222">Cadena</span><span class="sxs-lookup"><span data-stu-id="88f17-222">String</span></span>|<span data-ttu-id="88f17-223">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="88f17-223">The identity version.</span></span>|



## <a name="response"></a><span data-ttu-id="88f17-224">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88f17-224">Response</span></span>
<span data-ttu-id="88f17-225">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88f17-225">If successful, this method returns a `200 OK` response code and an updated [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="88f17-226">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88f17-226">Example</span></span>
### <a name="request"></a><span data-ttu-id="88f17-227">Solicitud</span><span class="sxs-lookup"><span data-stu-id="88f17-227">Request</span></span>
<span data-ttu-id="88f17-228">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="88f17-228">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1194

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

### <a name="response"></a><span data-ttu-id="88f17-229">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88f17-229">Response</span></span>
<span data-ttu-id="88f17-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="88f17-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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








