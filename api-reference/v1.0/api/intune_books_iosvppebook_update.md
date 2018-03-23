# <a name="update-iosvppebook"></a><span data-ttu-id="5bf67-101">Actualizar iosVppEBook</span><span class="sxs-lookup"><span data-stu-id="5bf67-101">Update iosVppEBook</span></span>

> <span data-ttu-id="5bf67-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5bf67-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5bf67-103">Actualice las propiedades de un objeto [iosVppEBook](../resources/intune_books_iosvppebook.md).</span><span class="sxs-lookup"><span data-stu-id="5bf67-103">Update the properties of a [calendar](../resources/intune_books_iosvppebook.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5bf67-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5bf67-104">Prerequisites</span></span>
<span data-ttu-id="5bf67-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5bf67-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5bf67-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5bf67-107">Permission type</span></span>|<span data-ttu-id="5bf67-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5bf67-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5bf67-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5bf67-109">Delegated (work or school account)</span></span>|<span data-ttu-id="5bf67-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5bf67-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="5bf67-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5bf67-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5bf67-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5bf67-112">Not supported.</span></span>|
|<span data-ttu-id="5bf67-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5bf67-113">Application</span></span>|<span data-ttu-id="5bf67-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5bf67-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5bf67-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5bf67-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}
```

## <a name="request-headers"></a><span data-ttu-id="5bf67-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5bf67-116">Request headers</span></span>
|<span data-ttu-id="5bf67-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5bf67-117">Header</span></span>|<span data-ttu-id="5bf67-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5bf67-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5bf67-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="5bf67-119">Authorization</span></span>|<span data-ttu-id="5bf67-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5bf67-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="5bf67-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5bf67-121">Accept</span></span>|<span data-ttu-id="5bf67-122">application/json</span><span class="sxs-lookup"><span data-stu-id="5bf67-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5bf67-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5bf67-123">Request body</span></span>
<span data-ttu-id="5bf67-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosVppEBook](../resources/intune_books_iosvppebook.md).</span><span class="sxs-lookup"><span data-stu-id="5bf67-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_books_iosvppebook.md) object.</span></span>

<span data-ttu-id="5bf67-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosVppEBook](../resources/intune_books_iosvppebook.md).</span><span class="sxs-lookup"><span data-stu-id="5bf67-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="5bf67-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5bf67-126">Property</span></span>|<span data-ttu-id="5bf67-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="5bf67-127">Type</span></span>|<span data-ttu-id="5bf67-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="5bf67-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5bf67-129">id</span><span class="sxs-lookup"><span data-stu-id="5bf67-129">id</span></span>|<span data-ttu-id="5bf67-130">String</span><span class="sxs-lookup"><span data-stu-id="5bf67-130">String</span></span>|<span data-ttu-id="5bf67-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5bf67-131">Key of the setting.</span></span> <span data-ttu-id="5bf67-132">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="5bf67-132">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="5bf67-133">displayName</span><span class="sxs-lookup"><span data-stu-id="5bf67-133">displayName</span></span>|<span data-ttu-id="5bf67-134">String</span><span class="sxs-lookup"><span data-stu-id="5bf67-134">String</span></span>|<span data-ttu-id="5bf67-135">Nombre del libro electrónico</span><span class="sxs-lookup"><span data-stu-id="5bf67-135">Name of the folder.</span></span> <span data-ttu-id="5bf67-136">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="5bf67-136">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="5bf67-137">description</span><span class="sxs-lookup"><span data-stu-id="5bf67-137">description</span></span>|<span data-ttu-id="5bf67-138">String</span><span class="sxs-lookup"><span data-stu-id="5bf67-138">String</span></span>|<span data-ttu-id="5bf67-139">Descripción.</span><span class="sxs-lookup"><span data-stu-id="5bf67-139">Description.</span></span> <span data-ttu-id="5bf67-140">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="5bf67-140">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="5bf67-141">publicador</span><span class="sxs-lookup"><span data-stu-id="5bf67-141">Publisher</span></span>|<span data-ttu-id="5bf67-142">String</span><span class="sxs-lookup"><span data-stu-id="5bf67-142">String</span></span>|<span data-ttu-id="5bf67-143">Publicador.</span><span class="sxs-lookup"><span data-stu-id="5bf67-143">Publisher</span></span> <span data-ttu-id="5bf67-144">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="5bf67-144">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="5bf67-145">publishedDateTime</span><span class="sxs-lookup"><span data-stu-id="5bf67-145">publishedDateTime</span></span>|<span data-ttu-id="5bf67-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5bf67-146">DateTimeOffset</span></span>|<span data-ttu-id="5bf67-147">La fecha y la hora en que se publicó el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="5bf67-147">The date and time when the page was created.</span></span> <span data-ttu-id="5bf67-148">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="5bf67-148">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="5bf67-149">largeCover</span><span class="sxs-lookup"><span data-stu-id="5bf67-149">largeCover</span></span>|[<span data-ttu-id="5bf67-150">mimeContent</span><span class="sxs-lookup"><span data-stu-id="5bf67-150">mimeContent</span></span>](../resources/intune_books_mimecontent.md)|<span data-ttu-id="5bf67-151">Cubierta de libro.</span><span class="sxs-lookup"><span data-stu-id="5bf67-151">Book cover</span></span> <span data-ttu-id="5bf67-152">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="5bf67-152">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="5bf67-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5bf67-153">createdDateTime</span></span>|<span data-ttu-id="5bf67-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5bf67-154">DateTimeOffset</span></span>|<span data-ttu-id="5bf67-155">La fecha y la hora en que se creó el archivo del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="5bf67-155">The date and time when the page was created.</span></span> <span data-ttu-id="5bf67-156">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="5bf67-156">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="5bf67-157">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="5bf67-157">lastModifiedDateTime</span></span>|<span data-ttu-id="5bf67-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5bf67-158">DateTimeOffset</span></span>|<span data-ttu-id="5bf67-159">La fecha y la hora en que se modificó por última vez el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="5bf67-159">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="5bf67-160">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="5bf67-160">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="5bf67-161">informationUrl</span><span class="sxs-lookup"><span data-stu-id="5bf67-161">informationUrl</span></span>|<span data-ttu-id="5bf67-162">String</span><span class="sxs-lookup"><span data-stu-id="5bf67-162">String</span></span>|<span data-ttu-id="5bf67-163">Dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="5bf67-163">The more information Url.</span></span> <span data-ttu-id="5bf67-164">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="5bf67-164">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="5bf67-165">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="5bf67-165">privacyInformationUrl</span></span>|<span data-ttu-id="5bf67-166">String</span><span class="sxs-lookup"><span data-stu-id="5bf67-166">String</span></span>|<span data-ttu-id="5bf67-167">Dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="5bf67-167">The privacy statement Url.</span></span> <span data-ttu-id="5bf67-168">Heredado de [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="5bf67-168">Inherited from [managedEBook](../resources/intune_books_managedebook.md)</span></span>|
|<span data-ttu-id="5bf67-169">vppTokenId</span><span class="sxs-lookup"><span data-stu-id="5bf67-169">vppTokenId</span></span>|<span data-ttu-id="5bf67-170">Guid</span><span class="sxs-lookup"><span data-stu-id="5bf67-170">Guid</span></span>|<span data-ttu-id="5bf67-171">El Id. de token de VPP.</span><span class="sxs-lookup"><span data-stu-id="5bf67-171">The Vpp token ID.</span></span>|
|<span data-ttu-id="5bf67-172">appleId</span><span class="sxs-lookup"><span data-stu-id="5bf67-172">appleId</span></span>|<span data-ttu-id="5bf67-173">String</span><span class="sxs-lookup"><span data-stu-id="5bf67-173">String</span></span>|<span data-ttu-id="5bf67-174">El ID de Apple asociado a un token de VPP.</span><span class="sxs-lookup"><span data-stu-id="5bf67-174">The Apple ID associated with Vpp token.</span></span>|
|<span data-ttu-id="5bf67-175">vppOrganizationName</span><span class="sxs-lookup"><span data-stu-id="5bf67-175">vppOrganizationName</span></span>|<span data-ttu-id="5bf67-176">String</span><span class="sxs-lookup"><span data-stu-id="5bf67-176">String</span></span>|<span data-ttu-id="5bf67-177">El nombre de la organización del token de VPP.</span><span class="sxs-lookup"><span data-stu-id="5bf67-177">The Vpp token's organization name.</span></span>|
|<span data-ttu-id="5bf67-178">géneros</span><span class="sxs-lookup"><span data-stu-id="5bf67-178">genres</span></span>|<span data-ttu-id="5bf67-179">Colección string</span><span class="sxs-lookup"><span data-stu-id="5bf67-179">String collection</span></span>|<span data-ttu-id="5bf67-180">Géneros.</span><span class="sxs-lookup"><span data-stu-id="5bf67-180">Genres.</span></span>|
|<span data-ttu-id="5bf67-181">language</span><span class="sxs-lookup"><span data-stu-id="5bf67-181">language</span></span>|<span data-ttu-id="5bf67-182">String</span><span class="sxs-lookup"><span data-stu-id="5bf67-182">String</span></span>|<span data-ttu-id="5bf67-183">Idioma.</span><span class="sxs-lookup"><span data-stu-id="5bf67-183">language</span></span>|
|<span data-ttu-id="5bf67-184">vendedor</span><span class="sxs-lookup"><span data-stu-id="5bf67-184">seller</span></span>|<span data-ttu-id="5bf67-185">String</span><span class="sxs-lookup"><span data-stu-id="5bf67-185">String</span></span>|<span data-ttu-id="5bf67-186">Vendedor.</span><span class="sxs-lookup"><span data-stu-id="5bf67-186">Seller Dashboard</span></span>|
|<span data-ttu-id="5bf67-187">totalLicenseCount</span><span class="sxs-lookup"><span data-stu-id="5bf67-187">totalLicenseCount</span></span>|<span data-ttu-id="5bf67-188">Int32</span><span class="sxs-lookup"><span data-stu-id="5bf67-188">Int32</span></span>|<span data-ttu-id="5bf67-189">Número total de licencias.</span><span class="sxs-lookup"><span data-stu-id="5bf67-189">Total license count.</span></span>|
|<span data-ttu-id="5bf67-190">usedLicenseCount</span><span class="sxs-lookup"><span data-stu-id="5bf67-190">usedLicenseCount</span></span>|<span data-ttu-id="5bf67-191">Int32</span><span class="sxs-lookup"><span data-stu-id="5bf67-191">Int32</span></span>|<span data-ttu-id="5bf67-192">Número de licencias usadas.</span><span class="sxs-lookup"><span data-stu-id="5bf67-192">Used license count.</span></span>|



## <a name="response"></a><span data-ttu-id="5bf67-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5bf67-193">Response</span></span>
<span data-ttu-id="5bf67-194">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosVppEBook](../resources/intune_books_iosvppebook.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5bf67-194">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_books_iosvppebook.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5bf67-195">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5bf67-195">Example</span></span>
### <a name="request"></a><span data-ttu-id="5bf67-196">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5bf67-196">Request</span></span>
<span data-ttu-id="5bf67-197">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5bf67-197">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}
Content-type: application/json
Content-length: 803

{
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

### <a name="response"></a><span data-ttu-id="5bf67-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5bf67-198">Response</span></span>
<span data-ttu-id="5bf67-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5bf67-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



