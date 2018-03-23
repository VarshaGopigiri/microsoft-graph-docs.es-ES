# <a name="create-macosofficesuiteapp"></a><span data-ttu-id="e9962-101">Crear macOSOfficeSuiteApp</span><span class="sxs-lookup"><span data-stu-id="e9962-101">Create macOSOfficeSuiteApp</span></span>

> <span data-ttu-id="e9962-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e9962-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e9962-103">Cree un objeto [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9962-103">Create a new [plannerBucket](../resources/intune_apps_macosofficesuiteapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e9962-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e9962-104">Prerequisites</span></span>
<span data-ttu-id="e9962-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e9962-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e9962-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e9962-107">Permission type</span></span>|<span data-ttu-id="e9962-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e9962-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e9962-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e9962-109">Delegated (work or school account)</span></span>|<span data-ttu-id="e9962-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e9962-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="e9962-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e9962-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e9962-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9962-112">Not supported.</span></span>|
|<span data-ttu-id="e9962-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e9962-113">Application</span></span>|<span data-ttu-id="e9962-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9962-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e9962-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e9962-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="e9962-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9962-116">Request headers</span></span>
|<span data-ttu-id="e9962-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9962-117">Header</span></span>|<span data-ttu-id="e9962-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e9962-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e9962-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="e9962-119">Authorization</span></span>|<span data-ttu-id="e9962-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e9962-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="e9962-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e9962-121">Accept</span></span>|<span data-ttu-id="e9962-122">application/json</span><span class="sxs-lookup"><span data-stu-id="e9962-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e9962-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e9962-123">Request body</span></span>
<span data-ttu-id="e9962-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto macOSOfficeSuiteApp.</span><span class="sxs-lookup"><span data-stu-id="e9962-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="e9962-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto macOSOfficeSuiteApp.</span><span class="sxs-lookup"><span data-stu-id="e9962-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="e9962-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e9962-126">Property</span></span>|<span data-ttu-id="e9962-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9962-127">Type</span></span>|<span data-ttu-id="e9962-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9962-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e9962-129">id</span><span class="sxs-lookup"><span data-stu-id="e9962-129">id</span></span>|<span data-ttu-id="e9962-130">String</span><span class="sxs-lookup"><span data-stu-id="e9962-130">String</span></span>|<span data-ttu-id="e9962-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e9962-131">Key of the setting.</span></span> <span data-ttu-id="e9962-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9962-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e9962-133">displayName</span><span class="sxs-lookup"><span data-stu-id="e9962-133">displayName</span></span>|<span data-ttu-id="e9962-134">String</span><span class="sxs-lookup"><span data-stu-id="e9962-134">String</span></span>|<span data-ttu-id="e9962-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="e9962-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="e9962-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9962-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e9962-137">description</span><span class="sxs-lookup"><span data-stu-id="e9962-137">description</span></span>|<span data-ttu-id="e9962-138">String</span><span class="sxs-lookup"><span data-stu-id="e9962-138">String</span></span>|<span data-ttu-id="e9962-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9962-139">The description of the app.</span></span> <span data-ttu-id="e9962-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9962-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e9962-141">publicador</span><span class="sxs-lookup"><span data-stu-id="e9962-141">Publisher</span></span>|<span data-ttu-id="e9962-142">String</span><span class="sxs-lookup"><span data-stu-id="e9962-142">String</span></span>|<span data-ttu-id="e9962-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9962-143">The name of the app.</span></span> <span data-ttu-id="e9962-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9962-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e9962-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="e9962-145">largeIcon</span></span>|[<span data-ttu-id="e9962-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="e9962-146">mimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="e9962-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="e9962-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="e9962-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9962-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e9962-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e9962-149">createdDateTime</span></span>|<span data-ttu-id="e9962-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e9962-150">DateTimeOffset</span></span>|<span data-ttu-id="e9962-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9962-151">The date and time when the page was created.</span></span> <span data-ttu-id="e9962-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9962-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e9962-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e9962-153">lastModifiedDateTime</span></span>|<span data-ttu-id="e9962-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e9962-154">DateTimeOffset</span></span>|<span data-ttu-id="e9962-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9962-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="e9962-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9962-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e9962-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="e9962-157">isFeatured</span></span>|<span data-ttu-id="e9962-158">Boolean</span><span class="sxs-lookup"><span data-stu-id="e9962-158">Boolean</span></span>|<span data-ttu-id="e9962-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9962-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e9962-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="e9962-160">privacyInformationUrl</span></span>|<span data-ttu-id="e9962-161">String</span><span class="sxs-lookup"><span data-stu-id="e9962-161">String</span></span>|<span data-ttu-id="e9962-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="e9962-162">The privacy statement Url.</span></span> <span data-ttu-id="e9962-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9962-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e9962-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="e9962-164">informationUrl</span></span>|<span data-ttu-id="e9962-165">String</span><span class="sxs-lookup"><span data-stu-id="e9962-165">String</span></span>|<span data-ttu-id="e9962-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="e9962-166">The more information Url.</span></span> <span data-ttu-id="e9962-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9962-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e9962-168">owner</span><span class="sxs-lookup"><span data-stu-id="e9962-168">owner</span></span>|<span data-ttu-id="e9962-169">String</span><span class="sxs-lookup"><span data-stu-id="e9962-169">String</span></span>|<span data-ttu-id="e9962-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9962-170">The owner of the timesheet.</span></span> <span data-ttu-id="e9962-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9962-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e9962-172">developer</span><span class="sxs-lookup"><span data-stu-id="e9962-172">developer</span></span>|<span data-ttu-id="e9962-173">String</span><span class="sxs-lookup"><span data-stu-id="e9962-173">String</span></span>|<span data-ttu-id="e9962-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9962-174">The name of the app.</span></span> <span data-ttu-id="e9962-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9962-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e9962-176">notas</span><span class="sxs-lookup"><span data-stu-id="e9962-176">Notes</span></span>|<span data-ttu-id="e9962-177">String</span><span class="sxs-lookup"><span data-stu-id="e9962-177">String</span></span>|<span data-ttu-id="e9962-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9962-178">Notes for the app.</span></span> <span data-ttu-id="e9962-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="e9962-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="e9962-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="e9962-180">publishingState</span></span>|<span data-ttu-id="e9962-181">String</span><span class="sxs-lookup"><span data-stu-id="e9962-181">String</span></span>|<span data-ttu-id="e9962-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9962-182">The publishing state for the app.</span></span> <span data-ttu-id="e9962-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="e9962-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="e9962-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="e9962-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|



## <a name="response"></a><span data-ttu-id="e9962-185">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9962-185">Response</span></span>
<span data-ttu-id="e9962-186">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9962-186">If successful, this method returns a `201 Created` response code and a [ListItemVersion](../resources/intune_apps_macosofficesuiteapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e9962-187">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e9962-187">Example</span></span>
### <a name="request"></a><span data-ttu-id="e9962-188">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9962-188">Request</span></span>
<span data-ttu-id="e9962-189">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9962-189">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 648

{
  "@odata.type": "#microsoft.graph.macOSOfficeSuiteApp",
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
  "publishingState": "processing"
}
```

### <a name="response"></a><span data-ttu-id="e9962-190">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9962-190">Response</span></span>
<span data-ttu-id="e9962-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e9962-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 756

{
  "@odata.type": "#microsoft.graph.macOSOfficeSuiteApp",
  "id": "bf39e35d-e35d-bf39-5de3-39bf5de339bf",
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
  "publishingState": "processing"
}
```



