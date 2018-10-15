# <a name="update-webapp"></a><span data-ttu-id="5b15b-101">Actualizar webApp</span><span class="sxs-lookup"><span data-stu-id="5b15b-101">Update webApp</span></span>

> <span data-ttu-id="5b15b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5b15b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5b15b-103">Actualice las propiedades de un objeto [webApp](../resources/intune_apps_webapp.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-103">Update the properties of a [webApp](../resources/intune_apps_webapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5b15b-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5b15b-104">Prerequisites</span></span>
<span data-ttu-id="5b15b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5b15b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5b15b-107">Permission type</span></span>|<span data-ttu-id="5b15b-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5b15b-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5b15b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5b15b-109">Delegated (work or school account)</span></span>|<span data-ttu-id="5b15b-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5b15b-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="5b15b-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5b15b-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5b15b-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5b15b-112">Not supported.</span></span>|
|<span data-ttu-id="5b15b-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5b15b-113">Application</span></span>|<span data-ttu-id="5b15b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5b15b-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5b15b-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5b15b-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="5b15b-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5b15b-116">Request headers</span></span>
|<span data-ttu-id="5b15b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b15b-117">Header</span></span>|<span data-ttu-id="5b15b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5b15b-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5b15b-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="5b15b-119">Authorization</span></span>|<span data-ttu-id="5b15b-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5b15b-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5b15b-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5b15b-121">Accept</span></span>|<span data-ttu-id="5b15b-122">application/json</span><span class="sxs-lookup"><span data-stu-id="5b15b-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5b15b-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5b15b-123">Request body</span></span>
<span data-ttu-id="5b15b-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [webApp](../resources/intune_apps_webapp.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-124">In the request body, supply a JSON representation for the [webApp](../resources/intune_apps_webapp.md) object.</span></span>

<span data-ttu-id="5b15b-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [webApp](../resources/intune_apps_webapp.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-125">The following table shows the properties that are required when you create the [webApp](../resources/intune_apps_webapp.md).</span></span>

|<span data-ttu-id="5b15b-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5b15b-126">Property</span></span>|<span data-ttu-id="5b15b-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="5b15b-127">Type</span></span>|<span data-ttu-id="5b15b-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b15b-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5b15b-129">id.</span><span class="sxs-lookup"><span data-stu-id="5b15b-129">id</span></span>|<span data-ttu-id="5b15b-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="5b15b-130">String</span></span>|<span data-ttu-id="5b15b-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5b15b-131">Key of the entity.</span></span> <span data-ttu-id="5b15b-132">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5b15b-133">displayName</span><span class="sxs-lookup"><span data-stu-id="5b15b-133">displayName</span></span>|<span data-ttu-id="5b15b-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="5b15b-134">String</span></span>|<span data-ttu-id="5b15b-135">Título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="5b15b-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="5b15b-136">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5b15b-137">descripción</span><span class="sxs-lookup"><span data-stu-id="5b15b-137">description</span></span>|<span data-ttu-id="5b15b-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="5b15b-138">String</span></span>|<span data-ttu-id="5b15b-139">Descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5b15b-139">The description of the app.</span></span> <span data-ttu-id="5b15b-140">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5b15b-141">publicador</span><span class="sxs-lookup"><span data-stu-id="5b15b-141">publisher</span></span>|<span data-ttu-id="5b15b-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="5b15b-142">String</span></span>|<span data-ttu-id="5b15b-143">Publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5b15b-143">The publisher of the app.</span></span> <span data-ttu-id="5b15b-144">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5b15b-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="5b15b-145">largeIcon</span></span>|[<span data-ttu-id="5b15b-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="5b15b-146">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="5b15b-147">Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="5b15b-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="5b15b-148">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5b15b-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5b15b-149">createdDateTime</span></span>|<span data-ttu-id="5b15b-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5b15b-150">DateTimeOffset</span></span>|<span data-ttu-id="5b15b-151">Fecha y hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5b15b-151">The date and time the app was created.</span></span> <span data-ttu-id="5b15b-152">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5b15b-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="5b15b-153">lastModifiedDateTime</span></span>|<span data-ttu-id="5b15b-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5b15b-154">DateTimeOffset</span></span>|<span data-ttu-id="5b15b-155">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5b15b-155">The date and time the app was last modified.</span></span> <span data-ttu-id="5b15b-156">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5b15b-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="5b15b-157">isFeatured</span></span>|<span data-ttu-id="5b15b-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="5b15b-158">Boolean</span></span>|<span data-ttu-id="5b15b-159">Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5b15b-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="5b15b-160">privacyInformationUrl</span></span>|<span data-ttu-id="5b15b-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="5b15b-161">String</span></span>|<span data-ttu-id="5b15b-162">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="5b15b-162">The privacy statement Url.</span></span> <span data-ttu-id="5b15b-163">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5b15b-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="5b15b-164">informationUrl</span></span>|<span data-ttu-id="5b15b-165">Cadena</span><span class="sxs-lookup"><span data-stu-id="5b15b-165">String</span></span>|<span data-ttu-id="5b15b-166">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="5b15b-166">The more information Url.</span></span> <span data-ttu-id="5b15b-167">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5b15b-168">propietario/a</span><span class="sxs-lookup"><span data-stu-id="5b15b-168">owner</span></span>|<span data-ttu-id="5b15b-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="5b15b-169">String</span></span>|<span data-ttu-id="5b15b-170">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5b15b-170">The owner of the app.</span></span> <span data-ttu-id="5b15b-171">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5b15b-172">programador</span><span class="sxs-lookup"><span data-stu-id="5b15b-172">developer</span></span>|<span data-ttu-id="5b15b-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="5b15b-173">String</span></span>|<span data-ttu-id="5b15b-174">Desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5b15b-174">The developer of the app.</span></span> <span data-ttu-id="5b15b-175">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5b15b-176">notas</span><span class="sxs-lookup"><span data-stu-id="5b15b-176">notes</span></span>|<span data-ttu-id="5b15b-177">Cadena</span><span class="sxs-lookup"><span data-stu-id="5b15b-177">String</span></span>|<span data-ttu-id="5b15b-178">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5b15b-178">Notes for the app.</span></span> <span data-ttu-id="5b15b-179">Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="5b15b-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5b15b-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="5b15b-180">publishingState</span></span>|[<span data-ttu-id="5b15b-181">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="5b15b-181">mobileAppPublishingState</span></span>](../resources/intune_apps_mobileapppublishingstate.md)|<span data-ttu-id="5b15b-p114">El estado de publicación de la aplicación. La aplicación no se puede asignar a menos que se publique la aplicación. Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="5b15b-p114">The publishing state for the app. The app cannot be assigned unless the app is published. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md). The possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="5b15b-186">appUrl</span><span class="sxs-lookup"><span data-stu-id="5b15b-186">appUrl</span></span>|<span data-ttu-id="5b15b-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="5b15b-187">String</span></span>|<span data-ttu-id="5b15b-188">Dirección URL de la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="5b15b-188">The web app URL.</span></span>|
|<span data-ttu-id="5b15b-189">useManagedBrowser</span><span class="sxs-lookup"><span data-stu-id="5b15b-189">useManagedBrowser</span></span>|<span data-ttu-id="5b15b-190">Booleano</span><span class="sxs-lookup"><span data-stu-id="5b15b-190">Boolean</span></span>|<span data-ttu-id="5b15b-191">Indica si se va a usar el explorador administrado.</span><span class="sxs-lookup"><span data-stu-id="5b15b-191">Whether or not to use managed browser.</span></span> <span data-ttu-id="5b15b-192">Esta propiedad solo es aplicable a iOS y Android.</span><span class="sxs-lookup"><span data-stu-id="5b15b-192">This property is only applicable for Android and IOS.</span></span>|



## <a name="response"></a><span data-ttu-id="5b15b-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5b15b-193">Response</span></span>
<span data-ttu-id="5b15b-194">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [webApp](../resources/intune_apps_webapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5b15b-194">If successful, this method returns a `200 OK` response code and an updated [webApp](../resources/intune_apps_webapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5b15b-195">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5b15b-195">Example</span></span>
### <a name="request"></a><span data-ttu-id="5b15b-196">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5b15b-196">Request</span></span>
<span data-ttu-id="5b15b-197">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5b15b-197">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 664

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
  "appUrl": "https://example.com/appUrl/",
  "useManagedBrowser": true
}
```

### <a name="response"></a><span data-ttu-id="5b15b-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5b15b-198">Response</span></span>
<span data-ttu-id="5b15b-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5b15b-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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








