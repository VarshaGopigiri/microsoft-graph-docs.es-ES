# <a name="create-iosvppebook"></a><span data-ttu-id="9111a-101">Crear iosVppEBook</span><span class="sxs-lookup"><span data-stu-id="9111a-101">Create iosVppEBook</span></span>

> <span data-ttu-id="9111a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9111a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9111a-103">Cree un objeto [iosVppEBook](../resources/intune_books_iosvppebook.md).</span><span class="sxs-lookup"><span data-stu-id="9111a-103">Create a new [plannerBucket](../resources/intune_books_iosvppebook.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9111a-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9111a-104">Prerequisites</span></span>
<span data-ttu-id="9111a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9111a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9111a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9111a-107">Permission type</span></span>|<span data-ttu-id="9111a-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9111a-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9111a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9111a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="9111a-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9111a-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="9111a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9111a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9111a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9111a-112">Not supported.</span></span>|
|<span data-ttu-id="9111a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9111a-113">Application</span></span>|<span data-ttu-id="9111a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9111a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9111a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9111a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks
```

## <a name="request-headers"></a><span data-ttu-id="9111a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9111a-116">Request headers</span></span>
|<span data-ttu-id="9111a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9111a-117">Header</span></span>|<span data-ttu-id="9111a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9111a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9111a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="9111a-119">Authorization</span></span>|<span data-ttu-id="9111a-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9111a-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="9111a-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9111a-121">Accept</span></span>|<span data-ttu-id="9111a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="9111a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9111a-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9111a-123">Request body</span></span>
<span data-ttu-id="9111a-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosVppEBook.</span><span class="sxs-lookup"><span data-stu-id="9111a-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="9111a-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosVppEBook.</span><span class="sxs-lookup"><span data-stu-id="9111a-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="9111a-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9111a-126">Property</span></span>|<span data-ttu-id="9111a-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="9111a-127">Type</span></span>|<span data-ttu-id="9111a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="9111a-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9111a-129">id</span><span class="sxs-lookup"><span data-stu-id="9111a-129">id</span></span>|<span data-ttu-id="9111a-130">String</span><span class="sxs-lookup"><span data-stu-id="9111a-130">String</span></span>|<span data-ttu-id="9111a-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9111a-131">Key of the setting.</span></span> <span data-ttu-id="9111a-132">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="9111a-132">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="9111a-133">displayName</span><span class="sxs-lookup"><span data-stu-id="9111a-133">displayName</span></span>|<span data-ttu-id="9111a-134">String</span><span class="sxs-lookup"><span data-stu-id="9111a-134">String</span></span>|<span data-ttu-id="9111a-135">Nombre del libro electrónico</span><span class="sxs-lookup"><span data-stu-id="9111a-135">Name of the folder.</span></span> <span data-ttu-id="9111a-136">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="9111a-136">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="9111a-137">description</span><span class="sxs-lookup"><span data-stu-id="9111a-137">description</span></span>|<span data-ttu-id="9111a-138">String</span><span class="sxs-lookup"><span data-stu-id="9111a-138">String</span></span>|<span data-ttu-id="9111a-139">Descripción.</span><span class="sxs-lookup"><span data-stu-id="9111a-139">Description.</span></span> <span data-ttu-id="9111a-140">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="9111a-140">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="9111a-141">publicador</span><span class="sxs-lookup"><span data-stu-id="9111a-141">Publisher</span></span>|<span data-ttu-id="9111a-142">String</span><span class="sxs-lookup"><span data-stu-id="9111a-142">String</span></span>|<span data-ttu-id="9111a-143">Publicador.</span><span class="sxs-lookup"><span data-stu-id="9111a-143">Publisher</span></span> <span data-ttu-id="9111a-144">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="9111a-144">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="9111a-145">publishedDateTime</span><span class="sxs-lookup"><span data-stu-id="9111a-145">publishedDateTime</span></span>|<span data-ttu-id="9111a-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9111a-146">DateTimeOffset</span></span>|<span data-ttu-id="9111a-147">La fecha y la hora en que se publicó el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="9111a-147">The date and time when the page was created.</span></span> <span data-ttu-id="9111a-148">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="9111a-148">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="9111a-149">largeCover</span><span class="sxs-lookup"><span data-stu-id="9111a-149">largeCover</span></span>|[<span data-ttu-id="9111a-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="9111a-150">mimeContent</span></span>](../resources/intune_books_mimecontent.md)|<span data-ttu-id="9111a-151">Cubierta de libro.</span><span class="sxs-lookup"><span data-stu-id="9111a-151">Book cover</span></span> <span data-ttu-id="9111a-152">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="9111a-152">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="9111a-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="9111a-153">createdDateTime</span></span>|<span data-ttu-id="9111a-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9111a-154">DateTimeOffset</span></span>|<span data-ttu-id="9111a-155">La fecha y la hora en que se creó el archivo del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="9111a-155">The date and time when the page was created.</span></span> <span data-ttu-id="9111a-156">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="9111a-156">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="9111a-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9111a-157">lastModifiedDateTime</span></span>|<span data-ttu-id="9111a-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9111a-158">DateTimeOffset</span></span>|<span data-ttu-id="9111a-159">La fecha y la hora en que el libro electrónico se modificó por última vez.</span><span class="sxs-lookup"><span data-stu-id="9111a-159">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="9111a-160">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="9111a-160">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="9111a-161">informationUrl</span><span class="sxs-lookup"><span data-stu-id="9111a-161">informationUrl</span></span>|<span data-ttu-id="9111a-162">String</span><span class="sxs-lookup"><span data-stu-id="9111a-162">String</span></span>|<span data-ttu-id="9111a-163">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9111a-163">The more information Url.</span></span> <span data-ttu-id="9111a-164">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="9111a-164">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="9111a-165">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="9111a-165">privacyInformationUrl</span></span>|<span data-ttu-id="9111a-166">String</span><span class="sxs-lookup"><span data-stu-id="9111a-166">String</span></span>|<span data-ttu-id="9111a-167">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="9111a-167">The privacy statement Url.</span></span> <span data-ttu-id="9111a-168">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="9111a-168">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="9111a-169">vppTokenId</span><span class="sxs-lookup"><span data-stu-id="9111a-169">vppTokenId</span></span>|<span data-ttu-id="9111a-170">Guid</span><span class="sxs-lookup"><span data-stu-id="9111a-170">Guid</span></span>|<span data-ttu-id="9111a-171">El Id. de token de VPP.</span><span class="sxs-lookup"><span data-stu-id="9111a-171">The Vpp token ID.</span></span>|
|<span data-ttu-id="9111a-172">appleId</span><span class="sxs-lookup"><span data-stu-id="9111a-172">appleId</span></span>|<span data-ttu-id="9111a-173">String</span><span class="sxs-lookup"><span data-stu-id="9111a-173">String</span></span>|<span data-ttu-id="9111a-174">El ID de Apple asociado a un token de VPP.</span><span class="sxs-lookup"><span data-stu-id="9111a-174">The Apple ID associated with Vpp token.</span></span>|
|<span data-ttu-id="9111a-175">vppOrganizationName</span><span class="sxs-lookup"><span data-stu-id="9111a-175">vppOrganizationName</span></span>|<span data-ttu-id="9111a-176">String</span><span class="sxs-lookup"><span data-stu-id="9111a-176">String</span></span>|<span data-ttu-id="9111a-177">El nombre de la organización del token de VPP.</span><span class="sxs-lookup"><span data-stu-id="9111a-177">The Vpp token's organization name.</span></span>|
|<span data-ttu-id="9111a-178">géneros</span><span class="sxs-lookup"><span data-stu-id="9111a-178">genres</span></span>|<span data-ttu-id="9111a-179">Colección string</span><span class="sxs-lookup"><span data-stu-id="9111a-179">String collection</span></span>|<span data-ttu-id="9111a-180">Géneros.</span><span class="sxs-lookup"><span data-stu-id="9111a-180">Genres.</span></span>|
|<span data-ttu-id="9111a-181">language</span><span class="sxs-lookup"><span data-stu-id="9111a-181">language</span></span>|<span data-ttu-id="9111a-182">String</span><span class="sxs-lookup"><span data-stu-id="9111a-182">String</span></span>|<span data-ttu-id="9111a-183">Idioma.</span><span class="sxs-lookup"><span data-stu-id="9111a-183">language</span></span>|
|<span data-ttu-id="9111a-184">vendedor</span><span class="sxs-lookup"><span data-stu-id="9111a-184">seller</span></span>|<span data-ttu-id="9111a-185">String</span><span class="sxs-lookup"><span data-stu-id="9111a-185">String</span></span>|<span data-ttu-id="9111a-186">Vendedor.</span><span class="sxs-lookup"><span data-stu-id="9111a-186">Seller Dashboard</span></span>|
|<span data-ttu-id="9111a-187">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="9111a-187">totalLicenseCount</span></span>|<span data-ttu-id="9111a-188">Int32</span><span class="sxs-lookup"><span data-stu-id="9111a-188">Int32</span></span>|<span data-ttu-id="9111a-189">Número total de licencias.</span><span class="sxs-lookup"><span data-stu-id="9111a-189">Total license count.</span></span>|
|<span data-ttu-id="9111a-190">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="9111a-190">usedLicenseCount</span></span>|<span data-ttu-id="9111a-191">Int32</span><span class="sxs-lookup"><span data-stu-id="9111a-191">Int32</span></span>|<span data-ttu-id="9111a-192">Número de licencias usadas.</span><span class="sxs-lookup"><span data-stu-id="9111a-192">Used license count.</span></span>|



## <a name="response"></a><span data-ttu-id="9111a-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9111a-193">Response</span></span>
<span data-ttu-id="9111a-194">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosVppEBook](../resources/intune_books_iosvppebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9111a-194">If successful, this method returns a `201 Created` response code and a [DriveItemVersion](../resources/intune_books_iosvppebook.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9111a-195">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9111a-195">Example</span></span>
### <a name="request"></a><span data-ttu-id="9111a-196">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9111a-196">Request</span></span>
<span data-ttu-id="9111a-197">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9111a-197">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="9111a-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9111a-198">Response</span></span>
<span data-ttu-id="9111a-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9111a-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



