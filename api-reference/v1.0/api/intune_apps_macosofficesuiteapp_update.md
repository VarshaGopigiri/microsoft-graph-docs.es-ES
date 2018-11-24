# <a name="update-macosofficesuiteapp"></a><span data-ttu-id="7a61e-101">Actualizar macOSOfficeSuiteApp</span><span class="sxs-lookup"><span data-stu-id="7a61e-101">Update macOSOfficeSuiteApp</span></span>

> <span data-ttu-id="7a61e-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7a61e-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7a61e-103">Actualice las propiedades de un objeto [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-103">Update the properties of a [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7a61e-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7a61e-104">Prerequisites</span></span>
<span data-ttu-id="7a61e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7a61e-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7a61e-107">Permission type</span></span>|<span data-ttu-id="7a61e-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7a61e-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7a61e-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7a61e-109">Delegated (work or school account)</span></span>|<span data-ttu-id="7a61e-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7a61e-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="7a61e-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7a61e-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7a61e-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7a61e-112">Not supported.</span></span>|
|<span data-ttu-id="7a61e-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7a61e-113">Application</span></span>|<span data-ttu-id="7a61e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7a61e-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7a61e-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7a61e-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="7a61e-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7a61e-116">Request headers</span></span>
|<span data-ttu-id="7a61e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7a61e-117">Header</span></span>|<span data-ttu-id="7a61e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7a61e-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7a61e-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="7a61e-119">Authorization</span></span>|<span data-ttu-id="7a61e-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7a61e-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7a61e-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7a61e-121">Accept</span></span>|<span data-ttu-id="7a61e-122">application/json</span><span class="sxs-lookup"><span data-stu-id="7a61e-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7a61e-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7a61e-123">Request body</span></span>
<span data-ttu-id="7a61e-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-124">In the request body, supply a JSON representation for the [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md) object.</span></span>

<span data-ttu-id="7a61e-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-125">The following table shows the properties that are required when you create the [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md).</span></span>

|<span data-ttu-id="7a61e-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7a61e-126">Property</span></span>|<span data-ttu-id="7a61e-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a61e-127">Type</span></span>|<span data-ttu-id="7a61e-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a61e-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7a61e-129">id</span><span class="sxs-lookup"><span data-stu-id="7a61e-129">id</span></span>|<span data-ttu-id="7a61e-130">String</span><span class="sxs-lookup"><span data-stu-id="7a61e-130">String</span></span>|<span data-ttu-id="7a61e-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7a61e-131">Key of the entity.</span></span> <span data-ttu-id="7a61e-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7a61e-133">displayName</span><span class="sxs-lookup"><span data-stu-id="7a61e-133">displayName</span></span>|<span data-ttu-id="7a61e-134">String</span><span class="sxs-lookup"><span data-stu-id="7a61e-134">String</span></span>|<span data-ttu-id="7a61e-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="7a61e-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="7a61e-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7a61e-137">description</span><span class="sxs-lookup"><span data-stu-id="7a61e-137">description</span></span>|<span data-ttu-id="7a61e-138">String</span><span class="sxs-lookup"><span data-stu-id="7a61e-138">String</span></span>|<span data-ttu-id="7a61e-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a61e-139">The description of the app.</span></span> <span data-ttu-id="7a61e-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7a61e-141">publicador</span><span class="sxs-lookup"><span data-stu-id="7a61e-141">publisher</span></span>|<span data-ttu-id="7a61e-142">String</span><span class="sxs-lookup"><span data-stu-id="7a61e-142">String</span></span>|<span data-ttu-id="7a61e-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a61e-143">The publisher of the app.</span></span> <span data-ttu-id="7a61e-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7a61e-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="7a61e-145">largeIcon</span></span>|[<span data-ttu-id="7a61e-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="7a61e-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="7a61e-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="7a61e-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="7a61e-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7a61e-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="7a61e-149">createdDateTime</span></span>|<span data-ttu-id="7a61e-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7a61e-150">DateTimeOffset</span></span>|<span data-ttu-id="7a61e-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a61e-151">The date and time the app was created.</span></span> <span data-ttu-id="7a61e-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7a61e-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7a61e-153">lastModifiedDateTime</span></span>|<span data-ttu-id="7a61e-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7a61e-154">DateTimeOffset</span></span>|<span data-ttu-id="7a61e-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a61e-155">The date and time the app was last modified.</span></span> <span data-ttu-id="7a61e-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7a61e-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="7a61e-157">isFeatured</span></span>|<span data-ttu-id="7a61e-158">Boolean</span><span class="sxs-lookup"><span data-stu-id="7a61e-158">Boolean</span></span>|<span data-ttu-id="7a61e-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7a61e-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="7a61e-160">privacyInformationUrl</span></span>|<span data-ttu-id="7a61e-161">String</span><span class="sxs-lookup"><span data-stu-id="7a61e-161">String</span></span>|<span data-ttu-id="7a61e-162">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="7a61e-162">The privacy statement Url.</span></span> <span data-ttu-id="7a61e-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7a61e-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="7a61e-164">informationUrl</span></span>|<span data-ttu-id="7a61e-165">String</span><span class="sxs-lookup"><span data-stu-id="7a61e-165">String</span></span>|<span data-ttu-id="7a61e-166">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="7a61e-166">The more information Url.</span></span> <span data-ttu-id="7a61e-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7a61e-168">owner</span><span class="sxs-lookup"><span data-stu-id="7a61e-168">owner</span></span>|<span data-ttu-id="7a61e-169">String</span><span class="sxs-lookup"><span data-stu-id="7a61e-169">String</span></span>|<span data-ttu-id="7a61e-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a61e-170">The owner of the app.</span></span> <span data-ttu-id="7a61e-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7a61e-172">developer</span><span class="sxs-lookup"><span data-stu-id="7a61e-172">developer</span></span>|<span data-ttu-id="7a61e-173">String</span><span class="sxs-lookup"><span data-stu-id="7a61e-173">String</span></span>|<span data-ttu-id="7a61e-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a61e-174">The developer of the app.</span></span> <span data-ttu-id="7a61e-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7a61e-176">notas</span><span class="sxs-lookup"><span data-stu-id="7a61e-176">notes</span></span>|<span data-ttu-id="7a61e-177">String</span><span class="sxs-lookup"><span data-stu-id="7a61e-177">String</span></span>|<span data-ttu-id="7a61e-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a61e-178">Notes for the app.</span></span> <span data-ttu-id="7a61e-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="7a61e-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="7a61e-180">publishingState</span></span>|[<span data-ttu-id="7a61e-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="7a61e-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="7a61e-182">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7a61e-182">The publishing state for the app.</span></span> <span data-ttu-id="7a61e-183">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="7a61e-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="7a61e-184">Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7a61e-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md).</span></span> <span data-ttu-id="7a61e-185">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="7a61e-185">Possible values are: `notPublished`, `processing`, `published`.</span></span>|



## <a name="response"></a><span data-ttu-id="7a61e-186">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a61e-186">Response</span></span>
<span data-ttu-id="7a61e-187">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7a61e-187">If successful, this method returns a `200 OK` response code and an updated [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7a61e-188">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7a61e-188">Example</span></span>
### <a name="request"></a><span data-ttu-id="7a61e-189">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7a61e-189">Request</span></span>
<span data-ttu-id="7a61e-190">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7a61e-190">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 584

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
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "publishingState": "processing"
}
```

### <a name="response"></a><span data-ttu-id="7a61e-191">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a61e-191">Response</span></span>
<span data-ttu-id="7a61e-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7a61e-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



