# <a name="update-androidforworkenrollmentprofile"></a><span data-ttu-id="ed760-101">Actualizar androidForWorkEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="ed760-101">Update androidForWorkEnrollmentProfile</span></span>

> <span data-ttu-id="ed760-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ed760-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ed760-103">Actualice las propiedades de un objeto [androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="ed760-103">Update the properties of a [calendar](../resources/intune_androidforwork_androidforworkenrollmentprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ed760-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ed760-104">Prerequisites</span></span>
<span data-ttu-id="ed760-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ed760-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ed760-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ed760-107">Permission type</span></span>|<span data-ttu-id="ed760-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ed760-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ed760-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ed760-109">Delegated (work or school account)</span></span>|<span data-ttu-id="ed760-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed760-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ed760-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ed760-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ed760-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed760-112">Not supported.</span></span>|
|<span data-ttu-id="ed760-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ed760-113">Application</span></span>|<span data-ttu-id="ed760-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed760-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ed760-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ed760-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/androidForWorkEnrollmentProfiles/{androidForWorkEnrollmentProfileId}
```

## <a name="request-headers"></a><span data-ttu-id="ed760-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ed760-116">Request headers</span></span>
|<span data-ttu-id="ed760-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed760-117">Header</span></span>|<span data-ttu-id="ed760-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ed760-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ed760-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="ed760-119">Authorization</span></span>|<span data-ttu-id="ed760-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ed760-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="ed760-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ed760-121">Accept</span></span>|<span data-ttu-id="ed760-122">application/json</span><span class="sxs-lookup"><span data-stu-id="ed760-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ed760-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ed760-123">Request body</span></span>
<span data-ttu-id="ed760-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="ed760-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_androidforwork_androidforworkenrollmentprofile.md) object.</span></span>

<span data-ttu-id="ed760-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="ed760-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="ed760-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ed760-126">Property</span></span>|<span data-ttu-id="ed760-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed760-127">Type</span></span>|<span data-ttu-id="ed760-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed760-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ed760-129">accountId</span><span class="sxs-lookup"><span data-stu-id="ed760-129">accountId</span></span>|<span data-ttu-id="ed760-130">String</span><span class="sxs-lookup"><span data-stu-id="ed760-130">String</span></span>|<span data-ttu-id="ed760-131">GUID del espacio empresarial al que pertenece el perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="ed760-131">Tenant GUID the enrollment profile belongs to.</span></span>|
|<span data-ttu-id="ed760-132">id</span><span class="sxs-lookup"><span data-stu-id="ed760-132">id</span></span>|<span data-ttu-id="ed760-133">String</span><span class="sxs-lookup"><span data-stu-id="ed760-133">String</span></span>|<span data-ttu-id="ed760-134">GUID único del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="ed760-134">Unique GUID for the enrollment profile.</span></span>|
|<span data-ttu-id="ed760-135">name</span><span class="sxs-lookup"><span data-stu-id="ed760-135">name</span></span>|<span data-ttu-id="ed760-136">String</span><span class="sxs-lookup"><span data-stu-id="ed760-136">String</span></span>|<span data-ttu-id="ed760-137">(En desuso) Nombre para mostrar del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="ed760-137">(Deprecated) Display name for the enrollment profile.</span></span>|
|<span data-ttu-id="ed760-138">displayName</span><span class="sxs-lookup"><span data-stu-id="ed760-138">displayName</span></span>|<span data-ttu-id="ed760-139">String</span><span class="sxs-lookup"><span data-stu-id="ed760-139">String</span></span>|<span data-ttu-id="ed760-140">Nombre para mostrar del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="ed760-140">Display name for the enrollment profile.</span></span>|
|<span data-ttu-id="ed760-141">description</span><span class="sxs-lookup"><span data-stu-id="ed760-141">description</span></span>|<span data-ttu-id="ed760-142">String</span><span class="sxs-lookup"><span data-stu-id="ed760-142">String</span></span>|<span data-ttu-id="ed760-143">Descripción del perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="ed760-143">Description for the enrollment profile.</span></span>|
|<span data-ttu-id="ed760-144">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ed760-144">createdDateTime</span></span>|<span data-ttu-id="ed760-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ed760-145">DateTimeOffset</span></span>|<span data-ttu-id="ed760-146">Fecha y hora en que se creó el perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="ed760-146">Date time the enrollment profile was created.</span></span>|
|<span data-ttu-id="ed760-147">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ed760-147">modifiedDateTime</span></span>|<span data-ttu-id="ed760-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ed760-148">DateTimeOffset</span></span>|<span data-ttu-id="ed760-149">(En desuso) Fecha y hora en que se modificó el perfil de inscripción por última vez.</span><span class="sxs-lookup"><span data-stu-id="ed760-149">(Deprecated) Date time the enrollment profile was last modified.</span></span>|
|<span data-ttu-id="ed760-150">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ed760-150">lastModifiedDateTime</span></span>|<span data-ttu-id="ed760-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ed760-151">DateTimeOffset</span></span>|<span data-ttu-id="ed760-152">Fecha y hora en que se modificó el perfil de inscripción por última vez.</span><span class="sxs-lookup"><span data-stu-id="ed760-152">Date time the enrollment profile was last modified.</span></span>|
|<span data-ttu-id="ed760-153">tokenValue</span><span class="sxs-lookup"><span data-stu-id="ed760-153">tokenValue</span></span>|<span data-ttu-id="ed760-154">String</span><span class="sxs-lookup"><span data-stu-id="ed760-154">String</span></span>|<span data-ttu-id="ed760-155">Valor del token creado más recientemente para este perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="ed760-155">Value of the most recently created token for this enrollment profile.</span></span>|
|<span data-ttu-id="ed760-156">tokenExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="ed760-156">tokenExpirationDateTime</span></span>|<span data-ttu-id="ed760-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ed760-157">DateTimeOffset</span></span>|<span data-ttu-id="ed760-158">Fecha y hora en que expirará el token creado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="ed760-158">Date time the most recently created token will expire.</span></span>|
|<span data-ttu-id="ed760-159">totalEnrollmentCount</span><span class="sxs-lookup"><span data-stu-id="ed760-159">totalEnrollmentCount</span></span>|<span data-ttu-id="ed760-160">Int32</span><span class="sxs-lookup"><span data-stu-id="ed760-160">Int32</span></span>|<span data-ttu-id="ed760-161">(En desuso) Número total de dispositivos Android que se han inscrito con este perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="ed760-161">(Deprecated) Total number of Android devices that have enrolled using this enrollment profile.</span></span>|
|<span data-ttu-id="ed760-162">enrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ed760-162">enrolledDeviceCount</span></span>|<span data-ttu-id="ed760-163">Int32</span><span class="sxs-lookup"><span data-stu-id="ed760-163">Int32</span></span>|<span data-ttu-id="ed760-164">Número total de dispositivos Android que se han inscrito con este perfil de inscripción.</span><span class="sxs-lookup"><span data-stu-id="ed760-164">Total number of Android devices that have enrolled using this enrollment profile.</span></span>|
|<span data-ttu-id="ed760-165">qrCode</span><span class="sxs-lookup"><span data-stu-id="ed760-165">qrCode</span></span>|<span data-ttu-id="ed760-166">String</span><span class="sxs-lookup"><span data-stu-id="ed760-166">String</span></span>|<span data-ttu-id="ed760-167">(En desuso) Cadena usada para generar un código QR para el token.</span><span class="sxs-lookup"><span data-stu-id="ed760-167">(Deprecated) String used to generate a QR code for the token.</span></span>|
|<span data-ttu-id="ed760-168">qrCodeContent</span><span class="sxs-lookup"><span data-stu-id="ed760-168">qrCodeContent</span></span>|<span data-ttu-id="ed760-169">String</span><span class="sxs-lookup"><span data-stu-id="ed760-169">String</span></span>|<span data-ttu-id="ed760-170">Cadena usada para generar un código QR para el token.</span><span class="sxs-lookup"><span data-stu-id="ed760-170">String used to generate a QR code for the token.</span></span>|
|<span data-ttu-id="ed760-171">qrCodeImage</span><span class="sxs-lookup"><span data-stu-id="ed760-171">qrCodeImage</span></span>|[<span data-ttu-id="ed760-172">mimeContent</span><span class="sxs-lookup"><span data-stu-id="ed760-172">mimeContent</span></span>](../resources/intune_androidforwork_mimecontent.md)|<span data-ttu-id="ed760-173">Cadena usada para generar un código QR para el token.</span><span class="sxs-lookup"><span data-stu-id="ed760-173">String used to generate a QR code for the token.</span></span>|



## <a name="response"></a><span data-ttu-id="ed760-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed760-174">Response</span></span>
<span data-ttu-id="ed760-175">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed760-175">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_androidforwork_androidforworkenrollmentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ed760-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ed760-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="ed760-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ed760-177">Request</span></span>
<span data-ttu-id="ed760-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ed760-178">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/androidForWorkEnrollmentProfiles/{androidForWorkEnrollmentProfileId}
Content-type: application/json
Content-length: 575

{
  "accountId": "Account Id value",
  "name": "Name value",
  "displayName": "Display Name value",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "tokenValue": "Token Value value",
  "tokenExpirationDateTime": "2016-12-31T23:59:54.0590989-08:00",
  "totalEnrollmentCount": 4,
  "enrolledDeviceCount": 3,
  "qrCode": "Qr Code value",
  "qrCodeContent": "Qr Code Content value",
  "qrCodeImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  }
}
```

### <a name="response"></a><span data-ttu-id="ed760-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed760-179">Response</span></span>
<span data-ttu-id="ed760-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ed760-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 813

{
  "@odata.type": "#microsoft.graph.androidForWorkEnrollmentProfile",
  "accountId": "Account Id value",
  "id": "e6742553-2553-e674-5325-74e6532574e6",
  "name": "Name value",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "tokenValue": "Token Value value",
  "tokenExpirationDateTime": "2016-12-31T23:59:54.0590989-08:00",
  "totalEnrollmentCount": 4,
  "enrolledDeviceCount": 3,
  "qrCode": "Qr Code value",
  "qrCodeContent": "Qr Code Content value",
  "qrCodeImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  }
}
```



