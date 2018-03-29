# <a name="create-webapp"></a><span data-ttu-id="907d1-101">Crear webApp</span><span class="sxs-lookup"><span data-stu-id="907d1-101">Create webApp</span></span>

> <span data-ttu-id="907d1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="907d1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="907d1-103">Cree un objeto [webApp](../resources/intune_apps_webapp.md).</span><span class="sxs-lookup"><span data-stu-id="907d1-103">Create a new [plannerBucket](../resources/intune_apps_webapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="907d1-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="907d1-104">Prerequisites</span></span>
<span data-ttu-id="907d1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="907d1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="907d1-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="907d1-107">Permission type</span></span>|<span data-ttu-id="907d1-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="907d1-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="907d1-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="907d1-109">Delegated (work or school account)</span></span>|<span data-ttu-id="907d1-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="907d1-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="907d1-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="907d1-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="907d1-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="907d1-112">Not supported.</span></span>|
|<span data-ttu-id="907d1-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="907d1-113">Application</span></span>|<span data-ttu-id="907d1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="907d1-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="907d1-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="907d1-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="907d1-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="907d1-116">Request headers</span></span>
|<span data-ttu-id="907d1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="907d1-117">Header</span></span>|<span data-ttu-id="907d1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="907d1-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="907d1-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="907d1-119">Authorization</span></span>|<span data-ttu-id="907d1-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="907d1-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="907d1-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="907d1-121">Accept</span></span>|<span data-ttu-id="907d1-122">application/json</span><span class="sxs-lookup"><span data-stu-id="907d1-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="907d1-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="907d1-123">Request body</span></span>
<span data-ttu-id="907d1-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto webApp.</span><span class="sxs-lookup"><span data-stu-id="907d1-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="907d1-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto webApp.</span><span class="sxs-lookup"><span data-stu-id="907d1-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="907d1-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="907d1-126">Property</span></span>|<span data-ttu-id="907d1-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="907d1-127">Type</span></span>|<span data-ttu-id="907d1-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="907d1-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="907d1-129">id</span><span class="sxs-lookup"><span data-stu-id="907d1-129">id</span></span>|<span data-ttu-id="907d1-130">String</span><span class="sxs-lookup"><span data-stu-id="907d1-130">String</span></span>|<span data-ttu-id="907d1-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="907d1-131">Key of the setting.</span></span> <span data-ttu-id="907d1-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="907d1-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="907d1-133">displayName</span><span class="sxs-lookup"><span data-stu-id="907d1-133">displayName</span></span>|<span data-ttu-id="907d1-134">String</span><span class="sxs-lookup"><span data-stu-id="907d1-134">String</span></span>|<span data-ttu-id="907d1-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="907d1-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="907d1-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="907d1-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="907d1-137">description</span><span class="sxs-lookup"><span data-stu-id="907d1-137">description</span></span>|<span data-ttu-id="907d1-138">String</span><span class="sxs-lookup"><span data-stu-id="907d1-138">String</span></span>|<span data-ttu-id="907d1-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="907d1-139">The description of the app.</span></span> <span data-ttu-id="907d1-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="907d1-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="907d1-141">publicador</span><span class="sxs-lookup"><span data-stu-id="907d1-141">Publisher</span></span>|<span data-ttu-id="907d1-142">String</span><span class="sxs-lookup"><span data-stu-id="907d1-142">String</span></span>|<span data-ttu-id="907d1-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="907d1-143">The name of the app.</span></span> <span data-ttu-id="907d1-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="907d1-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="907d1-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="907d1-145">largeIcon</span></span>|[<span data-ttu-id="907d1-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="907d1-146">mimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="907d1-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="907d1-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="907d1-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="907d1-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="907d1-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="907d1-149">createdDateTime</span></span>|<span data-ttu-id="907d1-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="907d1-150">DateTimeOffset</span></span>|<span data-ttu-id="907d1-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="907d1-151">The date and time when the page was created.</span></span> <span data-ttu-id="907d1-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="907d1-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="907d1-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="907d1-153">lastModifiedDateTime</span></span>|<span data-ttu-id="907d1-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="907d1-154">DateTimeOffset</span></span>|<span data-ttu-id="907d1-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="907d1-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="907d1-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="907d1-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="907d1-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="907d1-157">isFeatured</span></span>|<span data-ttu-id="907d1-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="907d1-158">Boolean</span></span>|<span data-ttu-id="907d1-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="907d1-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="907d1-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="907d1-160">privacyInformationUrl</span></span>|<span data-ttu-id="907d1-161">String</span><span class="sxs-lookup"><span data-stu-id="907d1-161">String</span></span>|<span data-ttu-id="907d1-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="907d1-162">The privacy statement Url.</span></span> <span data-ttu-id="907d1-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="907d1-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="907d1-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="907d1-164">informationUrl</span></span>|<span data-ttu-id="907d1-165">String</span><span class="sxs-lookup"><span data-stu-id="907d1-165">String</span></span>|<span data-ttu-id="907d1-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="907d1-166">The more information Url.</span></span> <span data-ttu-id="907d1-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="907d1-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="907d1-168">owner</span><span class="sxs-lookup"><span data-stu-id="907d1-168">owner</span></span>|<span data-ttu-id="907d1-169">String</span><span class="sxs-lookup"><span data-stu-id="907d1-169">String</span></span>|<span data-ttu-id="907d1-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="907d1-170">The owner of the timesheet.</span></span> <span data-ttu-id="907d1-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="907d1-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="907d1-172">developer</span><span class="sxs-lookup"><span data-stu-id="907d1-172">developer</span></span>|<span data-ttu-id="907d1-173">String</span><span class="sxs-lookup"><span data-stu-id="907d1-173">String</span></span>|<span data-ttu-id="907d1-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="907d1-174">The name of the app.</span></span> <span data-ttu-id="907d1-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="907d1-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="907d1-176">notas</span><span class="sxs-lookup"><span data-stu-id="907d1-176">Notes</span></span>|<span data-ttu-id="907d1-177">String</span><span class="sxs-lookup"><span data-stu-id="907d1-177">String</span></span>|<span data-ttu-id="907d1-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="907d1-178">Notes for the app.</span></span> <span data-ttu-id="907d1-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="907d1-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="907d1-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="907d1-180">publishingState</span></span>|<span data-ttu-id="907d1-181">String</span><span class="sxs-lookup"><span data-stu-id="907d1-181">String</span></span>|<span data-ttu-id="907d1-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="907d1-182">The publishing state for the app.</span></span> <span data-ttu-id="907d1-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="907d1-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="907d1-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="907d1-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="907d1-185">appUrl</span><span class="sxs-lookup"><span data-stu-id="907d1-185">appUrl</span></span>|<span data-ttu-id="907d1-186">String</span><span class="sxs-lookup"><span data-stu-id="907d1-186">String</span></span>|<span data-ttu-id="907d1-187">Dirección URL de la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="907d1-187">The web app URL.</span></span>|
|<span data-ttu-id="907d1-188">useManagedBrowser</span><span class="sxs-lookup"><span data-stu-id="907d1-188">useManagedBrowser</span></span>|<span data-ttu-id="907d1-189">Booleano</span><span class="sxs-lookup"><span data-stu-id="907d1-189">Boolean</span></span>|<span data-ttu-id="907d1-190">Indica si se va a usar el explorador administrado.</span><span class="sxs-lookup"><span data-stu-id="907d1-190">Whether or not to use managed browser.</span></span> <span data-ttu-id="907d1-191">Esta propiedad solo es aplicable a iOS y Android.</span><span class="sxs-lookup"><span data-stu-id="907d1-191">This property is only applicable for Android and IOS.</span></span>|



## <a name="response"></a><span data-ttu-id="907d1-192">Respuesta</span><span class="sxs-lookup"><span data-stu-id="907d1-192">Response</span></span>
<span data-ttu-id="907d1-193">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [webApp](../resources/intune_apps_webapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="907d1-193">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_apps_webapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="907d1-194">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="907d1-194">Example</span></span>
### <a name="request"></a><span data-ttu-id="907d1-195">Solicitud</span><span class="sxs-lookup"><span data-stu-id="907d1-195">Request</span></span>
<span data-ttu-id="907d1-196">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="907d1-196">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 709

{
  "@odata.type": "#microsoft.graph.webApp",
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
  "appUrl": "https://example.com/appUrl/",
  "useManagedBrowser": true
}
```

### <a name="response"></a><span data-ttu-id="907d1-197">Respuesta</span><span class="sxs-lookup"><span data-stu-id="907d1-197">Response</span></span>
<span data-ttu-id="907d1-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="907d1-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 817

{
  "@odata.type": "#microsoft.graph.webApp",
  "id": "4bdc5d30-5d30-4bdc-305d-dc4b305ddc4b",
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
  "appUrl": "https://example.com/appUrl/",
  "useManagedBrowser": true
}
```



