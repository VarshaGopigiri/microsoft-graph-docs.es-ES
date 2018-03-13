# <a name="create-windowsuniversalappx"></a><span data-ttu-id="31d71-101">Crear windowsUniversalAppX</span><span class="sxs-lookup"><span data-stu-id="31d71-101">Create windowsUniversalAppX</span></span>

> <span data-ttu-id="31d71-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="31d71-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="31d71-103">Crear un objeto [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-103">Create a new [plannerBucket](../resources/intune_apps_windowsuniversalappx.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="31d71-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="31d71-104">Prerequisites</span></span>
<span data-ttu-id="31d71-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="31d71-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="31d71-107">Permission type</span></span>|<span data-ttu-id="31d71-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="31d71-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="31d71-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="31d71-109">Delegated (work or school account)</span></span>|<span data-ttu-id="31d71-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="31d71-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="31d71-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="31d71-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="31d71-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="31d71-112">Not supported.</span></span>|
|<span data-ttu-id="31d71-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="31d71-113">Application</span></span>|<span data-ttu-id="31d71-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="31d71-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="31d71-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="31d71-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="31d71-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="31d71-116">Request headers</span></span>
|<span data-ttu-id="31d71-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31d71-117">Header</span></span>|<span data-ttu-id="31d71-118">Valor</span><span class="sxs-lookup"><span data-stu-id="31d71-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="31d71-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="31d71-119">Authorization</span></span>|<span data-ttu-id="31d71-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="31d71-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="31d71-121">Accept</span><span class="sxs-lookup"><span data-stu-id="31d71-121">Accept</span></span>|<span data-ttu-id="31d71-122">application/json</span><span class="sxs-lookup"><span data-stu-id="31d71-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="31d71-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="31d71-123">Request body</span></span>
<span data-ttu-id="31d71-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsUniversalAppX.</span><span class="sxs-lookup"><span data-stu-id="31d71-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="31d71-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsUniversalAppX.</span><span class="sxs-lookup"><span data-stu-id="31d71-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="31d71-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="31d71-126">Property</span></span>|<span data-ttu-id="31d71-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="31d71-127">Type</span></span>|<span data-ttu-id="31d71-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="31d71-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="31d71-129">id</span><span class="sxs-lookup"><span data-stu-id="31d71-129">id</span></span>|<span data-ttu-id="31d71-130">String</span><span class="sxs-lookup"><span data-stu-id="31d71-130">String</span></span>|<span data-ttu-id="31d71-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="31d71-131">Key of the setting.</span></span> <span data-ttu-id="31d71-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="31d71-133">displayName</span><span class="sxs-lookup"><span data-stu-id="31d71-133">displayName</span></span>|<span data-ttu-id="31d71-134">String</span><span class="sxs-lookup"><span data-stu-id="31d71-134">String</span></span>|<span data-ttu-id="31d71-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="31d71-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="31d71-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="31d71-137">description</span><span class="sxs-lookup"><span data-stu-id="31d71-137">description</span></span>|<span data-ttu-id="31d71-138">String</span><span class="sxs-lookup"><span data-stu-id="31d71-138">String</span></span>|<span data-ttu-id="31d71-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31d71-139">The description of the app.</span></span> <span data-ttu-id="31d71-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="31d71-141">publisher</span><span class="sxs-lookup"><span data-stu-id="31d71-141">Publisher</span></span>|<span data-ttu-id="31d71-142">String</span><span class="sxs-lookup"><span data-stu-id="31d71-142">String</span></span>|<span data-ttu-id="31d71-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31d71-143">The name of the app.</span></span> <span data-ttu-id="31d71-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="31d71-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="31d71-145">largeIcon</span></span>|[<span data-ttu-id="31d71-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="31d71-146">mimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="31d71-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="31d71-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="31d71-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="31d71-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="31d71-149">createdDateTime</span></span>|<span data-ttu-id="31d71-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="31d71-150">DateTimeOffset</span></span>|<span data-ttu-id="31d71-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31d71-151">The date and time when the page was created.</span></span> <span data-ttu-id="31d71-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="31d71-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="31d71-153">lastModifiedDateTime</span></span>|<span data-ttu-id="31d71-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="31d71-154">DateTimeOffset</span></span>|<span data-ttu-id="31d71-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31d71-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="31d71-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="31d71-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="31d71-157">isFeatured</span></span>|<span data-ttu-id="31d71-158">Boolean</span><span class="sxs-lookup"><span data-stu-id="31d71-158">Boolean</span></span>|<span data-ttu-id="31d71-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="31d71-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="31d71-160">privacyInformationUrl</span></span>|<span data-ttu-id="31d71-161">String</span><span class="sxs-lookup"><span data-stu-id="31d71-161">String</span></span>|<span data-ttu-id="31d71-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="31d71-162">The privacy statement Url.</span></span> <span data-ttu-id="31d71-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="31d71-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="31d71-164">informationUrl</span></span>|<span data-ttu-id="31d71-165">String</span><span class="sxs-lookup"><span data-stu-id="31d71-165">String</span></span>|<span data-ttu-id="31d71-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="31d71-166">The more information Url.</span></span> <span data-ttu-id="31d71-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="31d71-168">owner</span><span class="sxs-lookup"><span data-stu-id="31d71-168">owner</span></span>|<span data-ttu-id="31d71-169">String</span><span class="sxs-lookup"><span data-stu-id="31d71-169">String</span></span>|<span data-ttu-id="31d71-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31d71-170">The owner of the timesheet.</span></span> <span data-ttu-id="31d71-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="31d71-172">developer</span><span class="sxs-lookup"><span data-stu-id="31d71-172">developer</span></span>|<span data-ttu-id="31d71-173">String</span><span class="sxs-lookup"><span data-stu-id="31d71-173">String</span></span>|<span data-ttu-id="31d71-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31d71-174">The name of the app.</span></span> <span data-ttu-id="31d71-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="31d71-176">notes</span><span class="sxs-lookup"><span data-stu-id="31d71-176">Notes</span></span>|<span data-ttu-id="31d71-177">String</span><span class="sxs-lookup"><span data-stu-id="31d71-177">String</span></span>|<span data-ttu-id="31d71-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31d71-178">Notes for the app.</span></span> <span data-ttu-id="31d71-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="31d71-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="31d71-180">publishingState</span></span>|<span data-ttu-id="31d71-181">String</span><span class="sxs-lookup"><span data-stu-id="31d71-181">String</span></span>|<span data-ttu-id="31d71-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31d71-182">The publishing state for the app.</span></span> <span data-ttu-id="31d71-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="31d71-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="31d71-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="31d71-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="31d71-185">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="31d71-185">committedContentVersion</span></span>|<span data-ttu-id="31d71-186">String</span><span class="sxs-lookup"><span data-stu-id="31d71-186">String</span></span>|<span data-ttu-id="31d71-187">Versión interna del contenido confirmado.</span><span class="sxs-lookup"><span data-stu-id="31d71-187">The internal committed content version.</span></span> <span data-ttu-id="31d71-188">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-188">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="31d71-189">fileName</span><span class="sxs-lookup"><span data-stu-id="31d71-189">fileName</span></span>|<span data-ttu-id="31d71-190">String</span><span class="sxs-lookup"><span data-stu-id="31d71-190">String</span></span>|<span data-ttu-id="31d71-191">Nombre del archivo de la aplicación de LOB principal.</span><span class="sxs-lookup"><span data-stu-id="31d71-191">The name of the main Lob application file.</span></span> <span data-ttu-id="31d71-192">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-192">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="31d71-193">size</span><span class="sxs-lookup"><span data-stu-id="31d71-193">size</span></span>|<span data-ttu-id="31d71-194">Int64</span><span class="sxs-lookup"><span data-stu-id="31d71-194">Int64</span></span>|<span data-ttu-id="31d71-195">Tamaño total, incluidos todos los archivos cargados.</span><span class="sxs-lookup"><span data-stu-id="31d71-195">The total size, including all uploaded files.</span></span> <span data-ttu-id="31d71-196">Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).</span><span class="sxs-lookup"><span data-stu-id="31d71-196">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="31d71-197">applicableArchitectures</span><span class="sxs-lookup"><span data-stu-id="31d71-197">applicableArchitectures</span></span>|<span data-ttu-id="31d71-198">String</span><span class="sxs-lookup"><span data-stu-id="31d71-198">String</span></span>|<span data-ttu-id="31d71-199">Arquitecturas de Windows en las que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="31d71-199">The Windows architecture(s) for which this app can run on.</span></span> <span data-ttu-id="31d71-200">Los valores posibles son: `none`, `x86`, `x64`, `arm` y `neutral`.</span><span class="sxs-lookup"><span data-stu-id="31d71-200">Possible values are: `none`, `x86`, `x64`, `arm`, `neutral`.</span></span>|
|<span data-ttu-id="31d71-201">applicableDeviceTypes</span><span class="sxs-lookup"><span data-stu-id="31d71-201">applicableDeviceTypes</span></span>|<span data-ttu-id="31d71-202">String</span><span class="sxs-lookup"><span data-stu-id="31d71-202">String</span></span>|<span data-ttu-id="31d71-203">Tipos de dispositivos Windows en los que se puede ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="31d71-203">The Windows device type(s) for which this app can run on.</span></span> <span data-ttu-id="31d71-204">Los valores posibles son: `none`, `desktop`, `mobile`, `holographic` y `team`.</span><span class="sxs-lookup"><span data-stu-id="31d71-204">Possible values are: `none`, `desktop`, `mobile`, `holographic`, `team`.</span></span>|
|<span data-ttu-id="31d71-205">identityName</span><span class="sxs-lookup"><span data-stu-id="31d71-205">identityName</span></span>|<span data-ttu-id="31d71-206">String</span><span class="sxs-lookup"><span data-stu-id="31d71-206">String</span></span>|<span data-ttu-id="31d71-207">Nombre de la identidad.</span><span class="sxs-lookup"><span data-stu-id="31d71-207">The Identity Name.</span></span>|
|<span data-ttu-id="31d71-208">identityPublisherHash</span><span class="sxs-lookup"><span data-stu-id="31d71-208">identityPublisherHash</span></span>|<span data-ttu-id="31d71-209">String</span><span class="sxs-lookup"><span data-stu-id="31d71-209">String</span></span>|<span data-ttu-id="31d71-210">Hash del publicador de identidad.</span><span class="sxs-lookup"><span data-stu-id="31d71-210">The Identity Publisher Hash.</span></span>|
|<span data-ttu-id="31d71-211">identityResourceIdentifier</span><span class="sxs-lookup"><span data-stu-id="31d71-211">identityResourceIdentifier</span></span>|<span data-ttu-id="31d71-212">String</span><span class="sxs-lookup"><span data-stu-id="31d71-212">String</span></span>|<span data-ttu-id="31d71-213">Identificador del recurso de identidad.</span><span class="sxs-lookup"><span data-stu-id="31d71-213">The Identity Resource Identifier.</span></span>|
|<span data-ttu-id="31d71-214">isBundle</span><span class="sxs-lookup"><span data-stu-id="31d71-214">isBundle</span></span>|<span data-ttu-id="31d71-215">Boolean</span><span class="sxs-lookup"><span data-stu-id="31d71-215">Boolean</span></span>|<span data-ttu-id="31d71-216">Indica si la aplicación es una agrupación.</span><span class="sxs-lookup"><span data-stu-id="31d71-216">Whether or not the app is a bundle.</span></span>|
|<span data-ttu-id="31d71-217">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="31d71-217">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="31d71-218">windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="31d71-218">windowsMinimumOperatingSystem</span></span>](../resources/intune_apps_windowsminimumoperatingsystem.md)|<span data-ttu-id="31d71-219">Valor del sistema operativo mínimo aplicable.</span><span class="sxs-lookup"><span data-stu-id="31d71-219">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="31d71-220">identityVersion</span><span class="sxs-lookup"><span data-stu-id="31d71-220">identityVersion</span></span>|<span data-ttu-id="31d71-221">String</span><span class="sxs-lookup"><span data-stu-id="31d71-221">String</span></span>|<span data-ttu-id="31d71-222">Versión de la identidad.</span><span class="sxs-lookup"><span data-stu-id="31d71-222">The identity version.</span></span>|



## <a name="response"></a><span data-ttu-id="31d71-223">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31d71-223">Response</span></span>
<span data-ttu-id="31d71-224">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="31d71-224">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_apps_windowsuniversalappx.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="31d71-225">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="31d71-225">Example</span></span>
### <a name="request"></a><span data-ttu-id="31d71-226">Solicitud</span><span class="sxs-lookup"><span data-stu-id="31d71-226">Request</span></span>
<span data-ttu-id="31d71-227">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="31d71-227">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1253

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

### <a name="response"></a><span data-ttu-id="31d71-228">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31d71-228">Response</span></span>
<span data-ttu-id="31d71-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="31d71-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



