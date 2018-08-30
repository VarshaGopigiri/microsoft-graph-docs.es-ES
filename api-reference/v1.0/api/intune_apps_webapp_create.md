# <a name="create-webapp"></a><span data-ttu-id="95089-101">Crear webApp</span><span class="sxs-lookup"><span data-stu-id="95089-101">Create webApp</span></span>

> <span data-ttu-id="95089-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="95089-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="95089-103">Cree un objeto [webApp](../resources/intune_apps_webapp.md).</span><span class="sxs-lookup"><span data-stu-id="95089-103">Create a new [webApp](../resources/intune_apps_webapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="95089-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="95089-104">Prerequisites</span></span>
<span data-ttu-id="95089-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="95089-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="95089-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="95089-107">Permission type</span></span>|<span data-ttu-id="95089-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="95089-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="95089-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="95089-109">Delegated (work or school account)</span></span>|<span data-ttu-id="95089-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="95089-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="95089-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="95089-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="95089-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="95089-112">Not supported.</span></span>|
|<span data-ttu-id="95089-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="95089-113">Application</span></span>|<span data-ttu-id="95089-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="95089-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="95089-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="95089-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="95089-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="95089-116">Request headers</span></span>
|<span data-ttu-id="95089-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95089-117">Header</span></span>|<span data-ttu-id="95089-118">Valor</span><span class="sxs-lookup"><span data-stu-id="95089-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="95089-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="95089-119">Authorization</span></span>|<span data-ttu-id="95089-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="95089-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="95089-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="95089-121">Accept</span></span>|<span data-ttu-id="95089-122">application/json</span><span class="sxs-lookup"><span data-stu-id="95089-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="95089-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="95089-123">Request body</span></span>
<span data-ttu-id="95089-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto webApp.</span><span class="sxs-lookup"><span data-stu-id="95089-124">In the request body, supply a JSON representation for the webApp object.</span></span>

<span data-ttu-id="95089-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto webApp.</span><span class="sxs-lookup"><span data-stu-id="95089-125">The following table shows the properties that are required when you create the webApp.</span></span>

|<span data-ttu-id="95089-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="95089-126">Property</span></span>|<span data-ttu-id="95089-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="95089-127">Type</span></span>|<span data-ttu-id="95089-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="95089-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="95089-129">id</span><span class="sxs-lookup"><span data-stu-id="95089-129">id</span></span>|<span data-ttu-id="95089-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="95089-130">String</span></span>|<span data-ttu-id="95089-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="95089-131">Key of the entity.</span></span> <span data-ttu-id="95089-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="95089-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="95089-133">displayName</span><span class="sxs-lookup"><span data-stu-id="95089-133">displayName</span></span>|<span data-ttu-id="95089-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="95089-134">String</span></span>|<span data-ttu-id="95089-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="95089-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="95089-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="95089-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="95089-137">descripción</span><span class="sxs-lookup"><span data-stu-id="95089-137">description</span></span>|<span data-ttu-id="95089-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="95089-138">String</span></span>|<span data-ttu-id="95089-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="95089-139">The description of the app.</span></span> <span data-ttu-id="95089-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="95089-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="95089-141">publicador</span><span class="sxs-lookup"><span data-stu-id="95089-141">publisher</span></span>|<span data-ttu-id="95089-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="95089-142">String</span></span>|<span data-ttu-id="95089-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="95089-143">The publisher of the app.</span></span> <span data-ttu-id="95089-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="95089-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="95089-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="95089-145">largeIcon</span></span>|[<span data-ttu-id="95089-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="95089-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="95089-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="95089-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="95089-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="95089-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="95089-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="95089-149">createdDateTime</span></span>|<span data-ttu-id="95089-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="95089-150">DateTimeOffset</span></span>|<span data-ttu-id="95089-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="95089-151">The date and time the app was created.</span></span> <span data-ttu-id="95089-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="95089-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="95089-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="95089-153">lastModifiedDateTime</span></span>|<span data-ttu-id="95089-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="95089-154">DateTimeOffset</span></span>|<span data-ttu-id="95089-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="95089-155">The date and time the app was last modified.</span></span> <span data-ttu-id="95089-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="95089-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="95089-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="95089-157">isFeatured</span></span>|<span data-ttu-id="95089-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="95089-158">Boolean</span></span>|<span data-ttu-id="95089-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="95089-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="95089-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="95089-160">privacyInformationUrl</span></span>|<span data-ttu-id="95089-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="95089-161">String</span></span>|<span data-ttu-id="95089-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="95089-162">The privacy statement Url.</span></span> <span data-ttu-id="95089-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="95089-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="95089-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="95089-164">informationUrl</span></span>|<span data-ttu-id="95089-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="95089-165">String</span></span>|<span data-ttu-id="95089-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="95089-166">The more information Url.</span></span> <span data-ttu-id="95089-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="95089-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="95089-168">owner</span><span class="sxs-lookup"><span data-stu-id="95089-168">owner</span></span>|<span data-ttu-id="95089-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="95089-169">String</span></span>|<span data-ttu-id="95089-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="95089-170">The owner of the app.</span></span> <span data-ttu-id="95089-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="95089-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="95089-172">developer</span><span class="sxs-lookup"><span data-stu-id="95089-172">developer</span></span>|<span data-ttu-id="95089-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="95089-173">String</span></span>|<span data-ttu-id="95089-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="95089-174">The developer of the app.</span></span> <span data-ttu-id="95089-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="95089-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="95089-176">notes</span><span class="sxs-lookup"><span data-stu-id="95089-176">notes</span></span>|<span data-ttu-id="95089-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="95089-177">String</span></span>|<span data-ttu-id="95089-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="95089-178">Notes for the app.</span></span> <span data-ttu-id="95089-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="95089-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="95089-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="95089-180">publishingState</span></span>|[<span data-ttu-id="95089-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="95089-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="95089-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="95089-182">The publishing state for the app.</span></span> <span data-ttu-id="95089-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="95089-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="95089-184">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="95089-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span> <span data-ttu-id="95089-185">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="95089-185">The possible values are `notPublished`, `processing`, `published`, , , , , , , , , or .</span></span>|
|<span data-ttu-id="95089-186">appUrl</span><span class="sxs-lookup"><span data-stu-id="95089-186">appUrl</span></span>|<span data-ttu-id="95089-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="95089-187">String</span></span>|<span data-ttu-id="95089-188">Dirección URL de la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="95089-188">The web app URL.</span></span>|
|<span data-ttu-id="95089-189">useManagedBrowser</span><span class="sxs-lookup"><span data-stu-id="95089-189">useManagedBrowser</span></span>|<span data-ttu-id="95089-190">Booleano</span><span class="sxs-lookup"><span data-stu-id="95089-190">Boolean</span></span>|<span data-ttu-id="95089-191">Indica si se va a usar el explorador administrado.</span><span class="sxs-lookup"><span data-stu-id="95089-191">Whether or not to use managed browser.</span></span> <span data-ttu-id="95089-192">Esta propiedad solo es aplicable a iOS y Android.</span><span class="sxs-lookup"><span data-stu-id="95089-192">This property is only applicable for Android and IOS.</span></span>|



## <a name="response"></a><span data-ttu-id="95089-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="95089-193">Response</span></span>
<span data-ttu-id="95089-194">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [webApp](../resources/intune_apps_webapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="95089-194">If successful, this method returns a `201 Created` response code and a [webApp](../resources/intune_apps_webapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="95089-195">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="95089-195">Example</span></span>
### <a name="request"></a><span data-ttu-id="95089-196">Solicitud</span><span class="sxs-lookup"><span data-stu-id="95089-196">Request</span></span>
<span data-ttu-id="95089-197">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="95089-197">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="95089-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="95089-198">Response</span></span>
<span data-ttu-id="95089-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="95089-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



