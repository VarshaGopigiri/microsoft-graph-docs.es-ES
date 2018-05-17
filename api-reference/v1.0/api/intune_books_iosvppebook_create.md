# <a name="create-iosvppebook"></a><span data-ttu-id="be240-101">Crear iosVppEBook</span><span class="sxs-lookup"><span data-stu-id="be240-101">Create iosVppEBook</span></span>

> <span data-ttu-id="be240-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="be240-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="be240-103">Cree un objeto [iosVppEBook](../resources/intune_books_iosvppebook.md).</span><span class="sxs-lookup"><span data-stu-id="be240-103">Create a new [iosVppEBook](../resources/intune_books_iosvppebook.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="be240-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="be240-104">Prerequisites</span></span>
<span data-ttu-id="be240-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="be240-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="be240-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="be240-107">Permission type</span></span>|<span data-ttu-id="be240-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="be240-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="be240-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="be240-109">Delegated (work or school account)</span></span>|<span data-ttu-id="be240-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="be240-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="be240-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="be240-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="be240-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="be240-112">Not supported.</span></span>|
|<span data-ttu-id="be240-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="be240-113">Application</span></span>|<span data-ttu-id="be240-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="be240-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="be240-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="be240-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks
```

## <a name="request-headers"></a><span data-ttu-id="be240-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="be240-116">Request headers</span></span>
|<span data-ttu-id="be240-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be240-117">Header</span></span>|<span data-ttu-id="be240-118">Valor</span><span class="sxs-lookup"><span data-stu-id="be240-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="be240-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="be240-119">Authorization</span></span>|<span data-ttu-id="be240-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="be240-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="be240-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="be240-121">Accept</span></span>|<span data-ttu-id="be240-122">application/json</span><span class="sxs-lookup"><span data-stu-id="be240-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="be240-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="be240-123">Request body</span></span>
<span data-ttu-id="be240-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosVppEBook.</span><span class="sxs-lookup"><span data-stu-id="be240-124">In the request body, supply a JSON representation for the iosVppEBook object.</span></span>

<span data-ttu-id="be240-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosVppEBook.</span><span class="sxs-lookup"><span data-stu-id="be240-125">The following table shows the properties that are required when you create the iosVppEBook.</span></span>

|<span data-ttu-id="be240-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="be240-126">Property</span></span>|<span data-ttu-id="be240-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="be240-127">Type</span></span>|<span data-ttu-id="be240-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="be240-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="be240-129">id</span><span class="sxs-lookup"><span data-stu-id="be240-129">id</span></span>|<span data-ttu-id="be240-130">String</span><span class="sxs-lookup"><span data-stu-id="be240-130">String</span></span>|<span data-ttu-id="be240-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="be240-131">Key of the entity.</span></span> <span data-ttu-id="be240-132">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="be240-132">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="be240-133">displayName</span><span class="sxs-lookup"><span data-stu-id="be240-133">displayName</span></span>|<span data-ttu-id="be240-134">String</span><span class="sxs-lookup"><span data-stu-id="be240-134">String</span></span>|<span data-ttu-id="be240-135">Nombre del libro electrónico</span><span class="sxs-lookup"><span data-stu-id="be240-135">Name of the eBook.</span></span> <span data-ttu-id="be240-136">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="be240-136">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="be240-137">description</span><span class="sxs-lookup"><span data-stu-id="be240-137">description</span></span>|<span data-ttu-id="be240-138">String</span><span class="sxs-lookup"><span data-stu-id="be240-138">String</span></span>|<span data-ttu-id="be240-139">Descripción.</span><span class="sxs-lookup"><span data-stu-id="be240-139">Description.</span></span> <span data-ttu-id="be240-140">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="be240-140">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="be240-141">publicador</span><span class="sxs-lookup"><span data-stu-id="be240-141">publisher</span></span>|<span data-ttu-id="be240-142">String</span><span class="sxs-lookup"><span data-stu-id="be240-142">String</span></span>|<span data-ttu-id="be240-143">Publicador.</span><span class="sxs-lookup"><span data-stu-id="be240-143">Publisher.</span></span> <span data-ttu-id="be240-144">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="be240-144">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="be240-145">publishedDateTime</span><span class="sxs-lookup"><span data-stu-id="be240-145">publishedDateTime</span></span>|<span data-ttu-id="be240-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="be240-146">DateTimeOffset</span></span>|<span data-ttu-id="be240-147">La fecha y la hora en que se publicó el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="be240-147">The date and time when the eBook was published.</span></span> <span data-ttu-id="be240-148">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="be240-148">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="be240-149">largeCover</span><span class="sxs-lookup"><span data-stu-id="be240-149">largeCover</span></span>|[<span data-ttu-id="be240-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="be240-150">mimeContent</span></span>](../resources/intune_shared_mimecontent.md)|<span data-ttu-id="be240-151">Cubierta de libro.</span><span class="sxs-lookup"><span data-stu-id="be240-151">Book cover.</span></span> <span data-ttu-id="be240-152">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="be240-152">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="be240-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="be240-153">createdDateTime</span></span>|<span data-ttu-id="be240-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="be240-154">DateTimeOffset</span></span>|<span data-ttu-id="be240-155">La fecha y la hora en que se creó el archivo del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="be240-155">The date and time when the eBook file was created.</span></span> <span data-ttu-id="be240-156">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="be240-156">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="be240-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="be240-157">lastModifiedDateTime</span></span>|<span data-ttu-id="be240-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="be240-158">DateTimeOffset</span></span>|<span data-ttu-id="be240-159">La fecha y la hora en que se modificó por última vez el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="be240-159">The date and time when the eBook was last modified.</span></span> <span data-ttu-id="be240-160">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="be240-160">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="be240-161">informationUrl</span><span class="sxs-lookup"><span data-stu-id="be240-161">informationUrl</span></span>|<span data-ttu-id="be240-162">String</span><span class="sxs-lookup"><span data-stu-id="be240-162">String</span></span>|<span data-ttu-id="be240-163">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="be240-163">The more information Url.</span></span> <span data-ttu-id="be240-164">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="be240-164">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="be240-165">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="be240-165">privacyInformationUrl</span></span>|<span data-ttu-id="be240-166">String</span><span class="sxs-lookup"><span data-stu-id="be240-166">String</span></span>|<span data-ttu-id="be240-167">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="be240-167">The privacy statement Url.</span></span> <span data-ttu-id="be240-168">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="be240-168">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="be240-169">vppTokenId</span><span class="sxs-lookup"><span data-stu-id="be240-169">vppTokenId</span></span>|<span data-ttu-id="be240-170">Guid</span><span class="sxs-lookup"><span data-stu-id="be240-170">Guid</span></span>|<span data-ttu-id="be240-171">El Id. de token de VPP.</span><span class="sxs-lookup"><span data-stu-id="be240-171">The Vpp token ID.</span></span>|
|<span data-ttu-id="be240-172">appleId</span><span class="sxs-lookup"><span data-stu-id="be240-172">appleId</span></span>|<span data-ttu-id="be240-173">String</span><span class="sxs-lookup"><span data-stu-id="be240-173">String</span></span>|<span data-ttu-id="be240-174">El ID de Apple asociado a un token de VPP.</span><span class="sxs-lookup"><span data-stu-id="be240-174">The Apple ID associated with Vpp token.</span></span>|
|<span data-ttu-id="be240-175">vppOrganizationName</span><span class="sxs-lookup"><span data-stu-id="be240-175">vppOrganizationName</span></span>|<span data-ttu-id="be240-176">String</span><span class="sxs-lookup"><span data-stu-id="be240-176">String</span></span>|<span data-ttu-id="be240-177">El nombre de la organización del token de VPP.</span><span class="sxs-lookup"><span data-stu-id="be240-177">The Vpp token's organization name.</span></span>|
|<span data-ttu-id="be240-178">géneros</span><span class="sxs-lookup"><span data-stu-id="be240-178">genres</span></span>|<span data-ttu-id="be240-179">Colección string</span><span class="sxs-lookup"><span data-stu-id="be240-179">String collection</span></span>|<span data-ttu-id="be240-180">Géneros.</span><span class="sxs-lookup"><span data-stu-id="be240-180">Genres.</span></span>|
|<span data-ttu-id="be240-181">language</span><span class="sxs-lookup"><span data-stu-id="be240-181">language</span></span>|<span data-ttu-id="be240-182">String</span><span class="sxs-lookup"><span data-stu-id="be240-182">String</span></span>|<span data-ttu-id="be240-183">Idioma.</span><span class="sxs-lookup"><span data-stu-id="be240-183">Language.</span></span>|
|<span data-ttu-id="be240-184">vendedor</span><span class="sxs-lookup"><span data-stu-id="be240-184">seller</span></span>|<span data-ttu-id="be240-185">String</span><span class="sxs-lookup"><span data-stu-id="be240-185">String</span></span>|<span data-ttu-id="be240-186">Vendedor.</span><span class="sxs-lookup"><span data-stu-id="be240-186">Seller.</span></span>|
|<span data-ttu-id="be240-187">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="be240-187">totalLicenseCount</span></span>|<span data-ttu-id="be240-188">Int32</span><span class="sxs-lookup"><span data-stu-id="be240-188">Int32</span></span>|<span data-ttu-id="be240-189">Número total de licencias.</span><span class="sxs-lookup"><span data-stu-id="be240-189">Total license count.</span></span>|
|<span data-ttu-id="be240-190">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="be240-190">usedLicenseCount</span></span>|<span data-ttu-id="be240-191">Int32</span><span class="sxs-lookup"><span data-stu-id="be240-191">Int32</span></span>|<span data-ttu-id="be240-192">Número de licencias usadas.</span><span class="sxs-lookup"><span data-stu-id="be240-192">Used license count.</span></span>|



## <a name="response"></a><span data-ttu-id="be240-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="be240-193">Response</span></span>
<span data-ttu-id="be240-194">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosVppEBook](../resources/intune_books_iosvppebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="be240-194">If successful, this method returns a `201 Created` response code and a [iosVppEBook](../resources/intune_books_iosvppebook.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="be240-195">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="be240-195">Example</span></span>
### <a name="request"></a><span data-ttu-id="be240-196">Solicitud</span><span class="sxs-lookup"><span data-stu-id="be240-196">Request</span></span>
<span data-ttu-id="be240-197">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="be240-197">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks
Content-type: application/json
Content-length: 853

{
  "@odata.type": "#microsoft.graph.iosVppEBook",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "publishedDateTime": "2016-12-31T23:58:16.1180489-08:00",
  "largeCover": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "informationUrl": "https://example.com/informationUrl/",
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "vppTokenId": "<Unknown Primitive Type Edm.Guid>",
  "appleId": "Apple Id value",
  "vppOrganizationName": "Vpp Organization Name value",
  "genres": [
    "Genres value"
  ],
  "language": "Language value",
  "seller": "Seller value",
  "totalLicenseCount": 1,
  "usedLicenseCount": 0
}
```

### <a name="response"></a><span data-ttu-id="be240-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="be240-198">Response</span></span>
<span data-ttu-id="be240-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="be240-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 961

{
  "@odata.type": "#microsoft.graph.iosVppEBook",
  "id": "3b9f627e-627e-3b9f-7e62-9f3b7e629f3b",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "publishedDateTime": "2016-12-31T23:58:16.1180489-08:00",
  "largeCover": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "informationUrl": "https://example.com/informationUrl/",
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "vppTokenId": "<Unknown Primitive Type Edm.Guid>",
  "appleId": "Apple Id value",
  "vppOrganizationName": "Vpp Organization Name value",
  "genres": [
    "Genres value"
  ],
  "language": "Language value",
  "seller": "Seller value",
  "totalLicenseCount": 1,
  "usedLicenseCount": 0
}
```



